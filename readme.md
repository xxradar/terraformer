## Terraformer 
https://github.com/GoogleCloudPlatform/terraformer <br>
https://github.com/GoogleCloudPlatform/terraformer/blob/master/docs/aws.md <br>

## Install
```
export PROVIDER=all
curl -LO https://github.com/GoogleCloudPlatform/terraformer/releases/download/$(curl -s https://api.github.com/repos/GoogleCloudPlatform/terraformer/releases/latest | grep tag_name | cut -d '"' -f 4)/terraformer-${PROVIDER}-linux-amd64
chmod +x terraformer-${PROVIDER}-linux-amd64
sudo mv terraformer-${PROVIDER}-linux-amd64 /usr/local/bin/terraformer
```
``` 
terraformer version
```
## Import and save to Terraform template
```
terraformer import aws --resources=vpc,subnet  --regions=eu-west-3
```
