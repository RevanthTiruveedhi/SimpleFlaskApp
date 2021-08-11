pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                // checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/RevanthTiruveedhi/PythonFlaskApp.git']]])
                //git branch: 'main', url: 'https://github.com/RevanthTiruveedhi/PythonFlaskApp.git'  
                sh 'python -m py_compile main.py'
                sh 'sudo cp -f /var/lib/jenkins/workspace/Flaskapp/main.py /var/www/flaskapp/flaskapp/'
            }
        }
        stage('Test') { 
            steps {
                echo 'Test'
                //sh 'pytest test_unit_app.py' 
            }
        }
        stage('Deploy') { 
            steps {
                echo 'Deploy'
                //sh 'python setup.py bdist_wheel -d /etc/html/PythonApp/'
                //sh 'pip install Python_flaskapp-1.0.0-py3-none-any.whl'
            }
        }
    }
}
