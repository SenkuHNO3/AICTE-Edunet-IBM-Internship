# College Admission Agent (RAG-Based with IBM Cloud & Granite)

A conversational AI agent that streamlines the college admission process by answering applicants’ questions in real-time using Retrieval-Augmented Generation (RAG) and IBM Granite foundation models, deployed end-to-end on IBM Cloud.

## Demo Screenshots

<img src="https://github.com/SenkuHNO3/AICTE-Edunet-IBM-Internship/blob/2c71b2c89678fcebdaeab4754f700ac7fe941e4d/project%20info/preview.png" alt="" width="50%">
<img src="https://github.com/SenkuHNO3/AICTE-Edunet-IBM-Internship/blob/2c71b2c89678fcebdaeab4754f700ac7fe941e4d/project%20info/ex1.png" alt="" width="50%">
<img src="https://github.com/SenkuHNO3/AICTE-Edunet-IBM-Internship/blob/2c71b2c89678fcebdaeab4754f700ac7fe941e4d/project%20info/ex2.png" alt="" width="50%">

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Step-by-Step Deployment Guide](#step-by-step-deployment-guide)
  - [1. Set up IBM Cloud Account](#1-set-up-ibm-cloud-account)
  - [2. Create watsonx.ai Studio & Object Storage](#2-create-watsonxai-studio--object-storage)
  - [3. Set Up Project & Associate Services](#3-set-up-project--associate-services)
  - [4. Create and Configure Agent with Granite Model](#4-create-and-configure-agent-with-granite-model)
  - [5. Vector Index Creation and Knowledge Base Upload](#5-vector-index-creation-and-knowledge-base-upload)
  - [6. Agent Customization, Tools, and Testing](#6-agent-customization-tools-and-testing)
  - [7. Deployment and API Access](#7-deployment-and-api-access)

## Overview

The College Admission Agent answers queries on eligibility, deadlines, fees, application steps, and more by retrieving and summarizing up-to-date institutional documents and policies. Built with IBM Granite models using Retrieval-Augmented Generation (RAG), it delivers personalized, instant support to students, parents, and staff.

## Features

- **Smart Retrieval**: Finds and summarizes official admissions data (policies, FAQs, forms, deadlines).
- **Conversational Interface**: Natural language Q&A via web or chat.
- **Always Up-to-Date**: Pulls the latest information from designated college sources.
- **Personalized Guidance**: Offers context-aware recommendations and eligibility insights.
- **Automated Notifications**: Exam timelines, fee due dates, and application status.
- **Scalable**: Ready for multi-institution and multilingual deployment.

## Architecture

- **Frontend/UI**: Chat/web interface for user interaction.
- **Backend**: RAG pipeline with IBM Granite model for answer generation.
- **Knowledge Base**: Uploaded PDFs, DOCX, TXT, and policy files vectorized and used for semantic search.
- **IBM Cloud**: Manages infrastructure, storage, and secure deployment.

## Step-by-Step Deployment Guide

### 1. Set up IBM Cloud Account

- Visit [IBM Cloud](https://cloud.ibm.com/) and **sign up** or log in.
- Complete email verification and account registration.

### 2. Create watsonx.ai Studio & Object Storage

- In the IBM Cloud **Catalog**, search for “watsonx.ai Studio” and provision an instance (Lite plan for free trial).
- Select your region (e.g., London).
- Similarly, provision **Cloud Object Storage** (Lite plan).

### 3. Set Up Project & Associate Services

- In watsonx, **create a Project**: Define name and add the provisioned Object Storage.
- **Associate Services**: Add a watsonx.ai Runtime for foundation model access.

### 4. Create and Configure Agent with Granite Model

- Inside your Project, enter **Agent Lab** and click “Build an AI agent.”
- Change the model to IBM Granite (or the foundation model of your choice).
- Set instructions for your agent:  
  > You are a helpful assistant that answers college admission queries in detail...

### 5. Vector Index Creation and Knowledge Base Upload

- Go to **Knowledge → New vector index**.
- Upload college documents (PDFs, DOCX, TXT)—admission brochures, FAQs, rulebooks.
- Name and create your vector index.
- The agent will now have access to contextually search your knowledge base.

### 6. Agent Customization, Tools, and Testing

- Add custom tools (document search, web search if needed).
- Set up actions for main admission topics: e.g., courses offered, how to apply, important dates.
- Test sample queries in the preview/chat panel to ensure accurate retrieval and response.

### 7. Deployment and API Access

- **Save your agent** and deploy from the deployment menu.
- Create a Deployment Space if needed (delete any unused spaces if running into limits).
- On deploy, IBM Cloud provides public and private **API endpoints** for integration.
- View agent in preview or connect your UI/frontend for live queries.

## How It Works

1. **User asks a question** (e.g., "What is the last date to apply for BTech?")
2. **Backend retrieves relevant document passages** using the vector index (RAG).
3. **Granite model synthesizes a clear, contextually-grounded answer.**
4. **Response is displayed instantly** via chat or web interface.

## Contributing

Interested in improving the project?  
- Fork this repo, create a branch for your changes, and open a pull request.
- Please file issues or feature requests in the Issues tab.

