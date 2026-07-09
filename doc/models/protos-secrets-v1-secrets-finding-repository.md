
# Protos Secrets V1 Secrets Finding Repository

Repository where the finding was detected.

*This model accepts additional fields of type Object.*

## Structure

`ProtosSecretsV1SecretsFindingRepository`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | Repository name | String getName() | setName(String name) |
| `ScmType` | [`ScmType`](../../doc/models/scm-type.md) | Optional | Provider for the finding (e.g. GitHub, GitLab, GHE, etc).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SCM_TYPE_GITHUB \| GitHub Cloud \|<br>\| SCM_TYPE_GITHUB_ENTERPRISE \| GitHub Enterprise \|<br>\| SCM_TYPE_GITLAB \| GitLab Cloud \|<br>\| SCM_TYPE_GITLAB_SELFMANAGED \| GitLab Self-Managed \|<br>\| SCM_TYPE_BITBUCKET \| Bitbucket Cloud \|<br>\| SCM_TYPE_BITBUCKET_DATACENTER \| Bitbucket Data Center \|<br>\| SCM_TYPE_AZURE_DEVOPS \| Azure DevOps \|<br>\| SCM_TYPE_UNKNOWN \|  \|<br>\| SCM_TYPE_HARNESS \| Harness \| | ScmType getScmType() | setScmType(ScmType scmType) |
| `Url` | `String` | Optional | URL to the repository where the finding was detected. | String getUrl() | setUrl(String url) |
| `Visibility` | [`Visibility`](../../doc/models/visibility.md) | Optional | Repository visbility (e.g. public, private, unknown).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| REPOSITORY_VISIBILITY_PUBLIC \|  \|<br>\| REPOSITORY_VISIBILITY_PRIVATE \|  \|<br>\| REPOSITORY_VISIBILITY_UNKNOWN \|  \| | Visibility getVisibility() | setVisibility(Visibility visibility) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosSecretsV1SecretsFindingRepository;
import dev.semgrep.models.ScmType;
import dev.semgrep.models.Visibility;
import java.io.IOException;

ProtosSecretsV1SecretsFindingRepository protosSecretsV1SecretsFindingRepository = new ProtosSecretsV1SecretsFindingRepository.Builder()
    .name("name4")
    .scmType(ScmType.SCM_TYPE_BITBUCKET_DATACENTER)
    .url("url8")
    .visibility(Visibility.REPOSITORY_VISIBILITY_PRIVATE)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

