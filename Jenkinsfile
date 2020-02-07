pipeline {
   agent{
       kubernetes {
          containerTemplate {
            name 'maven'
            image 'maven:3.3.9-jdk-8-alpine'
            ttyEnabled true
            command 'cat'
          }
        }
   }

   stages {
      stage('Hello') {
         steps {
            echo 'Hello World'
         }
      }
      stage('Test') {
            parallel {
                stage('Chrome') {
                    steps {
                        sh 'echo "Chrome"'
                    }
                }
                stage('Firefox') {
                    steps {
                        sh 'echo "Firefox"'
                    }
                }
				stage('Edge') {
                    steps {
                        sh 'echo "Edge"'
                    }
                }
            }
   }
		stage('Test2') {
		parallel {
			stage('Hello') {
				steps {
					sh 'echo "IceCream"'
				}
			}
			stage('World') {
				steps {
					sh 'echo "IceCream"'
				}
			}
			stage('IceCream') {
				steps {
					sh 'echo "IceCream"'
				}
			}
		}
}
      
   }
   
   
}

