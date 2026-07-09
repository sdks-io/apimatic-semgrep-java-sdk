
# Protos Ai V1 Autotriage Feedback

*This model accepts additional fields of type Object.*

## Structure

`ProtosAiV1AutotriageFeedback`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AutotriageId` | `String` | Optional | - | String getAutotriageId() | setAutotriageId(String autotriageId) |
| `Note` | `String` | Optional | - | String getNote() | setNote(String note) |
| `Rating` | [`Rating`](../../doc/models/rating.md) | Optional | \| value \| description \|<br>\|-------\|---------------\|<br>\| RATING_GOOD \| Autotriage rated positively by a user. \|<br>\| RATING_BAD \| Autotriage rated negatively by a user. \| | Rating getRating() | setRating(Rating rating) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosAiV1AutotriageFeedback;
import dev.semgrep.models.Rating;
import java.io.IOException;

ProtosAiV1AutotriageFeedback protosAiV1AutotriageFeedback = new ProtosAiV1AutotriageFeedback.Builder()
    .autotriageId("autotriageId4")
    .note("note4")
    .rating(Rating.RATING_GOOD)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

