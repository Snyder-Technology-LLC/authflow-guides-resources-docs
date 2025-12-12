---
id: "paywall-not-appearing"
title: "Paywall Not Appearing"
description: "Solutions when your GPT doesn't show the verification prompt"
category: "troubleshooting"
tags: ["troubleshooting", "paywall", "integration", "instructions"]
contextKeys: ["paywall-view", "gpt-config"]
difficulty: "beginner"
estimatedTime: 5
displayOrder: 1
relatedDocs: ["gpt-instructions", "testing-integration"]
---

# Paywall Not Appearing

If your GPT isn't asking users to verify their subscription, follow this troubleshooting guide.

## Most Common Cause

> **90% of the time:** The Top Context Instructions are not at the very top of your Instructions field.

### The Fix

1. Open your GPT configuration
2. Go to the **Instructions** field
3. Check if Authflow instructions are at the **very beginning**
4. If not, cut them and paste at the absolute top
5. Save your GPT
6. Start a **new conversation** to test

## Troubleshooting Checklist

### 1. Check Instructions Placement

| ✅ Correct | ❌ Wrong |
|-----------|----------|
| Authflow instructions at top | Authflow instructions in middle |
| Authflow instructions first | Authflow instructions at bottom |
| | Mixed with other instructions |

### 2. Verify Schema is Pasted

1. Open your GPT action configuration
2. Check the schema/OpenAPI field
3. Verify there's content (not empty)
4. Look for red error messages (should be none)
5. Confirm "check active paywall" action appears

### 3. Check Action is Enabled

1. In the action configuration
2. Verify the action isn't disabled
3. Make sure changes are saved

### 4. Verify API Key

1. Go to Authentication section
2. Confirm API Key is set
3. Verify "Custom" is selected (not Bearer)
4. Check header name matches Authflow's provided name

### 5. Test in New Conversation

> **Important:** Always test in a brand new conversation!

Old conversations may have cached behavior. Start fresh:
1. Close the current chat
2. Open your GPT
3. Start a completely new conversation
4. Don't type anything - observe if verification appears

## Still Not Working?

### Clear and Repaste Everything

Sometimes starting fresh helps:

1. Delete the schema from the action
2. Delete the authentication settings
3. Delete the Authflow instructions from GPT Instructions
4. Go to Authflow and recopy everything
5. Paste schema fresh
6. Configure authentication fresh
7. Paste instructions at the top fresh
8. Save and test

### Check for Conflicting Instructions

Your existing GPT instructions might conflict:

**Problematic patterns:**
- "Always help the user immediately"
- "Never ask for personal information"
- "Skip authentication steps"

**Solution:**
- Review your instructions for conflicts
- Ensure Authflow instructions take priority (at top)
- Consider simplifying custom instructions

### Verify Paywall is Active

In Authflow:
1. Go to "My Paywalls"
2. Check that your paywall is enabled
3. Verify it's not disabled or archived

## Getting Help

If you've tried everything above:

1. Double-check each step systematically
2. Take screenshots of your configuration
3. Contact Authflow support with details:
   - Your paywall ID
   - GPT configuration screenshots
   - Description of what happens/doesn't happen

## Related Issues

- [Authentication Issues](/troubleshooting/authentication-issues)
- [Schema Errors](/troubleshooting/schema-errors)
- [GPT Not Calling API](/troubleshooting/gpt-not-calling-api)
