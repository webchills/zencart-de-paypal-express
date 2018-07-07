Many European Zen Cart stores are setting up their PayPal Express module like this:

Payment Zone
--none--

Express Checkout Shortcut Button
Off

Express Checkout: Require Confirmed Address
No

Express Checkout: Select Cheapest Shipping Automatically
No

Express Checkout: Skip Payment Page
No

Express Checkout: Automatic Account Creation
No

Payment Action
Final Sale

Transaction Currency
Only EUR

Allow eCheck?
Instant Only

So there is no PayPal Express Checkout button or automatic account creation.
The customer has to register normally in the store and indicate a payment and shipping address during the checkout.
Lots of customers have old adresses in their PayPal accounts and do not check their shipping address in PayPal.
In the current module the PayPal address is taken as shipping address for the Zen Cart order, the PayPal address overwrites the shipping address that the customer has selected before in the store.
So the shopowner gets lots of orders with wrong shipping addresses and can never be sure if the customer wants the shipping really to the address in the order confirmation email or shop administration.

To solve this issue here are some modifications for the PayPal Express module in Zen Cart 1.5.5:

This is of course only suitable for stores which are configured as described above!

With these modifications PayPal does not care about shipping addresses and the customer is not able to change the shipping address at PayPal or able to select from his PayPal address book.
No shipping options are presented and the shipping address for the order will always be the one the customer selected before during the Zen Cart checkout.

This is kind of a quick and dirty solution as I just commented out or deleted some code. Would be great to address this issue in upcoming versions as the way it is now is a real pain for many shopowners. 

Installation:

Just choose your Zen Cart version in the folder GEAENDERTE DATEIEN (means changed files):
Zen Cart 155 (suitable for American 155 version only)
Zen Cart 155 German (suitable for German 155 version only)

Then upload the appropriate includes/modules/payment/paypalwpp.php to your Zen Cart installation.