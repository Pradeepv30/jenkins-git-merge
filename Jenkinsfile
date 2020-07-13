pipeline {

    agent any

    stages {

        stage("Interactive_Input") {
            steps {
                script {

                    // Variables for input
                    def inputRepo
                    def inputBranch

                    // Get the input
                    def userInput = input(
                            id: 'userInput', message: 'Enter Repo and Branch:?',
                            parameters: [

                                    string(defaultValue: 'None',
                                            description: 'Path of config file',
                                            name: 'Repo'),
                                    string(defaultValue: 'None',
                                            description: 'Test Info file',
                                            name: 'Branch'),
                            ])

                    // Save to variables. Default to empty string if not found.
                    inputRepo = userInput.Repo?:''
                    inputBranch = userInput.Branch?:''

                    // Echo to console
                    echo("IQA Sheet Path: ${inputRepo}")
                    echo("Test Info file path: ${inputBranch}")

                }
            }
        }
    }
}