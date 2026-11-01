echo 'Automatic build triggered after GitHub change!'
cat > Jenkinsfile <<'EOF'

pipeline {

&#x20;   agent any



&#x20;   stages {

&#x20;       stage('Build') {

&#x20;           steps {

&#x20;               echo 'Building the project...'

&#x20;           }

&#x20;       }



&#x20;       stage('Test') {

&#x20;           steps {

&#x20;               echo 'Testing the project...'

&#x20;           }

&#x20;       }



&#x20;       stage('Success') {

&#x20;           steps {

&#x20;               echo 'Jenkins pipeline completed successfully!'

&#x20;           }

&#x20;       }

&#x20;   }

}

EOF

