pipeline {
    agent any

    stages {
        stage('One') {
            steps {
                def testEnv = new XmlParser().parseText('config.xml')
            }
        }
    }
}