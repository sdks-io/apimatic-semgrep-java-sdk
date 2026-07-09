
# Triage Reasons 2

Which triage reasons do you want to include? If not specified, includes all. This filter is applicable when `status` is `ignored`. Valid values: acceptable_risk, false_positive, no_time, no_triage_reason, duplicate

## Enumeration

`TriageReasons2`

## Fields

| Name |
|  --- |
| `ACCEPTABLE_RISK` |
| `FALSE_POSITIVE` |
| `NO_TIME` |
| `NO_TRIAGE_REASON` |
| `DUPLICATE` |

## Example

```java
import dev.semgrep.models.TriageReasons2;

TriageReasons2 triageReasons2 = TriageReasons2.FALSE_POSITIVE;
```

