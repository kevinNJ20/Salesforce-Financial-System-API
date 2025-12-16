# Salesforce Financial System API

API System pour l'intégration avec Salesforce Financial Services Cloud - Données Financières.

## Description

Cette API fournit un accès standardisé aux comptes financiers, transactions et cartes dans Salesforce Financial Services Cloud via le connecteur Salesforce.

## Endpoints

### GET /api/salesforce/financial/accounts
Récupère les comptes financiers Salesforce.

**Query Parameters:**
- `sfId` (optional): ID Salesforce du compte
- `customerSfId` (optional): ID Salesforce du client propriétaire

### POST /api/salesforce/financial/accounts
Upsert d'un compte financier dans Salesforce.

### POST /api/salesforce/financial/transactions
Upsert d'une transaction financière dans Salesforce.

### POST /api/salesforce/financial/cards
Upsert d'une carte dans Salesforce.

## Configuration

Voir README.md de Salesforce Customers System API pour la configuration Salesforce de base.

### Objets Salesforce Utilisés

- `FinServ__FinancialAccount__c`: Comptes financiers
- `FinServ__FinancialAccountTransaction__c`: Transactions (si utilisé)
- Custom Objects pour les cartes (si applicable)

## Architecture Technique

### Flows Business-Logic

- `get-accounts-business-logic`: Requête SOQL vers Salesforce
- `upsert-account-business-logic`: Upsert compte financier
- `upsert-transaction-business-logic`: Upsert transaction
- `upsert-card-business-logic`: Upsert carte

