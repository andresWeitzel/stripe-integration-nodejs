# Stripe payment integration in Node JS

check

## Overview

This repository shows you how to create recurring subscriptions with Stripe and Node.js.

It uses Express for creating a simple server, Nunjucks for templating, and the Stripe API.

It features

1. An **Admin View** when you can create Stripe Products and Plans via the Stripe API.
2. A **Client View** where your users can view and pay for your subscription plans.

## How to install & use

### 1- Go to Stripe and signup for stripe developer account

Go to `https://dashboard.stripe.com/register` and signup<br /><br />

### 2- Clone this github-repository

Clone and open code in editor and go to .env<br /><br />

### 3- Edit the .env file

Go to mySql and create a database <br/>
Paste your databse name,username and db_password in .env file<br/><br/>

### 4- Edit the .env file

Go to stripe developer panel<br/>
Copy your 'Publishable Key' and 'App Secret' and paste in .env file<br/><br/>

### 5- Install node modules

Run this code in terminal <br /><br />

```
npm install
```

### 6- Run the migrations

Run this code in terminal <br /><br />

```
npx sequelize-cli db:migrate
```

### 7- Webhook the ngrok

Open 'ngrok' in your local machine and run this code in ngrok terminal <br /><br />

```
ngrok http 3000
```

Now copy the first forwarding link i.e: 'https://xxx-xxx-xxx.ngrok.io'

### 8- Add Endpoint in Stripe Account

Go to `https://dashboard.stripe.com/`. Now go developer account <br />
Go to webhooks tab. Click on Add Endpoint and paste the url copied from ngrok. Also add '/webhooks'at the end of link <br />
So your link will look like this 'https://xxx-xxx-xxx.ngrok.io/webhooks'
Now click on Select Events. Select 'Payment Intent' option and click on 'select all event'<br />
Now click on button "Add Events" 

### 9- Run the code

Now go to your code and run this command in terminal <br /><br />

```
node app.js
```

### 10- Open into browser

Open a browser and go to `http://localhost:3000/`.<br />
App will run.Yayyyy.<br /><br/>
