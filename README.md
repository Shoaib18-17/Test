(app.js) -

const express = require('express');
const app = express();
app.get('/',(req,res) => {
res.send("Hello World, I am from Nodejs");
});
app.listen(3020,() => {
console.log("Server is running on port 3020")
});

(Pipeline for app.js) -

pipeline {
agent any
stages {
stage('Clone Repository') {
steps {
git branch: 'main', url: 'https://github.com/deepak574/nodejsexample.git'
}
}
stage('Install Dependencies') {
steps {
bat 'npm install'
}
}
stage('Run Application') {
steps {
bat 'node app.js'
}
}
}
}

(Git commands) -

1. cd e:
2. mkdir gitcommandsexe
3. cd gitcommandsexe
4. git init
5. git config user.email "alishoaib7864@gmail.com"
6. git config user.name "shoaib"
7. vim Sample.java - (press i to insert text)
8. // Sample.java
public class Sample {
    public static void main(String[] args) {
        System.out.println("Hello, I am Shoaib!");
    }
}
9. git add .
10. git commit -m "A Sample java program with content Shoaib"
11. git log --oneline
12. git remote add origin " -------------------------git hub url "
13. git branch -M main
14. git push -u origin main

