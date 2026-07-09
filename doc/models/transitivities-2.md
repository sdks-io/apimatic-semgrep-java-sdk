
# Transitivities 2

List of transitivities to filter by. If not specified, returns all transitivities. This filter is applicable when `issue_type=sca` is specified. Valid values: direct, transitive, unknown

## Enumeration

`Transitivities2`

## Fields

| Name |
|  --- |
| `DIRECT` |
| `TRANSITIVE` |
| `UNKNOWN` |

## Example

```java
import dev.semgrep.models.Transitivities2;

Transitivities2 transitivities2 = Transitivities2.DIRECT;
```

