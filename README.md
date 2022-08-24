# Code Review
## Test scenario
`Environment:` GitHub Repository  
`Scan tool:` CodeQL  
`Target:` https://github.com/GopiNJ/jw-community-CodeScan  
## Scanning Method
`Scanning method used`: Static Application Security Testing (SAST)  

Inline with security programs best practises to be adapted in early stages of Software Development Lifecycle (SDLC), Static Application Security Testing (SAST) is often carried out on the source code without actually running it and reviews the way the code is written and points out any security risks. By analyzing the code in real time, it becomes easier for the developer to watch out for any problems that can impact the security of the code from begining of the development itself. 

## CodeQL configs  
### CodeQL scan tool was setup via Github actions and configured to scan only 'Javascript' related vulnerabilities on jw-community repo (forked from Jogetworkflow). Addtionally, cron job was set to continuously scan repo every day at 0630 & 1830 respectively.
![image](https://user-images.githubusercontent.com/95695894/186065367-f8f74ace-afa5-47be-bd2a-44ed4776168f.png)
---
`Code sample:` https://github.com/GopiNJ/jw-community-CodeScan/blob/7.0-SNAPSHOT/.github/workflows/codeql-analysis.yml

## Results and Summary
### Total of 122 alerts were flagged by the CodeQL scanning tool specifically related to Javascript based sample codes found within the target repository.
![image](https://user-images.githubusercontent.com/95695894/186072680-dee8e7c0-ea06-4d51-9912-3b643a1dfc59.png)

## Sample findings and remediations
### 5 common types of code vulnerabilities stating type, severity and remediation steps required to fix listed below for reference purpose. 
#### `Sample 1:`
![image](https://user-images.githubusercontent.com/95695894/186066687-2b7d1c36-ebf5-4874-9628-c1c0227b16bf.png)
---
#### `Sample 2:`
![image](https://user-images.githubusercontent.com/95695894/186066826-f6b99bc1-a442-4313-8e7c-dce3554fe574.png)
---
#### `Sample 3:`
![image](https://user-images.githubusercontent.com/95695894/186068794-ff819dab-18ef-44f5-9886-55c11ec93c40.png)
---
#### `Sample 4:`
![image](https://user-images.githubusercontent.com/95695894/186068885-1fea2da0-aafc-467b-bdf0-95c8790db17a.png)
---
#### `Sample 5:`
![image](https://user-images.githubusercontent.com/95695894/186068973-7b6cf141-6527-4cf4-9cf9-634677a6df21.png)
---
## Additional tasks in progress  
1. List of `alerts extraction from CodeQL via API calls` - Due to no options available to directly export list of alerts from GitHub, currently exploring API / other methods to extract to alerts to assist with proper reporting format.
2. `Configuring SonarCloud tool` - To explore additional code vulnerability management services and reporting structures offered via this tool.
## References
https://codeql.github.com/  
https://codeql.github.com/docs/  
https://cwe.mitre.org/index.html  
