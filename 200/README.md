# 200 - Requirements

Before we start, you need the following:

1. A domain name. We used [freenom.com](http://freenom.com/) in this example, and created ```serverlessexample.ga```
2. git for source control
Ensure you have the Azure CLI utilities. 
On OSX with Homebrew: brew install azure-cli
Login to Azure on the command line: az login
Ensure your Default Azure subscription is what you want to use for this. See great instructions in terraform docs here.
Clone the sample code repo: 
git clone git@github.com:dcolebatch/azure_serverless_example.git
Initialize your terraform, which downloads any providers we depend on: terraform init
Great, now you’re ready to tweak our terraform to your liking and see what affects your changes will have using the terraform plan command.
