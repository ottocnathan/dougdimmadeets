### Feel free to contribute!

# yahoo-fantasy-bot
Bot that alerts GroupMe, Slack, and Discord users about various things happening in their Yahoo Fantasy Sports league.

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## Follow these steps EXACTLY!
1. Click the above button.  It will auto-deploy the application to Heroku.
2. Name the application whatever you would like.
3. When it asks for environment variables at first, you do not need to put any in that are not already filled in.  These will be added later.
4. Click "Deploy App".  This will automatically configure the dynos and run all required scripts to get the app created.

5. Follow the below section.

---

### (REQUIRED) Setting up Yahoo API
You will need a Yahoo Access Token, Client ID, and Client Secret for this bot to work.

1. Go to https://developer.yahoo.com/apps/
2. Click "Create an App" button

![](https://imgur.com/VDgZ1Ze.png)

3. Fill out required information.
  * Name the application whatever you would like
  * Click "Installed Application"
  * The callback domain name will be <HEROKU APP NAME>.herokuapp.com (Do not put http:// or https://)
  * Click "Fantasy Sports" and then "Read"
  * Click "Create App"
  
![](https://imgur.com/VqctUfM.png)

4. You will see your: Yahoo Client ID and Client Secret.  Save these for later.

![](https://imgur.com/NbUwOmD.png)

---

5. **The following sections are all optional, but at least one of them is needed.  All of them can be used as well!**

(The following sections were taken from [dtcarls/ff_bot](https://github.com/dtcarls/ff_bot) as the steps are the exact same.  They are tweaked a little bit.)

--- 

### (Optional) GroupMe Setup

Go to www.groupme.com and sign up or login

If you don't have one for your league already, create a new "Group Chat"

![](https://i.imgur.com/32ioDoZ.png)

Next we will setup the bot for GroupMe

Go to https://dev.groupme.com/session/new and login

Click "Create Bot"

![](https://i.imgur.com/TI1bpwE.png)

Create your bot. GroupMe does a good job explaining what each thing is.

![](https://i.imgur.com/DQUcuuI.png)

After you have created your bot you will see something similar to this. Click "Edit"

![](https://i.imgur.com/Z9vwKKt.png)

This page is important as you will need the "Bot ID" on this page.You can also send a test message with the text box to be sure it is connected to your chat room.
Side note: If you use the bot id depicted in the page you will spam an empty chat room so not worth the effort

![](https://i.imgur.com/k65EZFJ.png)

--- 

### (Optional) Slack setup

Go to https://slack.com/signin and sign in to the workspace the bot will be in

If you don't have one for your league already, create a new League Channel

Next we will setup the bot for Slack

Go to https://api.slack.com/apps/new

Name the app, and choose the intended workspace from the dropdown.

Select the Incoming Webhooks section on the side.

![](https://i.imgur.com/ziRQCVP.png)

Change the toggle from Off to On.

Select Add New Webhook to Workspace

![](https://i.imgur.com/tJRRrfz.png)

In the Post to dropdown, select the channel you want to send messages to, then
select Authorize.

This page is important as you will need the "Webhook URL" on this page.

![](https://i.imgur.com/mmzhDS0.png)

--- 

### (Optional) Discord setup

Log into or create a discord account

Go to or create a discord server to receive messages in

Open the server settings

![](https://i.imgur.com/bDk2ttJ.png)

Go to Webhooks

![](https://i.imgur.com/mfFHGbT.png)

Create a webhook, give it a name and pick which channel to receive messages in

![](https://i.imgur.com/NAJLv6D.png)

Save the "Webhook URL" on this page

![](https://i.imgur.com/U4MKZSY.png)

--- 

6. Follow the below section.


### Heroku Setup

1. Go to your [dashboard](https://dashboard.heroku.com/apps). Now you will need to setup your environment variables so that it works for your league. Click Settings at your dashboard. Then click "Reveal Config Vars" button and you will see something like this.

![](https://imgur.com/8k1tZPs.png)

2. Fill out all of the variables from: Yahoo, (whichever you chose) GroupMe, Slack, and Discord
3. Click 'Overview"
4. Click "Configure Dynos"
5. Turn on the "bot" dyno
6. Click "Open App" at the top right
7. Follow the setup and then close the window once it says "You are authorized".
8. Click "Configure Dynos" and turn off the "web" dyno as it is not needed anymore

### You are all set!  Enjoy the bot!