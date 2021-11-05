pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Clean') {
            steps {
                // Get some code from a GitHub repository
                //git 'https://github.com/eosnica/MSPR.git'
                // Run Maven on a Unix agent.
                //sh "mvn clean"
                
                //git 'https://github.com/eosnica/MSPR.git'
                bat echo 'bonjour'

                // To run Maven on a Windows agent, use
                dir('go-securi') {
                    bat "mvn -Dmaven.test.failure.ignore=true clean"
                }
                
            }
        }
        
        stage('Package') 
        {
            steps 
            {
                // Get some code from a GitHub repository
                //git 'https://github.com/eosnica/MSPR.git'

                // Run Maven on a Unix agent.
                //sh "mvn clean"

                // To run Maven on a Windows agent, use
                dir('go-securi') 
                {
                    bat "mvn -Dmaven.test.failure.ignore=true package"
                }
                
            }
        }
        
        stage('Install') 
        {
            steps 
            {
                // Get some code from a GitHub repository
                //git 'https://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@github.com/eosnica/MSPR.git'

                // Run Maven on a Unix agent.
                //sh "mvn clean"

                // To run Maven on a Windows agent, use
                dir('go-securi') 
                {
                    bat "mvn -Dmaven.test.failure.ignore=true install"
                }
                
            }
        }
        
        stage('Test') 
        {
            steps 
            {
                // Get some code from a GitHub repository
                //git 'https://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@github.com/eosnica/MSPR.git'

                // Run Maven on a Unix agent.
                //sh "mvn clean"

                // To run Maven on a Windows agent, use
                dir('go-securi') 
                {
                    bat "mvn -Dmaven.test.failure.ignore=true test"
                }
                
            }
        }
    }
}
