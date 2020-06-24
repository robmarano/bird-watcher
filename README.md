#Summer 2020 NYU SPS Python Diploma Capstone Course
## bird-watcher
Computer-based bird detection system that uses computer vision as primary input. The output will be an alert to what bird is feeding that food station.

## Quick Tutorial on Using Flask with jinja2 and Deploy to AWS

Following (AWS tutorial using Elastic Beanstalk)[https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create-deploy-python-flask.html]

### Step 0
Signup for AWS and get a free tier for 1 year

### Step 1
Install AWS CLI 2 and configure with you programmatic access

### Step 2
(Install EB CLI)[https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html#eb-cli3-install.scripts]

### Step 3
Using the initial bird-watcher code using branch "intro_to_flask"
Initialize the AWS Elastic Beanstalk environment in your AWS account
```bash
eb init -p python-3.7 bird-watcher --region us-east-1
```

### Step 4
Initialize your EB environment with a security keypair; don't choose to use CodeCommit (yet)
```bash
eb init
```

### Step 5
Create the EB environment in the AWS cloud with the command
```bash
eb create flask-env
```

### Step 6
After about 5 minutes or so, use the eb cli to open your browser and hit the flask site you just deployed:
```bash
eb open
```

### Step 7
In order to terminate your EB environment (remember it costs you money to keep it running, even if it's just minimal), run the following eb cli command
```bash
eb terminate flask-env
```

Next, you can connect your GitHub repo directory to the EB environment. See (this page)[https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb3-cli-git.html]



