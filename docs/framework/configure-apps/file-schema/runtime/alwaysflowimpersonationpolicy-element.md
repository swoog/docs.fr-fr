---
title: <alwaysFlowImpersonationPolicy> Élément
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/alwaysFlowImpersonationPolicy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#alwaysFlowImpersonationPolicy
helpviewer_keywords:
- alwaysFlowImpersonationPolicy element
- <alwaysFlowImpersonationPolicy> element
ms.assetid: ee622801-9e46-470b-85ab-88c4b1dd2ee1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce1928254699f4de41e92087c76be9bc3c249523
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59108041"
---
# <a name="alwaysflowimpersonationpolicy-element"></a><span data-ttu-id="617db-102">\<alwaysFlowImpersonationPolicy > élément</span><span class="sxs-lookup"><span data-stu-id="617db-102">\<alwaysFlowImpersonationPolicy> Element</span></span>
<span data-ttu-id="617db-103">Spécifie que l’identité Windows est toujours transmise entre des points asynchrones, indépendamment du mode d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="617db-103">Specifies that the Windows identity always flows across asynchronous points, regardless of how impersonation was performed.</span></span>  
  
 <span data-ttu-id="617db-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="617db-104">\<configuration></span></span>  
<span data-ttu-id="617db-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="617db-105">\<runtime></span></span>  
<span data-ttu-id="617db-106">\<alwaysFlowImpersonationPolicy></span><span class="sxs-lookup"><span data-stu-id="617db-106">\<alwaysFlowImpersonationPolicy></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="617db-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="617db-107">Syntax</span></span>  
  
