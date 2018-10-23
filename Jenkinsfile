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

	echo "gitlabBranch: ${env.gitlabBranch}"
	echo "gitlabActionType: ${env.gitlabActionType}"
	echo "gitlabUserName: ${env.gitlabUserName}"
	echo "gitlabUserEmail: ${env.gitlabUserEmail}"

	echo "gitlabSourceBranch: ${env.gitlabSourceBranch}"
	echo "gitlabSourceRepoHomepage: ${env.gitlabSourceRepoHomepage}"
	echo "gitlabSourceRepoName: ${env.gitlabSourceRepoName}"
	echo "gitlabSourceNamespace: ${env.gitlabSourceNamespace}"
	echo "gitlabSourceRepoURL: ${env.gitlabSourceRepoURL}"
	echo "gitlabSourceRepoSshUrl: ${env.gitlabSourceRepoSshUrl}"
	echo "gitlabSourceRepoHttpUrl: ${env.gitlabSourceRepoHttpUrl}"

	echo "gitlabMergeRequestTitle: ${env.gitlabMergeRequestTitle}"
	echo "gitlabMergeRequestDescription: ${env.gitlabMergeRequestDescription}"
	echo "gitlabMergeRequestId: ${env.gitlabMergeRequestId}"
	echo "gitlabMergeRequestIid: ${env.gitlabMergeRequestIid}"
	echo "gitlabMergeRequestLastCommit: ${env.gitlabMergeRequestLastCommit}"

	echo "gitlabTargetBranch: ${env.gitlabTargetBranch}"
	echo "gitlabTargetRepoName: ${env.gitlabTargetRepoName}"
	echo "gitlabTargetNamespace: ${env.gitlabTargetNamespace}"
	echo "gitlabTargetRepoSshUrl: ${env.gitlabTargetRepoSshUrl}"
	echo "gitlabTargetRepoHttpUrl: ${env.gitlabTargetRepoHttpUrl}"

	echo "gitlabBefore: ${env.gitlabBefore}"
	echo "gitlabAfter: ${env.gitlabAfter}"
	echo "gitlabTriggerPhrase: ${env.gitlabTriggerPhrase}"
	echo "------------------printPipelineEnv-start--------------"

	echo "BRANCH_NAME:${env.BRANCH_NAME}"

	echo "BUILD_ID:${env.BUILD_ID}"
	echo "BUILD_NUMBER:${env.BUILD_NUMBER}"
	echo "BUILD_DISPLAY_NAME:${env.BUILD_DISPLAY_NAME}"
	echo "BUILD_TAG:${env.BUILD_TAG}"
	echo "BUILD_URL:${env.BUILD_URL}"

	echo "CHANGE_ID:${env.CHANGE_ID}"
	echo "CHANGE_TYPE:${env.CHANGE_TYPE}"
	echo "CHANGE_URL:${env.CHANGE_URL}"
	echo "CHANGE_TITLE:${env.CHANGE_TITLE}"

	echo "CHANGE_AUTHOR:${env.CHANGE_AUTHOR}"
	echo "CHANGE_AUTHOR_DISPLAY_NAME:${env.CHANGE_AUTHOR_DISPLAY_NAME}"
	echo "CHANGE_AUTHOR_EMAIL:${env.CHANGE_AUTHOR_EMAIL}"
	echo "CHANGE_TARGET:${env.CHANGE_TARGET}"

    echo "USER_ID:${env.USER_ID}"
