# Crypto-Payment.Services User.API
This API allows to get user pay-in address, statistical info and rates. It also allows to configure slack webhook to recieve messages about failed notifications.

API (TestNet): https://test.crypto-payment.services/user/swagger/index.html

## How to use API
You can use API directly from your applications or you can call it directly from swagger.

## API Access Key
In order to use the system you need an API access key. Getting a key is free and easy, sign up here: https://crypto-payment.services (MainNet networks) or https://test.crypto-payment.services (TestNet networks)

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
