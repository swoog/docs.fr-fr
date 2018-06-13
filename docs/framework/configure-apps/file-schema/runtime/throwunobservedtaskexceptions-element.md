---
title: '&lt;ThrowUnobservedTaskExceptions&gt; élément'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ThrowUnobservedTaskExceptions element
- <ThrowUnobservedTaskExceptions> element
ms.assetid: cea7e588-8b8d-48d2-9ad5-8feaf3642c18
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3f72bedbaaf0b15ade7ff6b7b8c3edcdfd3fda6d
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32749424"
---
# <a name="ltthrowunobservedtaskexceptionsgt-element"></a><span data-ttu-id="c7245-102">&lt;ThrowUnobservedTaskExceptions&gt; élément</span><span class="sxs-lookup"><span data-stu-id="c7245-102">&lt;ThrowUnobservedTaskExceptions&gt; Element</span></span>
<span data-ttu-id="c7245-103">Indique si les exceptions de tâches non gérées doivent arrêter un processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c7245-103">Specifies whether unhandled task exceptions should terminate a running process.</span></span>  
  
 <span data-ttu-id="c7245-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="c7245-104">\<configuration></span></span>  
<span data-ttu-id="c7245-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="c7245-105">\<runtime></span></span>  
<span data-ttu-id="c7245-106">\<ThrowUnobservedTaskExceptions ></span><span class="sxs-lookup"><span data-stu-id="c7245-106">\<ThrowUnobservedTaskExceptions></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7245-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7245-107">Syntax</span></span>  
  
