# Salesforce Bot for Lego City

Follow the instructions below to create your own instance of the bot:


### Step 1: Deploy the Messenger Bot on Heroku

1. Make sure you are logged in to the [Heroku Dashboard](https://dashboard.heroku.com/)
1. Click the button below to deploy the Messenger bot on Heroku:

    [![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

1. Fill in the config variables as described.

    - Leave **FB_PAGE_TOKEN** blank for now
    - For **FB_VERIFY_TOKEN**, enter a passphrase of your choice. You'll have to enter the same passphrase when you create the webhook in Facebook.

### Step 2 : Create a Facebook App

1. Follow [these instructions](https://developers.facebook.com/docs/messenger-platform/quickstart) to create a Facebook app. You'll have to create a Facebook page, a Facebook application, and configure Messenger for your application.

    - When asked for a **Callback URL**, enter the URL of the Heroku app you just deployed followed by /webhook. For example:
        ```
        https://myapp.herokuapp.com/webhook
        ```
    - When the Page Access Token is generated, login to the Heroku Dashboard, and set the Heroku **FB_PAGE_TOKEN** config variable to the value of that token (**Setting>Reveal Config Vars**)
    - When asked for the **Verify Token**, enter the value you entered for the **FB_VERIFY_TOKEN** config variable when you deployed the Heroku app.
    - Make sure you select a page in the **Select a page to subscribe your webhook...** dropdown
    
1. Visit the Facebook page you created in the previous step, and click the **Message** button. Type **help** in the chat bot. You can continue the conversation with the bot in the Messenger app on your phone or in the browser (http://messenger.com).
