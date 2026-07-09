
# New Triage State

The triage state you would like to bulk triage your findings to.

## Enumeration

`NewTriageState`

## Fields

| Name |
|  --- |
| `IGNORED` |
| `REVIEWING` |
| `FIXING` |
| `REOPENED` |
| `PROVISIONALLY_IGNORED` |

## Example

```java
import dev.semgrep.models.NewTriageState;

NewTriageState newTriageState = NewTriageState.PROVISIONALLY_IGNORED;
```

