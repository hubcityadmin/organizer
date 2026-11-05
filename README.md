# organizer
Online 1040 Tax Organizer

A web-based tax organizer that clients fill out online, published as a page on the Hub City Tax Pros blog.

## Required Rules

These rules are mandatory. Any code, page, form, or tool built for this organizer must follow every rule below. If a request or change conflicts with these rules, the rules win.

### 1. Never ask for a Social Security Number
- The organizer must never request, collect, or store a Social Security Number (SSN) for the client, spouse, dependents, or anyone else.
- This also covers partial SSNs (such as the last four digits) and Individual Taxpayer Identification Numbers (ITINs).
- No field, prompt, upload instruction, or free-text label may ask for this information.

### 2. Only collect data used in a tax return
- Only request information that can be used to prepare the client's tax return.
- Do not ask for information that is not needed for the return (for example: passwords, bank login credentials, PINs, mother's maiden name, or unrelated personal details).
- Every field must have a clear tax-return purpose.

### 3. Address the tax year first
- The first thing the organizer does is confirm the tax year in question.
- No other data may be requested until the tax year has been selected or confirmed.
- All later questions and labels must refer to that selected tax year.

### 4. Only send data to approved recipients
- Submitted data may be sent **only** to:
  1. `cpa@hubcitytaxpros.com`
  2. The email address the user enters in the organizer's email field (and only that one address).
- The data must never be provided to any other outside source, person, service, or address.

### 5. No other copies
- No other copies of the data may be sent to anyone else, in any form (email, CC, BCC, forwarding, file upload, third-party storage, analytics, logging, or any other method).
- The only exception is if instructions allowing it are written in this README.md file.

## How the organizer works

- `index.html` is the whole organizer: one self-contained web page with no outside scripts, no analytics, no server, and no browser storage.
- `Organizer.pdf` is the reference organizer the questions are based on.
- Order of questions: **Tax year** (required first) → **About You** (everyone) → **Household** → then sections that open only when an answer calls for them (Spouse, Dependents, Self-Employment, Rental Property, and follow-up questions inside each section).
- The client finishes with a **Review & Send** page showing their completed organizer and a printable **Documents to bring** checklist.
- **Email** opens the client's own email app, addressed to `cpa@hubcitytaxpros.com` with a copy to the address in the email field only. Nothing is sent anywhere else.
- If anything is typed that looks like a Social Security number, the page blocks it and asks the client to remove it.
