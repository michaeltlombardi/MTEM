# PowerShell Module Rubric
This rubric grades a particular product on how well it supports PowerShell for management - a score of 0 indicates that the product does not support PowerShell at all.

##TO-DO

If the scoring criteria is additive, simply add up the values of the relevant criteria the PowerShell module meets.
If the scoring is percentage based, then the values are judged using the following formula:

```Posh
ForEach($Criterion in $CriteriaGroups){
  $Score += ($Criterion.ActualScore / $Criterion.PossibleScore) * $Criterion.Weight
}
```

Where `$CriteriaGroups` are those Criteria which begin the same. If a product's PowerShell tools are published as a snap-in, contain comment-based help, 100% test coverage, no pester tests, and average documentation, that product's score would then be `58%`.
```
(3/5*10) + (5/5*10) + (100/100*25) + (0/100*25) + (4/6*25) = 57.67
```

| Criteria                                                       | Value | Weight |
|:---------------------------------------------------------------|:-----:|:------:|
| [Published](#publishing) as example snippets targeting the API | +1    | 10     |
| Published as a PowerShell snap-in                              | +2    | 10     |
| Published as a PowerShell Module with DLL(s)                   | +3    | 10     |
| Published as a PowerShell module                               | +4    | 10     |
| Published as a PowerShell module in the Gallery                | +5    | 10     |
| [Comment-Based Help for Cmdlets](#comment-based-help)          | +5    | 10     |
| [Use-Case Coverage](#use-case-coverage) (per percent)          | +1    | 25     |
| [Pester Test Coverage](#pester-test-coverage) (per percent)    | +1    | 25     |
| [Documentation Reference](#documentation-reference) (Minimal)  | +2    | 25     |
| Documentation Reference (Average)                              | +4    | 25     |
| Documentation Reference (Extensive)                            | +6    | 25     |

## Publishing
The ideal publishing for a PowerShell module is to the [PowerShell Gallery](https://www.PowerShellgallery.com/); with [Package Management](https://github.com/OneGet/oneget), the PowerShell Gallery is the location with the most discoverability and is the easiest way for users to acquire a PowerShell module.

The next best publishing method is as a PowerShell module - as a zip or some other method which requires placement of the folder but not the running of an installation executable. This makes the PowerShell Module easy to deploy and update.

The next best publishing method is as a PowerShell module with one or more DLLs - script modules are preferred over modules with assemblies as the code can be more easily reviewed.

The next best publishing method is as a PowerShell snap-in.  PowerShell snap-ins are deprecated and should be replaced with modules. They require installation and update the registry of the machine they are installed on.

The minimal publishing method counted by this rubric is as example PowerShell snippets which target the product's API.

## Comment-Based Help
[Comment-Based Help](https://technet.microsoft.com/en-us/library/hh847834.aspx) is the standard for ensuring a function or cmdlet is usable and provides at-the-shell help for that use.  It is also useful when reviewing code.

## Use-Case Coverage
The purpose of a PowerShell module is, presumably, to ensure that all management of a given product can be performed programmatically. If an action can be taken via the API or GUI, it should also be possible to perform from the PowerShell module.

## Pester Test Coverage
[Pester](https://github.com/pester/Pester) is the testing framework for PowerShell.  It is as important to have testable functions/cmdlets as it is to have the cmdlets themselves. Pester tests provide some documentation of the function and assurance that the function performs as advertised.

## Documentation Reference
The ideal documentation for a PowerShell Module includes parity with the full range of [comment-based help](https://technet.microsoft.com/en-us/library/hh847834.aspx), extensive references of all custom object types introduced by the module, example usages of each cmdlet, example scripts combining multiple cmdlets to perform at least one complex task, and guidance on building scripts using the cmdlets.  An example of this type of documentation is Microsoft's [Technet](https://technet.microsoft.com/en-us/library/ms714469(v=vs.85).aspx) documentation for PowerShell.

Average documentation for a PowerShell Module includes parity with the full range of comment-based help for every cmdlet published in the module, references for all custom object types introduced by the module, and example usages of each cmdlet.

The minimal documentation counted by this rubric includes parity with the full range of comment-based help for every cmdlet published in the module.
