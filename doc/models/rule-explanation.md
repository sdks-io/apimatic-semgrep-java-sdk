
# Rule Explanation

AI-generated explanation of why a rule flagged this specific code

*This model accepts additional fields of type Object.*

## Structure

`RuleExplanation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Explanation` | `String` | Optional | Detailed explanation of why this rule flagged the code, including context about the security issue and why it applies to this specific code. AI generated content, review carefully | String getExplanation() | setExplanation(String explanation) |
| `Summary` | `String` | Optional | A concise summary of the rule explanation. May not be present for all findings | String getSummary() | setSummary(String summary) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.RuleExplanation;
import java.io.IOException;

RuleExplanation ruleExplanation = new RuleExplanation.Builder()
    .explanation("This code is vulnerable to SQL injection because user input from the `username` parameter is directly concatenated into the SQL query string without sanitization or parameterization.")
    .summary("User input directly concatenated into SQL query")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

