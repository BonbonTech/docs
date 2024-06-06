# Sailthru

## Creating a Sailthru API Key

To integrate with Sailthru and access their API, you need to create an API key. Follow these steps to create one:

### Step 1: Log in to Sailthru

1. Visit the [Sailthru Login Page](https://login.sailthru.com).
2. Enter your credentials and log in to your Sailthru account.

### Step 2: Navigate to API & Integrations

1. Once logged in, click on your account name in the top-right corner.
2. From the dropdown menu, select **Settings**.

### Step 3: Access API & Integrations

1. In the Settings menu, click on **API & Integrations** located in the left-hand sidebar.

### Step 4: Create a New API Key

1. In the API & Integrations section, click the **API Keys** tab.
2. Click the **Add API Key** button.

### Step 5: Configure the API Key

1. Enter a descriptive name for your API key (e.g., "Bonbon Integration").
2. Enable the User Data permissions for your API key.
    - **User Data**: Access and manage user data.

3. After selecting the User Data permissions, click the **Save** button.

### Step 6: Retrieve Your API Key

1. Your new API key will be displayed. Make sure to copy and store it securely.
2. You can view and manage your API keys anytime from the **API Keys** tab.

### Step 7: Securely Send your API Key to your Bonbon Technical Account Manager

Send the API Key securely through a service like https://onetimesecret.com/

## Creating Custom Fields in Sailthru

Custom fields in Sailthru allow you to store additional information about your users. Follow these steps to create custom fields in Sailthru:

### Step 1: Log in to Sailthru

1. Visit the [Sailthru Login Page](https://login.sailthru.com).
2. Enter your credentials and log in to your Sailthru account.

### Step 2: Navigate to User Fields

1. Once logged in, click on your account name in the top-right corner.
2. From the dropdown menu, select **Settings**.

### Step 3: Access User Fields

1. In the Settings menu, click on **User Fields** located in the left-hand sidebar.

### Step 4: Create a New Custom Field

1. In the User Fields section, click the **Add Field** button.
2. Enter a name for your custom field. This name should be descriptive of the data it will store (e.g., "Favorite_Color"). Please check the [data dictionary](/esp-integration/#data-dictionary) for more information on field names and data types.
3. Select the appropriate field type from the dropdown menu. Sailthru supports various field types such as:
    - **String**: Text data.
    - **Integer**: Numeric data.
    - **Float**: Decimal numbers.
    - **Boolean**: True/False values.
    - **Date**: Date values.
4. Optionally, you can set a default value for the field.
5. Click the **Save** button to create the custom field.


<!-- ## Step 6: Verifying Custom Field Data

1. To verify that the custom field data is being stored correctly, you can view a user's profile in the Sailthru UI.
2. Navigate to **Users** from the main menu.
3. Search for the user whose profile you want to view.
4. The custom field data will be displayed under the **Custom Fields** section of the user's profile.

By following these steps, you can successfully create and manage custom fields in Sailthru.
 -->