pipeline {
  agent any

  environment {
    AWS_REGION = "eu-west-2"
    ECR_REPO = "975050024946.dkr.ecr.eu-west-2.amazonaws.com/shashirepo"
  }

  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', url: 'https://github.com/erpostgr25/Microservices-Task.git'
      }
    }

    stage('Build Docker Image for gateway-service') {
      steps {
        sh '''
        cd ${PWD}/Microservices/gateway-service
        docker build -t gatewayservice .
        '''
      }
    }

    stage('Build Docker Image for order-service') {
      steps {
        sh '''
        cd ${PWD}/Microservices/order-service
        docker build -t orderservice .
        '''
      }
    }

    stage('Build Docker Image for product-service') {
      steps {
        sh '''
        cd ${PWD}/Microservices/product-service
        docker build -t productservice .
        '''
      }
    }

    stage('Build Docker Image for user-service') {
      steps {
        sh '''
        cd ${PWD}/Microservices/user-service
        docker build -t userservice .
        '''
      }
    }

    stage('Login to ECR') {
      steps {
        sh '''
          aws ecr get-login-password --region $AWS_REGION |
          docker login --username AWS --password-stdin $ECR_REPO
        '''
      }
    }

    stage('Push Image') {
      steps {
        sh '''
          docker tag userservice:latest $ECR_REPO:userservice
          docker push $ECR_REPO:userservice
          docker tag productservice:latest $ECR_REPO:productservice
          docker push $ECR_REPO:productservice
          docker tag orderservice:latest $ECR_REPO:orderservice
          docker push $ECR_REPO:orderservice
          docker tag gatewayservice:latest $ECR_REPO:gatewayservice
          docker push $ECR_REPO:gatewayservice
        '''
      }
    }
  }
}
