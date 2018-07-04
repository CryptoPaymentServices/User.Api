# Crypto-Payment.Services User.API
This API allows to get user pay-in address, statistical info and rates. It also allows to configure slack webhook to recieve messages about failed notifications.

API (MainNet): https://crypto-payment.services/user/swagger/index.html
API (TestNet): https://test.crypto-payment.services/user/swagger/index.html

## How to use API
You can use API directly from your applications or you can call it directly from swagger.

## API Access Key
In order to use the system you need an API access key. Getting a key is free and easy, sign up here: https://test.crypto-payment.services (TestNet networks)

## How to increase user balance
- Get user etherium pay-in address using `GET /api/info`
- Send funds ethers to this address (for the TestNet you can use ropsten faucet to get ethers)
- You will get payment confirmation email once we will see your transaction

## How to get rates
Call `GET /api/info` to find out all rates.

## How to get messages about failed notifications in slack
It is free. You can be informed about all issues (like, error while sending payment notifications to your url) via slack
- Get slack webhook url (it must look like this: https://hooks.slack.com/services/YYYYYYYYY/YYYYYYYYY/YYYYYYYYYYYYYYYYYYYYYYYY)
- Optional: Create separate channel if required
- Call `POST /api/settings` to save webhook url and channel

## How to get slack webhook url
- Sign in to the Slack desktop or web app.
- Select your <team name> drop-down menu. If you do not have a team set up, you will need to create one.
- Click Apps & integrations.
- Once redirected, type incoming webhooks in the "Search" field and click Incoming WebHooks from the search results.
- On the next page, click Add Configuration.
- In the "Post to Channel" section, select an existing Slack channel from the drop-down menu, or click create a new channel to make a new one. Once your channel is selected, click Add Incoming WebHooks integration.
- On the next page, a confirmation message, "New integration added!" is displayed in the top navigation.
- Locate the "Webhook URL" section, then highlight and copy the entire Webhook URL.
