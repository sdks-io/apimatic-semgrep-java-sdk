
# Finding Location

Location of the record in a file, as reported by Semgrep. If null, then the information does not exist or lacks integrity (older or broken scans)

*This model accepts additional fields of type Object.*

## Structure

`FindingLocation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Column` | `Long` | Optional | Column at which the target starts | Long getColumn() | setColumn(Long column) |
| `EndColumn` | `Long` | Optional | Column at which the target ends | Long getEndColumn() | setEndColumn(Long endColumn) |
| `EndLine` | `Long` | Optional | Line at which the target ends | Long getEndLine() | setEndLine(Long endLine) |
| `FilePath` | `String` | Optional | File path of the relevant line and column numbers | String getFilePath() | setFilePath(String filePath) |
| `Line` | `Long` | Optional | Line at which the target starts | Long getLine() | setLine(Long line) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.FindingLocation;
import java.io.IOException;

FindingLocation findingLocation = new FindingLocation.Builder()
    .column(8L)
    .endColumn(16L)
    .endLine(124L)
    .filePath("frontend/src/corpComponents/Code.tsx")
    .line(120L)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

