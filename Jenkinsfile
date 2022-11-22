Pipeline {
    agent any
    environment {
        MYSQL_USER = credentials('jenkins-app-mysql-user')
        MYSQL_PWD = credentials('jenkins-app-mysql-pwd')
        MYSQL_DB = credentials('jenkins-app-mysql-db')
        MYSQL_ROOT_PASSWORD = credentials ('jenkins-app-mysql-root-password')
    }
    stages('Build') {
        steps {
            sh 'docker compose build' 
        }
    }
    stages('Deploy') {
        steps {
            sh 'docker compose up -d'
        }
    }
}