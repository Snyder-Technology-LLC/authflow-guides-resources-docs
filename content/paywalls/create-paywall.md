# Create Your First Paywall

🟢 **Beginner** · ⏱️ ~5 min · 📘 Guide  
Step-by-step guide to creating and configuring a paywall for your GPT.

---

A paywall is what protects your GPT and enables you to charge users for access. This guide walks you through creating and configuring your first paywall.

## Navigate to Create Paywall

1. Log in to your Authflow account at [app.authflow.ai](https://authflow.ai/start?utm_source=github&utm_medium=docs&utm_campaign=github_docs&utm_content=createpaywall_login_cta)
2. In the left sidebar, under **"PAYWALLS"**, click **"Create Paywall"**
3. You'll see the "Paywall and Pricing Configuration" form

## Configure Paywall Details

Fill out the following fields in the paywall creation form:

### Basic Information

| Field | Description |
|-------|-------------|
| **Paywall Name** | A descriptive name for your paywall (e.g., "Premium GPT Access") |
| **Paywall Description** | Brief description of what users get with this paywall |
| **Product URL** | (Optional) The URL of your custom GPT. This is included in transaction emails |

### Thank You Page Settings

| Option | Description |
|--------|-------------|
| **Use Authflow thank you page** | Check to use Authflow's hosted thank you page (whitelabeled to your brand) |
| **Custom Success URL** | (Optional) Redirect users to a custom page after payment |

### Email Customization

| Field | Description |
|-------|-------------|
| **Custom Email Message** | (Optional) Additional text to include in transaction confirmation emails |

## Configure Pricing

### Pricing Model Options

Choose one of the following:

#### One-time Payment
Users pay once for lifetime access.

- **One-time Payment Amount**: Enter the price (e.g., 49.99)
- **Currency**: Select your currency (USD, EUR, GBP, etc.)

#### Subscription
Users pay recurring fees.

- **Subscription Price**: Enter the monthly or annual price
- **Subscription Interval**: Choose "Monthly" or "Annually"
- **Offer Free Trial**: Check to offer a free trial period
- **Trial Duration**: If offering a trial, select 1-14 days

### Statement Descriptor

This is what appears on customers' credit card statements.

- You can manually enter one
- Or click **"Auto-Generate"** to have Authflow create one for you

> **Tip:** Keep it short and recognizable so customers know what the charge is for.

## Create the Paywall

1. Review all your settings
2. Click the **"Create"** button at the bottom of the form
3. Your paywall will be created and you'll be redirected to the paywall details page

## After Creation

Once created, your paywall details page shows:

- **GPT Schema**: The OpenAPI schema for integration
- **API Header Key**: Your unique authentication token
- **API Header Name**: The header name for authentication
- **Privacy Policy**: The privacy policy URL for your GPT action
- **Top Context Instructions**: Instructions to add to your GPT

See the [Integration Guide](https://github.com/Snyder-Technology-LLC/authflow-guides-resources-docs/blob/main/content/integration/custom-gpt-overview.md) for next steps.

## Managing Your Paywall

After creation, you can:

- View and copy integration credentials
- Monitor statistics (Total Payout, Payments, Unique Auths, Paid Users)
- Download authentication reports
- Edit paywall settings
- Enable/disable the paywall
