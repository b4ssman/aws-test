This YouTube video is extremely useful

### AWS CDK deploy Hugo site
https://www.youtube.com/watch?v=HDpnVuj6gUY

### General AWS CDK Stuff
https://www.youtube.com/watch?v=Cf3yJv3klsg
https://www.youtube.com/watch?v=1ps0Wh19MHQ

### Circle CI Stuff

#### General Circle CI Pipeline
https://www.youtube.com/watch?v=WDy4-m4V76Q

#### Circle CI Windows
https://www.youtube.com/watch?v=stsLkbiskiM



## Prereq
1. Configure ~/.aws/config with named profile
2. Configure ~/.aws/credentials with access key id and secret
3. `export AWS_PROFILE=<named profile>`

## Steps
1. Create root directory for static HTML and CDK code
2. cd into the dir to contain the CDK code
3. run `cdk init --language python`
4. enable python venv `source .venv/bin/activate`
4. run `pip install -r requirements.txt`
5. run `cdk bootstrap -b <bucket name>`
6. update `setup.py` line 22 requirements with "aws-cdk.aws_s3" then re run step 4.

## Testing
`cdk ls` - This will run through the code and test syntax
`cdk synth` - This will create Cloud Formation code (not necessary as this is done in app.py but good practice for testing)
`cdk diff` - This is similar to terraform plan and will show what CDK is going to deploy

## Deploy
1. `cdk deploy` - Will prompt to confirm changes
2. cd to dir where site code is build (for Hugo this is /public) and run `aws s3 sync <html dir>/ s3://<bucket name> --acl public-read` 

