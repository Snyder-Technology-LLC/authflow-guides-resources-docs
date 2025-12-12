# Testing Your Integration

🟢 **Beginner** · ⏱️ ~5 min · 🛠️ How-To  
How to test and verify your Authflow integration is working correctly.

---

After completing the integration steps, it's important to test that everything works correctly before sharing your GPT with the world.

## Pre-Test Checklist

Before testing, verify:

- ✅ Schema is pasted without errors
- ✅ Authentication is configured (API Key, Custom type)
- ✅ Privacy policy URL is added
- ✅ Top Context Instructions are at the very top of Instructions
- ✅ GPT configuration is saved

## Testing Steps

### 1. Start a Fresh Conversation

> **Important:** Always start a NEW conversation for testing. Don't continue an existing chat.

1. Open your GPT
2. Start a brand new conversation
3. Don't type anything yet - observe what happens

### 2. Check for Verification Prompt

You should see a message like:

> "Before we continue, please verify your subscription with Authflow by providing your email address. You can register for your access [here]. Once verified, I'll be happy to assist you."

If you see this, the basic integration is working! ✅

### 3. Test with an Unregistered Email

1. Provide an email that doesn't have a subscription
2. The GPT should call the API
3. You should see:

> "There was an issue verifying your subscription. Please ensure you have an active subscription by visiting [link]."

This confirms the API is being called and responding correctly. ✅

### 4. Test with a Registered Email

1. Start a new conversation
2. Provide the email you used to sign up for Authflow (or a test subscriber)
3. You should see:

> "Thank you for verifying your subscription! How can I assist you today?"

4. You should now have full access to the GPT ✅

### 5. Test the Payment Link

1. Click the registration/signup link provided by the GPT
2. You should see your paywall page with:
   - Your paywall name
   - Pricing information
   - Free trial option (if enabled)
3. Complete a test signup to verify the full flow

## What to Look For

### Successful Integration ✅

- Verification prompt appears automatically
- API calls work (you can verify in Authflow dashboard)
- Correct response for subscribed users
- Correct response for non-subscribed users
- Payment link works

### Signs of Problems ❌

- No verification prompt → Instructions not at top
- API errors → Check authentication configuration
- Wrong paywall link → Verify you're using the right paywall
- GPT ignores the paywall → Instructions may be conflicting

## Verifying API Activity

You can confirm API calls in your Authflow dashboard:

1. Go to **My Paywalls**
2. Click on your paywall
3. Check the "Connection Status" panel
4. You should see activity after testing

## Testing Checklist

| Test | Expected Result | Status |
|------|-----------------|--------|
| Fresh conversation shows verification prompt | ✅ | |
| Unregistered email gets rejection | ✅ | |
| Registered email gets access | ✅ | |
| Payment link opens paywall | ✅ | |
| API activity shows in dashboard | ✅ | |

## Troubleshooting

If testing reveals issues:

- [Paywall Not Appearing](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/troubleshooting/paywall-not-appearing.md)
- [Authentication Issues](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/troubleshooting/authentication-issues.md)
- [Schema Errors](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/troubleshooting/schema-errors.md)

## Next Steps

After successful testing:

1. Do a final review of your GPT description and settings
2. [Publish your GPT](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/publishing-gpt.md)
3. Share your GPT link and start monetizing!
