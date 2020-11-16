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
        sh "mysql -u root -pavinashsingh -D testdb -e 'INSERT INTO contact (Firstname, Lastname,Phone,Mobile, email) VALUES ("Cardinal","Erichsen","Skagen 21","Stavanger","4006");'"
        
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
