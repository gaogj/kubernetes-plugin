    properties([gitLabConnection(''), 
        parameters([
            [$class: 'ChoiceParameter', 
            choiceType: 'PT_SINGLE_SELECT', 
            description: '选择branch将通过分支进行构建，选择tag将使用已构建tag部署', 
            filterLength: 1, 
            filterable: false, 
            name: 'Git_Source', 
            randomName: 'choice-parameter-24003326574975', 
            script: [$class: 'GroovyScript', 
                fallbackScript: [classpath: [], 
                    sandbox: false, script: ''], 
                    script: [classpath: [], 
                    sandbox: true, 
                    script: '''return[
                        \'branch\',
                        \'tag\'
                        ]''']]], 

            [$class: 'CascadeChoiceParameter',
            choiceType: 'PT_MULTI_SELECT', 
            description: '', 
            filterLength: 1, 
            filterable: true, 
            name: 'Choose', 
            randomName: 'choice-parameter-24003331033475', 
            referencedParameters: 'Git_Source', 
            script: [$class: 'GroovyScript', 
                fallbackScript: [classpath: [], 
                    sandbox: false, 
                    script: ''], 
                    script: [classpath: [], 
                        sandbox: true, 
                        script: '''if (Git_Source.equals("branch")) {
                              return ["Barretos", "Sao Paulo", "Itu"]
                            } else if (Git_Source.equals("tag")) {
                              return ["Rio de Janeiro", "Mangaratiba"]
                            } else {
                              return ["Unknown state"]
                            }''']]]])])
@echo off
echo GIT_COMMIT %GIT_COMMIT% 
echo GIT_BRANCH %GIT_BRANCH%
echo GIT_LOCAL_BRANCH %GIT_LOCAL_BRANCH%
echo GIT_PREVIOUS_COMMIT %GIT_PREVIOUS_COMMIT%
echo GIT_PREVIOUS_SUCCESSFUL_COMMIT %GIT_PREVIOUS_SUCCESSFUL_COMMIT%
echo GIT_URL %GIT_URL%
echo GIT_URL_N - %GIT_URL_N%
echo GIT_AUTHOR_NAME %GIT_AUTHOR_NAME%
echo GIT_COMMITTER_EMAIL %GIT_COMMITTER_EMAIL%
