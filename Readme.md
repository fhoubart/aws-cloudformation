# Deploy a Cloudformation Stack via Github

* The cloudformation stack is in cf1 folder and takes some parameters

* The stack is deployed with Github Actions and GitHub AWS action template for cloudformation. It can run in two different configuration :

  - in a GitHub hosted runner with AWS ServiceAccount keys
  - in a self-hosted runner that runs on a EC2 instance with the appropriate role to manage cloudformation stacks
 
To switch between the two configuration, comment or uncomment the keys in the `.github/workflows/cf.yml` pipeline file.

The Stack parameters are hardcoded in the pipeline file. It requires:

- an existing EC2 SSH key pair named `keypair`
- all resources created in the `us-east-1` region

