# Reading 34: Payment Processing

### How to read Technical Documents as fast as possible

1. Establish why you are reading it.

2. Get an overview of the content and structure of the document.

3. Take 30s to 2 minutes to scan the rest of the document.

4. If you want, stop at the interesting parts and take a deeper look. Stop when it gets boring.

5. Look at the table of contents again. You'll have a deeper understanding of the document after you look again.

6. Choose what to read next based on interesting-ness or usefulness. If there's nothing useful, close the doc.

### How Does Online Credit Card Processing Work?

**Merchant Accounts**
-  The Merchant Account is how you connect to the credit card processing network. 
- Merchant Accounts accept (or decline) credit cards and ultimately transfer the funds into your bank account.

**Payment Gateway**
- responsible for sending the credit card to the appropriate Internet Merchant Account over secure online channels.
- Gateway as a router that sends the credit card information to the appropriate account.

**Your Application**
- Can interact with the Payment Gateway in a number of different ways.  For simple applications, such as a shopping cart program, the user may simply be transferred to a web page on the Gateway for credit card processing.  When the transaction is complete, the user is transferred back to the application.

**How the process would work if you had an application such as online registration:**
- User enters credit card information into the application
- Credit card information is sent to the Payment Gateway via a secure channel
- The Payment Gateway routes the credit card to the appropriate Internet Merchant Account
- Internet Merchant Account connects to the Merchant Account for credit card processing.
- The result is passed back to the Gateway and then the application.

**Fees!**

The Merchant Account will have one or more of these fees:
- One-time setup fee
- Recurring monthly fees
- Per Transaction fees.