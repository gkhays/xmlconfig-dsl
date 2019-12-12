pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/gkhays/xmlconfig-dsl'
            }
        }
        stage('Update') {
            steps {
                def testEnv = new XmlParser().parseText('config.xml')
                testEnv.ApplicationServer.IP[0].replaceNode {
                    IP("10.204.96.24")
                }
                println(testEnv.ApplicationServer.IP.text())
            }
        }
    }
}