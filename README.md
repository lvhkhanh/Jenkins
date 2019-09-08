# Jenkins

`docker pull jenkins/jenkins`

`docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins`

 [Jenkins Tutorial](https://www.tutorialspoint.com/jenkins/index.htm)

```
choco install jenkins
refreshenv
```

```
java -jar jenkins.war
```

[Apache Tomcat®](http://tomcat.apache.org/)

```
choco install tomcat -y
refreshenv
cd <C:\ProgramData\chocolatey\lib\Tomcat\tools\apache-tomcat-9.0.24>
mk webapps
copy <jenkins.war> <C:\ProgramData\chocolatey\lib\Tomcat\tools\apache-tomcat-9.0.24\webapps>
<C:\ProgramData\chocolatey\lib\Tomcat\tools\apache-tomcat-9.0.24\bin\startup.bat>
```

Git Pluggin

Build

