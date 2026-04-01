# SWITCH Order Entry API Reference

## Overview

This folder contains documentation and reference implementation for the **SWITCH Order Entry API** used in the **BSE Star MF platform**.

The SWITCH Order Entry API allows members to switch investments from one mutual fund scheme to another scheme within the BSE Star MF system.

In a switch transaction, the system performs two operations:

- Redemption of units from the **source scheme**
- Purchase of units in the **target scheme**

The request is submitted from the **member system** to the **BSE Star MF server** using **SOAP Web Services**.

This repository provides:

- Detailed API structure explanation  
- Request and response parameter reference  
- Sample SOAP request and response  
- Python reference implementation for understanding the API structure  

The API method used for SWITCH transactions is:


---

# API Details

## API Name

SWITCH Order Entry API

## API Method

switchOrderEntryParam

## Endpoint

https://bsestarmfdemo.bseindia.com/MFOrderEntry/MFOrder.svc/Secure

## SOAP Action

http://bsestarmf.in/MFOrderEntry/switchOrderEntryParam


---

# Folder Contents

This folder contains the following files:

## 1️⃣ SWITCH_Order_API_Structure_Document.ipynb

This notebook explains the complete structure of the SWITCH Order Entry API including:

- API introduction  
- Request parameters  
- Response structure  
- Sample SOAP request  
- Sample SOAP response  

This file acts as **technical documentation for the SWITCH Order API**.

---

## 2️⃣ switch_order_api_reference_Python_Structure.ipynb

This notebook contains a **Python reference implementation of the SWITCH Order Entry API**.

It includes:

- API basic information  
- Request parameter structure  
- Response structure  
- Example SOAP request  
- Python code reference for sending requests  

This file is intended for developers who want to understand **how to integrate the API programmatically**.

---

# SWITCH Transaction Types

The API supports the following transaction codes:

| Transaction Code | Description |
|------------------|-------------|
| NEW | Register a new SWITCH order |
| CXL | Cancel an existing SWITCH order |

---

# Key SWITCH Parameters

Some important parameters used in the SWITCH API request:

- TransCode  
- TransNo  
- OrderId  
- UserId  
- MemberId  
- ClientCode  
- FromSchemeCd  
- ToSchemeCd  
- BuySell  
- BuySellType  
- DPTxn  
- OrderVal  
- SwitchUnits  
- AllUnitsFlag  
- FolioNo  
- KYCStatus  
- Password (Encrypted)  
- PassKey  

These parameters help identify the **client, scheme details, transaction type, switch amount/units, and authentication credentials**.

---

# Authentication Requirement

The SWITCH Order API requires **encrypted password authentication**.

The encrypted password used in the request must be generated using the **Authentication API** before placing any order.

---

# Summary

The SWITCH Order Entry API enables members to switch investments between mutual fund schemes by combining redemption and purchase operations within the BSE Star MF platform.

This folder provides a structured explanation and Python reference implementation to help developers understand the **request structure, response format, and required parameters for successful SWITCH order execution**.

