# Stay Home, Check Your Stress
- Call for Code Challenge 2020
- Promotion Video https://youtu.be/UXoX6_Whm_U
- Apache License 2.0

# Deployment document
- Please read a [wiki](https://github.com/kolinz/stayhome-checkyourstress/wiki/Deployment)

# System Overview
![system-overview](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/system-overview.png)

This solution uses five IBM Cloud service.This chatbot ask questions and get answers with Watson Assistant. Finally the chatbot give appropriate advice to users. The answer data was stored in Db2 on Cloud.

| product | category | service name | Docs |
|:---|:---|:---|:---|
| Services | AI | Watson Assistant | [getting started](https://cloud.ibm.com/docs/services/assistant?topic=assistant-getting-started) |
| Services | AI | Discovery | [getting started](https://cloud.ibm.com/docs/services/discovery?topic=discovery-getting-started) |
| Services | Databases | Db2 | [getting started](https://cloud.ibm.com/docs/services/Db2onCloud?topic=Db2onCloud-getting-started#getting-started) |
| Services | Storage | Object Storage | [getting started](https://cloud.ibm.com/docs/cloud-object-storage?topic=cloud-object-storage-getting-started) |
| Software | Web and Application | Node-RED App | [About](https://cloud.ibm.com/catalog/starters/node-red-starter#about) |

# End user interface Overview
![enduser-interface](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/enduser-interface.png)

## Portal Site
![portal site](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/portal-site.png)

The End user interface have Portal Site and Chatbot. This Chatbot start by scanning a QR Code on the Portal Site.The map is one of the functions that will be developed in the future. It shows information of companies and organizations that support working at home.

## Chatbot
![line-bot](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/line-chatbot.png)

### Chatbot 
| Support App | staus | link |
|:---|:---|:---|
|LINE | confirmed | https://line.me/en/download |
|Slack | loadmap |  |
|Mattermost | loadmap |  |

### overview
The application asks the user 10 questions.Questions include exercise, diet, sleep, life rhythm, work efficiency, family and anxiety about infection.

You answer from "Strongly Agree" to "Strongly Disagree" with a number from 1 to 6.With just this, you'll know your stress situation and get some advice on how to reduce your stress.

The advice is designed to include elements of levels of loneliness, depression, harmful alcohol and drug use, that are expected to result from being forced to stay home.Please use the advice from the application to protect your mental health.

# Recorded Db2
![recorded-db2](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/insertdata-db2.png)

These answer data of chatbot users are recorded in Db2. Hygiene manager in companies and organizations will be able to download stress check data through Db2's console to manage their healthcare support.

