
# Protos Openapi V1 List Policy Rules Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1ListPolicyRulesResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cursor` | `String` | Optional | Cursor to paginate through the rules. | String getCursor() | setCursor(String cursor) |
| `Policy` | [`Policy`](../../doc/models/policy.md) | Optional | - | Policy getPolicy() | setPolicy(Policy policy) |
| `Rules` | [`List<Rule>`](../../doc/models/rule.md) | Optional | List of Rules for the given Policy. | List<Rule> getRules() | setRules(List<Rule> rules) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.DateTimeHelper;
import dev.semgrep.models.Confidence;
import dev.semgrep.models.Policy;
import dev.semgrep.models.PolicyMode;
import dev.semgrep.models.ProductType;
import dev.semgrep.models.ProtosOpenapiV1ListPolicyRulesResponse;
import dev.semgrep.models.Rule;
import dev.semgrep.models.Severity;
import dev.semgrep.models.Source;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1ListPolicyRulesResponse protosOpenapiV1ListPolicyRulesResponse = new ProtosOpenapiV1ListPolicyRulesResponse.Builder()
    .cursor("Pm0ROjIwMjQtMDItMDYgMjA6MDQ6NDguMEDzNzk2fmk6NYTM2zUxOTI")
    .policy(new Policy.Builder()
        .id("id4")
        .isDefault(false)
        .name("name4")
        .productType(ProductType.PRODUCT_TYPE_SAST)
        .slug("slug8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .rules(Arrays.asList(
        new Rule.Builder()
            .category("security")
            .confidence(Confidence.CONFIDENCE_HIGH)
            .cweCategories(Arrays.asList(
                "CWE-918: Server-Side Request Forgery (SSRF)"
            ))
            .hasValidators(false)
            .id("1")
            .languages(Arrays.asList(
                "python"
            ))
            .lastChangeAt(DateTimeHelper.fromRfc8601DateTime("2024-07-29T22:33:37.380293Z"))
            .owaspCategories(Arrays.asList(
                "A07: Cross-Site Scripting (XSS)"
            ))
            .path("python.rule.1")
            .policyMode(PolicyMode.MODE_MONITOR)
            .registryMaintainer("semgrep")
            .rulesets(Arrays.asList(

            ))
            .severity(Severity.SEVERITY_HIGH)
            .source(Source.SOURCE_COMMUNITY)
            .technologies(Arrays.asList(
                "django",
                "flask"
            ))
            .url("https://semgrep.com/r/123/python.rule.1")
            .vulnerabilityClass(Arrays.asList(
                "Improper Authentication"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Rule.Builder()
            .category("security")
            .confidence(Confidence.CONFIDENCE_HIGH)
            .cweCategories(Arrays.asList(
                "CWE-918: Server-Side Request Forgery (SSRF)"
            ))
            .hasValidators(false)
            .id("2")
            .languages(Arrays.asList(
                "python"
            ))
            .lastChangeAt(DateTimeHelper.fromRfc8601DateTime("2024-07-29T22:33:37.380293Z"))
            .owaspCategories(Arrays.asList(
                "A01:2021 - Broken Access Control",
                "A07: Cross-Site Scripting (XSS)"
            ))
            .path("python.rule.shared")
            .policyMode(PolicyMode.MODE_COMMENT)
            .registryMaintainer("semgrep")
            .rulesets(Arrays.asList(
                "comment",
                "default"
            ))
            .severity(Severity.SEVERITY_MEDIUM)
            .source(Source.SOURCE_PRO)
            .technologies(Arrays.asList(
                "django",
                "flask"
            ))
            .url("https://semgrep.com/r/123/python.rule.shared")
            .vulnerabilityClass(Arrays.asList(
                "Improper Authentication"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Rule.Builder()
            .category("best-practice")
            .confidence(Confidence.CONFIDENCE_HIGH)
            .cweCategories(Arrays.asList(

            ))
            .hasValidators(false)
            .id("3")
            .languages(Arrays.asList(
                "python"
            ))
            .lastChangeAt(DateTimeHelper.fromRfc8601DateTime("2024-07-29T22:33:37.380293Z"))
            .lastChangeBy("example-user")
            .owaspCategories(Arrays.asList(

            ))
            .path("python.rule.custom_rule")
            .policyMode(PolicyMode.MODE_BLOCK)
            .registryMaintainer("semgrep")
            .rulesets(Arrays.asList(

            ))
            .severity(Severity.SEVERITY_MEDIUM)
            .source(Source.SOURCE_CUSTOM)
            .technologies(Arrays.asList(
                "django",
                "flask"
            ))
            .url("https://semgrep.com/r/123/python.rule.custom_rule")
            .vulnerabilityClass(Arrays.asList(
                "Improper Authentication"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

