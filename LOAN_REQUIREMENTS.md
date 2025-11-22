# Mexico SMB (PyME) Loan Origination – Comprehensive Requirements

Below is a comprehensive, Mexico-specific requirements list you would typically need when automating a loan origination system for SMBs (PyMEs). It is divided into:

- Data required from the loan applicant (the SMB and its owners).
- Additional data typically required by banks in Mexico during origination.
- Data points needed for AI analysis and risk scoring.

This reflects requirements aligned with common practices in Mexican banking, CNBV regulations, AML/KYC rules, and standard PyME credit processes.

---

## ✅ 1. Information Required Directly from the Applicant (Business & Owners)

### A. Business Identity & Registration
- Business legal name (Razón social)  
- Commercial name (Nombre comercial)  
- RFC (Registro Federal de Contribuyentes)  
- CURP of legal representative (if applicable)  
- Type of entity (Persona Moral / Persona Física con Actividad Empresarial)  
- Incorporation documents:  
  - Acta constitutiva  
  - Powers of attorney (poderes notariales)  
- Industry/Sector (NAICS/SCIAN code)  
- Business address & proof of address (comprobante de domicilio)

### B. Legal Representative Information
- Full name  
- CURP  
- RFC  
- Official ID (INE/Passport)  
- Proof of address  
- Email + Phone  
- Ownership % (if also a shareholder)

### C. Shareholder / Beneficial Owner (UBO) Information
(Required under AML/KYC)
- Full name  
- CURP  
- RFC  
- ID documents  
- Percentage of ownership  
- Source of wealth/funds (Origen de recursos)

### D. Financial Information (Business)
- Monthly/annual revenue (Ingresos)  
- Monthly/annual expenses (Egresos)  
- Profit margins  
- **Financial statements**  
  - Balance sheet  
  - Income statement  
  - Cash flow statement  
- Last 3–12 months of bank statements  
- Tax compliance documents  
  - SAT Opinión de Cumplimiento Positiva  
  - SAT digital invoices (CFDI metadata)  
- Debts & obligations  
  - Existing loans  
  - Leasing  
  - Credit cards  
  - Supplier financing

### E. Operational & Business Profile
- Number of employees  
- Years in operation  
- Business model description  
- Main clients and suppliers  
- Sales channels (online/offline)  
- Inventory level (if applicable)  
- Key business risks (industry-specific)

### F. Loan-Specific Information
- Loan amount requested  
- Purpose of the loan  
- Preferred loan tenure  
- Collateral (if any)  
- Existing banking relationship

### G. Consent & Compliance
- Privacy/data usage consent  
- Permission to pull credit bureau data (Buró de Crédito / Círculo de Crédito)  
- AML/KYC declarations  
- e-Signature (Firma electrónica)

---

## ✅ 2. Additional Requirements Banks Typically Need in Mexico (Internal Origination Requirements)

### A. Credit Bureau Data (mandatory)
- Buró de Crédito score  
- Credit history (business + shareholders)  
- Credit lines, payment behavior  
- Historical defaults  
- Alerts (fraud, identity issues)

### B. SAT Data Extraction (API or OCR)
Banks typically extract:
- CFDI invoice history  
- IVA/ISR declarations  
- DIOT  
- Payroll (Nómina CFDIs)  
- Opinion de Cumplimiento  
- Monthly revenue trend from invoices  
- FIEL/e.firma validation

### C. Bank Verification
- Bank account ownership validation  
- Bank transaction categorization  
- Cash-flow pattern analysis  
- Concentration risk (client dependency)

### D. AML / Compliance Checks
- PLD/KYC questionnaires  
- UBO verification  
- PEP screening  
- Sanctions lists  
- Blacklists (SAT 69-B)  
- Suspicious behavior profiling

### E. Legal & Operational Requirements
- Review of incorporation & powers of attorney  
- Verification of legal representative identity  
- Business existence verification  
- Validation of contracts & agreements  
- Insurance requirements (for secured loans)

### F. Collateral Evaluation (if secured)
- Appraisal of real estate, vehicles, machinery  
- Liens verification (Registro Público de la Propiedad & REPUVE)  
- Inventory valuation  
- Guarantor information (ﬁadores/avales)

### G. Risk Analysis & Financial Modeling
- Debt-service coverage ratio (DSCR)  
- Leverage ratio  
- Liquidity ratios  
- Seasonality evaluation  
- Expense sensitivity analysis  
- Cash-flow volatility

### H. Fraud Prevention
- Identity verification  
- Document authenticity validation  
- Facial match / liveness detection  
- Device & geolocation consistency  
- Contract tamper detection

---

## ✅ 3. AI-Driven Data Points Needed for Automated Loan Origination

### A. Structured Financial Indicators
- Monthly revenue trend  
- Revenue volatility  
- Expense categorization  
- Net cash flow calculation  
- Burn rate  
- Credit utilization ratio  
- Payment punctuality

### B. Alternative/Behavioral Data
- Digital footprint (optional)  
- E-commerce sales data  
- POS transaction logs  
- Inventory turnover  
- Social media engagement (if permitted)

### C. Fraud & Risk AI Signals
- Inconsistencies between SAT and bank transactions  
- Fake invoices or inactive CFDIs  
- ID anomaly detection  
- Unusual cash spikes  
- Contradictory ownership records

### D. Predictive Scoring Inputs
- Probability of default (PD)  
- Loss given default (LGD)  
- Expected credit loss (ECL)  
- Contractual cash flow prediction  
- Industry risk profile

---

## ✅ Complete Data Needed for an SMB Loan Origination in Mexico
- Personal & business identity data  
- Financial statements  
- Bank statements  
- Invoices & SAT tax data (CFDIs)  
- Credit bureau data  
- Operational business profile  
- Collateral information  
- AML/KYC/UBO verification  
- Loan request & purpose  
- AI-extracted financial insights

---

If you'd like, I can also produce:

- **A full data schema (JSON/YAML)**  
- **A scoring model outline (PD, risk rules, cashflow models)**  
- **A workflow diagram**  
- **Mock onboarding UI flows**

Just tell me what you'd like next!
