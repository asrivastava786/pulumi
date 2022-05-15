pulumi new -y //create env setup selct language and Template

Pulumi stack ls // stack available

pulumi init test // initiate the new stack name test

pulumi stack select test //to select test stck

pulumi stack output --json // stack info

pulumi stack //all info about current stack and including info that hs been exported by stack

"//codes"
config = pulumi.Config();
numnode = config.require('numnode'); //require parameter
region = config.get('region'); // optional
db_cred = config.require_seceret('db-pass');

pulumi config set numnode 4// setting variable values numnode = 4

pulumi config set db-pass "pass123" --secret // 

pulumi stack export dev-stack.json // export settings

pulumi destoy --yes //delete all available resourse associated with stack

pulumi stack rm dev // remove stack dev

pip install pulumi_docker //

//setup local kubernities cluster
install kubectl
kubectl version --client

//kubernetes using mini kube locally
intall minikube
//setup kubertes cluster locally
minikube start


//new project kubernetes with pyhton, first create on pulumi dashboard
mkdir projectN-kubernetes-python && cd projectN-kubernetes-python //dir 

pulumi new kubernetes-python -s bobuser/projectN-kubernetes-python/dev  //pull down your project

kubectl get all //all running service 

kubectl port-forward service/service name 8080:80 //port forward to 8080


//setting up static website on AWS

//cmd locally to assign cred locally//
nano ~/.bash_profile
export AWS_ACCESS_KEY = ''
export AWS_SECRET_ACCESS_KEY = ''

 mkdir projectname && cd projectname
 pulumi new aws-python

//_main_.py codes
 
imort pulumi
from pulumi_aws import s3

#create an aws serouce bucket
bucket = s3.Bucket('projectName')

pulumi.export('bucketname', bucket.id)

//end










 







