
# Autotriage Verdict 2

Which autotriage verdict do you want to include? If not specified, includes all. This filter is applicable when `issue_type` is `sast` or unspecified. Valid values: true_positive, false_positive

## Enumeration

`AutotriageVerdict2`

## Fields

| Name |
|  --- |
| `TRUE_POSITIVE` |
| `FALSE_POSITIVE` |

## Example

```java
import dev.semgrep.models.AutotriageVerdict2;

AutotriageVerdict2 autotriageVerdict2 = AutotriageVerdict2.TRUE_POSITIVE;
```

