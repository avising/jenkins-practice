pipeline {

  environment {
    mysql_new_user = "root"
    mysql_new_user_password = "avinashsingh"
  }

  parameters {
    choice(name: 'TASK',choices: ['task_1','task_2','task_3'],description: "task number are according to assignment details")
  }

   agent any
  
  stages {
    
    
    stage('task1') {
      when {
        expression {
          ${params.TASK} == 'task_1'}
      }
      steps {
        echo "testing the task1 with ${mysql_root_user}"
        withCredentials([
          usernamePassword(credentials: 'database-credentilas', usernameVariable: USER, passwordVariable: PWD) ])
        {
          sh "some script ${USER} ${PWD}"
      }}
    }
    
    stage('task2') {
            when {
        expression {
          ${params.TASK} == 'task_2'}
      }
      steps{
        script {
            echo "testing the task2"
           withCredentials([
          usernamePassword(credentials: 'database-credentilas', usernameVariable: USER, passwordVariable: PWD) ])
        {
          sh "some script ${USER} ${PWD}"
      }
        }
      }
    }
    
    stage('task3') {
            when {
        expression {
          ${params.TASK} == 'task_3'}
      }
      steps{
        script {
            echo "testing the task3" 
           withCredentials([
          usernamePassword(credentials: 'database-credentilas', usernameVariable: USER, passwordVariable: PWD) ])
        {
          sh "some script ${USER} ${PWD}"
      }

          }
        }
      }        

  }  
}
