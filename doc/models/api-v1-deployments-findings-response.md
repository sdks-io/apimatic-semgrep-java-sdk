
# Api V1 Deployments Findings Response

*This model accepts additional fields of type Object.*

## Structure

`ApiV1DeploymentsFindingsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Findings` | [`List<ApiV1DeploymentsFindingsResponseFindings>`](../../doc/models/containers/api-v1-deployments-findings-response-findings.md) | Optional | This is List of a container for one-of cases. | List<ApiV1DeploymentsFindingsResponseFindings> getFindings() | setFindings(List<ApiV1DeploymentsFindingsResponseFindings> findings) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ApiV1DeploymentsFindingsResponse;
import dev.semgrep.models.Assistant;
import dev.semgrep.models.Autofix;
import dev.semgrep.models.Autotriage;
import dev.semgrep.models.ClickToFixFailure;
import dev.semgrep.models.ClickToFixPr;
import dev.semgrep.models.Component;
import dev.semgrep.models.Confidence1;
import dev.semgrep.models.Guidance;
import dev.semgrep.models.Risk;
import dev.semgrep.models.RuleExplanation;
import dev.semgrep.models.SastFinding;
import dev.semgrep.models.Verdict1;
import dev.semgrep.models.containers.ApiV1DeploymentsFindingsResponseFindings;
import java.io.IOException;
import java.util.Arrays;

ApiV1DeploymentsFindingsResponse apiV1DeploymentsFindingsResponse = new ApiV1DeploymentsFindingsResponse.Builder()
    .findings(Arrays.asList(
        ApiV1DeploymentsFindingsResponseFindings.fromSastFinding(
            new SastFinding.Builder()
                .assistant(new Assistant.Builder()
                    .autofix(new Autofix.Builder()
                        .explanation("explanation2")
                        .fixCode("fix_code4")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .autotriage(new Autotriage.Builder()
                        .reason("reason2")
                        .verdict(Verdict1.FALSE_POSITIVE)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .component(new Component.Builder()
                        .risk(Risk.HIGH)
                        .tag("tag8")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .guidance(new Guidance.Builder()
                        .instructions("instructions4")
                        .summary("summary8")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .ruleExplanation(new RuleExplanation.Builder()
                        .explanation("explanation8")
                        .summary("summary4")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .categories(Arrays.asList(
                    "categories4"
                ))
                .clickToFixFailures(Arrays.asList(
                    new ClickToFixFailure.Builder()
                        .createdAt("created_at8")
                        .reason("reason0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixFailure.Builder()
                        .createdAt("created_at8")
                        .reason("reason0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixFailure.Builder()
                        .createdAt("created_at8")
                        .reason("reason0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
                .clickToFixPrs(Arrays.asList(
                    new ClickToFixPr.Builder()
                        .createdAt("created_at4")
                        .url("url0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixPr.Builder()
                        .createdAt("created_at4")
                        .url("url0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixPr.Builder()
                        .createdAt("created_at4")
                        .url("url0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
                .confidence(Confidence1.HIGH)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ),
        ApiV1DeploymentsFindingsResponseFindings.fromSastFinding(
            new SastFinding.Builder()
                .assistant(new Assistant.Builder()
                    .autofix(new Autofix.Builder()
                        .explanation("explanation2")
                        .fixCode("fix_code4")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .autotriage(new Autotriage.Builder()
                        .reason("reason2")
                        .verdict(Verdict1.FALSE_POSITIVE)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .component(new Component.Builder()
                        .risk(Risk.HIGH)
                        .tag("tag8")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .guidance(new Guidance.Builder()
                        .instructions("instructions4")
                        .summary("summary8")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .ruleExplanation(new RuleExplanation.Builder()
                        .explanation("explanation8")
                        .summary("summary4")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .categories(Arrays.asList(
                    "categories4"
                ))
                .clickToFixFailures(Arrays.asList(
                    new ClickToFixFailure.Builder()
                        .createdAt("created_at8")
                        .reason("reason0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixFailure.Builder()
                        .createdAt("created_at8")
                        .reason("reason0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixFailure.Builder()
                        .createdAt("created_at8")
                        .reason("reason0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
                .clickToFixPrs(Arrays.asList(
                    new ClickToFixPr.Builder()
                        .createdAt("created_at4")
                        .url("url0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixPr.Builder()
                        .createdAt("created_at4")
                        .url("url0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixPr.Builder()
                        .createdAt("created_at4")
                        .url("url0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
                .confidence(Confidence1.HIGH)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ),
        ApiV1DeploymentsFindingsResponseFindings.fromSastFinding(
            new SastFinding.Builder()
                .assistant(new Assistant.Builder()
                    .autofix(new Autofix.Builder()
                        .explanation("explanation2")
                        .fixCode("fix_code4")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .autotriage(new Autotriage.Builder()
                        .reason("reason2")
                        .verdict(Verdict1.FALSE_POSITIVE)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .component(new Component.Builder()
                        .risk(Risk.HIGH)
                        .tag("tag8")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .guidance(new Guidance.Builder()
                        .instructions("instructions4")
                        .summary("summary8")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                    .ruleExplanation(new RuleExplanation.Builder()
                        .explanation("explanation8")
                        .summary("summary4")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .categories(Arrays.asList(
                    "categories4"
                ))
                .clickToFixFailures(Arrays.asList(
                    new ClickToFixFailure.Builder()
                        .createdAt("created_at8")
                        .reason("reason0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixFailure.Builder()
                        .createdAt("created_at8")
                        .reason("reason0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixFailure.Builder()
                        .createdAt("created_at8")
                        .reason("reason0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
                .clickToFixPrs(Arrays.asList(
                    new ClickToFixPr.Builder()
                        .createdAt("created_at4")
                        .url("url0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixPr.Builder()
                        .createdAt("created_at4")
                        .url("url0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new ClickToFixPr.Builder()
                        .createdAt("created_at4")
                        .url("url0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
                .confidence(Confidence1.HIGH)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        )
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

