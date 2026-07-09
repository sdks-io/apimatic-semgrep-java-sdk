
# Status 3

Status of the SBOM export job.

| value | description |
|-------|---------------|
| SBOM_EXPORT_STATUS_IN_PROGRESS | The SBOM export job is in progress. |
| SBOM_EXPORT_STATUS_COMPLETED | The SBOM export job has completed. |
| SBOM_EXPORT_STATUS_FAILED | The SBOM export job has failed. |

## Enumeration

`Status3`

## Fields

| Name |
|  --- |
| `SBOM_EXPORT_STATUS_IN_PROGRESS` |
| `SBOM_EXPORT_STATUS_COMPLETED` |
| `SBOM_EXPORT_STATUS_FAILED` |

## Example

```java
import dev.semgrep.models.Status3;

Status3 status3 = Status3.SBOM_EXPORT_STATUS_COMPLETED;
```

