
# Reachability

Indicates whether the vulnerable code is reachable

## Enumeration

`Reachability`

## Fields

| Name |
|  --- |
| `ENUM_NO_REACHABILITY_ANALYSIS` |
| `REACHABLE` |
| `ENUM_ALWAYS_REACHABLE` |
| `ENUM_CONDITIONALLY_REACHABLE` |
| `UNREACHABLE` |

## Example

```java
import dev.semgrep.models.Reachability;

Reachability reachability = Reachability.ENUM_NO_REACHABILITY_ANALYSIS;
```

