# Using Paywalls with Multiple GPTs

🟡 **Intermediate** · ⏱️ ~4 min · 📘 Guide  
How to use one paywall across multiple GPTs or create separate paywalls.

---

As you grow, you may want to monetize multiple GPTs. Authflow offers flexibility in how you structure your paywalls.

## Option 1: One Paywall, Multiple GPTs

**Scenario:** You want subscribers to access all your GPTs with a single subscription.

### How It Works

- Create one paywall in Authflow
- Copy the same schema into multiple GPTs
- All GPTs share the same subscription check
- Users authenticate once and can access all GPTs

### Best For

- Bundle offerings ("Subscribe for access to all my GPTs")
- Related GPTs that complement each other
- Simplifying user experience
- Building a suite of tools

### Setup

1. Create your paywall (or use existing)
2. For each GPT:
   - Create a new action
   - Paste the same schema
   - Use the same API key and authentication
   - Add the same privacy policy
   - Add the same Top Context Instructions

### Example

**Your bundle:** "AI Business Suite"
- GPT 1: Email Writer Pro
- GPT 2: Meeting Summarizer
- GPT 3: Report Generator

All three use the same paywall → One subscription = access to all three

## Option 2: Separate Paywalls per GPT

**Scenario:** You want different pricing for different GPTs.

### How It Works

- Create a separate paywall for each GPT
- Each paywall has its own schema and credentials
- Users subscribe to each GPT individually
- Different pricing for different value propositions

### Best For

- GPTs with different value levels
- Testing different price points
- Targeting different audiences
- Maximizing revenue from premium tools

### Setup

1. Create a new paywall for each GPT
2. Configure pricing independently
3. Use each paywall's unique schema and credentials
4. Each GPT has its own subscription

### Example

- GPT 1: Basic Tool → $5/month
- GPT 2: Pro Tool → $15/month
- GPT 3: Enterprise Tool → $49/month

## Option 3: Tiered Access (Coming Soon)

**Scenario:** Different subscription tiers unlock different GPTs.

### Planned Features

- Create tiers (Basic, Pro, Enterprise)
- Assign GPTs to tiers
- Higher tiers include lower tier access
- One subscription, progressive unlocking

> **Note:** This feature is on the Authflow roadmap. Currently, you can achieve similar results with Option 1 (bundles) or Option 2 (separate paywalls).

## Current Limitations

### One Authflow Action per GPT

Currently, you can only have one Authflow action per GPT. This means:

- Can't have multiple pricing tiers in one GPT
- Can't offer both monthly and lifetime in the same GPT

**Workaround:** Create separate GPTs for different pricing:
- "My GPT - Monthly"
- "My GPT - Lifetime"

### Workaround for Multiple Tiers

If you need different tiers for the same GPT functionality:

1. Create multiple versions of your GPT
2. Each with a different paywall
3. Name them clearly (e.g., "Tool Pro - Monthly", "Tool Pro - Annual")

## Managing Multiple Paywalls

### Organization Tips

- Use clear, descriptive paywall names
- Include the GPT name in the paywall name
- Add notes in the description for your reference
- Keep a spreadsheet mapping paywalls to GPTs

### In Your Dashboard

- View all paywalls in "My Paywalls"
- Filter and search to find specific paywalls
- Monitor statistics for each paywall separately
- Download reports per paywall

## Sharing the Paywall Link

For direct marketing (outside the GPT), you can use the **Paywall Link**:

- Share payment links directly
- Use in email marketing
- Post on social media
- Include in landing pages

Users don't need to go through the GPT to subscribe - they can pay first, then access any GPT using that paywall.

## Best Practices

1. **Start simple** - Begin with one GPT, one paywall
2. **Bundle when related** - Group complementary GPTs
3. **Separate when different** - Different audiences = different paywalls
4. **Monitor metrics** - Track which approach performs better
5. **Iterate** - Adjust your strategy based on data
