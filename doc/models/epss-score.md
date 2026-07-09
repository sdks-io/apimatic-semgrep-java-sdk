
# Epss Score

The score assigned by FIRST.org's Exploitation Probability Scoring System

*This model accepts additional fields of type Object.*

## Structure

`EpssScore`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Percentile` | `Double` | Optional | This EPSS score's percentile among all EPSS scores, from 0 to 1 | Double getPercentile() | setPercentile(Double percentile) |
| `Score` | `Double` | Optional | The explotation probability, from 0 to 1 | Double getScore() | setScore(Double score) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.EpssScore;
import java.io.IOException;

EpssScore epssScore = new EpssScore.Builder()
    .percentile(0.994D)
    .score(0.97D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

