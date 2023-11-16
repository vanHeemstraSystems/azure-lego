# 200 - Requirements

Before we start, you need the following:

1. A domain name. You could use [freenom.com](http://freenom.com/) for example. We created ```ascode.app```
2. [git](https://git-scm.com/) for source control
3. Ensure you have the [Azure CLI utilities](https://github.com/Azure/azure-cli).<br/> 
On OSX with [Homebrew](https://brew.sh/): ```$ brew install azure-cli```<br/>
On Linux with [Install Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=apt): ```$ curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash```
4. Login to Azure on the command line: ```az login``` or alternatively ```$ az login --use-device-code --allow-no-subscriptions```
5. Ensure your Default Azure subscription is what you want to use for this. *See great instructions in [terraform docs](https://www.terraform.io/docs/providers/azurerm/authenticating_via_azure_cli.html) here*.
6. Clone the sample code repo: <br/>
```$ git clone git@github.com:ascode-app/lego-as-code.git``` or alternatively ```$ git clone https://github.com/ascode-app/lego-as-code.git```
7. If not already installed (```$ terraform -v```), [install Terraform](https://developer.hashicorp.com/terraform/install) as follows: <br/>On Linux Ubuntu: <br/>```$ wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg```<br/>
```$ echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list```<br/>
```$ sudo apt update && sudo apt install terraform```
8. Initialize your terraform, which downloads any providers we depend on: ```$ cd lego-as-code/setup```<br/>```$ terraform init```

Great, now you’re ready to tweak our terraform to your liking and see what affects your changes will have using the ```terraform plan``` command.
