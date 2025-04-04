# Big Willy's Fabric Dye Emporium

A simple landing page for Purple Jesus Fabric Dye with integrated payment processing.

## Payment Integration Instructions

### Google Pay Integration

To complete the Google Pay integration:

1. **Register as a Google Pay merchant**:
   - Go to the [Google Pay Business Console](https://pay.google.com/business/console/)
   - Create a merchant account if you don't have one
   - Complete the verification process

2. **Get API credentials**:
   - Once verified, get your Merchant ID
   - Update the `YOUR_MERCHANT_ID` placeholder in the code

3. **Set up a payment gateway**:
   - Google Pay requires a payment processor/gateway (Stripe, Braintree, etc.)
   - Sign up with a payment processor
   - Get your gateway credentials
   - Update the `YOUR_PAYMENT_GATEWAY` placeholder in the code

4. **Set up a server endpoint**:
   - Create a server endpoint to process the payment token
   - Uncomment the `processPaymentOnServer(paymentData)` line
   - Implement the server-side processing logic

5. **Switch to production**:
   - When ready to go live, change `environment: 'TEST'` to `environment: 'PRODUCTION'`

### Cash App Integration

To complete the Cash App integration:

1. **Create a Cash App for Business account**:
   - Sign up at [Cash App for Business](https://cash.app/business)
   - Complete the business verification process

2. **Set up Cash App API**:
   - Register as a developer at [Cash App Developer Portal](https://developers.cash.app/)
   - Create an application to get your API credentials

3. **Create a server endpoint**:
   - You'll need a server endpoint to create Cash App payments
   - Update the URL `https://your-server.com/create-cashapp-payment` with your actual endpoint
   - Your server should use the Cash App API to create a payment and return the payment URL

4. **Handle webhooks**:
   - Set up webhook handling to receive payment notifications
   - Update your database when payments are completed

## Important Security Notes

- Never expose API keys in client-side code
- Always process payments through a secure server
- Use HTTPS for all payment-related communications
- Test thoroughly before going live 