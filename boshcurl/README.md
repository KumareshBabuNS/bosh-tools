# boshcurl

A Bosh curl tool created following the steps described in the following blog entry:
[https://blog.starkandwayne.com/2016/04/02/whats-failing-in-my-bosh-deployment/]

Copy boshcurl to your local machine in a directory that is part of your PATH.

Issue the boshcurl command to get instructions on the three environment variables
required to be defined to run the script. Example:
- export bosh_target=https://10.58.111.45:25555  
- export bosh_username=admin  
- export bosh_password=admin

The available commands are:
- boshcurl /deployments
- boshcurl /info
- boshcurl /tasks

Please refer to the blog entry above for more examples on how to use the tool.
