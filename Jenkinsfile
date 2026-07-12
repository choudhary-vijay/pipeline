pipeline {
    agent any 
    stages {
        stage('pull') { 
            steps {
                git branch: 'terraform', url: 'https://github.com/choudhary-vijay/cdec-terraform.git'
            }
        }
        stage('init') { 
            steps {
                sh '''terraform init
                      terraform plan
                   '''
            }
        }
        stage('Approve') { 
           steps {
	            timeout(10) {
      				  input message: 'Do you approve?', ok: "Yes"
                }
		    }
        }
        stage('apply') { 
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
