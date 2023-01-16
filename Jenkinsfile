pipeline{
	agent any
	
	stages('login Azure') {
	steps{
	 script{
            withCredentials([
            string(credentialsId: 'AZ_USER', variable: 'azuser'),
            string(credentialsId: 'AZ_PASS', variable: 'azpass'),
            string(credentialsId: 'AZ_TENANT', variable: 'aztenant'),         
                ]) {
                sh 'az login --service-principal --username $azuser --password $azpass --tenant $aztenant
                sh 'az account subscription list'
                }
                }
	
		}
	
	}
}
