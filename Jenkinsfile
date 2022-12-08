pipeline {
	agent any
		stages {
			stage('First') {
				steps {
					sh 'echo "Step One"'
					script {
							env.EXECUTE="True"
						}

				}
			}
			stage('Second') {
				 when {
                         environment(name: "EXECUTE", value: "True")
            			}


				steps {
					sh 'echo "Updating Second Stage"'
					script {
							sh'echo ${EXECUTE}'
						}
				}
			} 
			stage('Third') {
				when {
                     environment(name: "EXECUTE", value: "False")
            		}
				steps {
					sh 'echo "Step Three"'
				}
			}
		}
}
