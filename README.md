# AWS Usage Alerts

Python program for send alerts for data transfer usage under free tier in aws to slack and also desktop notifications


## WARNING
This program uses Cost Explorer API which charges of $0.01 per request 

## Prerequisite:
pip install py-notifier
pacman -s aws-cli or apt-get install awscli

## Configure
* **Configure aws**
	aws configure

* **Configure Slack**
You can skip this step if you only want to receive desktop notifications. Just remove last line from program. Otherwise configure your slack bot using
https://github.com/Parveshdhull/slackbot
* **Configure filter.json**
filter.json file tells program which data to reterive using API. I tried different regions and value of USAGE_TYPE variable was different for different regions. You can find value of 'DataTransfer-Out-Bytes' for your region using
```aws ce get-dimension-values --time-period Start=2020-10-01,End=2020-10-31 --dimension USAGE_TYPE```
Some of values I found were
    APN1-DataTransfer-Out-Bytes
    APS1-DataTransfer-Out-Bytes
    USW1-DataTransfer-Out-Bytes

## Usage

	aws_usage

You can put this script in your cron file and this will send you regular updates about data usage. Just be careful you don't run often otherwise you will get huge bill because you are paying $0.01 per request 


## Liked my work?
<a href="https://www.buymeacoffee.com/parveshmonu" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

## Websites
https://github.com/Parveshdhull
<br />https://twitter.com/ParveshMonu
<br />https://youtube.com/right2trick
