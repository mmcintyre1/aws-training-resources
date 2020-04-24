## Athena
### what is athena?
interactive query service which enables you to analyze and query data located in S3 using SQL -- turns S3 into a giant database

### benefits of athena
- serverless, nothing to provision, pay per query / per TB scanned
- no need to set up complex ETL processes 
- works directly with data stored in S3

### what can athena be used for?
- log files 
- generate business reports on data stored in S3
- analyze AWS cost and usage reports 
- run queries on click-stream data


## Macie
### What is macie
security service that uses ML and NLP to discover, classify, and protect sensitive data stored in S3 (PII - personally identifiable data)
- uses AI to recognize if your S3 objects contain sensitive data
- dashboards, reporting, and alerts
- can also analyze cloudtrail logs
- great ofr PCI-DSS and preventing ID theft

### other resources
[Athena FAQs](https://aws.amazon.com/athena/faqs/)
[Macie FAQs](https://aws.amazon.com/macie/faq/)
