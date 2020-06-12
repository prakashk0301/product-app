pipeline {
    agent any


    stages {
        stage('SCM Checkout'){
          git 'https://github.com/prakashk0301/product-app.git'
        }
    }
    {
		stage('trigger the docker-compose') {
			steps {
				sh label: '', script: 'docker-compose -f docker-compose.yml up -d --build'
				
			}
		}
	    
//	    //     stage("Deploy To Kuberates Cluster"){
//        kubernetesDeploy(
//         configs: 'springBootMongo.yml', 
//         kubeconfigId: 'KUBERNETES_CLUSTER_CONFIG',
//         enableConfigSubstitution: true
//        )
//     }
//	 
//	  /**
 //     stage("Deploy To Kuberates Cluster"){
 //       sh 'kubectl apply -f production-app-k8s-manifestfile.yml'
 //     } **/
 //    
}
	    
	    
	}
}
