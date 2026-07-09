
# Protos Sca V1 Sbom Format Version

*This model accepts additional fields of type Object.*

## Structure

`ProtosScaV1SbomFormatVersion`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CyclonedxVersion` | [`CyclonedxVersion`](../../doc/models/cyclonedx-version.md) | Optional | CycloneDX schema version for the SBOM export. Supported: 1.4, 1.5, 1.6, 1.7. Defaults to 1.4 when unset.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_CYCLONE_DX_VERSION_V1_4 \|  \|<br>\| SBOM_CYCLONE_DX_VERSION_V1_5 \|  \|<br>\| SBOM_CYCLONE_DX_VERSION_V1_6 \|  \|<br>\| SBOM_CYCLONE_DX_VERSION_V1_7 \|  \| | CyclonedxVersion getCyclonedxVersion() | setCyclonedxVersion(CyclonedxVersion cyclonedxVersion) |
| `Format` | [`Format`](../../doc/models/format.md) | Optional | Format for the SBOM export.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_FORMAT_CYCLONEDX \|  \|<br><br>**Default**: `Format.SBOM_FORMAT_CYCLONEDX` | Format getFormat() | setFormat(Format format) |
| `Version` | `String` | Optional | Deprecated. Use `cyclonedx_version`. Free-text CycloneDX version, e.g. "1.7". | String getVersion() | setVersion(String version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.CyclonedxVersion;
import dev.semgrep.models.Format;
import dev.semgrep.models.ProtosScaV1SbomFormatVersion;
import java.io.IOException;

ProtosScaV1SbomFormatVersion protosScaV1SbomFormatVersion = new ProtosScaV1SbomFormatVersion.Builder()
    .cyclonedxVersion(CyclonedxVersion.SBOM_CYCLONE_DX_VERSION_V1_6)
    .format(Format.SBOM_FORMAT_CYCLONEDX)
    .version("version6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

