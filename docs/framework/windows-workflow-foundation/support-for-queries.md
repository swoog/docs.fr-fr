---
title: Prise en charge des requêtes
ms.date: 03/30/2017
ms.assetid: 093c22f5-3294-4642-857a-5252233d6796
ms.openlocfilehash: 30695fcd791a0d69c31a897068d69838c80c3957
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61641513"
---
# <a name="support-for-queries"></a><span data-ttu-id="90f4d-102">Prise en charge des requêtes</span><span class="sxs-lookup"><span data-stu-id="90f4d-102">Support for Queries</span></span>
<span data-ttu-id="90f4d-103">Le magasin d'instances de workflow SQL enregistre un jeu de propriétés connues dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="90f4d-103">The SQL Workflow Instance Store records a set of well-known properties in the store.</span></span> <span data-ttu-id="90f4d-104">Les utilisateurs peuvent demander des instances à partir de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="90f4d-104">Users can query for instances based on these properties.</span></span> <span data-ttu-id="90f4d-105">La liste suivante comprend quelques-unes de ces propriétés connues :</span><span class="sxs-lookup"><span data-stu-id="90f4d-105">The following list contains some of these well-known properties:</span></span>  
  
- <span data-ttu-id="90f4d-106">**Nom du site.**</span><span class="sxs-lookup"><span data-stu-id="90f4d-106">**Site Name.**</span></span> <span data-ttu-id="90f4d-107">Nom du site Web qui contient le service.</span><span class="sxs-lookup"><span data-stu-id="90f4d-107">Name of the Web site that contains the service.</span></span>  
  
- <span data-ttu-id="90f4d-108">**Chemin d’accès de l’Application relatif.**</span><span class="sxs-lookup"><span data-stu-id="90f4d-108">**Relative Application Path.**</span></span> <span data-ttu-id="90f4d-109">Chemin d’accès à l’application relatif au site Web.</span><span class="sxs-lookup"><span data-stu-id="90f4d-109">Path of the application relative to the Web site.</span></span>  
  
- <span data-ttu-id="90f4d-110">**Chemin d’accès relatif de Service.**</span><span class="sxs-lookup"><span data-stu-id="90f4d-110">**Relative Service Path.**</span></span> <span data-ttu-id="90f4d-111">Chemin d’accès au service relatif à l’application.</span><span class="sxs-lookup"><span data-stu-id="90f4d-111">Path of the service relative to the application.</span></span>  
  
- <span data-ttu-id="90f4d-112">**Nom du service.**</span><span class="sxs-lookup"><span data-stu-id="90f4d-112">**Service Name.**</span></span> <span data-ttu-id="90f4d-113">Nom du service.</span><span class="sxs-lookup"><span data-stu-id="90f4d-113">Name of the service.</span></span>  
  
- <span data-ttu-id="90f4d-114">**Service Namespace.**</span><span class="sxs-lookup"><span data-stu-id="90f4d-114">**Service Namespace.**</span></span> <span data-ttu-id="90f4d-115">Nom de l'espace de noms que le service utilise.</span><span class="sxs-lookup"><span data-stu-id="90f4d-115">Name of the namespace that the service uses.</span></span>  
  
- <span data-ttu-id="90f4d-116">**Ordinateur actuel.**</span><span class="sxs-lookup"><span data-stu-id="90f4d-116">**Current Machine.**</span></span>  
  
