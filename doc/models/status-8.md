
# Status 8

Status of the finding.

- FINDING_STATUS_UNSPECIFIED: Return results for all finding statuses (if used as a parameter).
- FINDING_STATUS_OPEN: Finding is open and needs to be triaged
- FINDING_STATUS_IGNORED: Finding has been triaged and is being ignored
- FINDING_STATUS_FIXED: Finding has been fixed
- FINDING_STATUS_REMOVED: Finding has been removed
- FINDING_STATUS_UNKNOWN: Finding status is unknown

## Enumeration

`Status8`

## Fields

| Name |
|  --- |
| `FINDING_STATUS_UNSPECIFIED` |
| `FINDING_STATUS_OPEN` |
| `FINDING_STATUS_IGNORED` |
| `FINDING_STATUS_FIXED` |
| `FINDING_STATUS_REMOVED` |
| `FINDING_STATUS_UNKNOWN` |
| `FINDING_STATUS_PROVISIONALLY_IGNORED` |

## Example

```java
import dev.semgrep.models.Status8;

Status8 status8 = Status8.FINDING_STATUS_IGNORED;
```

