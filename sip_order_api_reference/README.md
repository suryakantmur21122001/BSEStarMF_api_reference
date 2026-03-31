# SIP Order Entry API Reference

## Overview

This folder contains documentation and reference implementation for the **Systematic Investment Plan (SIP) Order Entry API** used in the BSE Star MF platform.

The SIP Order Entry API allows members to **register a new SIP order or cancel an existing SIP registration** for a mutual fund scheme through the BSE Star MF web service.

This repository provides:

* Detailed **API structure explanation**
* **Request and response parameter reference**
* **Sample SOAP request and response**
* **Python reference implementation for understanding the API structure**

The API method used for SIP transactions is:

```
sipOrderEntryParam
```

---

## API Details

**API Name**

SIP Order Entry API

**API Method**

```
sipOrderEntryParam
```

**Endpoint**

```
https://bsestarmfdemo.bseindia.com/MFOrderEntry/MFOrder.svc/Secure
```

**SOAP Action**

```
http://bsestarmf.in/MFOrderEntry/sipOrderEntryParam
```

---

## Folder Contents

This folder contains the following files:

### 1️⃣ SIP_Order_API_Structure_Document.ipynb

This notebook explains the **complete structure of the SIP Order Entry API** including:

* API introduction
* Request parameters
* Response structure
* Sample SOAP request
* Sample SOAP response

This file acts as **technical documentation for the SIP API**.

---

### 2️⃣ sip_order_api_reference.ipynb

This notebook contains a **Python reference implementation** of the SIP Order Entry API.

It includes:

* API basic information
* Request parameter structure
* Response structure
* Example SOAP request
* Python code reference for sending requests

This file is intended for **developers who want to understand how to integrate the API programmatically**.

---

## SIP Transaction Types

The API supports the following transaction codes:

| Transaction Code | Description            |
| ---------------- | ---------------------- |
| NEW              | Register a new SIP     |
| CXL              | Cancel an existing SIP |

---

## Key SIP Parameters

Some important parameters used in the SIP API request:

* TransactionCode
* UniqueRefNo
* SchemeCode
* MemberCode
* ClientCode
* UserID
* StartDate
* FrequencyType
* InstallmentAmount
* NoOfInstallment
* Password (Encrypted)
* PassKey

These parameters help identify the **client, scheme, SIP frequency, installment amount, and authentication credentials**.

---

## Authentication Requirement

The SIP Order API requires **encrypted password authentication**.

The encrypted password used in the request must be generated using the **Authentication API** before placing any order.

---

## Summary

The **SIP Order Entry API** enables members to register and manage systematic investment plans for clients through the BSE Star MF platform.

This folder provides a **structured explanation and Python reference implementation** to help developers understand the request structure, response format, and required parameters for successful SIP registration.

---
