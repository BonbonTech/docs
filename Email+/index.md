# Bonbon Email+

## MailChimp

### Part I: Generate a MailChimp API Key

1. **Log in to MailChimp**
2. **Navigate to Account Settings**
   - Once logged in, click on your profile name or avatar in the bottom left corner.
   - From the dropdown menu, select "Account."

3. **Access API Keys Section**
   - In the "Account" page, click on the "Extras" dropdown menu.
   - Select "API keys" from the dropdown menu.

4. **Generate an API Key**
   - On the API keys page, scroll down to the "Your API keys" section.
   - Click the "Create A Key" button.
   - MailChimp will generate a new API key for you.

5. **Label Your API Key**
   - It's a good practice to label your API key for future reference, especially if you plan to generate multiple keys. In the "Label" column, enter a descriptive name for the API key.

6. **Copy Your API Key**
   - Once the API key is generated, copy it by clicking the "Copy" button or manually selecting and copying the key.

7. **Send your API key to Bonbon**


### Part II: Adding a Custom Field (`bonbonId`) in MailChimp

1. **Log in to MailChimp**
2. **Navigate to Audience**
3. **Select Your Audience**
   - If you have multiple audiences, select the one you want to add the custom field to.

4. **Manage Audience Fields and *|MERGE|* Tags**
   - In the "Audience" dashboard, click on "Settings."
   - Select "Audience fields and *|MERGE|* tags."

5. **Add a Field**

   - Click on the "Add A Field" button.
   - Select the type of field you want to add (e.g., Text).
   - In the "Field label" box, enter `bonbonId`.
   - The "Field tag" will automatically be generated, you should edit it to `BONBONID`.
   - Click on "Save Changes."

### Part III: Using the `bonbonId` Field in Email Template URLs

1. **Create or Edit an Email Template**
   - Navigate to the "Campaigns" section.
   - Choose to create a new email campaign or edit an existing one.

2. **Edit the Email Content**
   - In the email editor, locate the spot where you want to insert a URL that includes the `bonbonId` as a query string parameter.
   - Click on the text block or button block where the URL will be inserted.

3. **Insert a URL with the Query String Parameter**
   - Highlight the text or select the button where you want to add the link.
   - Click the "Link" button in the toolbar.
   - In the URL field, enter your base URL followed by the query string parameter using the merge tag for `bonbonId`. The merge tag for the custom field will look like `*|BONBONID|*`.
   - For example, if your base URL is `https://example.com`, you would enter:
     ```
     https://example.com?bonbonId=*|BONBONID|*
     ```
   - Click "Insert" or "Save" to add the link.

4. **Save and Test**
   - Save your email template.
   - To test, send a test email to yourself or use the preview function. Ensure that the `bonbonId` is properly populated in the URL.


### Additional Tips
- **Verify Merge Tag:** Ensure you are using the correct merge tag for `bonbonId`. MailChimp provides a list of available merge tags in the "Audience fields and *|MERGE|* tags" section.
- **Personalization:** You can use this method to personalize other aspects of your email by adding additional query string parameters.
- **Testing:** Always send a test email to verify that the `bonbonId` is correctly populated in the URL.