# Code Review

## Scan tool and configs

CodeQL scan tool was setup via Github actions and configured to scan only 'Javascript' related vulnerabilities on jw-community repo (forked from Jogetworkflow). Addtionally, cron job was set to continuously scan repo every day at 0630 & 1830 respectively.

![image](https://user-images.githubusercontent.com/95695894/186065367-f8f74ace-afa5-47be-bd2a-44ed4776168f.png)

Code sample: https://github.com/GopiNJ/jw-community-CodeScan/blob/7.0-SNAPSHOT/.github/workflows/codeql-analysis.yml

## Results and Summary
### Total of 122 alerts were flagged by the CodeQL scanning tool specifically related to Javascript based sample codes found within the repository.
![image](https://user-images.githubusercontent.com/95695894/186065125-ffb63d16-7a24-4343-bf83-44a1c06766eb.png)

## Sample findings and remediations
### 5 common types of code vulnerabilities stating type, severity and remediation steps required to fix listed below for reference purpose. 
#### Sample 1:
![image](https://user-images.githubusercontent.com/95695894/186066687-2b7d1c36-ebf5-4874-9628-c1c0227b16bf.png)

#### Sample 2:
![image](https://user-images.githubusercontent.com/95695894/186066826-f6b99bc1-a442-4313-8e7c-dce3554fe574.png)

