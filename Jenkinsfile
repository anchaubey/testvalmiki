pipeline {
         agent any
         stages {
                 stage('Build') {
                 steps {
                     echo 'Hi, GeekFlare. Starting to build the App.'
                 }
                 }
                 stage('Test') {
				 when { tag "v2023-*" }
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Deploy') {
				 when { tag "v2023-*" }
                 parallel { 
                            stage('Deploy start ') {
                           steps {
                                echo "Start the deploy .."
                           } 
                           }
                           }
                           }
                 stage('Prod') {
				 when { tag "v2023-*" }
                     steps {
                                echo "App is Prod Ready"
                              }
                 
              }
}
}
