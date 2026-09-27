# Azure Storage Redundancy Option Selection Study – Presentation

## Slide 1 – Title
Azure Storage Redundancy Option Selection Study

## Slide 2 – Problem Statement
Data availability and durability are important for cloud applications.
Azure provides LRS, ZRS, GRS and RA-GRS to protect stored data.

## Slide 3 – Objectives
- Configure LRS, ZRS, GRS and RA-GRS
- Create Blob containers and upload a test file
- Generate and test a SAS URL
- Test RA-GRS secondary access
- Compare protection and relative cost

## Slide 4 – Azure Storage Redundancy
LRS – Local copies
ZRS – Copies across availability zones
GRS – Replication to a secondary region
RA-GRS – GRS plus secondary read access

## Slide 5 – System Architecture
Azure Storage Account → Redundancy Configuration → Blob Storage → SAS URL → Testing → Cost Comparison

## Slide 6 – Implementation
Separate StorageV2 accounts were configured for LRS, ZRS, GRS and RA-GRS.
A `redundancy-test` container and `redundancy-test.txt` file were used.

## Slide 7 – SAS URL and Testing
Read-only HTTPS SAS was generated and tested in a browser.
RA-GRS secondary endpoint was also tested.

## Slide 8 – Results
LRS: Blob access – Yes; Geo-replication – No; Secondary read – No
ZRS: Blob access – Yes; Geo-replication – No; Secondary read – No
GRS: Blob access – Yes; Geo-replication – Yes; Secondary read – No
RA-GRS: Blob access – Yes; Geo-replication – Yes; Secondary read – Yes

## Slide 9 – Cost Comparison
LRS: Low relative cost
ZRS: Higher than LRS
GRS: Higher
RA-GRS: Higher

Actual Azure pricing depends on region, capacity, operations, access tier and transfer.

## Slide 10 – Conclusion
The project demonstrates Azure storage redundancy configuration, Blob access,
SAS-based testing and RA-GRS secondary read access.