```xml  
<alwaysFlowImpersonationPolicy    
  enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="617db-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="617db-108">Attributes and Elements</span></span>  
 <span data-ttu-id="617db-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="617db-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="617db-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="617db-110">Attributes</span></span>  
  
|<span data-ttu-id="617db-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="617db-111">Attribute</span></span>|<span data-ttu-id="617db-112">Description</span><span class="sxs-lookup"><span data-stu-id="617db-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="617db-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="617db-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="617db-114">Indique si l’identité Windows est transmise entre des points asynchrones.</span><span class="sxs-lookup"><span data-stu-id="617db-114">Indicates whether the Windows identity flows across asynchronous points.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="617db-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="617db-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="617db-116">Value</span><span class="sxs-lookup"><span data-stu-id="617db-116">Value</span></span>|<span data-ttu-id="617db-117">Description</span><span class="sxs-lookup"><span data-stu-id="617db-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="617db-118">L’identité n’est pas transmise entre des points asynchrones, à moins que l’emprunt d’identité est effectuée par le biais de Windows telles que les méthodes managées <xref:System.Security.Principal.WindowsIdentity.Impersonate%2A>.</span><span class="sxs-lookup"><span data-stu-id="617db-118">The Windows identity does not flow across asynchronous points, unless the impersonation is performed through managed methods such as <xref:System.Security.Principal.WindowsIdentity.Impersonate%2A>.</span></span> <span data-ttu-id="617db-119">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="617db-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="617db-120">L’identité Windows est toujours transmise entre des points asynchrones, indépendamment du mode d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="617db-120">The Windows identity always flows across asynchronous points, regardless of how impersonation was performed.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="617db-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="617db-121">Child Elements</span></span>  
 <span data-ttu-id="617db-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="617db-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="617db-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="617db-123">Parent Elements</span></span>  
  
|<span data-ttu-id="617db-124">Élément</span><span class="sxs-lookup"><span data-stu-id="617db-124">Element</span></span>|<span data-ttu-id="617db-125">Description</span><span class="sxs-lookup"><span data-stu-id="617db-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="617db-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="617db-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="617db-127">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="617db-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="617db-128">Notes</span><span class="sxs-lookup"><span data-stu-id="617db-128">Remarks</span></span>  
 <span data-ttu-id="617db-129">Dans les versions 1.0 et 1.1 du .NET Framework, l’identité de Windows n’est pas transmise entre des points asynchrones.</span><span class="sxs-lookup"><span data-stu-id="617db-129">In the .NET Framework versions 1.0 and 1.1, the Windows identity does not flow across asynchronous points.</span></span> <span data-ttu-id="617db-130">Dans le .NET Framework version 2.0, il existe un <xref:System.Threading.ExecutionContext> objet qui contient des informations sur le thread en cours d’exécution et les transmet entre des points asynchrones au sein d’un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="617db-130">In the .NET Framework version 2.0, there is an <xref:System.Threading.ExecutionContext> object that contains information about the currently executing thread, and flows it across asynchronous points within an application domain.</span></span> <span data-ttu-id="617db-131">Le <xref:System.Security.Principal.WindowsIdentity> également flux en tant que partie des informations qui circulent entre des points asynchrones, fournie par l’emprunt d’identité a été obtenue à l’aide de méthodes managées telles que <xref:System.Security.Principal.WindowsIdentity.Impersonate%2A> et non par le biais d’autres moyens, tels que platform invoke vers des méthodes natives.</span><span class="sxs-lookup"><span data-stu-id="617db-131">The <xref:System.Security.Principal.WindowsIdentity> also flows as part of the information that flows across the asynchronous points, provided the impersonation was achieved using managed methods such as <xref:System.Security.Principal.WindowsIdentity.Impersonate%2A> and not through other means such as platform invoke to native methods.</span></span> <span data-ttu-id="617db-132">Cet élément est utilisé pour spécifier que l’identité Windows est transmise entre des points asynchrones, indépendamment de la manière dont l’emprunt d’identité a été atteint.</span><span class="sxs-lookup"><span data-stu-id="617db-132">This element is used to specify that the Windows identity does flow across asynchronous points, regardless of how the impersonation was achieved.</span></span>  
  
 <span data-ttu-id="617db-133">Vous pouvez modifier ce comportement par défaut de deux manières :</span><span class="sxs-lookup"><span data-stu-id="617db-133">You can alter this default behavior in two other ways:</span></span>  
  
1.  <span data-ttu-id="617db-134">Dans le code managé sur un thread par thread.</span><span class="sxs-lookup"><span data-stu-id="617db-134">In managed code on a per-thread basis.</span></span>  
  
     <span data-ttu-id="617db-135">Vous pouvez supprimer le flux sur un thread par thread en modifiant le <xref:System.Threading.ExecutionContext> et <xref:System.Security.SecurityContext> paramètres à l’aide de la <xref:System.Threading.ExecutionContext.SuppressFlow%2A?displayProperty=nameWithType>, <xref:System.Security.SecurityContext.SuppressFlowWindowsIdentity%2A?displayProperty=nameWithType>, ou <xref:System.Security.SecurityContext.SuppressFlow%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="617db-135">You can suppress the flow on a per-thread basis by modifying the <xref:System.Threading.ExecutionContext> and <xref:System.Security.SecurityContext> settings by using the <xref:System.Threading.ExecutionContext.SuppressFlow%2A?displayProperty=nameWithType>, <xref:System.Security.SecurityContext.SuppressFlowWindowsIdentity%2A?displayProperty=nameWithType>, or <xref:System.Security.SecurityContext.SuppressFlow%2A?displayProperty=nameWithType> method.</span></span>  
  
2.  <span data-ttu-id="617db-136">Dans l’appel à l’interface d’hébergement non managée pour charger le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="617db-136">In the call to the unmanaged hosting interface to load the common language runtime (CLR).</span></span>  
  
     <span data-ttu-id="617db-137">Si une interface d’hébergement non managée (au lieu d’un simple fichier exécutable managé) est utilisée pour charger le CLR, vous pouvez spécifier un indicateur spécial dans l’appel à la [fonction CorBindToRuntimeEx](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="617db-137">If an unmanaged hosting interface (instead of a simple managed executable) is used to load the CLR, you can specify a special flag in the call to the [CorBindToRuntimeEx Function](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) function.</span></span> <span data-ttu-id="617db-138">Pour activer le mode de compatibilité pour l’ensemble du processus, définissez la `flags` paramètre pour [fonction CorBindToRuntimeEx](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) à `STARTUP_ALWAYSFLOW_IMPERSONATION`.</span><span class="sxs-lookup"><span data-stu-id="617db-138">To enable the compatibility mode for the entire process, set the `flags` parameter for [CorBindToRuntimeEx Function](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) to `STARTUP_ALWAYSFLOW_IMPERSONATION`.</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="617db-139">Fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="617db-139">Configuration File</span></span>  
 <span data-ttu-id="617db-140">Dans une application .NET Framework, cet élément peut être utilisé uniquement dans le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="617db-140">In a .NET Framework application, this element can be used only in the application configuration file.</span></span>  
  
 <span data-ttu-id="617db-141">Pour une application ASP.NET, le flux de l’emprunt d’identité peut être configuré dans le fichier aspnet.config dans le \<Windows dossier > \Microsoft.NET\Framework\vx.x.xxxx directory.</span><span class="sxs-lookup"><span data-stu-id="617db-141">For an ASP.NET application, the impersonation flow can be configured in the aspnet.config file found in the \<Windows Folder>\Microsoft.NET\Framework\vx.x.xxxx directory.</span></span>  
  
 <span data-ttu-id="617db-142">ASP.NET par défaut désactive le flux de l’emprunt d’identité dans le fichier aspnet.config à l’aide des paramètres de configuration suivants :</span><span class="sxs-lookup"><span data-stu-id="617db-142">ASP.NET by default disables the impersonation flow in the aspnet.config file by using the following configuration settings:</span></span>  
  
```xml
<configuration>  
   <runtime>  
      <legacyImpersonationPolicy enabled="true"/>  
      <alwaysFlowImpersonationPolicy enabled="false"/>  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="617db-143">Dans ASP.NET, si vous souhaitez autoriser le flux d’emprunt d’identité au lieu de cela, vous devez utiliser explicitement les paramètres de configuration suivants :</span><span class="sxs-lookup"><span data-stu-id="617db-143">In ASP.NET, if you want to allow the flow of impersonation instead, you must explicitly use the following configuration settings:</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <legacyImpersonationPolicy enabled="false"/>  
      <alwaysFlowImpersonationPolicy enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="example"></a><span data-ttu-id="617db-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="617db-144">Example</span></span>  
 <span data-ttu-id="617db-145">L’exemple suivant montre comment spécifier que l’identité Windows est transmise entre des points asynchrones, même lorsque l’emprunt d’identité est obtenue par des moyens autres que des méthodes managées.</span><span class="sxs-lookup"><span data-stu-id="617db-145">The following example shows how to specify that the Windows identity flows across asynchronous points, even when the impersonation is achieved through means other than managed methods.</span></span>  
  
```xml  
<configuration>  
  <runtime>  
    <alwaysFlowImpersonationPolicy enabled="true"/>  
  </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="617db-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="617db-146">See also</span></span>

- [<span data-ttu-id="617db-147">Schéma des paramètres d'exécution</span><span class="sxs-lookup"><span data-stu-id="617db-147">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="617db-148">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="617db-148">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="617db-149">\<legacyImpersonationPolicy > élément</span><span class="sxs-lookup"><span data-stu-id="617db-149">\<legacyImpersonationPolicy> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/legacyimpersonationpolicy-element.md)
