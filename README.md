# Entra ID PKI Sync Tool

## 🚀 Overview
This tool automates the synchronization of the **Microsoft Entra ID** trust store with the **Federal Common Policy CA G2** bundle.

---

## 🛠️ Setup Instructions

### 1. Azure AD App Registration
The script requires an App Registration with `PublicKeyInfrastructure.ReadWrite.All` permissions.
* **Guide:** [Register an application with Microsoft Identity](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app)

### 2. GitHub Personal Access Token (PAT)
Required to upload the `.p7b` bundle to your repository.
* **Guide:** [Creating a GitHub PAT](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)

### 3. Local Configuration
Create a `config.json` in the script root (see template below). **Warning: Do not commit this file to Git.**

```json
{
    "Entra": {
        "TenantId": "Your-GUID",
        "ClientId": "Your-App-ID",
        "CertificateThumbprint": "Your-Thumbprint"
    }
}
