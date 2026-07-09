
# Review Comment

External review comment information associated with a finding

*This model accepts additional fields of type Object.*

## Structure

`ReviewComment`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExternalDiscussionId` | `String` | Optional | External ID of the review comment or discussion thread | String getExternalDiscussionId() | setExternalDiscussionId(String externalDiscussionId) |
| `ExternalNoteId` | `String` | Optional | External ID of the specific note in the review comment discussion thread. Only applicable for GitLab.com, GitLab Self-Managed and Azure DevOps | String getExternalNoteId() | setExternalNoteId(String externalNoteId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ReviewComment;
import java.io.IOException;

ReviewComment reviewComment = new ReviewComment.Builder()
    .externalDiscussionId("af04762b69acfb74c8f9")
    .externalNoteId("123523")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

