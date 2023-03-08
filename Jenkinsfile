pipeline {
         agent any
         stages {
                 stage('Build') {
                 steps {
                     echo 'Hi, GeekFlare. Starting to build the App.'
                 }
                 }
                 stage('Test') {
				 when { tag "*" }
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Deploy') {
				 when { tag "*" }
                 parallel { 
                            stage('Deploy start ') {
                           steps {
                                echo "Start the deploy .."
                           } 
                           }
                           }
                           }
                 stage('Prod') {
				 when { tag "*" }
                     steps {
                                echo "App is Prod Ready"
                              }
                 
              }
}
}
