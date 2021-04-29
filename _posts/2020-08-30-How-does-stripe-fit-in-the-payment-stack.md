Stripe is a payment API company that is founded by Irish entrepreneur brothers John and Patrick Collison. Stripe has became extremely popular by building a payment infrastructure that is developer centric. Its customers include companies such as Shopify and Lyft.

In this article I will explain

1. What does Stripe do

1. Introducing the Payment Stack

1. Why use Stripe

1. Who are the competitors of Stripe

## What does Stripe do ?
> ***Stripe is a technology company that builds economic infrastructure for th21.30e internet. Businesses of every size — from new startups to public companies — use our software to accept payments and manage their businesses online.***

This is from [Stripe about page](https://stripe.com/about#:~:text=Stripe is a technology company,and manage their businesses online). Put it simply, Stripe allows businesses to accept money on the internet. Stripe has public companies using their service such as Shopify, Lyft, DoorDash and Instacart. Stripe also has a lot of small business customers. In 2017, Stripe acquired [IndieHacker](https://techcrunch.com/2017/04/11/stripe-acquires-indie-hackers-a-knowledge-sharing-community-for-entrepreneurs/), it is a website where founders of mostly independent business can share their stories transparently, and where entrepreneurs can come to read and learn from those examples. This serves as a gateway to let Stripe collect payments for these small business. In order to further understand how Stripe fits in the payment first we need to talk about the process of payment.

### Process of Payment

The form of payment has evolved over the years, from paying with cash to swiping credit cards and now just paying with your phone. However, the principles of payment hasn’t really changed over the years. It’s the exchange of money. Take the current payment of credit cards as example, it can be broken down into 3 steps: Authorization, Authentication and Settlement

![[https://wallethub.com/edu/cc/credit-card-transaction/25511/#:~:text=The%20issuing%20bank%20receives%20the,from%20the%20credit%20card%20network.&text=The%20merchant's%20POS%20terminal%20will,receipt%20to%20complete%20the%20sale](https://wallethub.com/edu/cc/credit-card-transaction/25511/#:~:text=The%20issuing%20bank%20receives%20the,from%20the%20credit%20card%20network.&text=The%20merchant's%20POS%20terminal%20will,receipt%20to%20complete%20the%20sale)](https://cdn-images-1.medium.com/max/2000/0*QsiJ8c3OlUvWj13n.png)

**Authorization: **The merchant after accepting credit cards, needs to obtain approval for payment from the customer’s credit card bank. It does this by sending the card information via the credit card network to the issuing bank.

**Authentication: **The issuing bank verifies the validity of the customer’s credit card.

**Settlement: **At the end of each day, the merchant batches and submits the transactions for settlement. The customers’ credit card bank then bills the cardholder.

An example would be, say you have a Bank of America (BOA) credit card on the Visa network. You buy a cup of coffee at Starbucks by swiping the credit card processor. The processor sends your information to BOA via the Visa network. After BOA verifies the information, it sends an approval code to the merchant via Visa. At the end of the day, Starbucks sends the batch of approved transactions to settle the payments.

That was a simplified version of the process. This [post](https://wallethub.com/edu/cc/credit-card-transaction/25511/#:~:text=The issuing bank receives the,from the credit card network.&text=The merchant's POS terminal will,receipt to complete the sale) explains the process in greater detail. Based on the process, the payment stack can be broken down into 3 component: Merchant, Payment Network and Consumer. The Merchant payment stack is also known as the acquiring stack. And the consumer payment stack is known as the Issuing stack. Stripe sits in the acquiring stack and can be categorized as a payment facilitator.

To better understand what payment facilitator does, I’ll talk about each entity in the payment stack

## Introducing the Payment Stack

![](https://cdn-images-1.medium.com/max/5200/0*hZ8eRduOER4xA55B)

source: [Finix](https://www.finixpayments.com/blog/understanding-the-payments-stack/#:~:text=The Issuing Payments Stack&text=They are the banks that,on consumer behavior and spending)

### Card Network

A credit card network makes using your credit card possible. Some credit card networks process transactions directly, or will work with card issuers so that your transactions can be completed. The four major credit card networks in the U.S. are Visa, Mastercard, Discover and American Express. It sits between the acquiring and issuing stack.

## Issuing Payment Stack

### Card Holder

Me and you who use the card to purchase products or services from the merchant.

### Card Issuer

A credit card issuer is a bank or credit union who offers credit cards. The credit card issuer extends a credit limit to cardholders who qualify for the credit card. When consumers make credit card purchases, the credit card issuer is responsible for sending payments to merchants for purchases made with credit cards from that bank. Its main job is to approve or deny credit card applications, pay transactions on behalf of the cardholder.

### Issuing Processor

Issuing processors are underlying technology and service providers which help power the cards that issuers offer. Their job includes collecting consumer information, pulls credit bureaus and makes yes/no decision on account opening, authorization/clearing functionality, network settlement.

## Acquiring Payment Stack

### Payment Processor

Send card information to the card network. They primarily process transactions but have also been empowered by acquiring banks to underwrite merchants, manage disputes, and make payouts to merchants.

### Merchant Acquirer ( Acquiring Bank )

Open merchant accounts. Merchant acquirer — A financial institution that enrolls merchants into programs that accept cards. Also referred as payment acquiring bank. Examples include First Data, Chase Paymentech and Vantiv.

### Payment Facilitator

A Payment Facilitator is the new term for entities formally known as Payment Service Providers. A Payment Facilitator is a third party agent that may sign a merchant acceptance contract on behalf of an acquirer and receive settlement of transaction proceeds from an acquirer on behalf of a sponsored merchant. The sponsored merchants are also known as sub-merchants.

### Merchant

Accept payments in exchange for services and goods.

## Why use Stripe?

As a Payment Facilitator, Stripe helps merchants accept payment by doing :

1. Setting up a Sub Merchant Account

1. Setting up a Customizable Payment Gateway

Let talk about them separately.

## Setting up a Sub Merchant Account

A sub merchant account is set up under a merchant account. Merchants with sub-merchant accounts don’t need to set up an account with an acquiring bank. This reduces the complexity of accepting payments online.

So what is a merchant account ? And why do merchants need it ? A merchant account is set up so that a business can accept payment cards (credit, debit and prepaid) from customers. This is different from a business bank account. A business bank account is used to handle expenses related to establishing and maintaining a business — rent and utilities, for example.

A merchant account is an agreement between a merchant and an acquiring bank. This agreement allows the former to process and accept credit card payments. By signing this agreement, a merchant agrees to abide by the operating regulations established by Visa, MasterCard, or any other brand. With a merchant account, it also sets up the necessary technology (including credit card terminals and various processing options including wireless and mobile), handles the authorization of your sales transactions by the issuing bank and deposits the proceeds into the designated bank account.

## Merchant Account Requirements

Setting up a merchant account, requires the payment service provider and the merchant to comply with credit card mandated programs established to ensure security. The program is known as a third-party agent (TPA), it is specified in this [link](https://usa.visa.com/dam/VCOM/download/merchants/tpa-registration-program-faqs.pdf).
> ***A TPA is a type of Agent, not directly connected to VisaNet, that provides payment-related services, directly or indirectly, to a Visa client and/or stores, processes or transmits Visa cardholder data.***

TPA includes independent sales organizations ( ISOs ), Payment Facilitators and other payment service providers. The card networks require banks to register these TPAs to ensure the following:

* Merchants and TPAs adhere to the card networks’ rules.

* Merchant has to meet KYC, AML, and OFAC compliance requirements:

* Receives settlement of transaction proceeds from the acquirer on behalf of the sponsored merchant

By using a payment facilitator, merchants don’t need to set up a merchant account. The payment facilitator onboard the merchant with simpler process. This makes it easier for merchants accept payments. Merchants just have to set up a sub-merchant account under the payment facilitator. The diagram below explains what a payment facilitator does.

![](https://cdn-images-1.medium.com/max/4016/0*FF9Zm7IwUVSyFmpC.png)

Source: [https://stripe.com/guides/payfacs](https://stripe.com/guides/payfacs)

One thing to note is the major card networks (Visa, MasterCard, American Express, Discover) tolerate Payment Facilitators for a business until its sales volume exceeds $100,000.

## Setting up a Customizable Payment Gateway

The second problem Stripe solves is setting a payment gateway. Stripe’s main product is its developer friendly payment API. It can integrate with customers’ system seamlessly. Not only can you collect payment via the API, it can also be used to help businesses efficiently detect fraud and understand their customers ( [Stripe engineering blog on using machine learning to detect fraud](https://stripe.com/blog/engineering) ).

Stripe allows merchants to have freedom to customize the payment experience they want. Compared to PayPal’s primary merchant services, you’ll redirect your customers to a PayPal branded webpage in order to pay. ( This is explained in this [Quora post](https://www.quora.com/How-is-Stripe-different-from-Paypal) )

## What are the advantages of using Stripe

**Customization:**

Stripe is a developer focused company. It provides custom UI toolkit and API. Use can create a customized payment experience. Also Stripe has clean and elegant documentation for it’s API. I’ve became a fanboy after using it’s payment solution myself,

**Transparent Pricing:**

Stripe has a simple, transparent pricing structure and only charges transaction fees. It only charges one rate for each transaction (starting at 2.9% + $0.30 per transaction for US businesses for online payments.

**Functionality:**

Stripe allows users to accept all types of payments including credit card, ACH, Apply Pay and etc. This is documented extensively in this [post](https://stripe.com/payments/payment-methods-guide#introduction). Stripe also provides multiple features to help manage payments, respond to dispute, monitor integration on the users’ platforms. Also as Stripe handles more and more payments, it will increase it’s ability to label fraud accounts.

## Why is Stripe suddenly gaining usage ? Why Now ?

Payment processing have been existing for a long time, companies like Paypal existed since 1999. Why is Stripe’s payment API suddenly gaining popularity ? Jay Kreps the founder of Confluent and also part of the team that built Kafka wrote a [great article](https://www.confluent.io/blog/every-company-is-becoming-software/) on the process of companies becoming software companies. Below is quoted from the article:
> ***The purpose of an application, in this emerging world, is much less likely to be serving a UI to aid a human in carrying out the activity of the business, and far more likely to be triggering actions or reacting to other pieces of software to carry out the business directly.***

![](https://cdn-images-1.medium.com/max/2202/0*3yF36PznZTUFtVOU.png)

As business logic increasingly gets encoded into software. Everything from payments, customer service, producing products, delivering services is executed in software. Companies now have to rely more on API services. This creates a huge market for Stripe to provide easy to use, easy to integrate payment API.

## Who are the competitors of Stripe

As online payment increases continues to increase. The share of e-commerce sales of total U.S. retail sales more than doubled from 5% in 2010 to 12% in 2020 ( [post](https://www.statista.com/statistics/187439/share-of-e-commerce-sales-in-total-us-retail-sales-in-2010/) ). There will be more and more players trying enter the payment infrastructure space as payment methods and consumer behavior keeps involving. I will talk about some of Stripe’s competitors:

**Square:** The main difference between Square and Stripe is Square is more specialized in the point of sales software and hardware. Square offers a more user friendly solution for building online and in person payments.

**Paypal:** Paypal is very similar to Stripe as it is focused on providing an online payment experience. If you are looking for a wide range of configuration and customization, then Stripe is the better option. If you want a straight forward configuration, then Paypal is more convenient.

**Adyen:** Adyen is similar to Stripe that it is also provides a [payment API](https://docs.adyen.com/api-explorer/#/PaymentSetupAndVerificationService/v53/overview). The biggest difference is it also a merchant provider. Adyen provides each of their customers a dedicated merchant account, which means it will take longer to apply for an Adyen account.

**Finix:** Finix might be the most different competitor out of the 4. Finix provides payment building blocks to companies. Unlike Stripe, Finix requires companies to control their own payment stack. It doesn’t charge merchants based on transaction, instead it makes money by a monthly licensing fee.

## Closing

This is a brief overview of how stripe fits in the payment stack. If you want to learn more about the company, the founders often show up on Podcasts to talk about how they manage the company, how they view the future of the company or how they view the world.

As Stripe continue to build a better payment experience for everyone with Stripe Terminal, Stripe issuing and increased Global payment. I believe Stripe will continue to play a big part in increasing the GDP of the Internet.

This article is based on me googling some stuff. If there’s some information that I got wrong feel free to let me know.

## References
[**Stripe Teardown: How The $35B Payments Company Plans To Supercharge Online Retail | CB Insights**
*As businesses and consumers become more comfortable using credit cards online, the proportion of US commerce that takes…*www.cbinsights.com](https://www.cbinsights.com/research/report/stripe-teardown/#next)
[**Deciphering the payments stack**
*You step out of your Uber and walk away without ever touching your wallet. It’s a magical experience. So what’s behind…*medium.com](https://medium.com/@stephenjcho/deciphering-the-payments-stack-efbcb9c8eac4)
