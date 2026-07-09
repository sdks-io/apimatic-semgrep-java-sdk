
# Unlink Ticket Request

Unlink ticket request

*This model accepts additional fields of type Object.*

## Structure

`UnlinkTicketRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeploymentId` | `String` | Required | Deployment ID. Can be found at /deployments, or in your Settings in the web UI. | String getDeploymentId() | setDeploymentId(String deploymentId) |
| `IssueIds` | `List<String>` | Required | An array of Semgrep finding IDs to unlink tickets from. | List<String> getIssueIds() | setIssueIds(List<String> issueIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.UnlinkTicketRequest;
import java.io.IOException;
import java.util.Arrays;

UnlinkTicketRequest unlinkTicketRequest = new UnlinkTicketRequest.Builder(
    "123",
    Arrays.asList(
        "issue_ids2",
        "issue_ids1"
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

