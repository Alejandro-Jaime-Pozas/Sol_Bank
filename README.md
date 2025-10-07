# Sol Bank Overview

Sol Bank is the most user-friendly Mexican online bank made for small businesses. It is based on the idea that my experience with BBVA and Banregio business banks were both very poor in terms of ease of onboarding, and ease of use and making payments. The overall experience was terrible, with account creation a pain and making payments even more pain. I had to switch from Banregio to BBVA because of the terrible experience (which was a bit better, but still a lot of pain points that needed solving).

So, Sol Bank is an online bank for pymes (small to medium businesses) that aims to create the best user experience ever. This includes anything related to saving a user's time.

The initial products offered are:

- business account (debit/checking account)
- credit card account
- business loan account
- savings account

Start ONLY with business account.

## Scope

The initial scope will include simulated money, not real money a user can deposit/withdraw into Sol accounts. The purpose is to learn and set up a banking simulator that can later be converted into an actual banking app.


## Business Account

This is a checking/debit account where the user deposits/withdraws money.

This includes the ability for the user to:

- transfer money to and from that business account
- get a debit card (virtual for now)
- view all of their transactions
- view all of their monthly statements
- download all of their monthly statements
- get AI chat support on any issues they have in their account

*Those are the initial main use cases, more may come.*


## Backend

### Data Architecture

The objects required to build out this initial phase of the app include:

- User
  - first name
  - last name
  - email
  - company name
    - extract via email domain, possibly integrate hunter.io to extract
  - password
- Company
- Bank Account
- Debit Card
  - first name
  - last name
  - card number
  - expiry date
  - CVC code
  - processor (visa, mastercard)
  - image (image of card to display in UI to user)
- Transaction
  - from
  - to
  - amount
  - timestamp created
  - user
  - bank account
- Statement
  - current balance
  - previous balance
  - transactions
  - user
  - bank account

