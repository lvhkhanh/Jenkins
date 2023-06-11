# Jenkins
## Certificates
- [x]  Jenkins: Beginner To Pro [UC-44f11b3e-f7b7-44a7-b14c-cd4bccb7a45a.pdf](https://github.com/lvhkhanh/Jenkins/files/11518336/UC-44f11b3e-f7b7-44a7-b14c-cd4bccb7a45a.pdf)

## Official
### https://www.cloudbees.com/jenkins/what-is-jenkins
### https://www.jenkins.io/solutions/pipeline/
### https://wiki.jenkins.io/display/JENKINS/Meet+Jenkins
### https://www.jenkins.io/2.0/
### https://jenkins.io/user-handbook.pdf
### https://www.jenkins.io/doc/book/pipeline/
### https://www.jenkins.io/
### [GUIDE] https://hub.docker.com/_/jenkins/
### https://hub.docker.com/r/jenkins/jenkins/
### https://www.jenkins.io/download/
### https://www.jenkins.io/doc/book/installing/
### https://plugins.jenkins.io/
### https://www.jenkins.io/doc/

## Courses
### https://app.pluralsight.com/library/courses/building-modern-ci-cd-pipeline-jenkins/table-of-contents
### https://app.pluralsight.com/library/courses/using-declarative-jenkins-pipelines/table-of-contents
### https://www.guru99.com/jenkin-continuous-integration.html
## Plugins

EZ Templates, Job DSL

## Samples
```
node('agentLabel'){}
```
```
agent 'agentLabel'
```
```
pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr:'3'))
  }
  parameters {
    string(name: 'GREETING',
           defaultValue: 'Hello',
           description: 'The way to say hello')
  }
  stages {
    stage('Say Hi to ...') {
      steps {
        checkout scm:[
          $class:'GitSCM',
          branches:[[name:'*/master']],
          userRemoteConfigs:[[
            url:'file:///path/to/config']]]
            
        // run shell, bat
      }
    }
  }
}
```

```
DSL Script

names = ['name1', 'name2']

names.each {n -> 
  String name = n
}

pipelineJob(name) {
  description('Say hi to ..' + name)
  
  logRotator {
      numToKeep(3)
  }
  
  parameters {
    stringParam('GREETING', 'Hello' + name, 'How to say hi')
  }
  
  definition {
    cpsScm {
      scm {
        git {
          branch('*/master')
          remote {
            url: 'file:///path/to/project'
          }
        }
        scriptPath('.Jenkinsfile')
      }
    }
  }
}
```

## Configuration

Using Global share library
```
#!groovy
@Library('jenkins-lib') _

options = {
  greeting: 'Hello',
  reindeer: 'your name'
}
reinder(options)
```
## Types

 Job DSL, Groovy


[Jenkins](https://code-maven.com/jenkins)

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

## Links
### https://www.infoworld.com/article/3239666/what-is-jenkins-the-ci-server-explained.html
### https://en.wikipedia.org/wiki/Jenkins_(software)
