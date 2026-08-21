# Diona-Project-2
# Criminal Risk Assessment Request — ODK XLSForm

## Overview

This project converts the provided Criminal Risk Assessment Request PDF into a functional ODK XLSForm.

The form uses XLSForm logic to handle conditional fields, required fields, validation rules, and consent-dependent behaviour instead of treating the PDF as a simple static form.

## Key Features

- Consent and unconsented workflow
- Consent-dependent assessment reason validation
- Two-piece identification validation
- Conditional identification fields
- Conditional requiredness for ID details
- Automatic subject-name display on the request section
- Required-field validation
- Email format validation
- Phone and fax number validation
- Signature capture
- ODK-compatible XForm generation

## Form Logic

### Consent

When the subject provides consent, the consent date, signature, and witness fields are available.

When the form is marked as **Unconsented**, these fields are hidden.

The assessment reason is also validated based on the consent status.

### Identification

The form requires at least **two pieces of identification**.

If `Other (specify ID)` is selected, the user must provide the identification details.

If `MB Driver's License with Photo` is selected, the licence number becomes required.

### Validation

The form validates important data before submission, including:

- Required fields
- Email format
- Phone numbers
- Fax numbers
- Identification requirements
- Consent-dependent rules

## Files

- `Criminal_Risk_Assessment_Request_XLSForm.xlsx` — XLSForm source
- `Criminal_Risk_Assessment_Request_XLSForm.xml` — Generated XForm
- `survey.csv` — Survey structure
- `choices.csv` — Choice lists
- `settings.csv` — Form settings

## Validation

The XLSForm was converted and validated using `pyxform`.

**Result:** 0 errors.

## Technologies

- ODK XLSForm
- XLSForm / Excel
- XPath expressions
- pyxform
- XForm / XML
## Video Submission

[Round 2 Assignment Walkthrough](videos/Round2-walkthrough.mp4), 
[Round 2 Assignment Walkthrough](https://drive.google.com/file/d/1ufem2Nujpq1eikbeRjk2BsXpGFM9SICv/view?usp=sharing)[Google Drive Link]