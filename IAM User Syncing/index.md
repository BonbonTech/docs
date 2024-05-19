# IAM User Syncing

If you have your own Identity and Access Management (IAM) system, Bonbon can streamline the synchronization of users between your systems and ours.

<b><i>This integration requires making changes to your server-side systems and will require engineering resources.  Please connect with your Technical Account Manager (TAM) to discuss integrating Bonbon’s IAM User Syncing. </i></b>

## Bonbon -> Publisher

For this integration you’ll need your Bonbon Client ID (same as from the initial Bonbon Web Tags installation), a Client Secret Key (get from your TAM) and an earn token JWT, such as one from a bonbon::login event.

The first thing you’ll want to do is set up a webhook endpoint that will receive POST requests of the following form:

```
curl -X POST -H "Authorization: Bearer EARN_TOKEN_JWT" https://your-webhook-endpoint/your-path
```

Next, your webhook server code will call the Bonbon API using your Client ID, Client Secret and Earn Token JWT value from the Authorization header of the webhook endpoint like in this sample cURL request:

```
curl -X GET -H "x-bonbon-clientid: YOUR_CLIENT_ID" -H "x-bonbon-api-key: YOUR_CLIENT_SECRET" -H "Authorization: Bearer EARN_TOKEN_JWT" https://api.bonbon.tech/v1/earn/user
```

Which will return you a user object like this:

```
{
  "id": "12345",
  "first_name": "Alyssa",
  "last_name": "P. Hacker",
  "postal": "90403",
  "gender": "Male",
  "email": "alyssa.p.hacker@bonbon.tech",
  "email_verified": true,
  "bonbons": 100,
  "preferences": {
     "pAds": true,
     "newsletter": true
  },
  "reward": "airpods_v1"
}
```

You can use that information to update your user datastore and/or set a cookie to log the user into your site.

<b>Note: If your system already has an account for the user with the provided email address, for added security, it is recommended that you prompt the user to login to your system to link the accounts. Upon successful authentication, you should link the accounts in your IAM system. Once the accounts are linked, the additional authentication is not required on subsequent logins.</b>


Note: Bonbon’s servers will hit your webhook periodically to update user information, for example, when new profile data is supplied or if the user changes preferences to things like newsletters, personalized ads, etc.


## Publisher -> Bonbon

If a user is logged into your system, we recommend you let Bonbon Web Tags know by identifying them on the page using the JavaScript below:

```
bonbontag("signal", "loggedIn", "[BONBON_ID_TOKEN]");
```

The value of `BONBON_ID_TOKEN` token can be generated using our <a href="https://developers.bonbon.tech/#/paths/~1jwt/post">`/v1/jwt` API endpoint</a> 

With the call to `bonbontag` above, Bonbon will tailor all widget experiences so that the user does not need to re-enter their email address and can simply opt-in to Bonbon Rewards with a single click.

