# Jenkins

`docker pull jenkins/jenkins`

`docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins`

 [Jenkins Tutorial](https://www.tutorialspoint.com/jenkins/index.htm)

```
Install choco
 @"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
        Jenkins

choco install --force jenkins -y && refreshenv
jenkins.exe start
jenkins.exe restart
jenkins.exe stop
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

