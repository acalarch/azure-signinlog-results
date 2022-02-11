# azure-signinlog-results
This project is an attempt to statically document all 'result type' values, messages, and remediations for Azure Signinlog. This type of information is important to defenders. There are many security relevant error codes in here that one may want to monitor for. These are this projects purposes, but there are many other legitimate reasons this may be useful to you. 

The primary reason to publish this list is to spare others from enumerating millions (billions?) of possible error codes.  

### Mappings 
For whatever reason, Microsoft does not keep their language consistent between the sign-in log schema and the error code resource (login.microsoft.com/error)
https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/reference-azure-monitor-sign-ins-log-schema

ErrorCode = resultType
Message = resultDescription
Remediation = No Mapping in Schema as of 2/11/2022

### New Values
Is the project missing a value? Feel free to create an issue or make a pull request. Your finding will be validated and added to the project. 

### Troubleshooting?
Looking for troubleshooting help on an ambigious error code? Error codes near yours may provide an insight. Additionally, Microsoft (and therefore this project) provides remediation steps that do not appear in the sign-in logs as of Feb. 11 2022. 

All codes are available through Microsoft officially:
https://login.microsoftonline.com/error 

An example of how the search is performed:
https://login.microsoftonline.com/error?code=0

### Validation & Timeliness
1. The values may not be static. Microsoft probably doesn't publish a static list for a reason. This project is not (yet) tracking changes over time. 
2. This repository may (and if you are using this in production, must) be validated by performing a lookup of each error codes at https://login.microsoftonline.com/error
3. This project likely will recieve bursts of support as @acalarch requires it to be up-to-date. Otherwise, I am relying somewhat on the community to help identify gaps / updates. 

#### Contributing Examples
I am very much interested in expanding this project to include specific examples of interesting sign-in log errors. If you have a sample to share, please create an issue or reach out to me directly. 
