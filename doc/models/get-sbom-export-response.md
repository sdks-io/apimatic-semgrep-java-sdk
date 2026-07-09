
# Get Sbom Export Response

*This model accepts additional fields of type Object.*

## Structure

`GetSbomExportResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DownloadUrl` | `String` | Optional | URL to download the SBOM when status is COMPLETED. | String getDownloadUrl() | setDownloadUrl(String downloadUrl) |
| `ErrorMessage` | `String` | Optional | Error message when status is FAILED. | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `Status` | [`Status3`](../../doc/models/status-3.md) | Required | Status of the SBOM export job.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_EXPORT_STATUS_IN_PROGRESS \| The SBOM export job is in progress. \|<br>\| SBOM_EXPORT_STATUS_COMPLETED \| The SBOM export job has completed. \|<br>\| SBOM_EXPORT_STATUS_FAILED \| The SBOM export job has failed. \| | Status3 getStatus() | setStatus(Status3 status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.GetSbomExportResponse;
import dev.semgrep.models.Status3;
import java.io.IOException;

GetSbomExportResponse getSbomExportResponse = new GetSbomExportResponse.Builder(
    Status3.SBOM_EXPORT_STATUS_COMPLETED
)
.downloadUrl("downloadUrl6")
.errorMessage("errorMessage2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

