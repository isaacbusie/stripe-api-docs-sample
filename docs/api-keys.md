## Overview
This part of the guide explains what API keys are and how they help you set up your authentication request

**Definition**
An api key is a string which gives you access to parts of an application - in this case, Stripe. Your API key is unique to you, and it helps Stripe to confirm that the request originates from you - or your app. 

## Types of API Keys
Stripe has **3** main API keys: 
- Restricted API Key (RAK). Use this for specific access limits and permissions. Stripe advises the use of this API type from now on
- Publishable Key (prefixed ` pk `). This API is public-facing and can be used in client-side/front-end applications
- Secret Key (prefixed ` sk  `). This should be used only on the server-side, as it is highly secret

  
   Apps created after May 2026 are advised to use their generated RAK for requests
## Where to find your keys
1. Log in to your [Stripe Dashboard](https://dashboard.stripe.com/)
2. Navigate to the bottom of the screen and click ` Developers ` and then ` APIs `
3. Create a new Restricted API Key or use any of the existing RAK, PK or SK keys

## Making your first authentication request
Here is an example of how to make your first authentication request by creating a customer in Stripe 

```
stripe customers create --email=john.doe@examplemail.com --name="John Doe" --api-key sk_test_YOUR_KEY_HERE

```

## Security best practices
1. Never expose your secret or restricted keys in client-side code
2. Never commit API keys to GitHub — use environment variables
3. Use Restricted API Keys (RAKs) over secret keys wherever possible
4. Rotate keys immediately if you suspect they've been compromised


