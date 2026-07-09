
# Sca Findings

A list of Supply Chain findings that Semgrep has identified in your organization

*This model accepts additional fields of type Object.*

## Structure

`ScaFindings`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Findings` | [`List<ScaFinding>`](../../doc/models/sca-finding.md) | Optional | A list of Supply Chain findings. | List<ScaFinding> getFindings() | setFindings(List<ScaFinding> findings) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Confidence1;
import dev.semgrep.models.EpssScore;
import dev.semgrep.models.ExternalTicket;
import dev.semgrep.models.ScaFinding;
import dev.semgrep.models.ScaFindings;
import java.io.IOException;
import java.util.Arrays;

ScaFindings scaFindings = new ScaFindings.Builder()
    .findings(Arrays.asList(
        new ScaFinding.Builder()
            .categories(Arrays.asList(
                "categories4",
                "categories3"
            ))
            .confidence(Confidence1.LOW)
            .createdAt("created_at6")
            .epssScore(new EpssScore.Builder()
                .percentile(236.52D)
                .score(242.58D)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
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
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new ScaFinding.Builder()
            .categories(Arrays.asList(
                "categories4",
                "categories3"
            ))
            .confidence(Confidence1.LOW)
            .createdAt("created_at6")
            .epssScore(new EpssScore.Builder()
                .percentile(236.52D)
                .score(242.58D)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
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
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new ScaFinding.Builder()
            .categories(Arrays.asList(
                "categories4",
                "categories3"
            ))
            .confidence(Confidence1.LOW)
            .createdAt("created_at6")
            .epssScore(new EpssScore.Builder()
                .percentile(236.52D)
                .score(242.58D)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
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
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

