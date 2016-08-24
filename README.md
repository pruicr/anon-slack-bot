# Anonymous Slack Bot

This slack bot uses slack webhook and slash commands to send anonymous messages.

## Run On Your Channel

In order to run this bot on your own channel, clone this repo:

```sh
$ git clone 
```

Deploy to Heroku:

```sh
$ heroku create <app-name>
$ git push heroku master
```

Add a slash command configuration with a name of your choice to Slack with the url:

`https://<app-name>.herokuapp.com/anonmize`

with a method of `GET`.

Configure an Incoming Webhook on any channel, note the webhook url.

Set Heroku's environment variable in the shell:

```sh
$ heroku config:set SLACK_WEBHOOK_URL=<webhook url>
```

Now navigate to the channel you set the bot to, type the slash command before your message, and you will notice that it is anonymous once sent.