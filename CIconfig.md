#  Link to my MVP application serving a static HTML page
http://default-environment.4uijy9uppx.eu-west-2.elasticbeanstalk.com/

##  Brief description of my CD technology 
I'm be using GitHub, AWS CodePipeline and AWS Elastic Beanstalk to create a deployment pipeline for a my website This allows the website to be updated automatically every time I change my code. 

## How I setup and configure my build jobs 
After creating this repository on github with a simple php file saying "Hello World!". 

I. Setting Up the Deployment Environment
This environment is where the CodePipeline will deploy my code.
First I created an Elastic Beanstalk PHP application and an Elastic Beanstalk web server environment.
For my environment type, I chose Load Balancing, auto scaling. [1]

 II. Created and Configured AWS CodePipeline
After creating the pipeline and given it a name, I set my source provider - Github and pointed to my repository : https://github.com/UsagiBo/HackernewsProj . I added Jenkins as my build provider and AWS Elastic Beanstalk as deployment provider. I ponted to my application I created earlier. The last step was to create AWS service role which gives me premission to access resources on my account.[2]
 
 References
 1. Environment Types (Dec, 2017) https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features-managing-env-types.html
 2. IAM Roles (Dec, 2017) https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html
