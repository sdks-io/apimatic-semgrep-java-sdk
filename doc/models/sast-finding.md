
# Sast Finding

A Code finding that Semgrep has identified in your organization

*This model accepts additional fields of type Object.*

## Structure

`SastFinding`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Assistant` | [`Assistant`](../../doc/models/assistant.md) | Optional | Semgrep Assistant data. Only present if Assistant is enabled | Assistant getAssistant() | setAssistant(Assistant assistant) |
| `Categories` | `List<String>` | Optional | The categories of the finding as classified by the associated rule metadata | List<String> getCategories() | setCategories(List<String> categories) |
| `ClickToFixFailures` | [`List<ClickToFixFailure>`](../../doc/models/click-to-fix-failure.md) | Optional | Failed PR creation attempts by Semgrep's autofix feature (Click to Fix) for this finding | List<ClickToFixFailure> getClickToFixFailures() | setClickToFixFailures(List<ClickToFixFailure> clickToFixFailures) |
| `ClickToFixPrs` | [`List<ClickToFixPr>`](../../doc/models/click-to-fix-pr.md) | Optional | Pull requests created by Semgrep's autofix feature (Click to Fix) for this finding | List<ClickToFixPr> getClickToFixPrs() | setClickToFixPrs(List<ClickToFixPr> clickToFixPrs) |
| `Confidence` | [`Confidence1`](../../doc/models/confidence-1.md) | Optional | Confidence of the finding, derived from the rule that triggered it | Confidence1 getConfidence() | setConfidence(Confidence1 confidence) |
| `CreatedAt` | `String` | Optional | The timestamp when this finding was created | String getCreatedAt() | setCreatedAt(String createdAt) |
| `ExternalTicket` | [`ExternalTicket`](../../doc/models/external-ticket.md) | Optional | External ticket associated with finding | ExternalTicket getExternalTicket() | setExternalTicket(ExternalTicket externalTicket) |
| `FirstSeenScanId` | `Long` | Optional | Unique ID of the Semgrep scan that first identified this finding | Long getFirstSeenScanId() | setFirstSeenScanId(Long firstSeenScanId) |
| `Id` | `Long` | Optional | Unique ID of this finding | Long getId() | setId(Long id) |
| `LineOfCodeUrl` | `String` | Optional | The source URL including file and line number | String getLineOfCodeUrl() | setLineOfCodeUrl(String lineOfCodeUrl) |
| `Location` | [`FindingLocation`](../../doc/models/finding-location.md) | Optional | Location of the record in a file, as reported by Semgrep. If null, then the information does not exist or lacks integrity (older or broken scans) | FindingLocation getLocation() | setLocation(FindingLocation location) |
| `MatchBasedId` | `String` | Optional | ID calculated based on a finding's file path, rule identifier and pattern, and index | String getMatchBasedId() | setMatchBasedId(String matchBasedId) |
| `Ref` | `String` | Optional | External reference to the source of this finding (e.g. PR) | String getRef() | setRef(String ref) |
| `RelevantSince` | `String` | Optional | The timestamp when this finding was detected by Semgrep (the first time, or when reintroduced) | String getRelevantSince() | setRelevantSince(String relevantSince) |
| `Repository` | [`FindingRepository`](../../doc/models/finding-repository.md) | Optional | Which repository this finding was identified in | FindingRepository getRepository() | setRepository(FindingRepository repository) |
| `ReviewComments` | [`List<ReviewComment>`](../../doc/models/review-comment.md) | Optional | List of external review comment information associated with a finding | List<ReviewComment> getReviewComments() | setReviewComments(List<ReviewComment> reviewComments) |
| `Rule` | [`FindingRule`](../../doc/models/finding-rule.md) | Optional | Rule that applies to this finding | FindingRule getRule() | setRule(FindingRule rule) |
| `RuleMessage` | `String` | Optional | Deprecated in favor of rule.message. Rule message at the time of finding identification. Older findings may not have a value for this field | String getRuleMessage() | setRuleMessage(String ruleMessage) |
| `RuleName` | `String` | Optional | Deprecated in favor of rule.name | String getRuleName() | setRuleName(String ruleName) |
| `Severity` | [`Severity1`](../../doc/models/severity-1.md) | Optional | Severity of the finding, derived from the rule that triggered it. Low is equivalent to INFO, Medium to WARNING, and High to ERROR | Severity1 getSeverity() | setSeverity(Severity1 severity) |
| `SourcingPolicy` | [`PolicyReference`](../../doc/models/policy-reference.md) | Optional | Reference to a policy, with some basic information. If null, then the information does not exist or lacks integrity (older or broken scans) | PolicyReference getSourcingPolicy() | setSourcingPolicy(PolicyReference sourcingPolicy) |
| `State` | [`State`](../../doc/models/state.md) | Optional | The finding's resolution state. Managed only by changes detected at scan time, the `state` is combined with `triage_state` to ultimately determine a final `status` which is exposed in the UI and API | State getState() | setState(State state) |
| `StateUpdatedAt` | `String` | Optional | When this issue's `state` (resolution state) was last updated, as distinct from when the issue was triaged (`triaged_at`) | String getStateUpdatedAt() | setStateUpdatedAt(String stateUpdatedAt) |
| `Status` | [`Status`](../../doc/models/status.md) | Optional | The finding's status as exposed in the UI. Status is a derived property combining information from the finding `state` and `triage_state`. The `triage_state` can be used to override the scan state if the finding is still detected | Status getStatus() | setStatus(Status status) |
| `SyntacticId` | `String` | Optional | ID calculated based on a finding's file path, rule identifier and matched code, and index. Prefer `match_based_id` | String getSyntacticId() | setSyntacticId(String syntacticId) |
| `TriageComment` | `String` | Optional | The detailed comment provided during triage | String getTriageComment() | setTriageComment(String triageComment) |
| `TriageReason` | [`TriageReason`](../../doc/models/triage-reason.md) | Optional | Reason provided when this issue was triaged | TriageReason getTriageReason() | setTriageReason(TriageReason triageReason) |
| `TriageState` | [`TriageState`](../../doc/models/triage-state.md) | Optional | The finding's triage state. Note: "reviewing" and "fixing" are only in private beta. Set by the user and used along with state to generate the final "status" viewable in the UI | TriageState getTriageState() | setTriageState(TriageState triageState) |
| `TriagedAt` | `String` | Optional | When the finding was triaged | String getTriagedAt() | setTriagedAt(String triagedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Assistant;
import dev.semgrep.models.Autofix;
import dev.semgrep.models.Autotriage;
import dev.semgrep.models.ClickToFixFailure;
import dev.semgrep.models.ClickToFixPr;
import dev.semgrep.models.Component;
import dev.semgrep.models.Confidence1;
import dev.semgrep.models.Guidance;
import dev.semgrep.models.Risk;
import dev.semgrep.models.RuleExplanation;
import dev.semgrep.models.SastFinding;
import dev.semgrep.models.Severity1;
import dev.semgrep.models.State;
import dev.semgrep.models.Status;
import dev.semgrep.models.TriageReason;
import dev.semgrep.models.TriageState;
import dev.semgrep.models.Verdict1;
import java.io.IOException;
import java.util.Arrays;

SastFinding sastFinding = new SastFinding.Builder()
    .assistant(new Assistant.Builder()
        .autofix(new Autofix.Builder()
            .explanation("explanation2")
            .fixCode("fix_code4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .autotriage(new Autotriage.Builder()
            .reason("reason2")
            .verdict(Verdict1.FALSE_POSITIVE)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .component(new Component.Builder()
            .risk(Risk.HIGH)
            .tag("tag8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .guidance(new Guidance.Builder()
            .instructions("instructions4")
            .summary("summary8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .ruleExplanation(new RuleExplanation.Builder()
            .explanation("explanation8")
            .summary("summary4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .categories(Arrays.asList(
        "security"
    ))
    .clickToFixFailures(Arrays.asList(
        new ClickToFixFailure.Builder()
            .createdAt("created_at8")
            .reason("reason0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .clickToFixPrs(Arrays.asList(
        new ClickToFixPr.Builder()
            .createdAt("created_at4")
            .url("url0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .confidence(Confidence1.MEDIUM)
    .createdAt("2020-11-18 23:28:12.391807+00:00")
    .firstSeenScanId(1234L)
    .id(1234567L)
    .lineOfCodeUrl("https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1")
    .matchBasedId("0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1")
    .ref("refs/pull/1234/merge")
    .relevantSince("2020-11-18 23:28:12.391807+00:00")
    .ruleName("typescript.react.security.audit.react-no-refs.react-no-refs")
    .severity(Severity1.MEDIUM)
    .state(State.UNRESOLVED)
    .stateUpdatedAt("2020-11-19 23:28:12.391807+00:00")
    .status(Status.OPEN)
    .syntacticId("440eeface888e78afceac3dc7d4cc2cf")
    .triageComment("This finding is from the test repo")
    .triageReason(TriageReason.ACCEPTABLE_RISK)
    .triageState(TriageState.UNTRIAGED)
    .triagedAt("2020-11-19 23:28:12.391807+00:00")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

