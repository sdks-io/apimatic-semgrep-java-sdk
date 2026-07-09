
# Bulk Triage Request

*This model accepts additional fields of type Object.*

## Structure

`BulkTriageRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AutotriageVerdict` | [`AutotriageVerdict`](../../doc/models/autotriage-verdict.md) | Optional | The autotriage verdict to filter by | AutotriageVerdict getAutotriageVerdict() | setAutotriageVerdict(AutotriageVerdict autotriageVerdict) |
| `Categories` | `List<String>` | Optional | List of categories to filter by | List<String> getCategories() | setCategories(List<String> categories) |
| `ComponentTags` | `List<String>` | Optional | List of component tags to filter by | List<String> getComponentTags() | setComponentTags(List<String> componentTags) |
| `Confidence` | [`Confidence3`](../../doc/models/confidence-3.md) | Optional | List of confidence levels to filter by | Confidence3 getConfidence() | setConfidence(Confidence3 confidence) |
| `Dependencies` | `List<String>` | Optional | Filter by dependency name. Only applies for sca findings. | List<String> getDependencies() | setDependencies(List<String> dependencies) |
| `EpssProbability` | [`EpssProbability`](../../doc/models/epss-probability.md) | Optional | Filter by EPSS probability (likelihood of exploit). Only applies for sca findings. | EpssProbability getEpssProbability() | setEpssProbability(EpssProbability epssProbability) |
| `Exposures` | [`Exposures`](../../doc/models/exposures.md) | Optional | Filter by exposure (reachability type). Only applies for sca findings. Reachability is the ability of an attacker to access a vulnerability in a system. | Exposures getExposures() | setExposures(Exposures exposures) |
| `IncludeHistorical` | `Boolean` | Optional | Whether to include historical findings. Only applies for secrets findings. Defaults to true. | Boolean getIncludeHistorical() | setIncludeHistorical(Boolean includeHistorical) |
| `IssueIds` | `List<Long>` | Optional | An array of issue IDs to act on. If this is not provided, an issue filter should be provided. | List<Long> getIssueIds() | setIssueIds(List<Long> issueIds) |
| `IssueType` | [`IssueType`](../../doc/models/issue-type.md) | Required | Type of findings to bulk triage. | IssueType getIssueType() | setIssueType(IssueType issueType) |
| `Limit` | `Long` | Optional | Max number of issues to triage. Must be an integer between 1 and 3000. Defaults to 3000. When selecting findings to triage, Semgrep will also triage findings with the same fingerprint on other branches. As a result, the list of triaged issue_ids returned in the response may be higher than the specified limit.<br><br>**Default**: `3000L` | Long getLimit() | setLimit(Long limit) |
| `NewNote` | `String` | Optional | The note to attach to the bulk triaged findings. Maximum 3000 characters. | String getNewNote() | setNewNote(String newNote) |
| `NewTriageReason` | [`NewTriageReason`](../../doc/models/new-triage-reason.md) | Optional | The reason for triaging to a given triage state. | NewTriageReason getNewTriageReason() | setNewTriageReason(NewTriageReason newTriageReason) |
| `NewTriageState` | [`NewTriageState`](../../doc/models/new-triage-state.md) | Optional | The triage state you would like to bulk triage your findings to. | NewTriageState getNewTriageState() | setNewTriageState(NewTriageState newTriageState) |
| `Policies` | `List<String>` | Optional | List of policy modes to filter by | List<String> getPolicies() | setPolicies(List<String> policies) |
| `PolicyMode` | [`PolicyMode1`](../../doc/models/policy-mode-1.md) | Optional | List of policy modes to filter by | PolicyMode1 getPolicyMode() | setPolicyMode(PolicyMode1 policyMode) |
| `ProOnly` | `Boolean` | Optional | Filter by whether a finding is only available with Semgrep Pro features. | Boolean getProOnly() | setProOnly(Boolean proOnly) |
| `ProjectTags` | `List<String>` | Optional | List of project tags to filter by | List<String> getProjectTags() | setProjectTags(List<String> projectTags) |
| `Ref` | `String` | Optional | Branch reference to filter by | String getRef() | setRef(String ref) |
| `Repos` | `List<String>` | Optional | List of repository names to filter by | List<String> getRepos() | setRepos(List<String> repos) |
| `RepositoryVisibility` | [`RepositoryVisibility`](../../doc/models/repository-visibility.md) | Optional | Filter by repository visibility. Only applies for secrets findings. | RepositoryVisibility getRepositoryVisibility() | setRepositoryVisibility(RepositoryVisibility repositoryVisibility) |
| `Rules` | `List<String>` | Optional | List of rule names to filter by | List<String> getRules() | setRules(List<String> rules) |
| `Ruleset` | `List<String>` | Optional | List of Semgrep Registry rulesets to filter by | List<String> getRuleset() | setRuleset(List<String> ruleset) |
| `SecretTypes` | `List<String>` | Optional | Filter by type of secret (typically provider-related). Only applies for secrets findings. | List<String> getSecretTypes() | setSecretTypes(List<String> secretTypes) |
| `Severities` | [`Severities`](../../doc/models/severities.md) | Optional | List of severities to filter by | Severities getSeverities() | setSeverities(Severities severities) |
| `Since` | `String` | Optional | Epoch timestamp in seconds. Filters using the relevant_since field: the timestamp when this finding was detected by Semgrep (the first time, or when reintroduced). | String getSince() | setSince(String since) |
| `Status` | [`Status1`](../../doc/models/status-1.md) | Optional | The status to filter by | Status1 getStatus() | setStatus(Status1 status) |
| `Transitivities` | [`Transitivities`](../../doc/models/transitivities.md) | Optional | Filter by transitivity of a dependency. Only applies for sca findings. | Transitivities getTransitivities() | setTransitivities(Transitivities transitivities) |
| `TriageReasons` | [`TriageReasons`](../../doc/models/triage-reasons.md) | Optional | List of triage reasons to filter by | TriageReasons getTriageReasons() | setTriageReasons(TriageReasons triageReasons) |
| `ValidationState` | [`ValidationState`](../../doc/models/validation-state.md) | Optional | Filter by whether a secret could be validated. Only applies for secrets findings. | ValidationState getValidationState() | setValidationState(ValidationState validationState) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.AutotriageVerdict;
import dev.semgrep.models.BulkTriageRequest;
import dev.semgrep.models.Confidence3;
import dev.semgrep.models.IssueType;
import dev.semgrep.models.NewTriageReason;
import dev.semgrep.models.NewTriageState;
import dev.semgrep.models.Status1;
import java.io.IOException;
import java.util.Arrays;

