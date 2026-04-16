pipeline {
    agent any

    stages {
        stage('Bonjour') {
            steps {
                echo 'Pipeline démarré !'
                echo "Branche : ${env.BRANCH_NAME}"
            }
        }

        stage('Faux build') {
            steps {
                echo 'Je simule un build...'
                sh 'echo "Compilation OK"'
                sh 'sleep 2'
            }
        }

        stage('Faux test') {
            steps {
                echo 'Je simule des tests...'
                sh 'echo "Tests passés : 5/5"'
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
