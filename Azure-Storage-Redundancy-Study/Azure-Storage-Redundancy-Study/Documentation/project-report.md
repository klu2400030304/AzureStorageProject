# Azure Storage Redundancy Option Selection Study

## 1. Problem Statement
Data availability and durability are important for cloud applications.
Hardware, zone, or regional failures can affect data availability.
Azure provides different storage redundancy options to protect data.
This project compares LRS, ZRS, GRS and RA-GRS using Azure Blob Storage,
including access testing and relative cost comparison.

## 2. Objectives
- Implement LRS, ZRS, GRS and RA-GRS.
- Create Blob Storage containers.
- Upload and access a test `.txt` file.
- Generate a secure SAS URL with read permission.
- Test blob accessibility.
- Test secondary-region access for RA-GRS.
- Compare redundancy options based on protection and relative cost.

## 3. Redundancy Types
- LRS: Copies data within the primary region.
- ZRS: Copies data across availability zones in the primary region.
- GRS: Replicates data to a secondary region.
- RA-GRS: GRS with read access to the secondary region.

## 4. Implementation
A separate StorageV2 storage account was configured for each redundancy
option. A Blob container named `redundancy-test` was used and a test file
named `redundancy-test.txt` was uploaded.

## 5. SAS Testing
A Blob SAS was generated with:
- Permission: Read
- Protocol: HTTPS
- Start and expiry time configured

The SAS URL was opened in a browser to verify access to the test file.

For RA-GRS, the secondary endpoint was also tested to verify secondary
read access.

## 6. Results

| Storage Type | Blob Access | Geo-Replication | Secondary Read |
|---|---|---|---|
| LRS | Yes | No | No |
| ZRS | Yes | No | No |
| GRS | Yes | Yes | No |
| RA-GRS | Yes | Yes | Yes |

## 7. Cost Comparison
Relative cost generally increases as additional redundancy and geographic
protection are provided. Exact charges depend on the Azure region, storage
capacity, access tier, operations, replication, and data transfer.

| Option | Relative Cost | Protection |
|---|---|---|
| LRS | Low | Local |
| ZRS | Higher than LRS | Zone level |
| GRS | Higher | Geographic |
| RA-GRS | Higher | Geographic + secondary read |

## 8. Conclusion
The project demonstrates how Azure Storage redundancy can be configured,
tested and compared using Blob Storage. It also demonstrates controlled
blob access using SAS and secondary read access for RA-GRS.
