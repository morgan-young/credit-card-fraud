## Detecting Fraudulent Credit Card Transactions Using Deep Learning

![Credit Card](https://cdn.hswstatic.com/gif/revolving-credit-1.jpg)

### Data Summary

This data contains real card transactions from European cardholders over a two day period. There are over 250,000 transactions and the fraudulent transactions make up 0.172% of the total transactions. This may seem small, but is usual for this industry and nevertheless is still an issue that needs to be tackled.

Because the data is real and obtained (open source) from a third party, it has all been completely anonymised and normalised using PCA transformation, meaning the column names and the individual records won't make sense to us looking at it. There are only two columns that have been left as they were originally, 'Time' and 'Amount'. 'Time' is the number of seconds that transaction took place after the first in the dataset and 'Amount' is the amount of the transaction. The 'Class' identifier (1 or 0) indicates whether the transaction was indeed fraudulent or not.

### Problem Statement

Large financial institutions and brand new FinTech startups are all facing the same issues when it comes to KYC, regulatory compliance and fraud. The difference is that large institutions have well established means of detecting and dealing with fraud, but FinTech startups... not as much.

Initially, many FinTech's start off unregulated, becoming an Authorised Representative of an FCA authorised & regulated entity and in that case the buck stops with the regulated partner for compliance issues, but with the large boom recently of card companies/new banks (Revolut, N26, Monzo, Starling, Soldo, etc.) getting their own regulation directly with the FCA and taking the challenge to the incumbents, they are a potential goldmine for fraudsters in terms of card fraud.

Revolut have even been in the news recently for switching off their Anti-Money Laundering detection system for two months because it showed too many false positives (https://www.kycbench.com/revolut-and-its-aml/). 

For too long, FinTechs have had to rely on rules based systems for AML & fraud detection, for example:

1. Is the transaction 5 x larger than any transaction they've made before?
2. Is the transaction being made from an IP address outside of their registered domicile?
3. Is the transaction for a different/restricted/unusual merchant category code (MCC)?
4. Have they made 3 x the usual amount of transactions in a 24, 48 and 72 hour period?

The problem with rules based systems is they are only as good as the rules that are fed into them and can lead to a large amount of false positives for example when someone goes on holiday, or buys a car, or changes shopping habit... and these are not necessarily signs that there is fraudulent activity on the account and this also risks annoying customers and having them move on to the next FinTech upriser. So, what is a potential solution to this?

### Solution

An intelligent, non-rules based system that uses real card transactions, both fraudulent and non-fraudulent, to learn what aspects of a transaction make it likely to be fraud based on hundreds of thousands or millions of records, and flag potentially fraudulent transactions on that basis.

Deep learning is one way of achieving this that produced a very accurate result (99.4% accurate) in this case study.
