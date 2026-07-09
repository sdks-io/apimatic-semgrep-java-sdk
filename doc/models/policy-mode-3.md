
# Policy Mode 3

New policy mode to set for the Rule.

- MODE_MONITOR: Monitor mode, silently report findings
- MODE_COMMENT: Comment mode, leaves PR comments but does not block
- MODE_BLOCK: Block mode, leaves PR comments and blocks PR
- MODE_DISABLED: Disabled mode, not active

| value | description |
|-------|---------------|
| MODE_MONITOR | Monitor mode, silently report findings |
| MODE_COMMENT | Comment mode, leaves PR comments but does not block |
| MODE_BLOCK | Block mode, leaves PR comments and blocks PR |
| MODE_DISABLED | Disabled mode, not active |

## Enumeration

`PolicyMode3`

## Fields

| Name |
|  --- |
| `MODE_MONITOR` |
| `MODE_COMMENT` |
| `MODE_BLOCK` |
| `MODE_DISABLED` |

## Example

```java
import dev.semgrep.models.PolicyMode3;

PolicyMode3 policyMode3 = PolicyMode3.MODE_BLOCK;
```

