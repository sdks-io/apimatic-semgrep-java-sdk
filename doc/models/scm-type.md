
# Scm Type

Provider for the finding (e.g. GitHub, GitLab, GHE, etc).

| value | description |
|-------|---------------|
| SCM_TYPE_GITHUB | GitHub Cloud |
| SCM_TYPE_GITHUB_ENTERPRISE | GitHub Enterprise |
| SCM_TYPE_GITLAB | GitLab Cloud |
| SCM_TYPE_GITLAB_SELFMANAGED | GitLab Self-Managed |
| SCM_TYPE_BITBUCKET | Bitbucket Cloud |
| SCM_TYPE_BITBUCKET_DATACENTER | Bitbucket Data Center |
| SCM_TYPE_AZURE_DEVOPS | Azure DevOps |
| SCM_TYPE_UNKNOWN |  |
| SCM_TYPE_HARNESS | Harness |

## Enumeration

`ScmType`

## Fields

| Name |
|  --- |
| `SCM_TYPE_GITHUB` |
| `SCM_TYPE_GITHUB_ENTERPRISE` |
| `SCM_TYPE_GITLAB` |
| `SCM_TYPE_GITLAB_SELFMANAGED` |
| `SCM_TYPE_BITBUCKET` |
| `SCM_TYPE_BITBUCKET_DATACENTER` |
| `SCM_TYPE_AZURE_DEVOPS` |
| `SCM_TYPE_UNKNOWN` |
| `SCM_TYPE_HARNESS` |

## Example

```java
import dev.semgrep.models.ScmType;

ScmType scmType = ScmType.SCM_TYPE_GITHUB_ENTERPRISE;
```

