node {
    
    stage('Checkout') {
        git 'https://github.com/gkhays/xmlconfig-dsl'
    }

    stage('Update') {
        def workspace = build.getEnvVars()["WORKSPACE"]
        def xml = new File(workspace, 'config.xml').text

        def testEnv = new XmlParser().parseText(xml)
        testEnv.ApplicationServer.IP[0].replaceNode {
            IP("192.168.2.24")
        }
        println(testEnv.ApplicationServer.IP.text())           
    }

}