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


# Challenge - Jenkins Bootstrap Build Job

You are suppose to create a Jenkins job which will

- Luanch a Ubuntu Amazon EC2 instance (`t2.micro`) with an Elastic IP
- SSH on the server and install Jenkins
- Setup appropriate Jenkins permission, users and roles
- Secure your server using EC2 security groups
- Install NodeJS, Grunt, Bower, Jekyll, etc. on the server
- Create a new Jenkins Freestyle Project job or Jenkins [Pipeline](https://wiki.jenkins-ci.org/display/JENKINS/Pipeline+Plugin) job
- Clone the Bootstrap Git repository using SSH endpoint (`git@github.com:twbs/bootstrap.git`)
- Add the build step Execute shell command `jekyll build` in root directory
- Build step will create a new folder `_gh_pages`
- Drop a `version.txt` file in the `_gh_pages` which includes jenkins job name and build number
- Add a Post-build action `Publish artifacts to S3 Bucket` using the [S3 Plguin](https://wiki.jenkins-ci.org/display/JENKINS/S3+Plugin)
- Create a Amazon S3 Bucket, enable static website hosting and add appropriate bucket policy
- `Publish artifacts to S3 Bucket` should copy content of the `_gh_pages` to your S3 bucket
- Run the build job and you should see a Bootstrap static website similar to [this](http://getbootstrap.com/) on your S3 bucket URL

## Details

- Use Amazon EC2 for hosting Jenkins server. 
- For new users, AWS [offers Free tier](https://aws.amazon.com/free/)
- Once test is completed please share the Jenkins (IP/Port/Domain) and S3 Bucket URL with iSentia team
- If Jenkins is login protected create an admin user for iSentia and share username and password

# Bonus Point
If you use the [Jenkins Pipeline job](https://github.com/jenkinsci/workflow-plugin/blob/master/TUTORIAL.md) to create the job
