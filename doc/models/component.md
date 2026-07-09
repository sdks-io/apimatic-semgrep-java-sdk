
# Component

Semgrep Assistant's guess as for what the matched source code's purpose is

*This model accepts additional fields of type Object.*

## Structure

`Component`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Risk` | [`Risk`](../../doc/models/risk.md) | Optional | Component risk level | Risk getRisk() | setRisk(Risk risk) |
| `Tag` | `String` | Optional | Component tag | String getTag() | setTag(String tag) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Component;
import dev.semgrep.models.Risk;
import java.io.IOException;

Component component = new Component.Builder()
    .risk(Risk.HIGH)
    .tag("user data")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

