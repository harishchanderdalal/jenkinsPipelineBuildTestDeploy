node('master') {

   stage 'Git Checkout'
   		git 'https://github.com/executeautomation/cucumberbasic.git'
         echo 'checkout done'
   
   stage 'Maven Validate'
   		sh 'mvn validate'
         echo 'maven validate'
   
   stage 'Maven Compile'
   		echo 'Maven Project Compile'

   stage 'Test Case'
    	echo 'Test Case will running'

   stage 'Reporting'
    	echo 'Reporting Getting Creating'

   stage 'Email Status'
      step([$class: 'Mailer', notifyEveryUnstableBuild: true, recipients: 'alert@harish.com', sendToIndividuals: false])
    	echo 'Notification Sending'            
}
