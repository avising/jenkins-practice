pipeline {

  environment {
    mysql_new_user = "root"
    mysql_new_user_password = "avinashsingh"
  }

  parameters {
    choice(name: 'TASK',choices: ['task_1','task_2','task_3'],description: 'task number are according to assignment details')
  }

   agent any
  
  stages {
    
    
    stage("task1") {
      when {
        expression {
          params.TASK == "task_1"}
      }
      steps {
        echo "Running task 1"
        sh "mysql -h localhost -uroot -pavinashsingh contact -e 'INSERT INTO contact VALUES ('Avinash','Singh','9999999999','9999999999','avi@gmail.com');' "
        
      }
    }
    
    stage("task2") {
       when {
        expression {
          params.TASK == "task_2"}
      }
      steps{
        script {
            echo "testing the task2"
           
        }
      }
    }
    
    stage("task3") {
            when {
        expression {
          params.TASK == 'task_3'}
      }
      steps{
        script {
            echo "testing the task3" 
        
          }
        }
      }        

  }  
}
