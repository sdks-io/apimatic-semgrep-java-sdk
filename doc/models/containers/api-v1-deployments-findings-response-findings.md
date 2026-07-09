
# Api V1 Deployments Findings Response Findings

## Class Name

`ApiV1DeploymentsFindingsResponseFindings`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`SastFinding`](../../../doc/models/sast-finding.md) | ApiV1DeploymentsFindingsResponseFindings.fromSastFinding(SastFinding sastFinding) |
| [`ScaFinding`](../../../doc/models/sca-finding.md) | ApiV1DeploymentsFindingsResponseFindings.fromScaFinding(ScaFinding scaFinding) |
| [`AiPoweredScanFinding`](../../../doc/models/ai-powered-scan-finding.md) | ApiV1DeploymentsFindingsResponseFindings.fromAiPoweredScanFinding(AiPoweredScanFinding aiPoweredScanFinding) |

## SastFinding

### Initialization Code

#### Example

```java
ApiV1DeploymentsFindingsResponseFindings.fromSastFinding(
        new SastFinding.Builder()
            .categories(Arrays.asList(
                "security"
            ))
            .confidence(Confidence1.MEDIUM)
            .createdAt("2020-11-18 23:28:12.391807+00:00")
            .firstSeenScanId(1234L)
            .id(1234567L)
            .lineOfCodeUrl("https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1")
            .matchBasedId("0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1")
            .ref("refs/pull/1234/merge")
            .relevantSince("2020-11-18 23:28:12.391807+00:00")
            .ruleName("typescript.react.security.audit.react-no-refs.react-no-refs")
            .severity(Severity1.MEDIUM)
            .state(State.UNRESOLVED)
            .stateUpdatedAt("2020-11-19 23:28:12.391807+00:00")
            .status(Status.OPEN)
            .syntacticId("440eeface888e78afceac3dc7d4cc2cf")
            .triageComment("This finding is from the test repo")
            .triageReason(TriageReason.ACCEPTABLE_RISK)
            .triageState(TriageState.UNTRIAGED)
            .triagedAt("2020-11-19 23:28:12.391807+00:00")
            .build()
    )
```

## ScaFinding

### Initialization Code

#### Example

```java
ApiV1DeploymentsFindingsResponseFindings.fromScaFinding(
        new ScaFinding.Builder()
            .categories(Arrays.asList(
                "security"
            ))
            .confidence(Confidence1.MEDIUM)
            .createdAt("2020-11-18 23:28:12.391807+00:00")
            .firstSeenScanId(1234L)
            .id(1234567L)
            .isMalicious(true)
            .lineOfCodeUrl("https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1")
            .matchBasedId("0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1")
            .reachability(Reachability.REACHABLE)
            .reachableCondition("you use the package on a host running Linux or MacOS")
            .ref("refs/pull/1234/merge")
            .relevantSince("2020-11-18 23:28:12.391807+00:00")
            .ruleName("typescript.react.security.audit.react-no-refs.react-no-refs")
            .severity(Severity1.MEDIUM)
            .state(State.UNRESOLVED)
            .stateUpdatedAt("2020-11-19 23:28:12.391807+00:00")
            .status(Status.OPEN)
            .syntacticId("440eeface888e78afceac3dc7d4cc2cf")
            .triageComment("This finding is from the test repo")
            .triageReason(TriageReason.ACCEPTABLE_RISK)
            .triageState(TriageState.UNTRIAGED)
            .triagedAt("2020-11-19 23:28:12.391807+00:00")
            .vulnerabilityIdentifier("CVE-2021-24112")
            .build()
    )
```

## AiPoweredScanFinding

### Initialization Code

#### Example

```java
ApiV1DeploymentsFindingsResponseFindings.fromAiPoweredScanFinding(
        new AiPoweredScanFinding.Builder()
            .aiImpact("An attacker could access or modify other users' data by manipulating the resource identifier in the request")
            .confidence(Confidence1.MEDIUM)
            .createdAt("2020-11-18 23:28:12.391807+00:00")
            .firstSeenScanId(1234L)
            .id(1234567L)
            .lineOfCodeUrl("https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1")
            .matchBasedId("0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1")
            .ref("refs/pull/1234/merge")
            .relevantSince("2020-11-18 23:28:12.391807+00:00")
            .ruleName("ai.detection.idor")
            .severity(Severity1.HIGH)
            .state(State.UNRESOLVED)
            .stateUpdatedAt("2020-11-19 23:28:12.391807+00:00")
            .status(Status.OPEN)
            .syntacticId("440eeface888e78afceac3dc7d4cc2cf")
            .triageComment("This finding is from the test repo")
            .triageReason(TriageReason.ACCEPTABLE_RISK)
            .triageState(TriageState.UNTRIAGED)
            .triagedAt("2020-11-19 23:28:12.391807+00:00")
            .build()
    )
```

