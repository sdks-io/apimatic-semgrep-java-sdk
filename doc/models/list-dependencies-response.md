
# List Dependencies Response

*This model accepts additional fields of type Object.*

## Structure

`ListDependenciesResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cursor` | `String` | Optional | Pass to next request to get next page of results. | String getCursor() | setCursor(String cursor) |
| `Dependencies` | [`List<ProtosScaV1FoundDependency>`](../../doc/models/protos-sca-v1-found-dependency.md) | Required | List of dependencies. | List<ProtosScaV1FoundDependency> getDependencies() | setDependencies(List<ProtosScaV1FoundDependency> dependencies) |
| `HasMore` | `boolean` | Required | True if there are more dependencies to get. | boolean getHasMore() | setHasMore(boolean hasMore) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.DateTimeHelper;
import dev.semgrep.models.Ecosystem1;
import dev.semgrep.models.ListDependenciesResponse;
import dev.semgrep.models.ProtosScaV1CodeLocation;
import dev.semgrep.models.ProtosScaV1Dependency;
import dev.semgrep.models.ProtosScaV1FoundDependency;
import java.io.IOException;
import java.util.Arrays;

ListDependenciesResponse listDependenciesResponse = new ListDependenciesResponse.Builder(
    Arrays.asList(
        new ProtosScaV1FoundDependency.Builder()
            .definedAt(new ProtosScaV1CodeLocation.Builder()
                .committedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .endCol("endCol8")
                .endLine("endLine2")
                .path("path2")
                .startCol("startCol2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .ecosystem(Ecosystem1.COCOAPODS)
            .licenses(Arrays.asList(
                "licenses3",
                "licenses4",
                "licenses5"
            ))
            .manifestDefinition(new ProtosScaV1CodeLocation.Builder()
                .committedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .endCol("endCol0")
                .endLine("endLine4")
                .path("path4")
                .startCol("startCol4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .mPackage(new ProtosScaV1Dependency.Builder()
                .name("name8")
                .versionSpecifier("versionSpecifier6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("id", ApiHelper.deserialize("\"1\""))
        .additionalProperty("name", ApiHelper.deserialize("\"dependency1\""))
        .additionalProperty("version", ApiHelper.deserialize("\"1.0.0\""))
            .build(),
        new ProtosScaV1FoundDependency.Builder()
            .definedAt(new ProtosScaV1CodeLocation.Builder()
                .committedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .endCol("endCol8")
                .endLine("endLine2")
                .path("path2")
                .startCol("startCol2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .ecosystem(Ecosystem1.COCOAPODS)
            .licenses(Arrays.asList(
                "licenses3",
                "licenses4",
                "licenses5"
            ))
            .manifestDefinition(new ProtosScaV1CodeLocation.Builder()
                .committedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .endCol("endCol0")
                .endLine("endLine4")
                .path("path4")
                .startCol("startCol4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .mPackage(new ProtosScaV1Dependency.Builder()
                .name("name8")
                .versionSpecifier("versionSpecifier6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("id", ApiHelper.deserialize("\"2\""))
        .additionalProperty("name", ApiHelper.deserialize("\"dependency2\""))
        .additionalProperty("version", ApiHelper.deserialize("\"2.0.0\""))
            .build()
    ),
    false
)
.cursor("cursor2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

