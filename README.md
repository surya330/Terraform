# Terraform Commands

**terraform -help:** It'll list all the available execution commands. It shows primary workflow commands first and less commonly used commands second.

**terraform version:** It'll give the version of current terraform you're using and let you know whether there is any latest version/update of terraform is avaiable or not.

**terraform init:** It'll prepare our working directory to use terraform by initializing the backend, installing plugins and child modules. This is the first command you need to run after writing the new configuration file. It is safe to run this command multiple times. It'll intialize the backend to store the state locally, so
that multiple people can access and work on it.

**terraform fmt:** It'll format our configuration file with Hashicorp Configuration Language(HCL) standard.

**terraform fmt -diff:** It'll display the differences between original configuration files and formatting changes.

**terraform validate:** It'll validate the syntax of configuration files and display warnings or errors if any files contains invalid syntax.

**terraform plan:** It'll generate an execution plan and displays all the actions that are going to be performed.

**terraform plan -out=<path>:** It'll save the plan file to a given path. + indicates the creation of resource. - indicates destruction of resource. -/+ indicates replacement of resource.
  
**terraform apply:** It'll actually perform the planned actions and will create or update the infrastrucute.

**terraform apply -auto-approve:** It'll apply changes automatically without manually typing 'yes' to the plan.
  
**terraform destroy:** It'll destroy or delete the infrastrucutre managed by terraform, It's exactly opposite of apply command.
  
**terraform taint <resource_type.name>:** It informs terraform that this resource is damaged or degraded and marks it as tainted, so that It'll get replaced whenever the next apply command is executed.
  
**terraform untaint <resource_type.name>:** Untaint the already tainted resource.

**terraform state list:** It'll display all the resources in the current state file.
  
**terraform state push:** It'll update terraform state file from local to remote.
  
**terraform state show <resourcename>:** It'll display the specified resource in the terraform state file.

**terraform output:** It'll list all the outputs of the current state and by default it'll display the output at the end of apply command.
  
**terraform console:** It'll be useful for testing on the interactive console rusing command line.
  
**terraform providers:** It'll provide the list of providers that are required.

#Terraform Q&A#

<details>
<summary>What are terraform variables ?</summary>
<br>
Terraform variables are used to store the values which can be used throughout the configuration file.
</details>