- <span data-ttu-id="90f4d-117">**Dernier ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="90f4d-117">**Last Machine**.</span></span> <span data-ttu-id="90f4d-118">Ordinateur sur lequel l'instance de service de workflow a été exécutée la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="90f4d-118">The computer on which the workflow service instance ran the last time.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="90f4d-119">Pour les scénarios auto-hébergés à l'aide de l'hôte du service de workflow, seules les quatre dernières propriétés sont remplies.</span><span class="sxs-lookup"><span data-stu-id="90f4d-119">For self-hosted scenarios using Workflow Service Host, only the last four properties are populated.</span></span> <span data-ttu-id="90f4d-120">Pour les scénarios d'application de workflow, seule la dernière propriété est remplie.</span><span class="sxs-lookup"><span data-stu-id="90f4d-120">For Workflow Application scenarios, only the last property is populated.</span></span>  
  
 <span data-ttu-id="90f4d-121">Le runtime du workflow fournit des valeurs pour les trois premières propriétés.</span><span class="sxs-lookup"><span data-stu-id="90f4d-121">The workflow runtime supplies values for the first three properties.</span></span> <span data-ttu-id="90f4d-122">L’hôte de service de workflow fournit la valeur pour le **raison de l’interruption** propriété.</span><span class="sxs-lookup"><span data-stu-id="90f4d-122">The workflow service host supplies the value for the **Suspend Reason** property.</span></span> <span data-ttu-id="90f4d-123">Le Store d’Instance de Workflow SQL lui-même fournit des valeurs pour le **dernier ordinateur mis à jour** propriété.</span><span class="sxs-lookup"><span data-stu-id="90f4d-123">The SQL Workflow Instance Store itself supplies values for the **Last Updated Machine** property.</span></span>  
  
 <span data-ttu-id="90f4d-124">La fonctionnalité de magasin d'instances de workflow SQL vous permet également de spécifier les propriétés personnalisées pour lesquelles vous souhaitez stocker les valeurs dans la base de données de persistance et que vous souhaitez utiliser dans les requêtes.</span><span class="sxs-lookup"><span data-stu-id="90f4d-124">The SQL Workflow Instance Store feature also lets you specify the custom properties for which you want to store the values in the persistence database and that you want to use in queries.</span></span> <span data-ttu-id="90f4d-125">Pour plus d’informations sur les promotions personnalisées, consultez [Store extensibilité](store-extensibility.md).</span><span class="sxs-lookup"><span data-stu-id="90f4d-125">For more information about custom promotions, see [Store Extensibility](store-extensibility.md).</span></span>  
  
## <a name="views"></a><span data-ttu-id="90f4d-126">Affichages</span><span class="sxs-lookup"><span data-stu-id="90f4d-126">Views</span></span>  
 <span data-ttu-id="90f4d-127">Le magasin d'instances contient les vues suivantes.</span><span class="sxs-lookup"><span data-stu-id="90f4d-127">The instance store contains the following views.</span></span> <span data-ttu-id="90f4d-128">Consultez [schéma de base de données de persistance](persistence-database-schema.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="90f4d-128">See [Persistence Database Schema](persistence-database-schema.md) for further details.</span></span>  
  
### <a name="the-instances-view"></a><span data-ttu-id="90f4d-129">Vue Instances</span><span class="sxs-lookup"><span data-stu-id="90f4d-129">The Instances View</span></span>  
 <span data-ttu-id="90f4d-130">La vue Instances contient les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="90f4d-130">The Instances view contains the following fields:</span></span>  
  
1. <span data-ttu-id="90f4d-131">**Id**</span><span class="sxs-lookup"><span data-stu-id="90f4d-131">**Id**</span></span>  
  
2. <span data-ttu-id="90f4d-132">**PendingTimer**</span><span class="sxs-lookup"><span data-stu-id="90f4d-132">**PendingTimer**</span></span>  
  
3. <span data-ttu-id="90f4d-133">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="90f4d-133">**CreationTime**</span></span>  
  
4. <span data-ttu-id="90f4d-134">**LastUpdatedTime**</span><span class="sxs-lookup"><span data-stu-id="90f4d-134">**LastUpdatedTime**</span></span>  
  
5. <span data-ttu-id="90f4d-135">**ServiceDeploymentId**</span><span class="sxs-lookup"><span data-stu-id="90f4d-135">**ServiceDeploymentId**</span></span>  
  
6. <span data-ttu-id="90f4d-136">**SuspensionExceptionName**</span><span class="sxs-lookup"><span data-stu-id="90f4d-136">**SuspensionExceptionName**</span></span>  
  
7. <span data-ttu-id="90f4d-137">**SuspensionReason**</span><span class="sxs-lookup"><span data-stu-id="90f4d-137">**SuspensionReason**</span></span>  
  
8. <span data-ttu-id="90f4d-138">**ActiveBookmarks**</span><span class="sxs-lookup"><span data-stu-id="90f4d-138">**ActiveBookmarks**</span></span>  
  
9. <span data-ttu-id="90f4d-139">**CurrentMachine**</span><span class="sxs-lookup"><span data-stu-id="90f4d-139">**CurrentMachine**</span></span>  
  
10. <span data-ttu-id="90f4d-140">**LastMachine**</span><span class="sxs-lookup"><span data-stu-id="90f4d-140">**LastMachine**</span></span>  
  
11. <span data-ttu-id="90f4d-141">**ExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="90f4d-141">**ExecutionStatus**</span></span>  
  
