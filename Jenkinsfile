podTemplate(containers: [
    containerTemplate(name: 'maven', image: 'maven:3.8.1-jdk-8', command: 'sleep', args: '99d'
  )]
  ) {

    node(POD_LABEL) {
        stage('Get a Maven project') {
//             git 'https://github.com/DelphineN/SpringDemo.git'
            container('maven') {
                stage('Build a Maven project') {
                    sh 'mvn clean package'
                }
            }
        }

    }
}
