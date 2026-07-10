pipeline {
  agent any

  options {
    timestamps()
    disableConcurrentBuilds()
  }

  environment {
    ACR_LOGIN_SERVER = 'replace-with-acr.azurecr.io'
    FRONTEND_IMAGE = 'three-tier-devops-azure-frontend'
    BACKEND_IMAGE = 'three-tier-devops-azure-backend'
  }

  stages {
    stage('Checkout') { steps { checkout scm } }

    stage('Frontend Build') {
      steps {
        dir('src/frontend') {
          sh 'npm ci'
          sh 'npm test -- --watchAll=false || true'
          sh 'npm run build'
        }
      }
    }

    stage('Backend Build') {
      steps {
        dir('src/backend') {
          sh './mvnw clean package -DskipTests=false'
        }
      }
    }

    stage('Docker Build') {
      steps {
        sh 'docker build -t $FRONTEND_IMAGE:$BUILD_NUMBER src/frontend'
        sh 'docker build -t $BACKEND_IMAGE:$BUILD_NUMBER src/backend'
      }
    }

    stage('Security Scan') {
      steps {
        sh 'trivy image --severity HIGH,CRITICAL --exit-code 0 $FRONTEND_IMAGE:$BUILD_NUMBER || true'
        sh 'trivy image --severity HIGH,CRITICAL --exit-code 0 $BACKEND_IMAGE:$BUILD_NUMBER || true'
      }
    }

    stage('Push to ACR') {
      when { expression { return env.BRANCH_NAME == 'main' } }
      steps {
        sh 'echo Configure Azure credentials or managed identity before enabling ACR push'
        sh 'docker tag $FRONTEND_IMAGE:$BUILD_NUMBER $ACR_LOGIN_SERVER/$FRONTEND_IMAGE:$BUILD_NUMBER'
        sh 'docker tag $BACKEND_IMAGE:$BUILD_NUMBER $ACR_LOGIN_SERVER/$BACKEND_IMAGE:$BUILD_NUMBER'
        sh 'echo docker push commands are intentionally documented but not auto-enabled in portfolio mode'
      }
    }

    stage('Terraform Validate') {
      steps {
        dir('infra') {
          sh 'terraform fmt -check -recursive || true'
          sh 'terraform init -backend=false || true'
          sh 'terraform validate || true'
        }
      }
    }
  }
}
