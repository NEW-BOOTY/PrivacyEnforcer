# PrivacyEnforcer

PrivacyEnforcer is an open-source tool designed to automate the exercise of your privacy rights under laws like CCPA, CPRA, and GDPR. It allows users to send requests to hundreds of companies to opt-out of data sharing, delete personal data, stop processing, and require confirmation—all in a legally compliant, headless manner without relying on browsers or bypassing security.

## Features
- **Headless CMP Negotiation Layer (HCNL)**: Uses alternative channels like email, form POSTs, DSAR inboxes, and manual fallbacks to avoid JavaScript-heavy portals.
- **SEOS Architecture**: Self-contained script where logic is separated from user-editable data (edit only the CONFIG block at the bottom).
- **Capability Matrix**: A customizable 12-field schema per company to determine the best submission method.
- **Automation with Compliance**: Prioritizes legal channels, adds rate limiting, and generates logs/reports.
- **Cross-Platform**: Available in Bash and Python versions.
- **Scalable**: Handles hundreds of companies with options for dry runs, limits, and specific targets.

## Why PrivacyEnforcer?
In an era where data is currency, companies often make it difficult to exercise your rights with complex web forms. PrivacyEnforcer simplifies this by automating requests through verified, public channels. It's inspired by best practices from sources like California's OAG and tools like Ethyca's Fides, but focused on consumer-side sending.

**Disclaimer**: This tool is for personal, lawful use. Consult a lawyer for advice. Mass sending may trigger spam filters—use responsibly.

## Setup
### Bash Version
1. Save as `privacyenforcer.sh`.
2. Make executable: `chmod +x privacyenforcer.sh`.
3. Edit the SEALED DATA BLOCK at the bottom with your details and company matrix.

### Python Version
1. Save as `privacyenforcer.py`.
2. Install dependencies: `pip install requests`.
3. Edit the SEALED CONFIG BLOCK at the bottom.
4. For email: Configure SMTP (e.g., Gmail with app password).

## Usage
### Bash
```bash
./privacyenforcer.sh [--dry-run] [--limit 10] [--company "Google"]