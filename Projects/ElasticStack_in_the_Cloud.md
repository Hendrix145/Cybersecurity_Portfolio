ELK combines three technologies and provides a powerful solution when working with large data sets. In addition, we are able to setup SIEM rules to alert us as defenders to attacks on our organization.

E - Elasticsearch
L - Logstash
K - Kibana
ELK enables defenders to detect attacks and conduct threat hunting.

To learn ELK, we don't need several servers or to spend large sums of money. We can get into the driver's seat and experiment with ELK by using the Elastic Cloud 14-day trial. The trial does not require a credit card to get started. You only need an email and a password.

1. Set up an account.

https://cloud.elastic.co/registration?settings=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJsZW5ndGgiOjE1MCwic2l6ZSI6NDA5NiwiZGVmYXVsdF9zaXplIjoxMDI0fQ.dS6xqdrcNBVkANlcS19AnsZmHVSqoPROLHprdeN-Qbc&source=education

This link is for the trial sign up page. Start a trial by signing up.

![elk](https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/d2a4bfe8-47c9-4854-baa5-b138dfbf732a)

Watch your email for a confirmation. Click "Verify and Accept." You should be redirected to the cloud login page. If you're not redirected, you can find it here.

https://cloud.elastic.co/login

After logging in, the page will look like this.

Fill out the proper filed with the correct information pictured below and select the check boxes with red dots.

Once those fields are filled out click "Next"


<img width="248" alt="Capture1" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/22938bcc-e434-4f61-a76d-cf70e7b785e3">


2. Start an ELK instance.

Upon clicking next you will see the following page. For my instance I will be calling it "security-development. Make sure to enter the name of your deployment and click "Create Deployment".


<img width="433" alt="deployment2" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/7c5de5e4-a6fd-4356-b845-61382d0c5882">

Next we will see this page.

Elastic will present the credentials for this ELK stack. There is the option to download a CSV of the credentials. However you decide to hold onto these credentials, don't lose them.


<img width="396" alt="creds3" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/09396d70-f4de-4fa4-b45c-9cd3a81b226a">


Then we will need to wait for the continue button to turn blue, once that's done click continue

We will be greeted with menu of options, we want to skip that menu.


<img width="646" alt="skip_prompt5" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/0453c7ae-a010-4b91-8a5d-a819e2e54817">

Then at the top of the page we want to click search and type "kibana" and hit enter.


<img width="908" alt="kibana_search6" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/bac54461-f43e-4d93-8ed1-159a52987315">

Once the next page load we want to add kibana. Select "Add Kibana"


We will next be prompted to "Install Elastic Agent" This is what we are going to put on our machine that monitors what's happening. Click "Install Elastic Agent"



<img width="917" alt="kibana_loading8" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/6fc9a5e1-e1c2-4294-b860-ccbd5a4f46e9">



The next page we meet will have a wall of text. Select windows.

We will need to click the "Copy to Clipboard".



<img width="796" alt="windows_kibana" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/44408475-6983-4419-9b9e-9bf96799bd62">


Hold onto this command. It is recommended to paste this command into some file where you won't lose it. In this example, I saved it to a file I called "agent.txt." We will use this command later.


The ELK stack is now configured and we have our connection information saved. 


The Elastic Agent software enables users to easily send logs to our ELK instance, a process typically called "ingesting."



1. Download the Elastic Agent.

Press the windows button and type powershell, make sure to click "Run as Admin"



<img width="431" alt="powershell_kibana9" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/d3998353-56e9-4ea1-afac-2a02904b6447">



Once the powershell instance opens, copy what you kept in the file in my case it was "Agent.txt" and paste it into the powershell and hit enter.



<img width="520" alt="powershell" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/f0d50daa-6419-4b90-9146-d00ecf019a69">



Make sure you type y and hit enter when prompted by powershell.


Switch back over to your browser and you should see "1 Agent has been enrolled".



<img width="724" alt="finish_button" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/4cc344c0-cd7a-4eaf-8d04-d08e939cd365">


Then Click "Add to Integration".


2. Check The Fleet.

Once thats done we should be connected, But first lets make sure the device has successfully connected.


<img width="185" alt="fleet_loc" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/34e426dc-b351-41f6-8755-fab6c03a5d9e">




<img width="918" alt="pic_of_box" src="https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/b2d8c475-1f44-4b0b-8e04-42ccaeb3c332">



Our Elastic Agent is installed and configured to be connected to our ELK instance in the cloud. Next, we will cover how to configure Sysmon to submit logs to this Elastic Agent, which will ingest the logs to appear in Kibana.



By default, Windows logs are not ideal. To get logs that are more readable and useful, we can use Sysmon.

1. Download Sysmon

Follow this link to download Sysmon.


https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon


Find the "Download Sysmon" link


![sysmon_download](https://github.com/Hendrix145/Cybersecurity_Portfolio/assets/97060217/6dcfad7d-23e9-45fd-ac72-bfd27efd56d5)




