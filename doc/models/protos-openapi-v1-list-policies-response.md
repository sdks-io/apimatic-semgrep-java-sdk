
# Protos Openapi V1 List Policies Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1ListPoliciesResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Policies` | [`List<Policy>`](../../doc/models/policy.md) | Optional | List of Policies associated with the given Deployment. | List<Policy> getPolicies() | setPolicies(List<Policy> policies) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Policy;
import dev.semgrep.models.ProductType;
import dev.semgrep.models.ProtosOpenapiV1ListPoliciesResponse;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1ListPoliciesResponse protosOpenapiV1ListPoliciesResponse = new ProtosOpenapiV1ListPoliciesResponse.Builder()
    .policies(Arrays.asList(
        new Policy.Builder()
            .id("1")
            .isDefault(true)
            .name("Global Policy")
            .productType(ProductType.PRODUCT_TYPE_SAST)
            .slug("global_policy")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Policy.Builder()
            .id("2")
            .isDefault(false)
            .name("Semgrep test")
            .productType(ProductType.PRODUCT_TYPE_SAST)
            .slug("semgrep_test")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Policy.Builder()
            .id("3")
            .isDefault(true)
            .name("Global Secrets Policy")
            .productType(ProductType.PRODUCT_TYPE_SECRETS)
            .slug("global_secrets_policy")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

