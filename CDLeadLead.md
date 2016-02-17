# Coding challenge
This page consists a challenge for Continouse Delivery Lead role at iSentia.

# Purpose
Aim of this test is three fold,

- evaluate your Jenkins abilities 
- judge your technical experince with CI/CD
- understand how you automation design experince 

# How you will be judged
You will be scored on,

- quality of your Jenkins job
- your overall scripting experince

# Intructions

- Please use Jenkins and you can install any Jenkins plugin
- You can use Groovy, Bash, Python, Ruby or any other scripting framework if required


# Challenge - Jenkins Build Job

You are suppose to create a Jenkins job which will

- Luanch a Ubuntu Amazon EC2 instance (`t2.micro`) with an Elastic IP
- SSH on the server and install Jenkins
- Install NodeJS, Grunt, Bower and Jekyll on the server
- Create a new Jenkins Freestyle Project job or Jenkins Pipeline job
- Clone the Bootstrap Git repository using SSH endpoint (`git@github.com:twbs/bootstrap.git`)
- Add the build step Execute shell commands  `npm install`, `grunt dist`, `grunt docs`, `jekyll build`
- Build step will create a new folder `_gh_pages`
- Add a Post-build action Publish artifacts to S3 Bucket using the [S3 Plguin](https://wiki.jenkins-ci.org/display/JENKINS/S3+Plugin)
- Create a Amazon S3 Bucket, enable static website hosting and add appropriate bucket policy
- Copy content of the `_gh_pages` to your S3 bucket and share the 

## Details

- Use Amazon EC2 for hosting Jenkins server. 
- For new users, AWS [offers Free tier](https://aws.amazon.com/free/)
- Once test is completed please share the Jenkins and S3 Bucket URL with iSentia team


