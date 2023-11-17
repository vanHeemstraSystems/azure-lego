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

You will be promted as follows:

```
Initializing the backend...

Initializing provider plugins...
- Finding hashicorp/azurerm versions matching "~> 1.3"...
- Finding latest version of cloudflare/cloudflare...
- Installing hashicorp/azurerm v1.44.0...
- Installed hashicorp/azurerm v1.44.0 (signed by HashiCorp)
- Installing cloudflare/cloudflare v4.19.0...
- Installed cloudflare/cloudflare v4.19.0 (self-signed, key ID ###################)

Partner and community providers are signed by their developers.
If you'd like to know more about provider signing, you can read about it here:
https://www.terraform.io/docs/cli/plugins/signing.html

Terraform has created a lock file .terraform.lock.hcl to record the provider
selections it made above. Include this file in your version control repository
so that Terraform can guarantee to make the same selections by default when
you run "terraform init" in the future.

Terraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.
```

Great, now you’re ready to tweak our terraform to your liking and see what affects your changes will have using the ```terraform plan``` command.
