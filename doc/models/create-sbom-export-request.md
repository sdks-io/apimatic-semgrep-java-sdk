
# Create Sbom Export Request

*This model accepts additional fields of type Object.*

## Structure

`CreateSbomExportRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeploymentId` | `String` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. | String getDeploymentId() | setDeploymentId(String deploymentId) |
| `FormatVersion` | [`ProtosScaV1SbomFormatVersion`](../../doc/models/protos-sca-v1-sbom-format-version.md) | Optional | - | ProtosScaV1SbomFormatVersion getFormatVersion() | setFormatVersion(ProtosScaV1SbomFormatVersion formatVersion) |
| `MetadataComponentType` | [`MetadataComponentType`](../../doc/models/metadata-component-type.md) | Optional | Metadata component type for the SBOM export.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_APPLICATION \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_FRAMEWORK \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_LIBRARY \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_CONTAINER \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_PLATFORM \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_OPERATING_SYSTEM \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_DEVICE \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_DEVICE_DRIVER \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_FIRMWARE \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_FILE \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_MACHINE_LEARNING_MODEL \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_DATA \|  \|<br><br>**Default**: `MetadataComponentType.SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_APPLICATION` | MetadataComponentType getMetadataComponentType() | setMetadataComponentType(MetadataComponentType metadataComponentType) |
| `MetadataSupplier` | [`ProtosScaV1SbomMetadataSupplier`](../../doc/models/protos-sca-v1-sbom-metadata-supplier.md) | Optional | - | ProtosScaV1SbomMetadataSupplier getMetadataSupplier() | setMetadataSupplier(ProtosScaV1SbomMetadataSupplier metadataSupplier) |
| `Ref` | `String` | Optional | Branch to export SBOM for (Ex. ref=`refs/pull/1234/merge`). | String getRef() | setRef(String ref) |
| `RepositoryId` | `String` | Optional | Repository ID to export SBOM for. | String getRepositoryId() | setRepositoryId(String repositoryId) |
| `SbomOutputFormat` | [`SbomOutputFormat`](../../doc/models/sbom-output-format.md) | Optional | SBOM output format for the SBOM export.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_OUTPUT_FORMAT_JSON \|  \| | SbomOutputFormat getSbomOutputFormat() | setSbomOutputFormat(SbomOutputFormat sbomOutputFormat) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.CreateSbomExportRequest;
import dev.semgrep.models.CyclonedxVersion;
import dev.semgrep.models.Format;
import dev.semgrep.models.MetadataComponentType;
import dev.semgrep.models.ProtosScaV1SbomFormatVersion;
import dev.semgrep.models.ProtosScaV1SbomMetadataContact;
import dev.semgrep.models.ProtosScaV1SbomMetadataSupplier;
import dev.semgrep.models.SbomOutputFormat;
import java.io.IOException;

CreateSbomExportRequest createSbomExportRequest = new CreateSbomExportRequest.Builder(
    "123"
)
.formatVersion(new ProtosScaV1SbomFormatVersion.Builder()
        .cyclonedxVersion(CyclonedxVersion.SBOM_CYCLONE_DX_VERSION_V1_6)
        .format(Format.SBOM_FORMAT_CYCLONEDX)
        .version("version8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.metadataComponentType(MetadataComponentType.SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_APPLICATION)
.metadataSupplier(new ProtosScaV1SbomMetadataSupplier.Builder()
        .contact(new ProtosScaV1SbomMetadataContact.Builder()
            .email("email4")
            .name("name2")
            .phone("phone2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .name("name4")
        .url("url8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.ref("refs/pull/1234/merge")
.repositoryId("123")
.sbomOutputFormat(SbomOutputFormat.SBOM_OUTPUT_FORMAT_JSON)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

