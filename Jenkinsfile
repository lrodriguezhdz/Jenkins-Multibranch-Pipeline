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
                         environment(name: "ENV", value: "testing")
            			}


				steps {
					sh 'echo "Updating Second Stage"'
					script {
							sh'echo ${EXECUTE}'
						}
				}
			} 
			stage('Third') {
				steps {
					sh 'echo "Step Three"'
				}
			}
		}
}
