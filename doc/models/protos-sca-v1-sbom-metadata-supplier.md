
# Protos Sca V1 Sbom Metadata Supplier

*This model accepts additional fields of type Object.*

## Structure

`ProtosScaV1SbomMetadataSupplier`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Contact` | [`ProtosScaV1SbomMetadataContact`](../../doc/models/protos-sca-v1-sbom-metadata-contact.md) | Optional | - | ProtosScaV1SbomMetadataContact getContact() | setContact(ProtosScaV1SbomMetadataContact contact) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Url` | `String` | Optional | - | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosScaV1SbomMetadataContact;
import dev.semgrep.models.ProtosScaV1SbomMetadataSupplier;
import java.io.IOException;

ProtosScaV1SbomMetadataSupplier protosScaV1SbomMetadataSupplier = new ProtosScaV1SbomMetadataSupplier.Builder()
    .contact(new ProtosScaV1SbomMetadataContact.Builder()
        .email("email4")
        .name("name2")
        .phone("phone2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .name("name2")
    .url("url6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

