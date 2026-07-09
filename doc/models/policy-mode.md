
# Policy Mode

Mode behavior: Monitor / Comment / Block / Disabled

| value | description |
|-------|---------------|
| MODE_MONITOR | Monitor mode, silently report findings |
| MODE_COMMENT | Comment mode, leaves PR comments but does not block |
| MODE_BLOCK | Block mode, leaves PR comments and blocks PR |
| MODE_DISABLED | Disabled mode, not active |

## Enumeration

`PolicyMode`

## Fields

| Name |
|  --- |
| `MODE_MONITOR` |
| `MODE_COMMENT` |
| `MODE_BLOCK` |
| `MODE_DISABLED` |

## Example

```java
import dev.semgrep.models.PolicyMode;

PolicyMode policyMode = PolicyMode.MODE_BLOCK;
```

