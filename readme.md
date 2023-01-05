# Buy domain name in Azure
App Service domains are custom domains that are managed directly in Azure.
* [Buy an App Service Domain & configure the Custom domain on App Service](https://learn.microsoft.com/en-us/azure/app-service/manage-custom-dns-buy-domain#buy-an-app-service-domain)

## Host your domain in Azure DNS
You can use Azure DNS to host your DNS domain and manage your DNS records. By hosting your domains in Azure, you can manage your DNS records by using the same credentials, APIs, tools, and billing as your other Azure services.
* [Host your domain in Azure DNS](https://learn.microsoft.com/en-us/azure/dns/dns-delegate-domain-azure-dns)
* [Verify the delegation](https://learn.microsoft.com/en-us/azure/dns/dns-delegate-domain-azure-dns#delegate-the-domain) - 
You may need to wait at least 10 minutes after you complete the delegation, before you can successfully verify that it's working. It can take a while for changes to propagate through the DNS system.
```bash
nslookup -type=SOA absazure1.com
```
> When you use the portal, the following things happen behind the scene to configure custom domain name:
>* A root "A" record pointing to your domain
> * A root "TXT" record for verification
> * A "CNAME" record for the www name that points to the A record
>
> [Create DNS records in a custom domain for a web app](https://learn.microsoft.com/en-us/azure/dns/dns-web-sites-custom-domain)

## FAQs on App Service Domain
[FAQ App Service Domain and Custom Domains](https://azure.github.io/AppService/2017/08/08/FAQ-App-Service-Domain-and-Custom-Domains.html)

## Use domain purchased in the Azure portal to point to an Azure VM or Storage
[Assign App Service domain to Azure VM or Azure Storage](https://azure.github.io/AppService/2017/07/31/Assign-App-Service-domain-to-Azure-VM-or-Azure-Storage)

## Azure DNS
Azure DNS is a hosting service for DNS domains that provides name resolution by using Microsoft Azure infrastructure. By hosting your domains in Azure, you can manage your DNS records by using the same credentials, APIs, tools, and billing as your other Azure services.

You can't use Azure DNS to buy a domain name. For an annual fee, you can buy a domain name by using App Service domains or a third-party domain name registrar. Your domains then can be hosted in Azure DNS for record management.
* [Azure DNS](https://learn.microsoft.com/en-us/azure/dns/dns-overview)
* [Create an Azure DNS zone and A record](https://learn.microsoft.com/en-us/azure/dns/dns-getstarted-portal)

## Release the domain purchased in Azure App Service Domain
* [Release domain in Azure App Service Domain](https://learn.microsoft.com/en-us/answers/questions/428697/azure-app-service-domain-release-domain.html)