BulkTriageRequest bulkTriageRequest = new BulkTriageRequest.Builder(
    IssueType.SCA
)
.autotriageVerdict(AutotriageVerdict.TRUE_POSITIVE)
.categories(Arrays.asList(
        "security",
        "performance"
    ))
.componentTags(Arrays.asList(
        "user authentication",
        "user data"
    ))
.confidence(Confidence3.HIGH)
.dependencies(Arrays.asList(
        "lodash",
        "express"
    ))
.includeHistorical(true)
.issueIds(Arrays.asList(
        123L,
        456L
    ))
.limit(100L)
.newNote("some note here")
.newTriageReason(NewTriageReason.ACCEPTABLE_RISK)
.newTriageState(NewTriageState.REOPENED)
.policies(Arrays.asList(
        "rule-board-block",
        "rule-board-pr-comments",
        "rule-board-audit"
    ))
.proOnly(true)
.projectTags(Arrays.asList(
        "my_project_tag_1",
        "my_project_tag_2"
    ))
.ref("refs/pull/1234/merge")
.repos(Arrays.asList(
        "myorg/repo1",
        "myorg/repo2"
    ))
.rules(Arrays.asList(
        "typescript.react.security.audit.react-no-refs.react-no-refs",
        "ajinabraham.njsscan.hardcoded_secrets.node_username"
    ))
.ruleset(Arrays.asList(
        "owasp-top-ten",
        "default"
    ))
.secretTypes(Arrays.asList(
        "Github",
        "Heroku",
        "AWS"
    ))
.since("1717334400")
.status(Status1.OPEN)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

