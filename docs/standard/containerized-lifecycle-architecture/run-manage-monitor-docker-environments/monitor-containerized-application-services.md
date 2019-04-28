---
title: Superviser des services d’application conteneurisée
description: Découvrez certains aspects essentiels de la surveillance des architectures de conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 4553a35c8db6cfc46187525ef2ffc65cb3ba07c9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61922744"
---
# <a name="monitor-containerized-application-services"></a><span data-ttu-id="3bdcf-103">Superviser des services d’application conteneurisée</span><span class="sxs-lookup"><span data-stu-id="3bdcf-103">Monitor containerized application services</span></span>

<span data-ttu-id="3bdcf-104">Il est essentiel pour les applications de fractionner en plusieurs conteneurs et microservices de disposer d’un moyen pour surveiller et analyser le comportement de l’application entière.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-104">It's critical for applications split into multiple containers and microservices to have a way to monitor and analyze the behavior of the whole application.</span></span>

## <a name="azure-monitor"></a><span data-ttu-id="3bdcf-105">Azure Monitor</span><span class="sxs-lookup"><span data-stu-id="3bdcf-105">Azure Monitor</span></span>

<span data-ttu-id="3bdcf-106">[Azure Monitor](https://azure.microsoft.com/services/monitor/) est un service analytique extensible qui surveille votre application en direct.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-106">[Azure Monitor](https://azure.microsoft.com/services/monitor/) is an extensible analytics service that monitors your live application.</span></span> <span data-ttu-id="3bdcf-107">Il vous aide à détecter et diagnostiquer les problèmes de performances et de comprendre ce que les utilisateurs font avec votre application.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-107">It helps you to detect and diagnose performance issues and to understand what users actually do with your app.</span></span> <span data-ttu-id="3bdcf-108">Il est conçu pour les développeurs, avec l’intention de vous aider à améliorer continuellement les performances et facilité d’utilisation de vos applications ou services.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-108">It's designed for developers, with the intent of helping you to continuously improve the performance and usability of your services or applications.</span></span> <span data-ttu-id="3bdcf-109">Azure Monitor fonctionne avec les services/web et autonome des applications sur un large éventail de plateformes telles que .NET, Java, Node.js et nombreuses autres plateformes, hébergées en local ou dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-109">Azure Monitor works with both web/services and standalone apps on a wide variety of platforms like .NET, Java, Node.js and many other platforms, hosted on-premises or in the cloud.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="3bdcf-110">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3bdcf-110">Additional resources</span></span>

- <span data-ttu-id="3bdcf-111">**Vue d’ensemble d’Azure Monitor** \\</span><span class="sxs-lookup"><span data-stu-id="3bdcf-111">**Overview of Azure Monitor** \\</span></span>
  <https://docs.microsoft.com/azure/azure-monitor/overview>

- <span data-ttu-id="3bdcf-112">**Présentation d’Application Insights**</span><span class="sxs-lookup"><span data-stu-id="3bdcf-112">**What is Application Insights?**</span></span> \
  <https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview>

- <span data-ttu-id="3bdcf-113">**Nouveautés des métriques Azure Monitor ?**</span><span class="sxs-lookup"><span data-stu-id="3bdcf-113">**What is Azure Monitor Metrics?**</span></span> \
  <https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-metrics>

- <span data-ttu-id="3bdcf-114">**Solution Container Monitoring dans Azure Monitor** \\</span><span class="sxs-lookup"><span data-stu-id="3bdcf-114">**Container Monitoring solution in Azure Monitor** \\</span></span>
  <https://docs.microsoft.com/azure/azure-monitor/insights/containers>

## <a name="security-and-backup-services"></a><span data-ttu-id="3bdcf-115">Services de sécurité et de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="3bdcf-115">Security and backup services</span></span>

<span data-ttu-id="3bdcf-116">Il existe de nombreuses tâches de prise en charge avec un grand nombre de détails que vous devez gérer pour garantir à que vos applications et votre infrastructure sont en état de haut de gamme pour prendre en charge les besoins de l’entreprise, et la situation devient plus complexe dans le domaine des microservices, donc un moyen ont des vues générales et détaillées lorsque vous avez besoin prendre des mesures.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-116">There are many support chores with lots of details that you have to handle to ensure your applications and infrastructure are in top notch condition to support business needs, and the situation becomes more complicated in the microservices realm, so you need a way to have both high-level and detailed views when you need to take action.</span></span>

<span data-ttu-id="3bdcf-117">Azure propose les outils nécessaires pour gérer et fournir une vue unifiée des quatre aspects critiques des ressources de votre cloud et en local :</span><span class="sxs-lookup"><span data-stu-id="3bdcf-117">Azure has the tools to manage and provide a unified view of four critical aspects of both your cloud and on-premises resources:</span></span>

- <span data-ttu-id="3bdcf-118">**Sécurité**.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-118">**Security**.</span></span> <span data-ttu-id="3bdcf-119">Avec [Azure Security Center](https://azure.microsoft.com/services/security-center/).</span><span class="sxs-lookup"><span data-stu-id="3bdcf-119">With [Azure Security Center](https://azure.microsoft.com/services/security-center/).</span></span>
  - <span data-ttu-id="3bdcf-120">Obtenir une visibilité complète et un contrôle accrus de la sécurité de vos machines virtuelles, les applications et les charges de travail.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-120">Get full visibility and control over the security of your virtual machines, apps, and workloads.</span></span>
  - <span data-ttu-id="3bdcf-121">Centraliser la gestion de vos stratégies de sécurité et d’intégrer des outils et processus existants.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-121">Centralize the management of your security policies and integrate existing processes and tools.</span></span>
  - <span data-ttu-id="3bdcf-122">Détecter les menaces réelles avec analytique avancée.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-122">Detect real threats with advanced analytics.</span></span>

- <span data-ttu-id="3bdcf-123">**Sauvegarde**.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-123">**Backup**.</span></span> <span data-ttu-id="3bdcf-124">Avec [sauvegarde Azure](https://azure.microsoft.com/services/backup/).</span><span class="sxs-lookup"><span data-stu-id="3bdcf-124">With [Azure Backup](https://azure.microsoft.com/services/backup/).</span></span>
  - <span data-ttu-id="3bdcf-125">Éviter les interruptions de l’entreprise, répondre aux objectifs de conformité et protégez vos données contre les ransomware et les erreurs humaines.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-125">Avoid costly business disruptions, meet compliance goals, and protect your data against ransomware and human errors.</span></span>
  - <span data-ttu-id="3bdcf-126">Gardez vos données de sauvegarde chiffrées en transit et au repos.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-126">Keep your backup data encrypted in transit and at rest.</span></span>
  - <span data-ttu-id="3bdcf-127">Garantir l’accès en fonction de l’authentification multifacteur pour empêcher toute utilisation non autorisée.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-127">Ensure access based on multifactor authentication to prevent unauthorized use.</span></span>

- <span data-ttu-id="3bdcf-128">**Ressources locales**.</span><span class="sxs-lookup"><span data-stu-id="3bdcf-128">**On-premises resources**.</span></span> <span data-ttu-id="3bdcf-129">Avec [un cloud hybride réellement cohérent](https://azure.microsoft.com/resources/truly-consistent-hybrid-cloud-with-microsoft-azure/).</span><span class="sxs-lookup"><span data-stu-id="3bdcf-129">With [a truly consistent hybrid cloud](https://azure.microsoft.com/resources/truly-consistent-hybrid-cloud-with-microsoft-azure/).</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="3bdcf-130">[Précédent](manage-production-docker-environments.md)
>[Suivant](../key-takeaways/index.md)</span><span class="sxs-lookup"><span data-stu-id="3bdcf-130">[Previous](manage-production-docker-environments.md)
[Next](../key-takeaways/index.md)</span></span>
