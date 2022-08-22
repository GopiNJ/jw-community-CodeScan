# Code Review

## Scan tool and configs

CodeQL scan tool was setup via Github actions and configured to scan only 'Javascript' related vulnerabilities on jw-community repo (forked from Jogetworkflow). 

Code sample: https://github.com/GopiNJ/jw-community-CodeScan/blob/7.0-SNAPSHOT/.github/workflows/codeql-analysis.yml


## Sample findings and remediations

### Sample-1
#### Type
Unsafe jquery plugin
#### Severity        
Medium

#### Results with error path and remediation     
https://github.com/GopiNJ/jw-community-CodeScan/security/code-scanning/45


     Sample-2
     -> DOM text reinterpreted as HTML
     
     Severity
     -> Medium
     
     
https://github.com/GopiNJ/jw-community-CodeScan/security/code-scanning/50

Prototype-polluting function
https://github.com/GopiNJ/jw-community-CodeScan/security/code-scanning/120

Incomplete URL substring sanitization
https://github.com/GopiNJ/jw-community-CodeScan/security/code-scanning/8

Uncontrolled data used in path expression
https://github.com/GopiNJ/jw-community-CodeScan/security/code-scanning/28

