
# Float Range

*This model accepts additional fields of type Object.*

## Structure

`FloatRange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Max` | `Double` | Optional | End of the range | Double getMax() | setMax(Double max) |
| `Min` | `Double` | Optional | Start of the range | Double getMin() | setMin(Double min) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.FloatRange;
import java.io.IOException;

FloatRange floatRange = new FloatRange.Builder()
    .max(69.02D)
    .min(4.4D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

