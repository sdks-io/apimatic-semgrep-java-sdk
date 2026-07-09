
# Protos Common V1 Review Comment

*This model accepts additional fields of type Object.*

## Structure

`ProtosCommonV1ReviewComment`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExternalDiscussionId` | `String` | Optional | External ID of the review comment or discussion thread. | String getExternalDiscussionId() | setExternalDiscussionId(String externalDiscussionId) |
| `ExternalNoteId` | `String` | Optional | External ID of the specific note in the review comment discussion thread. Only applicable for GitLab.com, GitLab Self-Managed and Azure DevOps. | String getExternalNoteId() | setExternalNoteId(String externalNoteId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosCommonV1ReviewComment;
import java.io.IOException;

ProtosCommonV1ReviewComment protosCommonV1ReviewComment = new ProtosCommonV1ReviewComment.Builder()
    .externalDiscussionId("externalDiscussionId8")
    .externalNoteId("externalNoteId0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

