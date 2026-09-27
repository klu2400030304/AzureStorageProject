# Azure Storage Redundancy Option Selection Study

## Project Overview
This project studies and compares Azure Storage redundancy options using Azure Blob Storage:
- LRS – Locally Redundant Storage
- ZRS – Zone-Redundant Storage
- GRS – Geo-Redundant Storage
- RA-GRS – Read-Access Geo-Redundant Storage

## Objectives
1. Configure LRS, ZRS, GRS and RA-GRS storage accounts.
2. Create Blob Storage containers.
3. Upload a test text file.
4. Generate a read-only SAS URL.
5. Test blob accessibility.
6. Test secondary-region access for RA-GRS.
7. Compare protection and relative cost.

## Project Workflow
Azure Storage Account → Redundancy Configuration → Blob Storage → SAS URL → Testing → Cost Comparison

## Experimental Results

| Redundancy | Blob Access | Geo-Replication | Secondary Read |
|---|---|---|---|
| LRS | Yes | No | No |
| ZRS | Yes | No | No |
| GRS | Yes | Yes | No |
| RA-GRS | Yes | Yes | Yes |

## Cost Comparison
Actual Azure cost depends on region, capacity, access tier, operations,
data transfer and the Azure subscription/offer. The project uses relative
cost comparison rather than claiming fixed prices.

## Security Note
Do NOT commit storage account keys or active SAS tokens/URLs to GitHub.
Screenshots should hide sensitive credentials where applicable.

## Repository Contents
- Architecture diagram
- Azure configuration screenshots
- Documentation
- Presentation
- Cost comparison
