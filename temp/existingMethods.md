Here is a list of methods in the HpsCreditService class along with their purposes:

**HpsCreditService** : Initializes a new instance of the HpsCreditService class, optionally accepting a configuration parameter.

**Get** : Retrieves an HPS transaction details given a Transaction ID.

**List** : Retrieves a list of transaction summaries between specified dates and filtered by transaction type, if provided.

**Charge** : Authorizes a sale purchased with a credit card and places the authorization in the current open batch, creating one if necessary. This method is overloaded to handle different types of payment inputs (credit card, token, track data).

**Verify** : Verifies that a credit card account is in good standing with the issuer. This is a zero dollar transaction with no associated authorization.

**Authorize** : Authorizes a credit card transaction without adding it to the batch. This can be committed later using the capture method.

**Capture** : Adds a previously authorized transaction to the current open batch, creating a batch if one does not exist.

**Refund** : Returns funds to the cardholder. This transaction is used as a counterpart to a credit card transaction that needs to be reversed, typically when the original transaction's batch has been closed.

**Reverse** : Reverses a charge or authorization from the active open authorizations or current open batch.

**Void** : Voids a transaction that is still within an open batch or is an open authorization.

**Edit** : Modifies details on a previously approved charge or authorization transaction, such as the amount or gratuity.

**OfflineCharge** : Processes a charge transaction without immediately submitting it online for authorization. This method supports various input types such as credit card information and track data.

**UpdateTokenExpiration** : Updates the expiration date for a stored token.

These methods are part of a service layer that handles various credit card transaction processes such as charging, authorizing, verifying, refunding, reversing, and editing transactions, among others.