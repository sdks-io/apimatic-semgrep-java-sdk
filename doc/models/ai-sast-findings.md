
# Ai Sast Findings

A list of AI-powered scan findings that Semgrep has identified in your organization

*This model accepts additional fields of type Object.*

## Structure

`AiSastFindings`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Findings` | [`List<AiPoweredScanFinding>`](../../doc/models/ai-powered-scan-finding.md) | Optional | A list of AI-powered scan findings. | List<AiPoweredScanFinding> getFindings() | setFindings(List<AiPoweredScanFinding> findings) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.AiPoweredScanFinding;
import dev.semgrep.models.AiSastFindings;
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
import dev.semgrep.models.Verdict1;
import java.io.IOException;
import java.util.Arrays;

AiSastFindings aiSastFindings = new AiSastFindings.Builder()
    .findings(Arrays.asList(
        new AiPoweredScanFinding.Builder()
            .aiImpact("ai_impact2")
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
            .clickToFixFailures(Arrays.asList(
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
                    .build()
            ))
            .confidence(Confidence1.LOW)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new AiPoweredScanFinding.Builder()
            .aiImpact("ai_impact2")
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
            .clickToFixFailures(Arrays.asList(
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
                    .build()
            ))
            .confidence(Confidence1.LOW)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new AiPoweredScanFinding.Builder()
            .aiImpact("ai_impact2")
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
            .clickToFixFailures(Arrays.asList(
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
                    .build()
            ))
            .confidence(Confidence1.LOW)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

