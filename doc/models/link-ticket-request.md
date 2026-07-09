
# Link Ticket Request

Link ticket request

*This model accepts additional fields of type Object.*

## Structure

`LinkTicketRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeploymentId` | `String` | Required | Deployment ID. Can be found at /deployments, or in your Settings in the web UI. | String getDeploymentId() | setDeploymentId(String deploymentId) |
| `IssueIds` | `List<String>` | Required | An array of Semgrep finding IDs to link the ticket to. | List<String> getIssueIds() | setIssueIds(List<String> issueIds) |
| `TicketUrl` | `String` | Required | The URL of the external ticket to link (e.g. https://myorg.atlassian.net/browse/SEC-123). | String getTicketUrl() | setTicketUrl(String ticketUrl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.LinkTicketRequest;
import java.io.IOException;
import java.util.Arrays;

LinkTicketRequest linkTicketRequest = new LinkTicketRequest.Builder(
    "123",
    Arrays.asList(
        "issue_ids4",
        "issue_ids5"
    ),
    "https://myorg.atlassian.net/browse/SEC-123"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

