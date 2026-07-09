
# Status

The finding's status as exposed in the UI. Status is a derived property combining information from the finding `state` and `triage_state`. The `triage_state` can be used to override the scan state if the finding is still detected

## Enumeration

`Status`

## Fields

| Name |
|  --- |
| `OPEN` |
| `FIXED` |
| `IGNORED` |
| `REVIEWING` |
| `FIXING` |
| `PROVISIONALLY_IGNORED` |

## Example

```java
import dev.semgrep.models.Status;

Status status = Status.IGNORED;
```

