# SPREAD Order Entry API Reference

## Overview

This folder contains documentation and reference implementation for the **SPREAD Order Entry API** used in the **BSE Star MF platform**.

The SPREAD Order Entry API allows members to place a **spread transaction**, where a **redemption order and purchase order are processed together**. This enables investors to **switch their investment from one mutual fund scheme to another scheme** within the BSE Star MF system.

The request is submitted from the **member system to the BSE Star MF server using SOAP Web Services**.

This repository provides:

- Detailed API structure explanation  
- Request and response parameter reference  
- Sample SOAP request and response  
- Python reference implementation for understanding the API structure  

The API method used for SPREAD transactions is:

`spreadOrderEntryParam`

---

# API Details

## API Name
SPREAD Order Entry API

## API Method
`spreadOrderEntryParam`

## Endpoint
`https://bsestarmfdemo.bseindia.com/MFOrderEntry/MFOrder.svc/Secure`

## SOAP Action
`http://bsestarmf.in/MFOrderEntry/spreadOrderEntryParam`

---

# Folder Contents

This folder contains the following files:

## 1️⃣ SPREAD_Order_API_Structure_Document.ipynb

This notebook explains the **complete structure of the SPREAD Order Entry API**, including:

- API introduction  
- Request parameters  
- Response structure  
- Sample SOAP request  
- Sample SOAP response  

This file acts as **technical documentation for the SPREAD Order API**.

---

## 2️⃣ spread_order_api_reference_Python_Structure.ipynb

This notebook contains a **Python reference implementation of the SPREAD Order Entry API**.

It includes:

- API basic information  
- Request parameter structure  
- Response structure  
- Example SOAP request  
- Python code reference for sending requests  

This file is intended for **developers who want to understand how to integrate the API programmatically**.

---

# SPREAD Transaction Types

The API supports the following transaction codes:

| Transaction Code | Description |
|------------------|-------------|
| NEW | Register a new SPREAD order |
| CXL | Cancel an existing SPREAD order |

---

# Key SPREAD Parameters

Some important parameters used in the SPREAD API request include:

- TransactionCode  
- UniqueRefNo  
- OrderID  
- UserID  
- MemberID  
- ClientCode  
- SchemeCode  
- BuySell  
- BuySellType  
- DPTxn  
- PurchaseAmount  
- RedemptionAmount  
- RedeemDate  
- KYCStatus  
- Password (Encrypted)  
- PassKey  

These parameters help identify:

- The client  
- Mutual fund scheme  
- Transaction type  
- Redemption and purchase details  
- Authentication credentials  

---

# Authentication Requirement

The **SPREAD Order API requires encrypted password authentication**.

The encrypted password used in the request must be **generated using the Authentication API** before placing any order.

Without proper authentication, the API request will not be processed by the BSE Star MF system.

---

# Summary

The **SPREAD Order Entry API** enables members to **switch investments between mutual fund schemes** by combining **redemption and purchase operations into a single transaction** through the **BSE Star MF platform**.

This folder provides:

- Structured explanation of the API  
- Python reference implementation  
- Request and response examples  

This documentation helps developers understand the **API structure, required parameters, and integration process** for successful SPREAD order execution.
