
# OAuth 2 Bearer token



Documentation for accessing and setting credentials for SemgrepAdminJWT.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| AccessToken | `String` | The OAuth 2.0 Access Token to use for API requests. | `accessToken` | `getAccessToken()` |



**Note:** Auth credentials can be set using `semgrepAdminJwtCredentials` in the client builder and accessed through `getSemgrepAdminJwtCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```java
import dev.semgrep.SemgrepWebAppClient;
import dev.semgrep.authentication.SemgrepAdminJwtModel;

public class Program {
    public static void main(String[] args) {
        SemgrepWebAppClient client = new SemgrepWebAppClient.Builder()
            .semgrepAdminJwtCredentials(new SemgrepAdminJwtModel.Builder(
                    "AccessToken"
                )
                .build())
            .build();
    }
}
```


