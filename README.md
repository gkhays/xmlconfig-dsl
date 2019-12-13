# xmlconfig-dsl
Jenkins pipeline DSL to update an XML file

Start the Jenkins Blue Ocean pipeline container.

```
docker run -d --name jenkinsci -p "8080:8080" -p "50000:50000" -e "-Djenkins.install.runSetupWizard=true" jenkinsci/blueocean
```
