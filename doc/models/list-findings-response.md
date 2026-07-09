
# List Findings Response

Response containing a paginated list of findings (either Code or Supply Chain findings) with optional filtering applied

*This model accepts additional fields of type Object.*

## Structure

`ListFindingsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AiSastFindings` | [`AiSastFindings`](../../doc/models/ai-sast-findings.md) | Optional | A list of AI-powered scan findings that Semgrep has identified in your organization | AiSastFindings getAiSastFindings() | setAiSastFindings(AiSastFindings aiSastFindings) |
| `SastFindings` | [`SastFindings`](../../doc/models/sast-findings.md) | Optional | A list of Code findings that Semgrep has identified in your organization | SastFindings getSastFindings() | setSastFindings(SastFindings sastFindings) |
| `ScaFindings` | [`ScaFindings`](../../doc/models/sca-findings.md) | Optional | A list of Supply Chain findings that Semgrep has identified in your organization | ScaFindings getScaFindings() | setScaFindings(ScaFindings scaFindings) |
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
import dev.semgrep.models.EpssScore;
import dev.semgrep.models.ExternalTicket;
import dev.semgrep.models.Guidance;
import dev.semgrep.models.ListFindingsResponse;
import dev.semgrep.models.Risk;
import dev.semgrep.models.RuleExplanation;
import dev.semgrep.models.SastFinding;
import dev.semgrep.models.SastFindings;
import dev.semgrep.models.ScaFinding;
import dev.semgrep.models.ScaFindings;
import dev.semgrep.models.Verdict1;
import java.io.IOException;
import java.util.Arrays;

ListFindingsResponse listFindingsResponse = new ListFindingsResponse.Builder()
    .aiSastFindings(new AiSastFindings.Builder()
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
        .build())
    .sastFindings(new SastFindings.Builder()
        .findings(Arrays.asList(
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
                    "categories4",
                    "categories3"
                ))
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
                    "categories4",
                    "categories3"
                ))
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
        .build())
    .scaFindings(new ScaFindings.Builder()
        .findings(Arrays.asList(
            new ScaFinding.Builder()
                .categories(Arrays.asList(
                    "categories4",
                    "categories3"
                ))
                .confidence(Confidence1.LOW)
                .createdAt("created_at6")
                .epssScore(new EpssScore.Builder()
                    .percentile(236.52D)
                    .score(242.58D)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .externalTicket(new ExternalTicket.Builder()
                    .externalSlug("external_slug4")
                    .id(228L)
                    .linkedIssueIds(Arrays.asList(
                        115L,
                        116L,
                        117L
                    ))
                    .url("url8")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new ScaFinding.Builder()
                .categories(Arrays.asList(
                    "categories4",
                    "categories3"
                ))
                .confidence(Confidence1.LOW)
                .createdAt("created_at6")
                .epssScore(new EpssScore.Builder()
                    .percentile(236.52D)
                    .score(242.58D)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .externalTicket(new ExternalTicket.Builder()
                    .externalSlug("external_slug4")
                    .id(228L)
                    .linkedIssueIds(Arrays.asList(
                        115L,
                        116L,
                        117L
                    ))
                    .url("url8")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new ScaFinding.Builder()
                .categories(Arrays.asList(
                    "categories4",
                    "categories3"
                ))
                .confidence(Confidence1.LOW)
                .createdAt("created_at6")
                .epssScore(new EpssScore.Builder()
                    .percentile(236.52D)
                    .score(242.58D)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .externalTicket(new ExternalTicket.Builder()
                    .externalSlug("external_slug4")
                    .id(228L)
                    .linkedIssueIds(Arrays.asList(
                        115L,
                        116L,
                        117L
                    ))
                    .url("url8")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

