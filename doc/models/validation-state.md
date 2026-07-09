
# Validation State

Filter by whether a secret could be validated. Only applies for secrets findings.

## Enumeration

`ValidationState`

## Fields

| Name |
|  --- |
| `CONFIRMED_VALID` |
| `CONFIRMED_INVALID` |
| `VALIDATION_ERROR` |
| `NO_VALIDATOR` |

## Example

```java
import dev.semgrep.models.ValidationState;

ValidationState validationState = ValidationState.VALIDATION_ERROR;
```

