
# Protos Sca V1 Code Location

Specific location in a file.

*This model accepts additional fields of type Object.*

## Structure

`ProtosScaV1CodeLocation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CommittedAt` | `LocalDateTime` | Optional | Timestamp when code file was last modified, if available. | LocalDateTime getCommittedAt() | setCommittedAt(LocalDateTime committedAt) |
| `EndCol` | `String` | Optional | Ending column number (1 indexed). | String getEndCol() | setEndCol(String endCol) |
| `EndLine` | `String` | Optional | Ending line number (1 indexed). | String getEndLine() | setEndLine(String endLine) |
| `Path` | `String` | Optional | Path to a file. | String getPath() | setPath(String path) |
| `StartCol` | `String` | Optional | Starting column number (1 indexed). | String getStartCol() | setStartCol(String startCol) |
| `StartLine` | `String` | Optional | Starting line number (1 indexed). | String getStartLine() | setStartLine(String startLine) |
| `Url` | `String` | Optional | URL to code location if available, otherwise empty. | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.DateTimeHelper;
import dev.semgrep.models.ProtosScaV1CodeLocation;
import java.io.IOException;

ProtosScaV1CodeLocation protosScaV1CodeLocation = new ProtosScaV1CodeLocation.Builder()
    .committedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .endCol("endCol6")
    .endLine("endLine0")
    .path("path0")
    .startCol("startCol0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

