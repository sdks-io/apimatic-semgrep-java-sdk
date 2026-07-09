
# Exposures 2

List of exposures or reachability types to filter by. If not specified, returns findings across all exposures. This filter is applicable when `issue_type=sca` is specified. Valid values: reachable, always_reachable, conditionally_reachable, unreachable, unknown

## Enumeration

`Exposures2`

## Fields

| Name |
|  --- |
| `REACHABLE` |
| `ALWAYS_REACHABLE` |
| `CONDITIONALLY_REACHABLE` |
| `UNREACHABLE` |
| `UNKNOWN` |

## Example

```java
import dev.semgrep.models.Exposures2;

Exposures2 exposures2 = Exposures2.UNKNOWN;
```

