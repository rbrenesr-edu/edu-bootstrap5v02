


pipeline {
    agent any
    
    stages {
        stage('Clonar Repositorio') {
            steps {
                // Clonar el repositorio de GitHub en la carpeta de trabajo actual
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/rbrenesr/edu-bootstrap5.git']]])
            }
        }
        
        stage('Mover a carpeta temporal') {
            steps {
                // Mover el directorio clonado a la carpeta temporal                
                bat 'xcopy /E /I /Y .\\edu-bootstrap5\\ C:\\Sites\\temp\\'
            }
        }
    }
}
