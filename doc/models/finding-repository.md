
# Finding Repository

Which repository this finding was identified in

*This model accepts additional fields of type Object.*

## Structure

`FindingRepository`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | The repository or named project that the finding is associated with | String getName() | setName(String name) |
| `Url` | `String` | Optional | The source URL from which this repository last scanned | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.FindingRepository;
import java.io.IOException;

FindingRepository findingRepository = new FindingRepository.Builder()
    .name("semgrep")
    .url("https://github.com/semgrep/semgrep")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

