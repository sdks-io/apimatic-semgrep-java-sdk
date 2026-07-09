
# Protos Openapi V1 Get Bootstrap Sms Vpc Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1GetBootstrapSmsVpcResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AwsTemplateFormatVersion` | `String` | Optional | The AWSTemplateFormatVersion that the template conforms to | String getAwsTemplateFormatVersion() | setAwsTemplateFormatVersion(String awsTemplateFormatVersion) |
| `Description` | `String` | Optional | Template description | String getDescription() | setDescription(String description) |
| `Metadata` | `Object` | Optional | Template metadata including version and last updated date | Object getMetadata() | setMetadata(Object metadata) |
| `Outputs` | `Object` | Optional | Output values of the stack | Object getOutputs() | setOutputs(Object outputs) |
| `Parameters` | `Object` | Optional | Template parameters | Object getParameters() | setParameters(Object parameters) |
| `Resources` | `Object` | Optional | Declaration of AWS resources | Object getResources() | setResources(Object resources) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1GetBootstrapSmsVpcResponse;
import java.io.IOException;

ProtosOpenapiV1GetBootstrapSmsVpcResponse protosOpenapiV1GetBootstrapSmsVpcResponse = new ProtosOpenapiV1GetBootstrapSmsVpcResponse.Builder()
    .awsTemplateFormatVersion("AWSTemplateFormatVersion0")
    .description("Description8")
    .metadata(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .outputs(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .parameters(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

