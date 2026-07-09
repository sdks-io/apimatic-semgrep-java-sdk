
# Protos Openapi V1 List Secrets Path Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1ListSecretsPathResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cursor` | `String` | Optional | Cursor to paginate through the results. | String getCursor() | setCursor(String cursor) |
| `Findings` | [`List<ProtosSecretsV1SecretsFinding>`](../../doc/models/protos-secrets-v1-secrets-finding.md) | Optional | List of Secrets associated with the given Deployment. | List<ProtosSecretsV1SecretsFinding> getFindings() | setFindings(List<ProtosSecretsV1SecretsFinding> findings) |
| `Previous` | `String` | Optional | Cursor to paginate backwards through the results. | String getPrevious() | setPrevious(String previous) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.DateTimeHelper;
import dev.semgrep.models.Confidence7;
import dev.semgrep.models.ProtosAiV1Autotriage;
import dev.semgrep.models.ProtosAiV1AutotriageFeedback;
import dev.semgrep.models.ProtosOpenapiV1ListSecretsPathResponse;
import dev.semgrep.models.ProtosSecretsV1SecretsFinding;
import dev.semgrep.models.ProtosTicketingV1ExternalTicket;
import dev.semgrep.models.Rating;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1ListSecretsPathResponse protosOpenapiV1ListSecretsPathResponse = new ProtosOpenapiV1ListSecretsPathResponse.Builder()
    .cursor("cursor4")
    .findings(Arrays.asList(
        new ProtosSecretsV1SecretsFinding.Builder()
            .autotriage(new ProtosAiV1Autotriage.Builder()
                .feedback(new ProtosAiV1AutotriageFeedback.Builder()
                    .autotriageId("autotriageId0")
                    .note("note2")
                    .rating(Rating.RATING_GOOD)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .id("id2")
                .issueId("issueId0")
                .matchBasedId("matchBasedId6")
                .memoryIdsReferenced(Arrays.asList(
                    "memoryIdsReferenced4"
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .confidence(Confidence7.CONFIDENCE_HIGH)
            .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .externalTicket(new ProtosTicketingV1ExternalTicket.Builder()
                .externalSlug("externalSlug6")
                .id("id6")
                .linkedIssueIds(Arrays.asList(
                    "linkedIssueIds7"
                ))
                .url("url0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .findingPath("findingPath8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new ProtosSecretsV1SecretsFinding.Builder()
            .autotriage(new ProtosAiV1Autotriage.Builder()
                .feedback(new ProtosAiV1AutotriageFeedback.Builder()
                    .autotriageId("autotriageId0")
                    .note("note2")
                    .rating(Rating.RATING_GOOD)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .id("id2")
                .issueId("issueId0")
                .matchBasedId("matchBasedId6")
                .memoryIdsReferenced(Arrays.asList(
                    "memoryIdsReferenced4"
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .confidence(Confidence7.CONFIDENCE_HIGH)
            .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .externalTicket(new ProtosTicketingV1ExternalTicket.Builder()
                .externalSlug("externalSlug6")
                .id("id6")
                .linkedIssueIds(Arrays.asList(
                    "linkedIssueIds7"
                ))
                .url("url0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .findingPath("findingPath8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .previous("previous0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

