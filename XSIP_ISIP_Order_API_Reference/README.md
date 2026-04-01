# XSIP / ISIP Order Entry API Reference

## Overview

This folder contains documentation and reference implementation for the **XSIP / ISIP Order Entry API** used in the **BSE StAR MF platform**.

The XSIP / ISIP Order Entry API allows members to register **electronic SIP (eSIP)** or **Internet SIP (iSIP)** mandates for mutual fund investments through the BSE StAR MF web service.

These SIP modes enable automated debit of installment amounts directly from the investor’s bank account through mandate-based payment systems.

This repository provides:

* Detailed API structure explanation
* Request and response parameter reference
* Sample SOAP request and response
* Python reference implementation for understanding the API structure

The API method used for XSIP / ISIP transactions is:

XSIPISIPOrderEntryParam

---

## API Details

### API Name

XSIP / ISIP Order Entry API

### API Method

XSIPISIPOrderEntryParam

### Endpoint

https://bsestarmfdemo.bseindia.com/MFOrderEntry/MFOrder.svc/Secure

### SOAP Action

http://bsestarmf.in/MFOrderEntry/XSIPISIPOrderEntryParam

---

## Folder Contents

This folder contains the following files:

### 1️⃣ XSIP_ISIP_API_Structure_Document.ipynb

This notebook explains the complete structure of the **XSIP / ISIP Order Entry API** including:

* API introduction
* Request parameters
* Response structure
* Sample SOAP request
* Sample SOAP response

This file acts as **technical documentation for the XSIP / ISIP API**.

### 2️⃣ xsip_isip_order_api_reference.ipynb

This notebook contains a **Python reference implementation** of the XSIP / ISIP Order Entry API.

It includes:

* API basic information
* Request parameter structure
* Response structure
* Example SOAP request
* Python code reference for sending requests

This file is intended for developers who want to understand how to **integrate the API programmatically**.

---

## XSIP / ISIP Transaction Types

The API supports the following transaction codes:

| Transaction Code | Description                            |
| ---------------- | -------------------------------------- |
| NEW              | Register a new XSIP / ISIP mandate     |
| CXL              | Cancel an existing XSIP / ISIP mandate |

---

## Key XSIP / ISIP Parameters

Some important parameters used in the XSIP / ISIP API request include:

TransactionCode
UniqueRefNo
SchemeCode
MemberCode
ClientCode
UserID
StartDate
FrequencyType
InstallmentAmount
NoOfInstallment
MandateType
MandateID
BankAccountNumber
IFSCCode
Password (Encrypted)
PassKey

These parameters help identify the **client, mutual fund scheme, mandate details, SIP frequency, installment amount, and authentication credentials**.

---

## Authentication Requirement

The XSIP / ISIP Order API requires **encrypted password authentication**.

The encrypted password used in the request must be generated using the **Authentication API** before placing any order request.

This ensures that the request is **securely authenticated between the member system and the BSE StAR MF server**.

---

## Summary

The **XSIP / ISIP Order Entry API** enables members to register and manage **electronic mandate-based SIP investments** for clients through the **BSE StAR MF platform**.

This folder provides a **structured explanation and Python reference implementation** to help developers understand:

* Request structure
* Response format
* Required parameters
* Authentication requirements

This documentation helps developers integrate the **XSIP / ISIP order functionality** into their applications effectively.
