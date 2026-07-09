
# Exposures

Filter by exposure (reachability type). Only applies for sca findings. Reachability is the ability of an attacker to access a vulnerability in a system.

## Enumeration

`Exposures`

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
import dev.semgrep.models.Exposures;

Exposures exposures = Exposures.ALWAYS_REACHABLE;
```

