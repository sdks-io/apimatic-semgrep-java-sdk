
# Update Policy Request

*This model accepts additional fields of type Object.*

## Structure

`UpdatePolicyRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeploymentId` | `String` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. | String getDeploymentId() | setDeploymentId(String deploymentId) |
| `PolicyId` | `String` | Required | Policy ID (numeric). Example: `456`. Can be found at `/deployments/{deploymentId}/policies`. | String getPolicyId() | setPolicyId(String policyId) |
| `PolicyMode` | [`PolicyMode3`](../../doc/models/policy-mode-3.md) | Required | New policy mode to set for the Rule.<br><br>- MODE_MONITOR: Monitor mode, silently report findings<br>- MODE_COMMENT: Comment mode, leaves PR comments but does not block<br>- MODE_BLOCK: Block mode, leaves PR comments and blocks PR<br>- MODE_DISABLED: Disabled mode, not active<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| MODE_MONITOR \| Monitor mode, silently report findings \|<br>\| MODE_COMMENT \| Comment mode, leaves PR comments but does not block \|<br>\| MODE_BLOCK \| Block mode, leaves PR comments and blocks PR \|<br>\| MODE_DISABLED \| Disabled mode, not active \| | PolicyMode3 getPolicyMode() | setPolicyMode(PolicyMode3 policyMode) |
| `RulePath` | `String` | Required | Full path of the Rule. | String getRulePath() | setRulePath(String rulePath) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.PolicyMode3;
import dev.semgrep.models.UpdatePolicyRequest;
import java.io.IOException;

UpdatePolicyRequest updatePolicyRequest = new UpdatePolicyRequest.Builder(
    "123",
    "456",
    PolicyMode3.MODE_MONITOR,
    "rulePath2"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

