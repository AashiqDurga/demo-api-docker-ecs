aws cloudformation create-stack --template-body file://$PWD/infra/vpc.yml --stack-name demo-api-docker-ecs-vpc

aws cloudformation create-stack --template-body file://$PWD/infra/iam.yml --stack-name demo-api-docker-ecs-iam --capabilities CAPABILITY_IAM

aws cloudformation create-stack --template-body file://$PWD/infra/app-cluster.yml --stack-name demo-api-docker-ecs-cluster

aws cloudformation create-stack --template-body file://$PWD/infra/api.yml --stack-name demo-api-docker-ecs-api
