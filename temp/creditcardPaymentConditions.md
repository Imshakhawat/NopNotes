credit card charging conditions - 

- **WithTransactionData**(TransactionData value): Sets transaction-specific data.

- **WithShippingDate**(DateTime value): Sets the shipping date for a transaction.

- **WithAccountType**(AccountType value): Sets the type of account (e.g., checking, savings) involved in the transaction.

- **WithAddress**(Address value, AddressType type): Sets the billing or shipping address for the transaction.

- **WithAlias**(AliasAction action, string value): Sets or modifies an alias used in the transaction.

- **WithAllowDuplicates**(bool value): Enables or disables the acceptance of duplicate transactions.

- **WithAllowPartialAuth**(bool value): Allows or disallows partial authorization of the transaction amount.

- **WithAmount**(decimal? value): Sets the amount for the transaction.

- **WithAutoSubstantiation**(AutoSubstantiation value): Associates auto substantiation data with the transaction.

- **WithBalanceInquiryType**(InquiryType? value): Sets the type of balance inquiry.

- **WithBills**(Bill[] values): Sets bills related to the transaction.

- **WithCustomer**(Customer value): Associates a customer with the transaction.

- **WithCashBack**(decimal? value): Sets the amount of cash back requested in the transaction.

- **WithClientTransactionId**(string value): Sets a unique identifier for the transaction from the client's side.

- **WithCurrency**(string value): Sets the currency for the transaction.

- **WithFraudFilter**(FraudFilterMode fraudFilter, FraudRuleCollection fraudRules): Configures fraud filters and rules for the transaction.

- **WithCustomData**(string[] values): Adds custom data fields to the transaction.

- **WithCvn**(string value): Sets the Card Verification Number for the transaction.

- **WithDescription**(string value): Provides a description for the transaction.

- **WithDynamicDescriptor**(string value): Sets a dynamic descriptor that appears on the customer’s statement.

- **WithEcommerceInfo**(EcommerceInfo value): Provides details related to an e-commerce transaction.

- **WithEmvFallbackData**(EmvFallbackCondition condition, EmvLastChipRead lastRead, string appVersion): Sets EMV fallback data for the transaction.

- **WithGratuity**(decimal? value): Sets the gratuity amount for the transaction.

- **WithIdempotencyKey**(string value): Sets an idempotency key to prevent duplicate transactions from processing.

- **WithInvoiceNumber**(string value): Sets the invoice number for the transaction.

- **WithOrderDetails**(OrderDetails value): Sets detailed information about the order associated with the transaction.

- **WithPaymentMethodUsageMode**(PaymentMethodUsageMode? value): Sets how the payment method is intended to be used.

- **WithPhoneNumber**(string phoneCountryCode, string number, PhoneNumberType type): Sets various types of phone numbers (home, work, mobile) related to the transaction.

- **WithProductData**(ProductData value): Adds product-specific data to the transaction.

- **WithSurchargeAmount**(decimal? value): Sets a surcharge amount that will be applied to the transaction.