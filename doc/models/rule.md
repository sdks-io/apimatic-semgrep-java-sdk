
# Rule

*This model accepts additional fields of type Object.*

## Structure

`Rule`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Category` | `String` | Optional | Category the Rule is associated with. | String getCategory() | setCategory(String category) |
| `Confidence` | [`Confidence`](../../doc/models/confidence.md) | Optional | Confidence based on the Rule's false-positive rate.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| CONFIDENCE_HIGH \|  \|<br>\| CONFIDENCE_MEDIUM \|  \|<br>\| CONFIDENCE_LOW \|  \| | Confidence getConfidence() | setConfidence(Confidence confidence) |
| `CweCategories` | `List<String>` | Optional | The CWE associated with the Rule. | List<String> getCweCategories() | setCweCategories(List<String> cweCategories) |
| `HasValidators` | `Boolean` | Optional | When True, the secrets rule has validators. | Boolean getHasValidators() | setHasValidators(Boolean hasValidators) |
| `Id` | `String` | Optional | ID of the Rule. | String getId() | setId(String id) |
| `Languages` | `List<String>` | Optional | Languages the Rule applies to. | List<String> getLanguages() | setLanguages(List<String> languages) |
| `LastChangeAt` | `LocalDateTime` | Optional | Timestamp of when the Rule was last changed. | LocalDateTime getLastChangeAt() | setLastChangeAt(LocalDateTime lastChangeAt) |
| `LastChangeBy` | `String` | Optional | Username of who last changed the Rule. | String getLastChangeBy() | setLastChangeBy(String lastChangeBy) |
| `OwaspCategories` | `List<String>` | Optional | Owasp categories the Rule is associated with. | List<String> getOwaspCategories() | setOwaspCategories(List<String> owaspCategories) |
| `Path` | `String` | Optional | Full path of the Rule. | String getPath() | setPath(String path) |
| `PolicyMode` | [`PolicyMode`](../../doc/models/policy-mode.md) | Optional | Mode behavior: Monitor / Comment / Block / Disabled<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| MODE_MONITOR \| Monitor mode, silently report findings \|<br>\| MODE_COMMENT \| Comment mode, leaves PR comments but does not block \|<br>\| MODE_BLOCK \| Block mode, leaves PR comments and blocks PR \|<br>\| MODE_DISABLED \| Disabled mode, not active \| | PolicyMode getPolicyMode() | setPolicyMode(PolicyMode policyMode) |
| `RegistryMaintainer` | `String` | Optional | The Registry maintainer associated with the Rule (if applicable). | String getRegistryMaintainer() | setRegistryMaintainer(String registryMaintainer) |
| `Rulesets` | `List<String>` | Optional | Rulesets to which the Rule belongs (if applicable). | List<String> getRulesets() | setRulesets(List<String> rulesets) |
| `SecretType` | `String` | Optional | The secret type (if applicable). | String getSecretType() | setSecretType(String secretType) |
| `Severity` | [`Severity`](../../doc/models/severity.md) | Optional | Severity level ("seriousness" of the finding)<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SEVERITY_HIGH \|  \|<br>\| SEVERITY_MEDIUM \|  \|<br>\| SEVERITY_LOW \|  \|<br>\| SEVERITY_CRITICAL \|  \| | Severity getSeverity() | setSeverity(Severity severity) |
| `Source` | [`Source`](../../doc/models/source.md) | Optional | Source of the Rule<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SOURCE_PRO \| From Pro rules \|<br>\| SOURCE_COMMUNITY \| From Semgrep Community rules \|<br>\| SOURCE_CUSTOM \| From Custom rules \| | Source getSource() | setSource(Source source) |
| `Technologies` | `List<String>` | Optional | Technologies the Rule is associated with. | List<String> getTechnologies() | setTechnologies(List<String> technologies) |
| `Url` | `String` | Optional | The URL of the Rule. | String getUrl() | setUrl(String url) |
| `VulnerabilityClass` | `List<String>` | Optional | Vulnerability classes the Rule is associated with. | List<String> getVulnerabilityClass() | setVulnerabilityClass(List<String> vulnerabilityClass) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.DateTimeHelper;
import dev.semgrep.models.Confidence;
import dev.semgrep.models.PolicyMode;
import dev.semgrep.models.Rule;
import dev.semgrep.models.Severity;
import dev.semgrep.models.Source;
import java.io.IOException;
import java.util.Arrays;

Rule rule = new Rule.Builder()
    .category("security")
    .confidence(Confidence.CONFIDENCE_HIGH)
    .cweCategories(Arrays.asList(
        "CWE-918: Server-Side Request Forgery (SSRF)"
    ))
    .hasValidators(false)
    .id("id0")
    .languages(Arrays.asList(
        "python"
    ))
    .lastChangeAt(DateTimeHelper.fromRfc8601DateTime("2024-07-29 22:33:37.380293+00:00"))
    .owaspCategories(Arrays.asList(
        "A07: Cross-Site Scripting (XSS)"
    ))
    .path("python.rule.1")
    .policyMode(PolicyMode.MODE_BLOCK)
    .registryMaintainer("semgrep")
    .rulesets(Arrays.asList(

    ))
    .severity(Severity.SEVERITY_HIGH)
    .source(Source.SOURCE_COMMUNITY)
    .technologies(Arrays.asList(
        "django",
        "flask"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

