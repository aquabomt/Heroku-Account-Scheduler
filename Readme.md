Heroku-Account-Scheduler
===============

Heroku-Account-Scheduler, A Simple Script Powered By GitHub Actions To Switch Heroku Accounts Every Thirteen Days.

This Repo Makes Sure You Never Run Out Of Dynos.

Deployment
----------

1. Fork the reposistory:

2. Deploy Both Your Apps On Seperate Heroku Accounts

```
Make Sure Each App Runs As Intended Individually Before Moving Onto The Next Step
```
3. Turn Both The Deployed Apps Off On Both The Accounts

4. Set The Following Github Actions Secrets:

```
HEROKU_EMAIL_1 : Your Heroku Account Email Of Your First Account.
HEROKU_EMAIL_2 : Your Heroku Account Email Of Your Second Account.
HEROKU_API_KEY_1 : Your Heroku Account API-KEY Of Your First Account. Get It From dashboard.heroku.com/account
HEROKU_API_KEY_2 : Your Heroku Account API-KEY Of Your Second Account. Get It From dashboard.heroku.com/account
HEROKU_APP_NAME_1 : Your Heroku Account APP-NAME Of First Account.
HEROKU_APP_NAME_2 : Your Heroku Account APP-NAME Of Second Account.
```
5. Make Sure Actions Are Enabled In GitHub:
- To Do This, Visit The "Actions" Tab Of Heroku
- If Done Right, The Script Would Swap Account Based On The Date Of The Month. Making Sure Your App Always Runs.

-------

Features Nobody Asked For(Additional Features)
----------

- Send Notification To Telegram Log Group About Switching Of The Accounts
- Set The Following Secrets In GitHub-Secrets

```
TG_TOKEN : Your Telegram Bot Token
TG_CHAT: Your Telegram Private Group ID
```

-------

Why Does This Script Exist?
----------

- Heroku Doesn't Provide Users Enough Dynos Under Their Free Quota For An App To Last An Entire Month Without Sleeping. And Not Everyone Has A Credit-Card. Even Worse. Heroku Refuses To Accept My Credit-Cards From Legit Banks, Even Though They Have International Payments Enabled. I'm Left With No Choice ;-;
- I Also Have Some Strange Deep Affection Towards Heroku.....um..yea, I'm Weird.

-------

## **Warnings :**
- This Bot/Script Uses GitHub Actions, Although Running One Lightweight Action Once In Thirteen Days, Is In No Way Considered Abuse Of It. You Are Still Warned Of Account Suspension(If You Reduce The Cron-Job Frequency)(If You Already Have A Billion Other Consecutive GitHub Actions Running[Although GitHub Allows Only 20 Concurrent Jobs Per Account])
- You Better Have A Backup Of Your App-Data/Configs As Heroku Can Ban Your Account Whenever They Please.