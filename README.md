# Cloud Corporation for Linux Developers
Details the corporation inside of cloud.

The cloud is the most popular shaped of machines conected in P2P or maybe told M2M, the proof is one features in the long bond of people conected in the world.
Then am explain the companies within the hierarchy and its dashboards. Am wrote from Mayor University for test only and the cash is non scalable solution for data protected.


| Companies		                | Description						                                | URL           		   	                          |
| ----------------------------| ------------------------------------------------------|-------------------------------------------------|
| AWS 			                  | AWS & Microsoft make and alliance for SQL Server and virtual Machines 				                        |https://aws.amazon.com/es/                 			|
| Kubernetes 		              | Virtual Machines run over Docker 				                        |https://kubernetes.io/ 			                                          |
| SAP			                    | Germany Software for ERP                							                        |	https://account.hanatrial.ondemand.com	                  	        |
| Azure Microsoft 	          | Database, Shell and Programming software  |	https://portal.azure.com	                  	|
| IBM 			                  | IBM is excluded since 29 March 2019 of UK		          | https://idaas.iam.ibm.com            		    	|
| Twilio Cloud		            | Communication API (SMS and Call) Developers                                        							|	https://www.twilio.com	                  	|
| Zeit			                  |	DNS application for Web Services						                                          |https://zeit.co/			                  |
| GitKraken		                | Dashboards for planification, Support GitHub 							                                        |https://app.gitkraken.com/glo/                  	|
| Docker		                  | Containers SDKs for run in Virtual Machines							                                          |https://cloud.docker.com			                  |
| Visual Studio		            |	Software for Developers. Some Lenguages (C,C++,C#, Java, Python, JS)						                                          |https://app.vssps.visualstudio.com 		                	|
| ElasticSearch		            | Server's Monitor							                                          |	https://www.elastic.co		                  |
| OpenShift		                |	Red Hat Plataform						                                          |	https://manage.openshift.com/		                  |
| Google Cloud                | Shell and scalables solution for Android and the Cloud                                                      |https://console.cloud.google.com                       |

# Next Step
Also view information in the next bond
[Cloud on Ubuntu](https://github.com/malejandromorenov/cloudubuntu)

Only try running in the shell for complete the process and once finished please restart the machine.

# Step Two
Learn and choice your preference in the cloud and develope for them.

# Step Three
Install each line with the shell. The stairsway in the process is success when your needs are organizate in your brain. Corporation is the progress in the capital line for the society are only most important that government. Almost your heads is basically. "i wish" "i need" the propietary is your OS.
I will try to be honest neutro in the order, the price is tax.

# Step Four
## a) Amazon Service Cloud
```shell
pip install awscli --upgrade --user

```
## b) Azure DB for Microsoft
```shell
AZ_REPO=$(lsb_release -cs)
echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
sudo tee /etc/apt/sources.list.d/azure-cli.list
sudo curl -L https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
sudo sudo apt-get update
sudo apt-get install apt-transport-https azure-cli

```
## c) SAP
Visit
https://tools.hana.ondemand.com/#

## d) IBMCloud
```shell
curl -fsSL https://clis.cloud.ibm.com/install/linux | sh
ibmcloud plugin repo-plugins -r 'IBM Cloud'

git clone https://github.com/malejandromorenov/cloudcorp
cd cloudcorp
sudo bash ibm-script.sh
apt-get update

```

## e) Twilio
```python
from twilio.rest import Client

# Your Account SID from twilio.com/console
account_sid = "AC737898c42503d9cdc285205b1e98b99f"
# Your Auth Token from twilio.com/console
auth_token  = "your_auth_token"

client = Client(account_sid, auth_token)

message = client.messages.create(
    to="+15558675309", 
    from_="+15017250604",
    body="Hello from Python!")

print(message.sid)
```
###### Install the Library
The easiest way to install the library is from PyPi using pip, a package manager for Python. Simply run this in the terminal:
```python
pip install twilio
If you get a pip: command not found error, you can also use easy_install. Run this in your terminal:.

easy_install twilio
```

###### Manual Installation
Or, you can download the source code (ZIP) for twilio-python, and then install the library by running:
```python
python setup.py install
```
in the folder containing the twilio-python library.

"Permission Denied"
If the command line gives you a big long error message that says Permission Denied in the middle of it, try running the above commands with sudo (e.g. sudo pip install twilio).

###### Test Your Installation
Try sending yourself an SMS message. Save the code sample on this page to your computer with a text editor. Be sure to update the account_sid, auth_token, and from_ phone number with values from your Twilio account. The to phone number can be your own mobile phone.

Save the file as send_sms.py. In the terminal, cd to the directory containing the file you just saved then run:
```python
python send_sms.py
You should receive the text message on your phone.
```

Using this Library
Authenticate Client
```python
from twilio.rest import Client

account_sid = "AC737898c42503d9cdc285205b1e98b99f"
auth_token = "your_auth_token"
client = Client(account_sid, auth_token)
```

Create a New Record
```python
from twilio.rest import Client

account_sid = "AC737898c42503d9cdc285205b1e98b99f"
auth_token = "your_auth_token"
client = Client(account_sid, auth_token)

call = client.calls.create(
    to="+14155551212",
    from_="+15017250604",
    url="http://demo.twilio.com/docs/voice.xml"
)

print(call.sid)
```

###### Get Existing Record
```python
from twilio.rest import TwilioRestClient

account_sid = "AC737898c42503d9cdc285205b1e98b99f"
auth_token = "your_auth_token"
client = TwilioRestClient(account_sid, auth_token)

call = client.calls.get("CA42ed11f93dc08b952027ffbc406d0868")
print(call.to)
```
###### Iterate Through Records
```python
from twilio.rest import Client

account_sid = "AC737898c42503d9cdc285205b1e98b99f"
auth_token = "your_auth_token"
client = Client(account_sid, auth_token)

for sms in client.messages.list():
    print(sms.to)
```
## d) Docker Containers
```bash
sudo apt-get update
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo apt-key fingerprint 0EBFCD88
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
sudo apt-get install docker-ce docker-ce-cli containerd.io
apt-cache madison docker-ce
sudo docker run hello-world
```
## d) Google CLoud
Create an environment variable for the correct distribution:
```bash
export CLOUD_SDK_REPO="cloud-sdk-$(lsb_release -c -s)"
```
Add the Cloud SDK distribution URI as a package source:
```bash
echo "deb http://packages.cloud.google.com/apt $CLOUD_SDK_REPO main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
```
Note: If you have apt-transport-https installed, you can use "https" instead of "http" in this step.
Import the Google Cloud public key:
```bash
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
```
Troubleshooting Tip: If you are unable to get latest updates due to an expired key, obtain the latest apt-get.gpg key file.
Update and install the Cloud SDK:
```bash
sudo apt-get update && sudo apt-get install google-cloud-sdk
```
Note: For additional apt-get options, such as disabling prompts or dry runs, refer to the apt-get man pages.
Optionally, install any of these additional components:
```bash
sudo apt-get install google-cloud-sdk-app-engine-python
sudo apt-get install google-cloud-sdk-app-engine-python-extras
sudo apt-get install google-cloud-sdk-app-engine-java
sudo apt-get install google-cloud-sdk-app-engine-go
sudo apt-get install google-cloud-sdk-datalab
sudo apt-get install google-cloud-sdk-datastore-emulator
sudo apt-get install google-cloud-sdk-pubsub-emulator
sudo apt-get install google-cloud-sdk-cbt
sudo apt-get install google-cloud-sdk-cloud-build-local
sudo apt-get install google-cloud-sdk-bigtable-emulator
sudo apt-get install kubectl
```
For example, the google-cloud-sdk-app-engine-java component can be installed as follows:
```bash
sudo apt-get install google-cloud-sdk-app-engine-java
```
Run gcloud init to get started:
```bash
gcloud init
```

# Step Five
Have peace and quite. This time is for developers and learn for the cloud, your are a server. Your totem is your label, your cheer up is only you. Better things incomming, the dead is the solution, the life is resurection and the moments in your life seem a monitor in sleep mode. But not worry more engineers work for this and your life is a volatil and your body and your soul is liberating for the universe.
Wait for the moment in your life with the computer like a couple and joy the threes. AUR