12. <span data-ttu-id="90f4d-142">**IsInitialized**</span><span class="sxs-lookup"><span data-stu-id="90f4d-142">**IsInitialized**</span></span>  
  
13. <span data-ttu-id="90f4d-143">**IsSuspended**</span><span class="sxs-lookup"><span data-stu-id="90f4d-143">**IsSuspended**</span></span>  
  
14. <span data-ttu-id="90f4d-144">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="90f4d-144">**IsCompleted**</span></span>  
  
15. <span data-ttu-id="90f4d-145">**EncodingOption**</span><span class="sxs-lookup"><span data-stu-id="90f4d-145">**EncodingOption**</span></span>  
  
16. <span data-ttu-id="90f4d-146">**ReadWritePrimitiveDataProperties**</span><span class="sxs-lookup"><span data-stu-id="90f4d-146">**ReadWritePrimitiveDataProperties**</span></span>  
  
17. <span data-ttu-id="90f4d-147">**WriteOnlyPrimitiveDataProperties**</span><span class="sxs-lookup"><span data-stu-id="90f4d-147">**WriteOnlyPrimitiveDataProperties**</span></span>  
  
18. <span data-ttu-id="90f4d-148">**ReadWriteComplexDataProperties**</span><span class="sxs-lookup"><span data-stu-id="90f4d-148">**ReadWriteComplexDataProperties**</span></span>  
  
19. <span data-ttu-id="90f4d-149">**WriteOnlyComplexDataProperties**</span><span class="sxs-lookup"><span data-stu-id="90f4d-149">**WriteOnlyComplexDataProperties**</span></span>  
  
### <a name="the-servicedeployments-view"></a><span data-ttu-id="90f4d-150">Vue ServiceDeployments</span><span class="sxs-lookup"><span data-stu-id="90f4d-150">The ServiceDeployments view</span></span>  
 <span data-ttu-id="90f4d-151">La vue ServiceDeployments contient les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="90f4d-151">The ServiceDeployments view contains the following fields:</span></span>  
  
1. <span data-ttu-id="90f4d-152">**SiteName**</span><span class="sxs-lookup"><span data-stu-id="90f4d-152">**SiteName**</span></span>  
  
2. <span data-ttu-id="90f4d-153">**RelativeServicePath**</span><span class="sxs-lookup"><span data-stu-id="90f4d-153">**RelativeServicePath**</span></span>  
  
3. <span data-ttu-id="90f4d-154">**RelativeApplicationPath**</span><span class="sxs-lookup"><span data-stu-id="90f4d-154">**RelativeApplicationPath**</span></span>  
  
4. <span data-ttu-id="90f4d-155">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="90f4d-155">**ServiceName**</span></span>  
  
5. <span data-ttu-id="90f4d-156">**ServiceNamespace**</span><span class="sxs-lookup"><span data-stu-id="90f4d-156">**ServiceNamespace**</span></span>  
  
### <a name="the-instancepromotedproperties-view"></a><span data-ttu-id="90f4d-157">Vue InstancePromotedProperties</span><span class="sxs-lookup"><span data-stu-id="90f4d-157">The InstancePromotedProperties view</span></span>  
 <span data-ttu-id="90f4d-158">La vue InstancePromotedProperties contient les champs suivants.</span><span class="sxs-lookup"><span data-stu-id="90f4d-158">The InstancePromotedProperties view contains the following fields.</span></span> <span data-ttu-id="90f4d-159">Pour plus d’informations sur les propriétés promues, consultez le [Store extensibilité](store-extensibility.md) rubrique.</span><span class="sxs-lookup"><span data-stu-id="90f4d-159">For details on promoted properties, see the [Store Extensibility](store-extensibility.md) topic.</span></span>  
  
1. <span data-ttu-id="90f4d-160">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="90f4d-160">**InstanceId**</span></span>  
  
2. <span data-ttu-id="90f4d-161">**EncodingOption**</span><span class="sxs-lookup"><span data-stu-id="90f4d-161">**EncodingOption**</span></span>  
  
3. <span data-ttu-id="90f4d-162">**PromotionName**</span><span class="sxs-lookup"><span data-stu-id="90f4d-162">**PromotionName**</span></span>  
  
4. <span data-ttu-id="90f4d-163">**Valeur #** (une plage de champs à partir de **Value1** à **Value64**).</span><span class="sxs-lookup"><span data-stu-id="90f4d-163">**Value#** (a range of fields from **Value1** to **Value64**).</span></span>