```xml  
<ThrowUnobservedTaskExceptions  
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c7245-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c7245-108">Attributes and Elements</span></span>  
 <span data-ttu-id="c7245-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c7245-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c7245-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="c7245-110">Attributes</span></span>  
  
|<span data-ttu-id="c7245-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="c7245-111">Attribute</span></span>|<span data-ttu-id="c7245-112">Description</span><span class="sxs-lookup"><span data-stu-id="c7245-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="c7245-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="c7245-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="c7245-114">Spécifie si les exceptions de tâche non gérée doivent s’arrêter le processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c7245-114">Specifies whether unhandled task exceptions should terminate the running process.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="c7245-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="c7245-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="c7245-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7245-116">Value</span></span>|<span data-ttu-id="c7245-117">Description</span><span class="sxs-lookup"><span data-stu-id="c7245-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="c7245-118">N’arrête pas le processus en cours d’exécution pour une exception de tâche non gérée.</span><span class="sxs-lookup"><span data-stu-id="c7245-118">Does not terminate the running process for an unhandled task exception.</span></span> <span data-ttu-id="c7245-119">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c7245-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="c7245-120">Termine le processus en cours d’exécution pour une exception de tâche non gérée.</span><span class="sxs-lookup"><span data-stu-id="c7245-120">Terminates the running process for an unhandled task exception.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c7245-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c7245-121">Child Elements</span></span>  
 <span data-ttu-id="c7245-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c7245-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c7245-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c7245-123">Parent Elements</span></span>  
  
|<span data-ttu-id="c7245-124">Élément</span><span class="sxs-lookup"><span data-stu-id="c7245-124">Element</span></span>|<span data-ttu-id="c7245-125">Description</span><span class="sxs-lookup"><span data-stu-id="c7245-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="c7245-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c7245-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="c7245-127">Contient des informations sur les options d'initialisation du runtime.</span><span class="sxs-lookup"><span data-stu-id="c7245-127">Contains information about runtime initialization options.</span></span>|  
|||  
  
## <a name="remarks"></a><span data-ttu-id="c7245-128">Notes</span><span class="sxs-lookup"><span data-stu-id="c7245-128">Remarks</span></span>  
 <span data-ttu-id="c7245-129">Si une exception qui est associée à un <xref:System.Threading.Tasks.Task> n’a pas été respectées, il est sans <xref:System.Threading.Tasks.Task.Wait%2A> opération, le parent n’est pas attachée et le <xref:System.Threading.Tasks.Task.Exception%2A?displayProperty=nameWithType> propriété n’a pas lu à l’exception de la tâche est considérée comme défaillante.</span><span class="sxs-lookup"><span data-stu-id="c7245-129">If an exception that is associated with a <xref:System.Threading.Tasks.Task> has not been observed, there is no <xref:System.Threading.Tasks.Task.Wait%2A> operation, the parent is not attached, and the <xref:System.Threading.Tasks.Task.Exception%2A?displayProperty=nameWithType> property was not read the task exception is considered to be unobserved.</span></span>  
  
 <span data-ttu-id="c7245-130">Dans le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], par défaut, si un <xref:System.Threading.Tasks.Task> qui a un défaillante exception est le garbage collector, le finaliseur lève une exception et met fin au processus.</span><span class="sxs-lookup"><span data-stu-id="c7245-130">In the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], by default, if a <xref:System.Threading.Tasks.Task> that has an unobserved exception is garbage collected, the finalizer throws an exception and terminates the process.</span></span> <span data-ttu-id="c7245-131">L’arrêt du processus est déterminée par la durée du garbage collection et la finalisation.</span><span class="sxs-lookup"><span data-stu-id="c7245-131">The termination of the process is determined by the timing of garbage collection and finalization.</span></span>  
  
 <span data-ttu-id="c7245-132">Pour le rendre plus facile pour les développeurs d’écrire du code asynchrone basé sur les tâches, les [!INCLUDE[net_v45](../../../../../includes/net-v45-md.md)] modifie ce comportement par défaut pour les exceptions non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c7245-132">To make it easier for developers to write asynchronous code based on tasks, the [!INCLUDE[net_v45](../../../../../includes/net-v45-md.md)] changes this default behavior for unobserved exceptions.</span></span> <span data-ttu-id="c7245-133">Non prises en charge les exceptions d’entraînent toujours le <xref:System.Threading.Tasks.TaskScheduler.UnobservedTaskException> événement soit déclenché, mais par défaut, le processus s’arrête.</span><span class="sxs-lookup"><span data-stu-id="c7245-133">Unobserved exceptions still cause the <xref:System.Threading.Tasks.TaskScheduler.UnobservedTaskException> event to be raised, but by default, the process does not terminate.</span></span> <span data-ttu-id="c7245-134">Au lieu de cela, l’exception est ignorée une fois que l’événement est déclenché, indépendamment de si un gestionnaire d’événements observe l’exception.</span><span class="sxs-lookup"><span data-stu-id="c7245-134">Instead, the exception is ignored after the event is raised, regardless of whether an event handler observes the exception.</span></span>  
  
 <span data-ttu-id="c7245-135">Dans le [!INCLUDE[net_v45](../../../../../includes/net-v45-md.md)], vous pouvez utiliser la [ \<ThrowUnobservedTaskExceptions > élément](../../../../../docs/framework/configure-apps/file-schema/runtime/throwunobservedtaskexceptions-element.md) dans un fichier de configuration d’application pour activer la [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] comportement de lever une exception.</span><span class="sxs-lookup"><span data-stu-id="c7245-135">In the [!INCLUDE[net_v45](../../../../../includes/net-v45-md.md)], you can use the [\<ThrowUnobservedTaskExceptions> element](../../../../../docs/framework/configure-apps/file-schema/runtime/throwunobservedtaskexceptions-element.md) in an application configuration file to enable the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] behavior of throwing an exception.</span></span>  
  
 <span data-ttu-id="c7245-136">Vous pouvez également spécifier le comportement d’exception dans une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7245-136">You can also specify the exception behavior in one of the following ways:</span></span>  
  
-   <span data-ttu-id="c7245-137">En définissant la variable d’environnement `COMPlus_ThrowUnobservedTaskExceptions` (`set COMPlus_ThrowUnobservedTaskExceptions=1`).</span><span class="sxs-lookup"><span data-stu-id="c7245-137">By setting the environment variable `COMPlus_ThrowUnobservedTaskExceptions` (`set COMPlus_ThrowUnobservedTaskExceptions=1`).</span></span>  
  
-   <span data-ttu-id="c7245-138">En définissant le Registre DWORD value ThrowUnobservedTaskExceptions = 1 dans le HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\\. NETFramework clé.</span><span class="sxs-lookup"><span data-stu-id="c7245-138">By setting the registry DWORD value ThrowUnobservedTaskExceptions = 1 in the HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\\.NETFramework key.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c7245-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="c7245-139">Example</span></span>  
 <span data-ttu-id="c7245-140">L’exemple suivant montre comment activer la levée d’exceptions dans les tâches à l’aide d’un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="c7245-140">The following example shows how to enable the throwing of exceptions in tasks by using an application configuration file.</span></span>  
  
```xml  
<configuration>   
    <runtime>   
        <ThrowUnobservedTaskExceptions enabled="true"/>   
    </runtime>   
</configuration>  
```  
  
## <a name="example"></a><span data-ttu-id="c7245-141">Exemple</span><span class="sxs-lookup"><span data-stu-id="c7245-141">Example</span></span>  
 <span data-ttu-id="c7245-142">L’exemple suivant montre comment une propagation de l’exception est levée à partir d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="c7245-142">The following example demonstrates how an unobserved exception is thrown from a task.</span></span> <span data-ttu-id="c7245-143">Le code doit être exécuté comme un programme lancé fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="c7245-143">The code must be run as a released program to work correctly.</span></span>  
  
 [!code-csharp[ThrowUnobservedTaskExceptions#1](../../../../../samples/snippets/csharp/VS_Snippets_CLR/throwunobservedtaskexceptions/cs/program.cs#1)]
 [!code-vb[ThrowUnobservedTaskExceptions#1](../../../../../samples/snippets/visualbasic/VS_Snippets_CLR/throwunobservedtaskexceptions/vb/program.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="c7245-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7245-144">See Also</span></span>  
 [<span data-ttu-id="c7245-145">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="c7245-145">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="c7245-146">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="c7245-146">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
