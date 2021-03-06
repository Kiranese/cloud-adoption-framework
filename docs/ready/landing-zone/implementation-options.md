---
title: Landing zone deployment options
description: Determine which landing zone deployment option best fits your requirements.
author: BrianBlanchard
ms.author: brblanch
ms.date: 06/15/2020
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: ready
---

# Landing zone implementation options

[Azure landing zones](./index.md) provide cloud adoption teams with a well-managed environment for their workloads. Follow the [landing zone design areas](./design-areas.md) guidance to take advantage of these capabilities.

Each implementation option below is designed for a specific set of operating model dependencies to support your nonfunctional requirements. Each implementation option includes distinct automation approaches. When available, reference architectures and reference implementations are included to accelerate your cloud adoption journey. While each option is mapped to a different operating model, they share the same design areas. The difference is how you choose to implement them.

## Platform development velocity

In addition to the recommended design areas, your platform development velocity (how fast your platform team can develop the required skills) is a key factor when choosing the best deployment option. Consider two primary modes:

**Start with enterprise scale:** When business requirements necessitate a rich initial implementation of landing zones, with fully integrated governance, security, and operations from the start, Microsoft recommends the enterprise-scale approach. With this approach, you can use either the Azure portal or infrastructure as code to set up and configure your environment. You can also transition between the portal and infrastructure as code (recommended) when your organization is ready. Infrastructure-as-code approaches require skills in Azure Resource Manager templates and GitHub.

**Start small and expand:** If it's more important to develop these skills and commit to your decisions as you learn more about the cloud, then consider a more modular approach. In this approach, the landing zones will only focus on implementing the basic landing zones considerations required to start cloud adoption. As adoption expands, modules in the Govern and Manage methodologies will build on top of your initial landing zones. The design principles of any Azure landing zone outline the specific design areas that will require refactoring over time.

## Implementation options

Some of the implementation options for landing zones and the variables that may drive the decision are shown below.

<!-- docsTest:ignore "CAF Enterprise-scale" "CAF Terraform" -->

| Implementation option | Description | Deployment velocity | Deeper design principles | Deployment instructions |
|---|---|---|---|---|---|---|---|
| [CAF Migration landing zone blueprint](./migrate-landing-zone.md) | Deploys the basic foundation for migrating low risk assets. | Start small | [Design principles](./migrate-landing-zone.md#design-principles) | [Deploy](./migrate-landing-zone.md) |
| [CAF Foundation blueprint](./foundation-blueprint.md) | Adds the minimum tools need to begin developing a governance strategy. | Start small | [Design principles](./foundation-blueprint.md#design-principles) | [Deploy](./foundation-blueprint.md) |
| [CAF Enterprise-scale landing zone](./enterprise-scale.md) | Deploys an enterprise-ready platform foundation with all the necessary shared services to support the full IT portfolio. | Enterprise-scale | [Design principles](../enterprise-scale/design-principles.md) | [Deploy](https://github.com/Azure/Enterprise-Scale/blob/main/docs/reference/contoso/Readme.md) |
| [CAF Terraform modules](./terraform-landing-zone.md) | Third-party path for multicloud operating models. This path can limit Azure-first operating models. | Start small | [Design principles](./terraform-landing-zone.md#design-decisions) | [Deploy](./terraform-landing-zone.md#customize-and-deploy-your-first-landing-zone) |

The following table looks at the same implementation options from a slightly different perspective to guide more technical decision processes.

| Implementation option | Hub | Spoke | Deployment technology | Deployment instructions |
|---|---|---|---|---|
| [CAF Enterprise-scale landing zone](./enterprise-scale.md) | Included  | Included | Azure Resource Manager templates, Azure portal, Azure Policy and GitHub | [Deploy](../enterprise-scale/implementation-guidelines.md) |
| [CAF Migration landing zone blueprint](./migrate-landing-zone.md) | Refactor required | Included | Azure Resource Manager templates, Azure portal, and Azure Blueprints | [Deploy](./migrate-landing-zone.md) |
| [CAF Terraform modules](./terraform-landing-zone.md)  | Included in virtual datacenter module | Included | Terraform | [Deploy](./terraform-landing-zone.md#customize-and-deploy-your-first-landing-zone) |

## Next steps

To proceed, choose one of the implementation options above. Each option includes a link to deployment instructions and the specific design principles that guide implementation.
