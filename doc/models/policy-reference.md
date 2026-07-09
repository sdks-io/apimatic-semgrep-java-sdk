
# Policy Reference

Reference to a policy, with some basic information. If null, then the information does not exist or lacks integrity (older or broken scans)

*This model accepts additional fields of type Object.*

## Structure

`PolicyReference`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `Long` | Optional | Unique numerical identifier of the policy | Long getId() | setId(Long id) |
| `Name` | `String` | Optional | Human readable name | String getName() | setName(String name) |
| `Slug` | `String` | Optional | Sanitized machine-readable name | String getSlug() | setSlug(String slug) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.PolicyReference;
import java.io.IOException;

PolicyReference policyReference = new PolicyReference.Builder()
    .id(120L)
    .name("Default Policy")
    .slug("default-policy")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

