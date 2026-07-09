
# Click to Fix Failure

A failed PR creation attempt by Semgrep's Click to Fix feature

*This model accepts additional fields of type Object.*

## Structure

`ClickToFixFailure`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `String` | Optional | When this failure occurred | String getCreatedAt() | setCreatedAt(String createdAt) |
| `Reason` | `String` | Optional | Reason for the PR creation failure | String getReason() | setReason(String reason) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ClickToFixFailure;
import java.io.IOException;

ClickToFixFailure clickToFixFailure = new ClickToFixFailure.Builder()
    .createdAt("2024-01-15 10:30:00+00:00")
    .reason("merge conflict in target branch")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

