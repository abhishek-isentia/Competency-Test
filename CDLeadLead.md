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
- Use Amazon EC2 for hosting Jenkins server. For new users, AWS [offers Free tier](https://aws.amazon.com/free/)
- Customise the your Ubuntu server according to your need - you will need NodeJS, Grunt, Bower and Jekyll installed on the server
- Candidate should put their test results on a public Jenkins server
- Once test is completed please share the Jenkins URL to hiring team so they can review your work

# Challenge - Jenkins Build Job

You are suppose to create a Jenkins job which will

- Luanch a Ubuntu Amazon EC2 instance (`t2.micro` is fine) with Elastic IP
- SSH on the server and install Jenkins as described here
- Create a new Jenkins Freestyle Project job or Jenkins Pipeline job
- Clone the Bootstrap Git repository using SSH endpoint (`git@github.com:twbs/bootstrap.git`)
- Run the build step which shell commands `npm install`, `grunt dist`, `grunt docs`, `jekyll build`

## Details



