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
				steps {
					sh 'echo "Updating Second Stage"'
					script {
							echo ${EXECUTE}
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
