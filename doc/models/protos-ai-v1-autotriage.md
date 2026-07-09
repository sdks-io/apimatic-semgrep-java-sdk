
# Protos Ai V1 Autotriage

*This model accepts additional fields of type Object.*

## Structure

`ProtosAiV1Autotriage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Feedback` | [`ProtosAiV1AutotriageFeedback`](../../doc/models/protos-ai-v1-autotriage-feedback.md) | Optional | - | ProtosAiV1AutotriageFeedback getFeedback() | setFeedback(ProtosAiV1AutotriageFeedback feedback) |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `IssueId` | `String` | Optional | - | String getIssueId() | setIssueId(String issueId) |
| `MatchBasedId` | `String` | Optional | - | String getMatchBasedId() | setMatchBasedId(String matchBasedId) |
| `MemoryIdsReferenced` | `List<String>` | Optional | - | List<String> getMemoryIdsReferenced() | setMemoryIdsReferenced(List<String> memoryIdsReferenced) |
| `MemoryIdsRendered` | `List<String>` | Optional | - | List<String> getMemoryIdsRendered() | setMemoryIdsRendered(List<String> memoryIdsRendered) |
| `Reason` | `String` | Optional | The reasoning for a false positive verdict, explaining why you might want to ignore the finding. Empty string if verdict is true positive. | String getReason() | setReason(String reason) |
| `Verdict` | [`Verdict`](../../doc/models/verdict.md) | Optional | \| value \| description \|<br>\|-------\|---------------\|<br>\| VERDICT_TRUE_POSITIVE \|  \|<br>\| VERDICT_FALSE_POSITIVE \|  \|<br>\| VERDICT_NO_VERDICT \|  \| | Verdict getVerdict() | setVerdict(Verdict verdict) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosAiV1Autotriage;
import dev.semgrep.models.ProtosAiV1AutotriageFeedback;
import dev.semgrep.models.Rating;
import java.io.IOException;
import java.util.Arrays;

ProtosAiV1Autotriage protosAiV1Autotriage = new ProtosAiV1Autotriage.Builder()
    .feedback(new ProtosAiV1AutotriageFeedback.Builder()
        .autotriageId("autotriageId0")
        .note("note2")
        .rating(Rating.RATING_GOOD)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .id("id0")
    .issueId("issueId8")
    .matchBasedId("matchBasedId2")
    .memoryIdsReferenced(Arrays.asList(
        "memoryIdsReferenced2"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

