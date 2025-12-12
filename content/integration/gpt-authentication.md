# Configure GPT Authentication

🟢 **Beginner** · ⏱️ ~3 min · 🛠️ How-To  
How to set up API key authentication for your GPT action.

---

Authentication connects your GPT to your specific Authflow paywall. This guide shows you how to set up API key authentication correctly.

## What You Need

From your Authflow paywall details page, you need:

1. **API Header Key** - Your unique authentication token (keep this secret!)
2. **API Header Name** - The header name (usually `x-api-key`)

## Step-by-Step Instructions

### 1. Find the Authentication Section

In your GPT action configuration:

1. Look for the **"Authentication"** section
2. It's usually below the schema/OpenAPI field

### 2. Select Authentication Type

1. Click on the authentication dropdown
2. Select **"API Key"**

> **⚠️ Important:** Choose **"API Key"**, not "Bearer" or "Basic" or "OAuth"

### 3. Configure as Custom Header

1. Select **"Custom"** for the API key type
2. This allows you to specify a custom header name

### 4. Enter Your API Key

1. Find the **API Key** input field
2. **Paste your API Header Key** from Authflow
3. Make sure there are no extra spaces before or after

### 5. Enter the Header Name

1. Find the **Custom Header Name** field
2. **Paste your API Header Name** from Authflow
3. This is typically `x-api-key`

### 6. Save the Configuration

1. Click **"Save"** to save your authentication settings
2. The action is now configured

## Verification

After saving, verify your setup:

- ✅ Authentication type shows "API Key"
- ✅ Auth type shows "Custom"
- ✅ A key is entered (shown as hidden/masked)
- ✅ Header name matches what Authflow provided

## Security Best Practices

> **🔒 Important Security Notes:**

- **Never share your API key publicly**
- Don't post it in forums, GitHub, or social media
- Don't include it in screenshots
- If compromised, contact Authflow support to rotate it

## Common Mistakes

| Mistake | Solution |
|---------|----------|
| Selected "Bearer" instead of "Custom" | Change to API Key with Custom type |
| Extra spaces in API key | Remove leading/trailing spaces |
| Wrong header name | Copy exactly from Authflow |
| Forgot to save | Click Save after entering values |

## Troubleshooting

### "Authentication Failed" Errors

1. Verify you copied the complete API key
2. Check there are no extra spaces
3. Confirm you selected "Custom" not "Bearer"
4. Make sure the header name matches exactly

### API Key Appears Invalid

1. Go back to Authflow and re-copy the key
2. Make sure you're copying from the correct paywall
3. Try clearing the field and pasting fresh

## Next Steps

After configuring authentication:

1. [Add the Privacy Policy](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/gpt-privacy-policy.md)
2. [Add Top Context Instructions](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/gpt-instructions.md) ⭐ Critical!
3. [Test your integration](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/testing-integration.md)
