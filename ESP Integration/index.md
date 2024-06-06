# Email Service Provider (ESP) Integration

Bonbon can plumb all of the 1st party data collected directly to your email service provider (ESP). We currently support the following email service providers:

1. **Mailchimp**
2. **Klaviyo**
3. **SendGrid**
4. **Campaign Monitor**
5. **Customer.io**
6. **ActiveCampaign**
7. **Salesforce Marketing Cloud**
8. **HubSpot**
9. **Iterable**
10. **Braze**
11. **[Sailthru](./sailthru)**
12. **Constant Contact**
13. **Marketo**
14. **Responsys**

## Data Dictionary

Bonbon collects the following pieces of 1st party data that can be synchronized to your ESP:

| Field Name | Description | Data Type |
| ---------- | ----------- | --------- |
| email | The user's normalized email address | String |
| first_name | The user's first name | String |
| last_name | The user's last name | String |
| last_login | The last time the user fully authenticated with Bonbon | Date |
| last_ip | The users' last seen IP Address | String |
| logins_count | The number of times the user has authenticated | Integer |
| interested_in | A comma separated list of offer IDs for items the user has expressed interest in. | String |
| email_opt_in | A flag indicating whether or not the user is opted into email marketing | Boolean |
| bonbons | The number of bonbons the user has earned | Integer |
| last_login_url | The last URL the user has logged in at | String |
| gender | The user's declared gender | String |
| postal | The user's declared postal code | String | 
| mobile | The user's declared mobile number | String |
| favorite_team | The user's declared favorite sports team | String |