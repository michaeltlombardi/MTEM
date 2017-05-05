# GlobalScape EFT: API Score Card

## Overall Score: 106 / 71%
Overall, GlobalScape's EFT product scores a `C-` on the API portion of its management tooling.

## Publishing (+2 / +4%)
EFT is published with a COM API. This API is only usable once the proprietary DLLs are registered on the client system.

**Note:** A (mostly undocumented) subset of EFT features *also* have a REST API.

## Use-Case Coverage (+100 / +40%)
The COM API has 100% coverage of **all** functions exposed in the management GUI and GlobalScape has verbally conveyed their committment to always maintaining this status.

**Note:** The 100% coverage *only* is true when the API is called on the same computer the server software is installed on. There are numerous use cases that have been intentionally prevented when the API is called remotely. See GlobalScape's [FAQ](http://help.globalscape.com/help/eft7-2/mergedprojects/eft/remote_administration.htm#FAQsAboutRemoteAdministration) section on Remote Administration.

## Documentation Reference (+4 / +26.7%)
The current score for the Documentation reference is "Average" because no proper metrics have been determined. 
The reference for the EFT COM API includes complete coverage of all properties and methods, though the organization is lackluster, difficult to peruse, and includes legacy information for each release.  The API examples are all targeted at C# and VBScript.
