
# Fix Recommendation

Recommendation for fixing the vulnerability

*This model accepts additional fields of type Object.*

## Structure

`FixRecommendation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Package` | `String` | Optional | The package for which a fix is recommended | String getPackage() | setPackage(String mPackage) |
| `Version` | `String` | Optional | The recommended version of the package | String getVersion() | setVersion(String version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.FixRecommendation;
import java.io.IOException;

FixRecommendation fixRecommendation = new FixRecommendation.Builder()
    .mPackage("System.Drawing.Common")
    .version("5.0.3")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

