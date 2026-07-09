
# Protos Secrets V1 Secrets Finding

A Finding represents a single secret finding.

*This model accepts additional fields of type Object.*

## Structure

`ProtosSecretsV1SecretsFinding`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Autotriage` | [`ProtosAiV1Autotriage`](../../doc/models/protos-ai-v1-autotriage.md) | Optional | * Autotriage info for the finding.<br>  This is used for the Generic Secrets Detection project, for<br>  autotriaging secrets findings with LLMs | ProtosAiV1Autotriage getAutotriage() | setAutotriage(ProtosAiV1Autotriage autotriage) |
| `Confidence` | [`Confidence7`](../../doc/models/confidence-7.md) | Optional | Confidence of the finding.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| CONFIDENCE_HIGH \|  \|<br>\| CONFIDENCE_MEDIUM \|  \|<br>\| CONFIDENCE_LOW \|  \| | Confidence7 getConfidence() | setConfidence(Confidence7 confidence) |
| `CreatedAt` | `LocalDateTime` | Optional | Creation timestamp. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `ExternalTicket` | [`ProtosTicketingV1ExternalTicket`](../../doc/models/protos-ticketing-v1-external-ticket.md) | Optional | The external ticket reference | ProtosTicketingV1ExternalTicket getExternalTicket() | setExternalTicket(ProtosTicketingV1ExternalTicket externalTicket) |
| `FindingPath` | `String` | Optional | File path where the finding was detected. | String getFindingPath() | setFindingPath(String findingPath) |
| `FindingPathUrl` | `String` | Optional | URL to the file where the finding was detected. | String getFindingPathUrl() | setFindingPathUrl(String findingPathUrl) |
| `HistoricalInfo` | [`ProtosSecretsV1HistoricalInfo`](../../doc/models/protos-secrets-v1-historical-info.md) | Optional | Historical scanning info for the finding. | ProtosSecretsV1HistoricalInfo getHistoricalInfo() | setHistoricalInfo(ProtosSecretsV1HistoricalInfo historicalInfo) |
| `Id` | `String` | Optional | ID of the finding. | String getId() | setId(String id) |
| `Mode` | [`Mode`](../../doc/models/mode.md) | Optional | The behavior of the finding reporting: Monitor / Comment / Block.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| MODE_MONITOR \| Monitor mode, silently report findings \|<br>\| MODE_COMMENT \| Comment mode, leaves PR comments but does not block \|<br>\| MODE_BLOCK \| Block mode, leaves PR comments and blocks PR \|<br>\| MODE_DISABLED \| Disabled mode, not active \| | Mode getMode() | setMode(Mode mode) |
| `Ref` | `String` | Optional | Branch where the finding was detected. | String getRef() | setRef(String ref) |
| `RefUrl` | `String` | Optional | URL to the branch where the finding was detected. | String getRefUrl() | setRefUrl(String refUrl) |
| `Repository` | [`ProtosSecretsV1SecretsFindingRepository`](../../doc/models/protos-secrets-v1-secrets-finding-repository.md) | Optional | Repository where the finding was detected. | ProtosSecretsV1SecretsFindingRepository getRepository() | setRepository(ProtosSecretsV1SecretsFindingRepository repository) |
| `ReviewComments` | [`List<ProtosCommonV1ReviewComment>`](../../doc/models/protos-common-v1-review-comment.md) | Optional | List of external review comment information associated with a finding | List<ProtosCommonV1ReviewComment> getReviewComments() | setReviewComments(List<ProtosCommonV1ReviewComment> reviewComments) |
| `RuleHashId` | `String` | Optional | ID of the rule that triggered the finding. | String getRuleHashId() | setRuleHashId(String ruleHashId) |
| `Severity` | [`Severity4`](../../doc/models/severity-4.md) | Optional | Severity of the finding.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SEVERITY_HIGH \|  \|<br>\| SEVERITY_MEDIUM \|  \|<br>\| SEVERITY_LOW \|  \|<br>\| SEVERITY_CRITICAL \|  \| | Severity4 getSeverity() | setSeverity(Severity4 severity) |
| `Status` | [`Status6`](../../doc/models/status-6.md) | Optional | Status of the finding.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| FINDING_STATUS_OPEN \|  \|<br>\| FINDING_STATUS_IGNORED \|  \|<br>\| FINDING_STATUS_FIXED \|  \|<br>\| FINDING_STATUS_REMOVED \|  \|<br>\| FINDING_STATUS_UNKNOWN \|  \|<br>\| FINDING_STATUS_PROVISIONALLY_IGNORED \|  \| | Status6 getStatus() | setStatus(Status6 status) |
| `Type` | `String` | Optional | Service type for the secrets finding (e.g. AWS, GitHub, GitLab, etc). | String getType() | setType(String type) |
| `UpdatedAt` | `LocalDateTime` | Optional | Update timestamp. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `ValidationState` | [`ValidationState2`](../../doc/models/validation-state-2.md) | Optional | Whether the finding was validated or not.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| VALIDATION_STATE_CONFIRMED_VALID \|  \|<br>\| VALIDATION_STATE_CONFIRMED_INVALID \|  \|<br>\| VALIDATION_STATE_VALIDATION_ERROR \|  \|<br>\| VALIDATION_STATE_NO_VALIDATOR \|  \| | ValidationState2 getValidationState() | setValidationState(ValidationState2 validationState) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.DateTimeHelper;
import dev.semgrep.models.Confidence7;
import dev.semgrep.models.ProtosAiV1Autotriage;
import dev.semgrep.models.ProtosAiV1AutotriageFeedback;
import dev.semgrep.models.ProtosSecretsV1SecretsFinding;
import dev.semgrep.models.ProtosTicketingV1ExternalTicket;
import dev.semgrep.models.Rating;
import java.io.IOException;
import java.util.Arrays;

ProtosSecretsV1SecretsFinding protosSecretsV1SecretsFinding = new ProtosSecretsV1SecretsFinding.Builder()
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
    .confidence(Confidence7.CONFIDENCE_LOW)
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
    .findingPath("findingPath2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

