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





