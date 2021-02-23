# API Security Workshop

## Multi Tenancy 

Red Hat 3scale API Management allows multiple independent instances of 3scale accounts to exist on a single on-premises deployment. Accounts operate independently from one another, and cannot share information among themselves.

https://access.redhat.com/documentation/en-us/red_hat_3scale_api_management/2.9/html-single/admin_portal_guide/index#multitenancy

* Access the **Master Tenant**:

![Multi Tenancy - Master tenant](images/multi-tenancy/01-master-tenant.png)

* Access the **Audience** option from the top menu:

![Multi Tenancy - Master Tenant Audience](images/multi-tenancy/02-access-audience.png)

### Create a tenant using the Console Web

* Click in the button **Create** in order to create a new account

![Multi Tenancy - Master Tenant Accounts](images/multi-tenancy/03-accounts.png)

* Fill the form with the new tenant information

![Multi Tenancy - Master Tenant - New Accounts](images/multi-tenancy/04-new-account.png)

* Look at the new admin-portal and developer portal link generated at this step. 

![Multi Tenancy - Master Tenant - Account Created](images/multi-tenancy/05-account-created.png)

* Before to access this link we need to approve the new User created.

![Multi Tenancy - Master Tenant - Users approval](images/multi-tenancy/06-users-approval.png)

* Access the **Admin portal** and log in with the credentials that you provided on the form before.

![Multi Tenancy - Login Admin Portal](images/multi-tenancy/07-login-admin-portal.png)

* Look that you have a new brand admin portal with everything fresh

![Multi Tenancy - Logged in Admin Portal](images/multi-tenancy/08-logged-in-admin-portal.png)

* Access the developer portal option from the side menu, it's a fresh developer portal.

![Multi Tenancy - Developer Portal](images/multi-tenancy/09-developer-portal.png)

### Create a tenant using the Tenant CRD

https://github.com/3scale/3scale-operator/blob/master/doc/tenant-reference.md
https://access.redhat.com/documentation/en-us/red_hat_3scale_api_management/2.8/html/operating_3scale/provision-threescale-services-via-operator#deploying-optional-tenants-custom-resource

* You can create a tenant using the CRD

```
oc create -f support/ecorp-admin-secret.yaml
oc create -f support/tenant-crd.yaml
```

![Multi Tenancy - Tenant using the Operator](images/multi-tenancy/10-tenant-using-operator.png)
