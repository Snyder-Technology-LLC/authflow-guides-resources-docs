# Integrating Authflow with Custom GPTs

🟢 **Beginner** · ⏱️ ~15 min · 📘 Guide  
Complete overview of integrating your Authflow paywall with ChatGPT Custom GPTs.

---

This guide walks you through the complete process of integrating your Authflow paywall into your custom GPT on ChatGPT. 

> **💡 Pro Tip:** "If you can copy and paste, you can implement a paywall." It's really that simple!

## Prerequisites

Before starting the integration, make sure you have:

- ✅ Created a paywall in Authflow (see [Create Your First Paywall](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/paywalls/create-paywall.md))
- ✅ A custom GPT created in ChatGPT
- ✅ Access to edit your custom GPT's configuration

## Integration Overview

The integration process involves these steps:

1. **Get your credentials** from Authflow
2. **Create a new Action** in your GPT
3. **Paste the Schema** for the Authflow API
4. **Configure Authentication** with your API key
5. **Add the Privacy Policy** URL
6. **Add Top Context Instructions** to your GPT
7. **Test the integration**

**Total time:** Approximately 10-15 minutes

## Quick Start

### Step 1: Get Your Integration Details

1. In your Authflow dashboard, go to **"My Paywalls"**
2. Find your paywall and click the **"Go"** button
3. You'll see all integration information on the paywall details page:
   - **GPT Schema** - The OpenAPI schema code
   - **API Header Key** - Your unique authentication token
   - **API Header Name** - The header name for authentication
   - **Privacy Policy** - URL for the GPT action
   - **Top Context Instructions** - Instructions for your GPT

### Step 2: Open Your GPT in ChatGPT

1. Go to [chat.openai.com](https://chat.openai.com)
2. Navigate to your custom GPT
3. Click to edit it
4. Make sure you're in the **"Configure"** tab

### Step 3: Create a New Action

> **⚠️ Important:** If you already have actions in your GPT (like RapidAPI integrations), **DO NOT edit those existing actions**. The paywall needs to be its own separate action.

1. Scroll down to the **"Actions"** section
2. Click **"Create new action"** or the **"+"** button
3. You can have multiple actions in one GPT

### Step 4: Complete the Integration

Follow the detailed guides for each step:

1. [Paste the Schema](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/gpt-schema-setup.md)
2. [Configure Authentication](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/gpt-authentication.md)
3. [Add Privacy Policy](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/gpt-privacy-policy.md)
4. [Add Top Context Instructions](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/gpt-instructions.md) ⭐ **Critical step!**

### Step 5: Save and Test

1. **Save** all your GPT configuration changes
2. **Test** by starting a new conversation
3. See [Testing Your Integration](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/testing-integration.md) for details

## What Happens After Integration

Once integrated, here's what users will experience:

1. **User Opens Your GPT** - They start a conversation
2. **Verification Prompt** - GPT asks for email verification
3. **Email Check** - GPT calls Authflow API to verify subscription
4. **Access Granted or Denied**:
   - ✅ Verified: Full access to your GPT
   - ❌ Not verified: Directed to sign up

## Time to Set Up

- **Total Time:** ~10-15 minutes from start to finish
- **You can start making money the same day!**
- No coding required - just copy and paste

## Next Steps

After integration:

1. [Test your integration](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/testing-integration.md)
2. [Learn about multiple GPTs](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/multiple-gpts.md)
3. [Monitor your performance](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/getting-started/understanding-dashboard.md)
