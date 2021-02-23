## Toolbox

- https://access.redhat.com/documentation/en-us/red_hat_3scale_api_management/2.9/html/operating_3scale/api-lifecyle-toolbox-3scale
- https://github.com/3scale/3scale_toolbox
- https://github.com/rh-integration/3scale-toolbox-jenkins

### Install 

- [Install Official Doc](https://access.redhat.com/documentation/en-us/red_hat_3scale_api_management/2.9/html-single/operating_3scale/index#installing-the-toolbox)

https://<provider_key>|<access_token>@<3scale-instance-domain>

```
3scale remote add rhpds "https://e3f32fcb730753ca722b855c793065c5@3scale-admin.apps.cluster-8cb5.8cb5.example.opentlc.com/"
```

### Importing API from an OpenAPI Specification

```
3scale import openapi support/banks-api.json --default-credentials-userkey 123 -d rhpds
```