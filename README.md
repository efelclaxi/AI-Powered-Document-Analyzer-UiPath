# 🚀 ABUTTO: Smart Operation Assistant (TTO Hyperautomation)

![Status](https://img.shields.io/badge/Status-Pilot%20Prototype-blue) ![Platform](https://img.shields.io/badge/UiPath-2025.x-orange) ![AI](https://img.shields.io/badge/AI-Hybrid%20(Ollama%20%2F%20Gemini)-purple)

**Project Owner:** Hakan Aksoy  
**Institution:** Antalya Bilim University (ABUTTO)  
**Vision:** TÜBİTAK 1505 - University-Industry Cooperation

## 📄 Project Overview
This project is an **Agentic RPA (Robotic Process Automation)** solution designed to optimize the operational workflows of Technology Transfer Offices (TTOs).

TTOs process thousands of unstructured documents (Project Applications, Invoices, NDAs) manually. **ABUTTO Smart Assistant** automates this by using **Generative AI** to read, analyze, and extract structured data from these documents, acting as a digital workforce.

## 🏗 Agentic Architecture
The solution is built upon a "Human-in-the-Loop" architecture consisting of three main digital agents:

1.  **Observer Agent:** Monitors input channels (Folders/Emails) 24/7 and triggers the workflow upon new file arrival.
2.  **Analyst Agent (Reasoning Engine):** Uses LLMs to semantically analyze the document. It determines:
    * Document Type (Application, Contract, Invoice)
    * Urgency Score (1-10)
    * Missing Signatures or Critical Data
3.  **Operation Agent:** Executes the final action (Database entry or Email notification) based on the Analyst's structured output.

## 💡 Hybrid AI Strategy (Dev vs. Prod)
This project implements a cost-effective and secure development lifecycle:

* **Development & Pilot Phase (Current):**
    * Uses **Ollama (Phi-3 Mini)** running locally.
    * **Reason:** Zero API costs during testing and ensures sensitive TTO data remains on-premise (Localhost) without leaking to the cloud.
* **Production Phase (Planned):**
    * Will switch to **Google Gemini 1.5 Flash API**.
    * **Reason:** Higher context window (1M tokens) for processing lengthy academic CVs and complex R&D project files.

> *Note: The UiPath architecture is modular. Switching from Ollama to Gemini requires only updating the API Endpoint in the configuration.*

## 🛠 Setup & Installation (Local Dev Environment)

To run this pilot project on your local machine, follow these steps:

### 1. Prerequisites
* **UiPath Studio** (v2024.10+)
* **Ollama** (Local LLM Server)

### 2. Install the AI Model
Since we are in the "Pilot Phase", we use the local model. Open your terminal (CMD/PowerShell) and run:

```bash
ollama pull phi3:mini