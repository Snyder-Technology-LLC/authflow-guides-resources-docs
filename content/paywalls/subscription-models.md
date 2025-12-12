---
id: "subscription-models"
title: "Subscription Models"
description: "Understanding and setting up subscription-based pricing for your GPTs"
category: "paywalls"
tags: ["subscription", "recurring", "billing", "revenue"]
contextKeys: ["create-paywall", "pricing"]
difficulty: "beginner"
estimatedTime: 5
displayOrder: 3
relatedDocs: ["create-paywall", "pricing-strategies", "free-trials"]
---

# Subscription Models

Subscriptions provide recurring revenue, making your income more predictable and sustainable. Authflow makes it easy to set up and manage subscription-based paywalls.

## Subscription vs. One-Time Payments

| Aspect | Subscription | One-Time |
|--------|--------------|----------|
| Revenue | Recurring, predictable | Single payment |
| User commitment | Ongoing relationship | One-time transaction |
| Updates | Users expect ongoing improvements | Less pressure to update |
| Churn risk | Users can cancel anytime | No churn risk |
| Lifetime value | Higher over time | Fixed |

## Setting Up Subscriptions

When creating a paywall, choose **"Subscription"** as your pricing model:

### Monthly Subscriptions

- Users are charged every month
- Lower per-payment amount = easier to commit
- Higher lifetime value if users stay subscribed
- Most common for individual users

### Annual Subscriptions

- Users are charged once per year
- Offer a discount (typically 15-30% off monthly rate)
- Better cash flow (full year upfront)
- Lower churn (users committed for the year)
- Great for serious users

## Subscription Intervals

| Interval | Best For | Typical Discount |
|----------|----------|------------------|
| Monthly | Casual users, testing the waters | None (base price) |
| Annual | Committed users, businesses | 15-30% off monthly |

> **Pro Tip:** Offer both options. Show annual as "best value" with the savings highlighted.

## Managing Subscriptions

### Automatic Renewals

Authflow automatically handles subscription renewals:

- Users are charged on their billing date
- Failed payments trigger Stripe's retry logic
- You receive notifications about renewals and issues

### Handling Cancellations

When users cancel:

- They retain access until the end of their billing period
- Authflow handles the cancellation process
- You can view cancellation data in your analytics

### Payment Failures

Stripe handles payment failures with smart retry logic:

1. Initial attempt fails
2. Stripe retries over several days
3. If all retries fail, subscription is cancelled
4. User is notified at each step

## Subscription Metrics to Track

| Metric | What It Means |
|--------|---------------|
| **MRR** | Monthly Recurring Revenue - your predictable income |
| **Churn Rate** | Percentage of users who cancel per month |
| **LTV** | Lifetime Value - average revenue per customer |
| **Conversion Rate** | Visitors who become paying subscribers |

## Tips for Reducing Churn

1. **Deliver consistent value** - Keep improving your GPT
2. **Engage regularly** - Send helpful tips and updates
3. **Offer annual discounts** - Annual users churn less
4. **Use free trials wisely** - Let users experience value first
5. **Collect feedback** - Understand why users might leave

## Example Subscription Setup

**GPT:** Marketing Content Creator

**Configuration:**
- Monthly price: $15
- Annual price: $144 (save $36 = 20% off)
- Free trial: 7 days

**Why this works:**
- $15/month is accessible for freelancers and small businesses
- Annual option rewards committed users
- Free trial lets users experience the value
- 20% annual discount is meaningful without being too steep
