# Stay Home, Check Your Stress
- Call for Code Challenge 2020
- Promotion Video https://youtu.be/UXoX6_Whm_U
- Apache License 2.0

# Deployment document
- Please read a [wiki](https://github.com/kolinz/stayhome-checkyourstress/wiki/Deployment)

# System Overview
![system-overview](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/system-overview.png)

This solution uses five IBM Cloud services: Node-RED, Cloud Object Storage, Watson Assistant, Watson Discovery, and Db2 on Cloud.This chatbot ask questions and get answers with Watson Assistant. Finally the chatbot give appropriate advice to users. The answer data was stored in Db2 on Cloud.

# End user Overview
![enduser-interface](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/enduser-interface.png)

## Portal Site
![portal site](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/portal-site.png)

The End user interface have Portal Site and Chatbot. This Chatbot start by scanning a QR Code on the Portal Site.The map is one of the functions that will be developed in the future. It shows information of companies and organizations that support working at home.

## Chatbot
![line-bot](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/line-chatbot.png)

The application asks the user 10 questions.Questions include exercise, diet, sleep, life rhythm, work efficiency, family and anxiety about infection.

You answer from "Strongly Agree" to "Strongly Disagree" with a number from 1 to 6.With just this, you'll know your stress situation and get some advice on how to reduce your stress.

The advice is designed to include elements of levels of loneliness, depression, harmful alcohol and drug use, that are expected to result from being forced to stay home.Please use the advice from the application to protect your mental health.

# Recorded Db2
![recorded-db2](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/insertdata-db2.png)

These answer data of chatbot users are recorded in Db2. Hygiene manager in companies and organizations will be able to download stress check data through Db2's console to manage their healthcare support.

