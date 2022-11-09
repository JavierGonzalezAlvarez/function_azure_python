## install Azure Functions Core Tools

$ curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
$ sudo mv microsoft.gpg /etc/apt/trusted.gpg.d/microsoft.gpg
$ sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-$(lsb_release -cs)-prod $(lsb_release -cs) main" > /etc/apt/sources.list.d/dotnetdev.list'
$ sudo apt-get update
$ sudo apt-get install azure-functions-core-tools-4

## create virtualenv on linux, version 3.7
$ virtualenv entorno_virtual -p python3.7

## activate virtualenv on linux
$ source entorno_virtual/bin/activate

$ func init CopyTransactionTriger --python
$ cd CopyTransactionTriger
$ func new --name LocalFunction --template "HTTP trigger" --authlevel "anonymous"

$ sudo apt install python3.7-distutils

# install requirements.txt
$ pip install -r requirements.txt

# run function
from functionAzure_test folder
$ func init
choose: python

$ func start
