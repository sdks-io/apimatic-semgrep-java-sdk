
# Usage

Usage of the vulnerable package in the codebase. Applies to reachable findings

*This model accepts additional fields of type Object.*

## Structure

`Usage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExternalTicket` | [`ExternalTicket`](../../doc/models/external-ticket.md) | Optional | External ticket associated with finding | ExternalTicket getExternalTicket() | setExternalTicket(ExternalTicket externalTicket) |
| `Location` | [`FindingLocation`](../../doc/models/finding-location.md) | Optional | Location of the record in a file, as reported by Semgrep. If null, then the information does not exist or lacks integrity (older or broken scans) | FindingLocation getLocation() | setLocation(FindingLocation location) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ExternalTicket;
import dev.semgrep.models.FindingLocation;
import dev.semgrep.models.Usage;
import java.io.IOException;
import java.util.Arrays;

Usage usage = new Usage.Builder()
    .externalTicket(new ExternalTicket.Builder()
        .externalSlug("external_slug4")
        .id(228L)
        .linkedIssueIds(Arrays.asList(
            115L,
            116L,
            117L
        ))
        .url("url8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .location(new FindingLocation.Builder()
        .column(222L)
        .endColumn(174L)
        .endLine(120L)
        .filePath("file_path0")
        .line(114L)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

