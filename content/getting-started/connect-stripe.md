# Connect Stripe for Payouts

🟢 **Beginner** · ⏱️ ~5 min · 📘 Guide  
How to connect your Stripe account to receive payments from your GPT subscribers.

---

Stripe is how you receive payments from your GPT subscribers. Authflow uses Stripe Connect to securely handle all payment processing, so your customers' payment information is never stored on Authflow's servers.

## Why Stripe?

- **Industry Standard**: Stripe is used by millions of businesses worldwide
- **PCI DSS Level 1 Certified**: The highest level of payment security
- **Global Coverage**: Accept payments from customers anywhere in the world
- **Multiple Payment Methods**: Credit cards, digital wallets, bank transfers, and more

## Connecting Your Stripe Account

### If You Don't Have a Stripe Account

1. During the onboarding process, click **"Review"** on the "Connect Stripe for Payouts" step
2. You'll be guided to create a new Stripe account
3. Follow Stripe's signup process:
   - Enter your email and create a password
   - Provide business information
   - Add bank account details for payouts
   - Verify your identity
4. Once complete, you'll be redirected back to Authflow

### If You Already Have a Stripe Account

1. Click **"Review"** on the "Connect Stripe for Payouts" step
2. Log in to your existing Stripe account when prompted
3. Authorize Authflow to connect to your account
4. You'll be redirected back to Authflow

## Verifying Your Connection

After connecting, you can verify your Stripe connection:

1. Go to **"Stripe Connect"** under the ACCOUNT section
2. Check that your account status shows as connected
3. You should see your Stripe account ID and connection status

## Managing Your Stripe Connection

### Viewing Payouts

- Payouts are handled by Stripe according to your account settings
- Typically, payouts occur weekly or monthly
- View payout details in your Stripe dashboard

### Resetting Your Connection

If you need to reconnect Stripe:

1. Go to **"Stripe Connect"** under ACCOUNT
2. Use the reset option to disconnect
3. Follow the connection process again

## Stripe Fees

When you receive payments through Authflow, you'll see:

- **Stripe Processing Fee**: Typically 2.9% + $0.30 per transaction
- **Authflow Fee**: 10% per transaction (varies by plan)

**Example:**
- Customer pays $10/month
- Stripe fee: ~$0.59
- Authflow fee: $1.00
- Your net payout: ~$8.41

## Troubleshooting

### Connection Failed

- Make sure you're using the correct Stripe account
- Check that your Stripe account is fully verified
- Try clearing your browser cache and reconnecting

### Payouts Not Appearing

- Verify your bank account is correctly added in Stripe
- Check Stripe's payout schedule settings
- Review any pending verifications in Stripe

For more help, see the **Stripe Guide** in the Support section of your dashboard.
