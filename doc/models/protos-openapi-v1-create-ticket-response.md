
# Protos Openapi V1 Create Ticket Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1CreateTicketResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Failed` | [`List<ProtosOpenapiV1CreateTicketResponseTicketCreationFailed>`](../../doc/models/protos-openapi-v1-create-ticket-response-ticket-creation-failed.md) | Optional | List of issues where ticket creation failed. This list may include issues that were skipped because they exceed the specified limit. | List<ProtosOpenapiV1CreateTicketResponseTicketCreationFailed> getFailed() | setFailed(List<ProtosOpenapiV1CreateTicketResponseTicketCreationFailed> failed) |
| `Skipped` | [`List<ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped>`](../../doc/models/protos-openapi-v1-create-ticket-response-ticket-creation-skipped.md) | Optional | List of issues that were skipped | List<ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped> getSkipped() | setSkipped(List<ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped> skipped) |
| `Succeeded` | [`List<ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess>`](../../doc/models/protos-openapi-v1-create-ticket-response-ticket-creation-success.md) | Optional | List of successfully created tickets | List<ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess> getSucceeded() | setSucceeded(List<ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess> succeeded) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1CreateTicketResponse;
import dev.semgrep.models.ProtosOpenapiV1CreateTicketResponseTicketCreationFailed;
import dev.semgrep.models.ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped;
import dev.semgrep.models.ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1CreateTicketResponse protosOpenapiV1CreateTicketResponse = new ProtosOpenapiV1CreateTicketResponse.Builder()
    .failed(Arrays.asList(
        new ProtosOpenapiV1CreateTicketResponseTicketCreationFailed.Builder()
            .error("error6")
            .issueIds(Arrays.asList(
                196L
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new ProtosOpenapiV1CreateTicketResponseTicketCreationFailed.Builder()
            .error("error6")
            .issueIds(Arrays.asList(
                196L
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .skipped(Arrays.asList(
        new ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped.Builder()
            .issueIds(Arrays.asList(
                38L
            ))
            .reason("reason4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped.Builder()
            .issueIds(Arrays.asList(
                38L
            ))
            .reason("reason4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .succeeded(Arrays.asList(
        new ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess.Builder()
            .externalSlug("external_slug4")
            .issueIds(Arrays.asList(
                230L,
                229L,
                228L
            ))
            .ticketId(2L)
            .ticketUrl("ticket_url0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess.Builder()
            .externalSlug("external_slug4")
            .issueIds(Arrays.asList(
                230L,
                229L,
                228L
            ))
            .ticketId(2L)
            .ticketUrl("ticket_url0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess.Builder()
            .externalSlug("external_slug4")
            .issueIds(Arrays.asList(
                230L,
                229L,
                228L
            ))
            .ticketId(2L)
            .ticketUrl("ticket_url0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

