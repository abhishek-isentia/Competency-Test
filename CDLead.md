# Coding challenge
This page consists a challenge for Continuous Delivery Lead role at Isentia.

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


# Challenge - Bootstrap Build Job

You are suppose to create a Jenkins Job,

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

# Challenge - Continuous Delivery Workflow

You are suppose to create a Jenkins Continuous Delivery Workflow,

- Install the Build Pipeline Plugin and Parameterized Trigger Plugin
- Break the above job in two Jenkin jobs: 1) Bootstrap static build job 2) Bootstrap static deployment to S3 job
- Job 1 will use `Trigger parameterized build on other projects` post-build action to trigger job 2
- Approproate build parameters from job 1 to job 2 should be passed to make sure that `version.txt` created by job 2 has both Jenkins job name and build number from job 1

## Details

- Use Amazon EC2 for hosting Jenkins server. 
- For new users, AWS [offers Free tier](https://aws.amazon.com/free/)
- Once test is completed please share the Jenkins (IP/Port/Domain) and S3 Bucket URL with Isentia team
- If Jenkins is login protected create an admin user for iSentia and share username and password

# Bonus Point
If you use the [Jenkins Pipeline job](https://github.com/jenkinsci/workflow-plugin/blob/master/TUTORIAL.md) to create the job
