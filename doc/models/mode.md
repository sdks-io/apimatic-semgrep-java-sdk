
# Mode

The behavior of the finding reporting: Monitor / Comment / Block.

| value | description |
|-------|---------------|
| MODE_MONITOR | Monitor mode, silently report findings |
| MODE_COMMENT | Comment mode, leaves PR comments but does not block |
| MODE_BLOCK | Block mode, leaves PR comments and blocks PR |
| MODE_DISABLED | Disabled mode, not active |

## Enumeration

`Mode`

## Fields

| Name |
|  --- |
| `MODE_MONITOR` |
| `MODE_COMMENT` |
| `MODE_BLOCK` |
| `MODE_DISABLED` |

## Example

```java
import dev.semgrep.models.Mode;

Mode mode = Mode.MODE_BLOCK;
```

