# API Rubric
This rubric grades a particular product on how well it supports one or more APIs for management - a score of 0 indicates that the product does not have an API at all.

##TO-DO##
If the scoring criteria is additive, simply add up the values of the relevant criteria the API meets.
If the scoring is percentage based, then the values are judged using the following formula:

```Posh
ForEach($Criterion in $CriteriaGroups){
  $Score += ($Criterion.ActualScore / $Criterion.PossibleScore) * $Criterion.Weight
}
```

Where `$CriteriaGroups` are those Criteria which begin the same. If a product's API is published as .NET Language API, has 100% use-case coverage,  and average documentation, that product's score would then be `73%`.
```
(3/5*10) + (100/100*40) + (4/6*40) = 72.67
```

| Criteria                                                       | Value | Weight |
|:---------------------------------------------------------------|:-----:|:------:|
| [Published](#publishing) as a non .NET language only API       | +1    | 10     |
| Published as a COM API                                         | +2    | 10     |
| Published as a .NET language API                               | +3    | 10     |
| Published as a SOAP API                                        | +4    | 10     |
| Published as a RESTful API                                     | +5    | 10     |
| [Use-Case Coverage](#use-case-coverage) (per percent)          | +1    | 40     |
| [Documentation Reference](#documentation-reference) (Minimal)  | +2    | 40     |
| Documentation Reference (Average)                              | +4    | 40     |
| Documentation Reference (Extensive)                            | +6    | 40     |

##Publishing
The ideal API is as a RESTful API. REST APIs are simple to use, discoverable, and easy to wrap PowerShell around.

The next best API is a SOAP API. While more complex and difficult to target/wrap than a RESTful API, a SOAP API is usable and does not require client-side libraries.

The next best API is one implemented in a .NET language. Because PowerShell is built on .NET, developing functions to target the API is simple and convenient. However, this often requires the installation of libraries on the client machine.

The next best API is a COM API.  A COM API is less PowerShell friendly than a .NET API but still useable. Again, it often requires the installation of libraries on the client machine.

The minimal publishing method counted by this rubric is an API which can be targeted by a non .NET language only. This requires programmatic management of the product to be performed without PowerShell, but does still allow for some level of programmatic management.

##Use-Case Coverage
The purpose of an API is, presumably, to ensure that all management of a given product can be performed programmatically. If an action can be taken via the GUI, it should also be possible to perform via the API.

##Documentation Reference
The ideal documentation for an API...

Average documentation for an API...

The minimal documentation counted by this rubric includes...
