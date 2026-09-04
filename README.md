# Expense Recorder

A lightweight expense-tracking app for quickly recording personal, household, couple, and business expenses.

## Current version

**v2.3.1**

## What this repository is for

This repository hosts the standalone voice-capture page used by the Expense Recorder. The voice page runs outside the Google Apps Script sandbox so browser microphone access can work reliably.

## Core expense types

- Personal
- Household
- Couple
- Business

Business expenses can also be assigned to a project such as **Bridge** or **Olive Oil**.

## Voice input examples

- `1500 dinner McDonald's Aileen couple`
- `4500 groceries S&R Aileen household`
- `3000 Facebook ads George business Bridge`
- `2500 bottles Aileen business Olive Oil`

## Architecture

- **Google Sheets** — expense data and reporting
- **Google Apps Script** — main app and backend logic
- **GitHub Pages** — standalone browser voice capture
- **Web Speech API / microphone access** — voice input on the standalone page

The voice page sends the recognized transcript back to the main Expense Recorder window, where the existing parser handles amount, description, payer, expense type, and project.

## Main file

- `index.html` — standalone Expense Recorder voice interface

## Design goals

The interface is intentionally matched to the main Expense Recorder so voice capture feels like part of the same app rather than a separate utility.

## Deployment

Publish this repository with GitHub Pages from the `main` branch and repository root. The resulting public HTTPS page is then used as the voice-capture URL inside the main Google Apps Script app.
