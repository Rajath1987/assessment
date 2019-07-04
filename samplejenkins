node {
    def app

    stage('Clone repository') {
         checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("Rajath1987/assessment")
    }

   
    stage('Push image') {
            sh ' docker login -u Rajath1987 -p Settykoppa@123'
            app.push("${env.BUILD_NUMBER}")
            app.push("latest")
       /* }*/
    }
}
