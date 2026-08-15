# Corporate Azure Terraform Security Policy

## Azure Naming Conventions
- Resource Group names must start with rg- (e.g., rg-dev-eastus).
- Storage Account names must be lowercase numbers/letters, max 24 chars, starting with st.

## Mandatory Security Guardrails
1. Network Security Groups (NSG): Inbound rules MUST NOT allow traffic from 0.0.0.0/0 on management ports (SSH: 22, RDP: 3389).
2. Storage Accounts: Must enforce TLS 1.2 (min_tls_version = "TLS1_2") and disable public access.
3. App Services / Azure Functions: Must force HTTPS (https_only = true).
