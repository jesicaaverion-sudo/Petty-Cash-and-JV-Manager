# 💰 Petty Cash and JV Manager
https://inescapable-cash-flow-snap.base44.app
A web application for managing petty cash transactions and Journal Vouchers (JVs),
built with [Base44](https://base44.com).

## 📖 Overview

The Petty Cash and JV Manager helps finance teams and small businesses track
day-to-day petty cash spending and create, review, and approve journal vouchers —
replacing spreadsheets and paper vouchers with one organized system.

## ✨ Features

### 💵 Petty Cash Management
- Record cash **top-ups** and **disbursements**
- Maintain a **running balance** so the float is always known
- Categorize entries by date, amount, and purpose

### 📝 Journal Vouchers (JVs)
- Create journal vouchers with debit/credit lines and notes
- **Review and approval workflow** before a JV is finalized
- Full JV history with approval status at a glance

### 📊 Reports & Export
- Summaries of cash movements over any period
- Exportable statements for reconciliation, bookkeeping, and audits

### 🔐 Secure Access
- User authentication so only registered staff can record and approve entries
- Responsive design — works on desktop and mobile

## 🛠️ Tech Stack

- **Frontend:** React 18, Tailwind CSS, shadcn/ui components, Vite
- **Backend & Auth:** Base44 platform services (entities, auth, serverless functions)
- **State & Data fetching:** TanStack React Query

> **Note:** This app runs on the Base44 platform. The code in this repository is a
> copy of the frontend and backend function source, but it still depends on
> Base44's backend (database, authentication) to run. App data, secrets, and
> users are not included in the repository.

## 🚀 Getting Started

```bash
# Install dependencies
npm install

# Start the dev server
npm run dev

You will need a Base44 account and workspace for the backend services
(entities, auth) to work.


📁 Project Structure

├── src/
│   ├── components/     # Reusable UI components
│   │   └── ui/         # shadcn/ui primitives
│   ├── pages/          # Application pages/screens
│   ├── lib/            # Utilities, auth context, query client
│   └── App.jsx         # Routes and app shell
├── base44/
│   ├── entities/       # Data model definitions
│   └── functions/      # Backend (serverless) functions
└── tailwind.config.js

🗃️ Data Model

Entity	Description
PettyCashEntry	Cash received or disbursed — date, amount, type (top-up/disbursement), purpose, running balance
JournalVoucher	JV number, date, debit/credit lines, notes, and approval status (draft / pending / approved)

(Adjust entity names and fields to match the schemas in base44/entities/ in your export.)


📄 License

All rights reserved.
