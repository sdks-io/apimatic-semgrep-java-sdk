
# Search Scans Request

*This model accepts additional fields of type Object.*

## Structure

`SearchScansRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Branch` | `String` | Optional | Only get scans from the specified branch | String getBranch() | setBranch(String branch) |
| `Cursor` | `String` | Optional | Cursor to paginate through the results | String getCursor() | setCursor(String cursor) |
| `DeploymentId` | `String` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. | String getDeploymentId() | setDeploymentId(String deploymentId) |
| `IsFullScan` | `Integer` | Optional | Only get scans that are full scans (if false, only get diff scans) | Integer getIsFullScan() | setIsFullScan(Integer isFullScan) |
| `Limit` | `Integer` | Optional | Page size to paginate through the results (default is 100, max is 500) | Integer getLimit() | setLimit(Integer limit) |
| `Products` | [`Products`](../../doc/models/products.md) | Optional | Only get scans that have these enabled products<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| PRODUCT_SAST \|  \|<br>\| PRODUCT_SCA \|  \|<br>\| PRODUCT_SECRETS \|  \|<br>\| PRODUCT_AI_SAST \|  \| | Products getProducts() | setProducts(Products products) |
| `RepositoryId` | `Integer` | Optional | Only get scans for this repo | Integer getRepositoryId() | setRepositoryId(Integer repositoryId) |
| `Since` | `LocalDateTime` | Optional | Only get scans created after this time. Provide time in ISO 8601 format. | LocalDateTime getSince() | setSince(LocalDateTime since) |
| `Statuses` | [`Statuses`](../../doc/models/statuses.md) | Optional | Only get scans that have one of these statuses<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SCAN_STATUS_RUNNING \| The scan is currently running \|<br>\| SCAN_STATUS_COMPLETED \| The scan has completed successfully (0 or 1 exit code) \|<br>\| SCAN_STATUS_PENDING \| The scan is queued and waiting to start \|<br>\| SCAN_STATUS_CANCELLED \| The scan was cancelled before completion \|<br>\| SCAN_STATUS_ERROR \| The scan has exited with a failure (exit code not 0 or 1) \|<br>\| SCAN_STATUS_NEVER_FINISHED \| The scan did not report an error or success after over an hour \| | Statuses getStatuses() | setStatuses(Statuses statuses) |
| `TotalTime` | [`FloatRange`](../../doc/models/float-range.md) | Optional | - | FloatRange getTotalTime() | setTotalTime(FloatRange totalTime) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Products;
import dev.semgrep.models.SearchScansRequest;
import java.io.IOException;

SearchScansRequest searchScansRequest = new SearchScansRequest.Builder(
    "123"
)
.branch("branch6")
.cursor("cursor6")
.isFullScan(26)
.limit(236)
.products(Products.PRODUCT_SAST)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

