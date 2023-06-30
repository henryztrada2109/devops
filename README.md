# DevOps

### Package stack
    aws cloudformation package --template-file root.yaml --output-template-file root.yaml --s3-bucket cloudformation-files-devops --s3-prefix devops --profile sitecode

### Deploy
    aws cloudformation deploy --template-file root.yaml --stack-name devops --parameter-overrides ResourcePrefix=devops KeyNameJenkins=sitecode --capabilities CAPABILITY_IAM CAPABILITY_NAMED_IAM CAPABILITY_AUTO_EXPAND --profile sitecode  
