# Choosing

:::note Auditing

In this document the following auditing rules are covered:

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-PERF-026-v1
</code>
<br></br>
Static websites should be deployed to a static hosting service such as Azure Static Web Apps.

<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-PERF-027-v1
</code>
<br></br>
Virtual machines like Droplets should be used only when there is no other option.

<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-PERF-028-v1
</code>
<br></br>
High traffic static websites should be deployed to a CDN.

<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-PERF-029-v1
</code>
<br></br>
High traffic web services should be deployed to a serverless service such as Azure App Service or Kubernetes for non-serverless services.

<br></br>
<br></br>

Check out all the rules in the [Auditor Rules](/auditing/rules) section.
:::

Even if deploying is the last step in the development process, it is one of the most important steps. What good is a project if it is not available to users?

We can split most projects into the following categories:

- **Web services**: These are services that are accessed via a web browser. Examples include server side rendering websites, and web APIs.
- **Static websites**: These are websites that are not generated dynamically. They are usually written in HTML, CSS, and JavaScript.
- **Workers**: These are services that run in the background and are not directly accessed by users. Examples include cron jobs, and background workers.
- **Packages**: These are libraries that are used by other projects. Examples include npm packages, net core nuget packages, etc.

## Recommended Resources

### Azure App Service

This is a fully managed web hosting service for building web apps, mobile back ends, and RESTful APIs.
It supports a number of languages and frameworks including .NET, .NET Core, Node.js, Java, PHP, Ruby, and Python. 
It also supports Docker containers.

:::success PROS
- Continuous deployment: It supports continuous deployment using GitHub, Bitbucket, or Azure DevOps.
- Custom domains: It's very easy to set up custom domains.
- SSL certificates: Adding SSL certificates is very easy and free for any domain.
- Automatic scaling: Simple scaling is supported, not recommended for cases of quick and high spikes in traffic.
:::

:::caution CONS
- Static websites: Azure App Service is not a good choice for hosting static websites. Even if it's possible by setting the App type to be ASP.NET Core, it's not recommended.
- Containers: Azure App Service is not the ideal choice for hosting containers since deployment is usually very slow and buggy.
:::


### Azure Container Instances

This is a serverless container hosting service that lets you run containers on Azure without having to manage the underlying infrastructure.
Main benefit of this resource is you can set the exact amount of memory and CPU you need and you are charged by the hour.

:::success PROS
- Customize computing resources: You can set the exact amount of memory and CPU you need.
- Quick deployments: You can deploy a container in a couple of minutes.
:::

:::caution CONS
- Price: Container Instances are quite expensive compared to other resources.
- Container Registry: You should consider that using this resource means having your container hosted somewhere such as Azure Container Registry or Docker Hub which will add to the cost.
:::

### Azure Kubernetes Service

This is a managed Kubernetes service that lets you deploy and manage containerized applications without having to manage the underlying infrastructure.

:::success Good for
- Projects which serious scaling requirements.
- Projects which require to run as a container.
:::

:::caution Bad
Azure Kubernetes Service is not the cheapest or easiest solution to use.
:::

### Digital Ocean Droplets

This is a fully managed virtual machine that lets you run any application on it. They are well known for their simplicity and ease of use and their low price. You can find Dropplets for as low as $5 per month.

:::success PROS
- Custom environments: You can install any software you want on the Droplet. You can also install Docker and run containers on it. Even if the Droplet is restarted, the software will still be there.
- Low cost: Droplets are very cheap. You can find Droplets for as low as $5 per month.
:::

:::caution CONS
- Difficult Deployment: Digital Ocean Droplets are not the best choice for projects which require frequent deployments.
- Backup: Backups have to be done manually.
- Replicate: Creating a Dropplet with the same code and environment as another is not easy since changes are not tracked.
- Databases: Avoid completely hosting databases on Droplets, instead use a managed database services, even if they are more expensive.
:::

### Azure Static Web Apps

This is a static web hosting service that lets you host static websites and serverless APIs with zero configuration.

:::success PROS
- Static websites: Azure Static Web Apps is the best choice for hosting static websites.
- Custom domains: It's very easy to set up custom domains.
- SSL certificates: Adding SSL certificates is very easy and free for any domain.
- Cost: Azure Static Web Apps is free for up to 100GB of bandwidth per month.
:::

:::caution CONS
- CDN: For high traffic websites, you should consider using a CDN.
:::


