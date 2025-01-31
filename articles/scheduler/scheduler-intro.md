---
title: What is Azure Scheduler?
description: Create schedule, and run automated jobs that call services inside or outside Azure.
services: scheduler
ms.service: scheduler
ms.suite: infrastructure-services
author: ecfan
ms.author: estfan
ms.reviewer: deli, azla
ms.topic: conceptual
ms.date: 02/15/2022
---

# What is Azure Scheduler?

> [!IMPORTANT]
> [Azure Logic Apps](../logic-apps/logic-apps-overview.md) has replaced Azure Scheduler, which is fully retired 
> since January 31, 2022. Please migrate your Azure Scheduler jobs by recreating them as workflows in Azure Logic Apps 
> following the steps in [Migrate Azure Scheduler jobs to Azure Logic Apps](migrate-from-scheduler-to-logic-apps.md). 
> Azure Scheduler is longer available in the Azure portal. The [Azure Scheduler REST API](/rest/api/scheduler) and 
> [Azure Scheduler PowerShell cmdlets](scheduler-powershell-reference.md) no longer work.

[Azure Scheduler](https://azure.microsoft.com/services/scheduler/) helps you create [jobs](../scheduler/scheduler-concepts-terms.md) that run in the cloud by declaratively describing actions. The service then automatically schedules and runs those actions. For example, you can call services inside and outside Azure, such as calling HTTP or HTTPS endpoints, and also post messages to Azure Storage queues and Azure Service Bus queues or topics. You can run jobs immediately or at a later time. Scheduler easily supports [complex schedules and advanced recurrence](../scheduler/scheduler-advanced-complexity.md). Scheduler specifies when to run jobs, keeps a history of job results that you can review, and then predictably and reliably schedules workloads to run.

Other Azure scheduling capabilities also use Scheduler in the background, for example, [Azure WebJobs](../app-service/webjobs-create.md), which is a [Web Apps](https://azure.microsoft.com/services/app-service/web/) feature in Azure App Service. You can manage communication for these actions by using the [Scheduler REST API](/rest/api/scheduler/), which helps you manage the communication for these actions.

Here are some scenarios where Scheduler can help you:

* Run recurring app actions: For example, periodically collect data from Twitter into a feed.

* Perform daily maintenance: Such as pruning logs daily, performing backups, and other maintenance tasks.

  For example, as an administrator, you might want to back up your database at 1:00 AM every day for the next nine months.

Although you can use Scheduler to create, maintain, and run scheduled workloads, Scheduler doesn't host the workloads or run code. The service only *invokes* the services or code hosted elsewhere, for example, in Azure, on-premises, or with another provider. Scheduler can invoke through HTTP, HTTPS, a Storage queue, a Service Bus queue, or a Service Bus topic.

To create, schedule, manage, update, or delete jobs and [job collections](../scheduler/scheduler-concepts-terms.md), you can use code, the [Scheduler REST API](/rest/api/scheduler/), or the [Azure Scheduler PowerShell cmdlets](scheduler-powershell-reference.md).

## Next steps

* [Azure Scheduler concepts, terminology, and entity hierarchy](scheduler-concepts-terms.md)
* [Plans and billing for Azure Scheduler](scheduler-plans-billing.md)
* [Build complex schedules and advanced recurrence with Azure Scheduler](scheduler-advanced-complexity.md)
* [Azure Scheduler REST API reference](/rest/api/scheduler)
* [Azure Scheduler PowerShell cmdlets reference](scheduler-powershell-reference.md)