
# Protos Openapi V1 Update Policy Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1UpdatePolicyResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PolicyId` | `String` | Optional | Policy ID (numeric). Example: `456`. Can be found at `/deployments/{deploymentId}/policies`. | String getPolicyId() | setPolicyId(String policyId) |
| `UpdatedRule` | [`Rule`](../../doc/models/rule.md) | Optional | - | Rule getUpdatedRule() | setUpdatedRule(Rule updatedRule) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Confidence;
import dev.semgrep.models.ProtosOpenapiV1UpdatePolicyResponse;
import dev.semgrep.models.Rule;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1UpdatePolicyResponse protosOpenapiV1UpdatePolicyResponse = new ProtosOpenapiV1UpdatePolicyResponse.Builder()
    .policyId("1")
    .updatedRule(new Rule.Builder()
        .category("category4")
        .confidence(Confidence.CONFIDENCE_HIGH)
        .cweCategories(Arrays.asList(
            "cweCategories9"
        ))
        .hasValidators(false)
        .id("id6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

