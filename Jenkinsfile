pipeline {
  agent any
  stages {

    stage("Maven Clean") {
      steps {
        script {
          sh "mvn -f'./pom.xml' clean -DskipTests=true -Drevision=${VERSION}"
        }
      }
    }
    stage("Maven Compile") {
      steps {
        script {
          sh "mvn -f'./pom.xml' compile -DskipTests=true -Drevision=${VERSION}"
        }
      }
    }
    stage("Maven test") {
      steps {
        script {
          sh "mvn -f'./pom.xml' test -Drevision=${VERSION}"
        }
      }
    }
   
    }
}
