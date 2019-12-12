node {
    
    stage('Checkout') {
        git 'https://github.com/gkhays/xmlconfig-dsl'
    }

    stage('Update') {
        //def pathBase = new File(".").getCanonicalPath();
        //def xml = new File(pathBase, "config.xml").text
        def xml = new File("config.xml")

        def testEnv = new XmlParser().parseText(xml)
        testEnv.ApplicationServer.IP[0].replaceNode {
            IP("192.168.2.24")
        }
        println(testEnv.ApplicationServer.IP.text())           
    }

}