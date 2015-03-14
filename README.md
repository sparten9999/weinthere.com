# weinthere.com
The site for the run.

## How to deploy
   1. install the `s3_website` gem
   2. make sure you have `S3_ID` and `S3_SECRET` defined in `.env` with permissions to push to the `weinthere.com`
   3. run `s3_website push`


## How to update cloudconfig
If for some reason you need to update the AWS stack. Update the `cloudconfig.json` file and run the following command using aws tools to push the update.

```bash
aws cloudformation update-stack --stack-name weinthere --template-body file://cloudformation.json --parameters ParameterKey=HostedZone,ParameterValue=weinthere.com
```
