
# Protos Sca V1 Sbom Metadata Contact

*This model accepts additional fields of type Object.*

## Structure

`ProtosScaV1SbomMetadataContact`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Email` | `String` | Optional | - | String getEmail() | setEmail(String email) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Phone` | `String` | Optional | - | String getPhone() | setPhone(String phone) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosScaV1SbomMetadataContact;
import java.io.IOException;

ProtosScaV1SbomMetadataContact protosScaV1SbomMetadataContact = new ProtosScaV1SbomMetadataContact.Builder()
    .email("email0")
    .name("name6")
    .phone("phone6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

