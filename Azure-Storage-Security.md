# Azure Storage Security
## Storage Access Methods

Azure Storage resources can be accessed using:

- Shared Access Signatures (SAS)
- Access Keys (Account Keys)

## Shared Access Signatures (SAS)

SAS stands for Shared Access Signature.

Types:

### Account SAS
Provides delegated access across multiple storage services.

Examples:
- Blob
- Queue
- Table
- File

### Service SAS
Provides access to a single Azure storage service.

## Access Keys
Also known as:

- Account Keys

Characteristics:

- Grant full access to storage resources
- Used by applications
- Can be used to sign SAS tokens

## Security Recommendations
Microsoft recommends:

- Using Azure Entra ID authentication
- Using Managed Identities
- Avoiding long-term Access Keys where possible

## Key Rotation
Storage accounts typically contain:

- Key 1
- Key 2

This enables key rotation without service interruption.

## Components of a SAS URI
Common parameters include:

- sig (Signature)
- se (Expiry Time)
- sp (Permissions)
- ss (Services)
- srt (Resource Types)

Example:

?sv=xxxx&ss=xxxx&srt=xxxx&sp=xxxx&sig=xxxx
