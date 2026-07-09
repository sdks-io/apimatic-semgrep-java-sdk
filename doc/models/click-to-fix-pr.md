
# Click to Fix Pr

A pull request created by Semgrep's Click to Fix feature

*This model accepts additional fields of type Object.*

## Structure

`ClickToFixPr`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `String` | Optional | When this PR was created | String getCreatedAt() | setCreatedAt(String createdAt) |
| `Url` | `String` | Optional | URL of the pull request | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ClickToFixPr;
import java.io.IOException;

ClickToFixPr clickToFixPr = new ClickToFixPr.Builder()
    .createdAt("2024-01-15 10:30:00+00:00")
    .url("https://github.com/myorg/myrepo/pull/123")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

