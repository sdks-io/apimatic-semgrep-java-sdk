
# Protos Openapi V1 Delete Ticket Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1DeleteTicketResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IssueIds` | `List<String>` | Optional | List of issue IDs unlinked from ticket | List<String> getIssueIds() | setIssueIds(List<String> issueIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1DeleteTicketResponse;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1DeleteTicketResponse protosOpenapiV1DeleteTicketResponse = new ProtosOpenapiV1DeleteTicketResponse.Builder()
    .issueIds(Arrays.asList(
        "18759",
        "18760"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

