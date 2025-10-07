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
  - id
  - email
  - first name
  - last name
  - company_id
    - extract via email domain, possibly integrate hunter.io to extract
  - password (hidden, no access in general db)
  - created_at
  - updated_at
  - rfc
  - curp
  - address (use an address api where user types and gets autocomplete for now)
  - phone
  - FK company_id (m2m)
- Company
  - id
  - name
  - legal name (ideally if customer creating a new account, this connects to SAT/gov db with existing company names to get the legal company name as customer types)
  - email_domain
  - created_at
  - updated_at
  - FK user_id (m2m)
- Bank Account
  - id
  - account_number
  - clabe
  - currency
  - name (default 'Cuenta Sol')
  - created_at
  - updated_at
  - type (checking, savings, default checking)
  - status
  - current_balance
  - available_balance
  - FK company_id
- Debit Card
  - id
  - first name
  - last name
  - last4_digits_card
  - pan_token (encrypted version of the full card number)
  - expiry month
  - expiry year
  - cvc_token
  - network (visa, mastercard)
  - image_url (image of card to display in UI to user)
  - status
  - daily_spend_limit
  - billing_address (ideally user inputs and UI autofills the address)
  - created_at
  - updated_at
  - FK bank_account_id
- Transaction
  - id
  - from
  - to
  - amount
  - type (ACH, debit card, interest, adjustment,)
  - direction (debit or credit)
  - currency
  - description
  - counterparty_type
  - counterparty_name
  - counterparty_account_id
  - counterparty_type
  - counterparty_data (json value of all received data from counterparty)
  - fx_rate
  - status
  - posted_at
  - created_at
  - updated_at
  - FK user_id
  - FK bank_account
  - FK company_id
  - FK debit_card_id
  - FK statement_id
- Statement
  - id
  - opening_balance
  - closing_balance
  - transactions
  - FK bank_account_id
  - FK company_id
  - created_at
  - updated_at
  - period_start
  - period_end
  - file_url (pdf)
