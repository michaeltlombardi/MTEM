#MTEM: Management Tooling Excellence Matrix

###Synopsis
The matrix is supposed to be a reference for anyone who needs to administer Windows Servers and is curious about the level of support a given vendor provides for programmatic management. The matrix scores each specific software offering of a vendor separately, as applications do not always have parity of support from a vendor. 

The matrix scores the software on API, Powershell Module, and Desired State Configuration based on the [rubrics](#rubrics) on a scale of 0 to 100 where 0 indicates non-existant and 100 represents best-in-class. 

This matrix cannot be made accurate and relevent without community input. Please see the [contributing](#contributing) section for more information.

**NOTE:** This matrix is always subject to revisions. The matrix is organized alphabetically, first by vendor, then by product.

###Matrix
| Vendor         | Product        | API | PS  | DSC |
|:---------------|:---------------|:---:|:---:|:---:|
| A10 Networks   | -              |  -  |  -  |  -  |
| Adobe          | Echosign       |  -  |  -  |  -  |
| Amazon         | AWS            |  -  |  -  |  -  |
| Chef           | -              |  -  |  -  |  -  |
| Citrix         | -              |  -  |  -  |  -  |
| Cisco          | UCS            |  -  |  -  |  -  |
| CloudBerry     | -              |  -  |  -  |  -  |
| DataCore       | SANsymphony-V  |  -  |  -  |  -  |
| Dell           | -              |  -  |  -  |  -  |
| DH2i           | DxEnterprise   |  -  |  -  |  -  |
| ElasticBox     | ElasticBox     |  -  |  -  |  -  |
| EMC            | XtremIO        |  -  |  -  |  -  |
| F5             | -              |  -  |  -  |  -  |
| HP             | -              |  -  |  -  |  -  |
| ITRS Group     | GeneOS         |  -  |  -  |  -  |
| Jenkins        | Jenkins        |  -  |  -  |  -  |
| LogRhythm      | -              |  -  |  -  |  -  |
| Microsoft      | -              |  -  |  -  |  -  |
| Nimble Storage | Nimble OS      |  -  |  -  |  -  |
| Octopus Deploy | Octopus Deploy |  -  |  -  |  -  |
| Okta           | -              |  -  |  -  |  -  |
| Puppet         | -              |  -  |  -  |  -  |
| Pure Storage   | -              |  -  |  -  |  -  |
| Service Now    | -              |  -  |  -  |  -  |
| Slack          | Slack          |  -  |  -  |  -  |
| SolarWinds     | -              |  -  |  -  |  -  |
| Splunk         | -              |  -  |  -  |  -  |
| StorMagic      | vSAN           |  -  |  -  |  -  |
| Symantec       | BackUp Exec    |  -  |  -  |  -  |
| Veeam          | -              |  -  |  -  |  -  |
| VMWare         | -              |  -  |  -  |  -  |
| WinSCP         | WinSCP         |  -  |  -  |  -  |


###Rubrics
There is a separate rubric for each category. These rubrics are also living documents that may need to be updated over time. 
* [API Rubric](\Rubrics\API.md)
* [Powershell Module Rubric](\Rubrics\PS.md)
* [Desired State Configuration Rubric](\Rubrics\DSC.md)

###Contributing
Please file an issue or submit a pull request for any updates or corrections - this makes it much easier to follow and track. Contributions are encouraged and welcome. :)

For more specific guidance on contributing to the MTEM, please see the [Contributions](Contributions.md) document. 
