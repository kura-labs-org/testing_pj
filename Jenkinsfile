pipeline {
  agent any
   stages {
    stage ('InputOpt') {
      steps {
       input(message: 'Welcome would you like to continue? ', ok: 'continue')
     }
   }
    stage ('GitHub update stagging') {
      steps {
        sh '''#!/bin/bash
          git config user.email admin@example.com
          git config user.name ty
          git add .
          git commit -m 'Triggered Build: $BUILD_NUMBER'
          git push 
        ''' 
      }
    }
   
  }
 }
