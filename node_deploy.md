This section is about deploying node express API's on Elastic Beanstalk with CI/CD.

Please review my folder structure before starting.

![folder-structure](nodedeploy/FolderStructure.png)

(We need a package.json on the Root Directory because our Elastic Beanstalk will scan through it.)

## Step 1. (Login to the AWS Console First...) Click on the services tab and click elastic beanstalk

![step-1](nodedeploy/Step1.png)

## Step 2. Click create new application.

![step-2](nodedeploy/Step2.png)

## Step 3. Give it a name

![step-3](nodedeploy/Step3.png)

## Step 4. Now that you created a new beanstalk application create a environtment for it!

![step-4](nodedeploy/Step4.png)

## Step 5. Choose Web Server Environment.

![step-5](nodedeploy/Step5.png)

## Step 6. Make sure you create a preconfigured platform and click NodeJS You can also add your app name and your custom domain if you want to then click create environment.

![step-6](nodedeploy/Step6.png)

_Now we will get started on deploying code with continous deployment into our environment!_

## Step 7. Click services and find AWS Codepipeline

![step-7](nodedeploy/Step7.png)

## Step 8. Create a new pipeline! (Keep in mind that the pipeline is going to be our CI/CD).

![step-8](nodedeploy/Step8.png)

## Step 9. Add a name to the pipeline and leave the advanced settings to default.

![step-9](nodedeploy/Step9.png)

## Step 10. Add a source! Click github as a source provider and Choose your repository and branch you want to deploy and choose github webhooks. So you will trigger deployment when something gets pushed or merged to the repo.

![step-10](nodedeploy/Step10.png)

## Step 11. SKIP THE BUILD STAGE

![step-11](nodedeploy/Step11.png)

## Step 12. Choose AWS Elastic Beanstalk as your deploy provider choose a region choose your NewApp created and choose your NewApp ENV with nodeJS installed to it!

![step-12](nodedeploy/Step12.png)

## Step 13. Review and Create the Pipeline!

![step-13](nodedeploy/Step13.png)

### Made by Carlo Clamucha. Feel free to DM me in slack for more info
