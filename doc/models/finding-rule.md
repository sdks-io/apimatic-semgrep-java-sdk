
# Finding Rule

Rule that applies to this finding

*This model accepts additional fields of type Object.*

## Structure

`FindingRule`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Category` | `String` | Optional | Category the rule is associated with | String getCategory() | setCategory(String category) |
| `Confidence` | [`Confidence2`](../../doc/models/confidence-2.md) | Optional | Confidence level of the rule | Confidence2 getConfidence() | setConfidence(Confidence2 confidence) |
| `CweNames` | `List<String>` | Optional | CWE names associated with the rule | List<String> getCweNames() | setCweNames(List<String> cweNames) |
| `Message` | `String` | Optional | Rule message | String getMessage() | setMessage(String message) |
| `Name` | `String` | Optional | Name of the rule | String getName() | setName(String name) |
| `OwaspNames` | `List<String>` | Optional | OWASP names associated with the rule | List<String> getOwaspNames() | setOwaspNames(List<String> owaspNames) |
| `Subcategories` | `List<String>` | Optional | Subcategories of the rule | List<String> getSubcategories() | setSubcategories(List<String> subcategories) |
| `VulnerabilityClasses` | `List<String>` | Optional | Vulnerability classes the rule is associated with | List<String> getVulnerabilityClasses() | setVulnerabilityClasses(List<String> vulnerabilityClasses) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Confidence2;
import dev.semgrep.models.FindingRule;
import java.io.IOException;
import java.util.Arrays;

FindingRule findingRule = new FindingRule.Builder()
    .category("security")
    .confidence(Confidence2.HIGH)
    .cweNames(Arrays.asList(
        "CWE-319: Cleartext Transmission of Sensitive Information"
    ))
    .message("This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.")
    .name("html.security.plaintext-http-link.plaintext-http-link")
    .owaspNames(Arrays.asList(
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures"
    ))
    .subcategories(Arrays.asList(
        "vuln"
    ))
    .vulnerabilityClasses(Arrays.asList(
        "Mishandled Sensitive Information"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

