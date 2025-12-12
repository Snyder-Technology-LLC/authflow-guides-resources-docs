---
id: "gpt-instructions"
title: "Add Top Context Instructions"
description: "The critical step - adding Authflow instructions to your GPT's system prompt"
category: "integration"
tags: ["gpt", "instructions", "prompt", "context", "critical"]
contextKeys: ["paywall-view", "gpt-config"]
difficulty: "beginner"
estimatedTime: 2
displayOrder: 5
relatedDocs: ["custom-gpt-overview", "gpt-authentication", "testing-integration", "character-limit"]
featuredImage: "https://firebasestorage.googleapis.com/v0/b/facesift.firebasestorage.app/o/user_uploads%2F83EXwNWgaKe1BHmyd9ISw3HCEfi2%2F1765257184057-Screenshot%202025-12-09%20001258.png?alt=media&token=f646bdcb-0ea6-43ad-8600-a0af5f540ef5"
---

# Add Top Context Instructions

> **⚠️ This is the MOST IMPORTANT step!** Without these instructions, your paywall won't work.

The Top Context Instructions tell your GPT how to check for subscriptions and handle the paywall flow.

## Why This Step is Critical

These instructions:

- Tell your GPT to call the Authflow API
- Define the verification flow
- Control how users are prompted for their email
- Determine what happens for verified vs. unverified users

**Without them at the top, the paywall functionality won't activate.**

## Step-by-Step Instructions

### 1. Copy the Instructions from Authflow

1. Go to your paywall details page in Authflow
2. Find the section labeled **"Top Context Instructions"**
3. Click the **"Copy"** button

### 2. Open Your GPT Configuration

1. Go to your GPT in ChatGPT
2. Click to edit it
3. Navigate to the **"Configure"** tab
4. Find the **"Instructions"** field (the main system prompt)

### 3. Paste at the VERY TOP

> **⚠️ Critical:** These instructions MUST be at the very top of your Instructions field!

1. Click at the beginning of your Instructions field
2. **Paste** the Authflow instructions
3. Press Enter a couple times to separate from your other instructions
4. Your existing instructions should now be BELOW the Authflow instructions

### 4. Save Your GPT

Click Save to apply the changes.

## Correct Placement

```
[AUTHFLOW INSTRUCTIONS - PASTED AT TOP]

[Your existing GPT instructions below]
```

**Wrong placement (won't work):**
```
[Your existing GPT instructions]

[AUTHFLOW INSTRUCTIONS - TOO LOW, WON'T WORK]
```

## What Happens After Adding Instructions

When users interact with your GPT:

1. **GPT asks for verification** - Prompts users to provide email
2. **API call** - GPT calls Authflow to check subscription status
3. **Access decision**:
   - ✅ Verified → "Thank you! How can I assist you today?"
   - ❌ Not verified → "Please sign up at [link]"

## Example User Experience

**User opens GPT:**

> "Before we continue, please verify your subscription with Authflow by providing your email address. You can register for your access [here]. Once verified, I'll be happy to assist you."

**User provides email:**

> (GPT calls Authflow API)

**If verified:**

> "Thank you for verifying your subscription! How can I assist you today?"

**If not verified:**

> "There was an issue verifying your subscription. Please ensure you have an active subscription by visiting [link]."

## Customizing the Message (Optional)

You can customize how the GPT asks for verification by adding instructions below the Authflow instructions:

```
When asking users to verify their subscription, refer to it as 
"[Your GPT Name] subscription" instead of "Authflow subscription"
```

This makes the message more branded to your GPT.

## Troubleshooting

### Paywall Not Appearing

- **Most common cause:** Instructions not at the very top
- Move them to the absolute beginning of your Instructions field

### GPT Not Calling the API

- Verify instructions are at the top
- Make sure your custom instructions don't conflict
- Test by explicitly asking the GPT to check authentication

### Character Limit Issues

See [Character Limit Troubleshooting](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/troubleshooting/character-limit.md) for tips on managing the 8,000 character limit.

## Next Steps

After adding the instructions:

1. **Save** your GPT configuration
2. [Test your integration](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/testing-integration.md)
3. [Publish your GPT](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/publishing-gpt.md)
