
# Product Type

Product type the Policy applies to.

| value | description |
|-------|---------------|
| PRODUCT_TYPE_SAST | The product type for Code rules. |
| PRODUCT_TYPE_SECRETS | The product type for Secrets rules. |

## Enumeration

`ProductType`

## Fields

| Name |
|  --- |
| `PRODUCT_TYPE_SAST` |
| `PRODUCT_TYPE_SECRETS` |

## Example

```java
import dev.semgrep.models.ProductType;

ProductType productType = ProductType.PRODUCT_TYPE_SAST;
```

