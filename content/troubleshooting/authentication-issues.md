---
id: "authentication-issues"
title: "Authentication Issues"
description: "Troubleshooting API key and authentication problems"
category: "troubleshooting"
tags: ["troubleshooting", "authentication", "api-key", "errors"]
contextKeys: ["paywall-view", "gpt-config"]
difficulty: "beginner"
estimatedTime: 4
displayOrder: 2
relatedDocs: ["gpt-authentication", "testing-integration"]
---

# Authentication Issues

If your GPT can't authenticate with Authflow or you're seeing authentication errors, follow this guide.

## Common Authentication Problems

### "Authentication Failed" Error

**Causes:**
- Wrong API key
- Incorrect authentication type
- Extra spaces in the API key
- Wrong header name

**Solutions:**

1. **Verify API Key**
   - Go to your paywall in Authflow
   - Copy the API Header Key fresh
   - Paste it again (overwrite existing)
   - Ensure no extra spaces before/after

2. **Check Authentication Type**
   - Must be "API Key" (not OAuth, Bearer, or Basic)
   - Auth type must be "Custom" (not Bearer)
   - Header name must match Authflow exactly

3. **Verify Header Name**
   - Copy the API Header Name from Authflow
   - Paste into Custom Header Name field
   - Typically `x-api-key` - verify exact spelling

### API Key Not Recognized

**Causes:**
- Using key from wrong paywall
- Paywall disabled/deleted
- Key format corrupted

**Solutions:**

1. **Verify Correct Paywall**
   - Go to My Paywalls in Authflow
   - Open the specific paywall you want
   - Copy credentials from that paywall

2. **Check Paywall Status**
   - Ensure paywall is enabled
   - Verify it's not archived or deleted

3. **Recopy Fresh**
   - Delete current API key
   - Copy fresh from Authflow
   - Paste carefully

### Connection Errors

**Causes:**
- Schema pointing to wrong endpoint
- Network issues
- Authflow service temporarily unavailable

**Solutions:**

1. **Repaste Schema**
   - Get fresh schema from Authflow
   - Delete existing schema
   - Paste new schema
   - Save and test

2. **Wait and Retry**
   - If Authflow has temporary issues
   - Try again in a few minutes

## Step-by-Step Verification

### 1. Check Authentication Configuration

Open your GPT action and verify:

| Setting | Required Value |
|---------|----------------|
| Auth Type | API Key |
| API Key Type | Custom |
| API Key | [Your key from Authflow] |
| Custom Header Name | [Usually x-api-key] |

### 2. Test the Action

1. Start a new conversation
2. Try to trigger the paywall check
3. Watch for error messages
4. Check if API is being called

### 3. Verify in Authflow Dashboard

1. Go to My Paywalls
2. Open your paywall
3. Check Connection Status
4. Look for API activity

If you see API activity but errors, the connection is working but authentication is failing.

## Common Mistakes

| Mistake | How to Fix |
|---------|-----------|
| Selected "Bearer" type | Change to "Custom" |
| Extra space in API key | Remove all spaces |
| Wrong header name | Copy exact name from Authflow |
| Used old/wrong key | Get fresh key from correct paywall |
| Forgot to save | Save after making changes |

## Header Name Troubleshooting

The header name must match exactly:

✅ Correct: `x-api-key` (lowercase, with hyphen)
❌ Wrong: `X-API-Key` (wrong case)
❌ Wrong: `x-api-Key` (mixed case)
❌ Wrong: `x_api_key` (underscores instead of hyphens)
❌ Wrong: `xapikey` (no separators)

Copy the exact header name from Authflow - don't type it manually.

## Resetting Authentication

If nothing works, try a complete reset:

1. Delete the existing action entirely
2. Create a new action
3. Paste fresh schema
4. Configure authentication from scratch
5. Add privacy policy
6. Save and test

## Getting Help

If issues persist:

1. Screenshot your authentication configuration
2. Note any error messages exactly
3. Check when it last worked (if ever)
4. Contact Authflow support with details

## Related Issues

- [Schema Errors](/troubleshooting/schema-errors)
- [Paywall Not Appearing](/troubleshooting/paywall-not-appearing)
- [GPT Not Calling API](/troubleshooting/gpt-not-calling-api)
