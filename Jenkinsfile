pipeline {
    agent any

    stages {
        stage('Bonjour') {
            steps {
                echo 'Pipeline démarré !'
            }
        }

        stage('Faux build') {
            steps {
                echo 'Je simule un build...'
                bat 'echo Compilation OK'
            }
        }

        stage('Faux test') {
            steps {
                echo 'Je simule des tests...'
                bat 'echo Tests passes : 5/5'
            }
        }

        stage('Résultat') {
            steps {
                echo 'Tout est bon, pipeline terminé !'
            }
        }
    }

    post {
        success {
            echo 'SUCCÈS — pipeline complet'
        }
        failure {
            echo 'ÉCHEC — quelque chose a planté'
        }
    }
}
