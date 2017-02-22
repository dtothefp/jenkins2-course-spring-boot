node {
    def project_path = 'spring-boot-samples/spring-boot-sample-atmosphere'

    stage('checkout') {
        git 'https://github.com/dtothefp/jenkins2-course-spring-boot.git'
    }

    dir(project_path) {
        stage('clean and package') {
            sh 'mvn clean package'
        }

        stage('archive') {
            archiveArtifacts 'target/*.jar'
        }
    }
}
