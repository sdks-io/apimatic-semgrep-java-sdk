
# Policy

*This model accepts additional fields of type Object.*

## Structure

`Policy`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | ID of the Policy. | String getId() | setId(String id) |
| `IsDefault` | `Boolean` | Optional | When True, the Policy applies to all repositories. | Boolean getIsDefault() | setIsDefault(Boolean isDefault) |
| `Name` | `String` | Optional | Name of the Policy. | String getName() | setName(String name) |
| `ProductType` | [`ProductType`](../../doc/models/product-type.md) | Optional | Product type the Policy applies to.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| PRODUCT_TYPE_SAST \| The product type for Code rules. \|<br>\| PRODUCT_TYPE_SECRETS \| The product type for Secrets rules. \| | ProductType getProductType() | setProductType(ProductType productType) |
| `Slug` | `String` | Optional | Sanitized machine-readable name of the Policy. | String getSlug() | setSlug(String slug) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Policy;
import dev.semgrep.models.ProductType;
import java.io.IOException;

Policy policy = new Policy.Builder()
    .id("1")
    .isDefault(true)
    .name("Global Policy")
    .productType(ProductType.PRODUCT_TYPE_SAST)
    .slug("global_policy")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

