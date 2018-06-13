---
title: '&lt;legacyImpersonationPolicy&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#legacyImpersonationPolicy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/legacyImpersonationPolicy
helpviewer_keywords:
- <legacyImpersonationPolicy> element
- legacyImpersonationPolicy element
ms.assetid: 6e00af10-42f3-4235-8415-1bb2db78394e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f90853a93b40eeb72f07ad9b1849aa99c8e8bf3d
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32745186"
---
# <a name="ltlegacyimpersonationpolicygt-element"></a><span data-ttu-id="c56d7-102">&lt;legacyImpersonationPolicy&gt; élément</span><span class="sxs-lookup"><span data-stu-id="c56d7-102">&lt;legacyImpersonationPolicy&gt; Element</span></span>
<span data-ttu-id="c56d7-103">Spécifie que l’identité Windows n’est pas transmise entre des points asynchrones, indépendamment des paramètres de flux du contexte d’exécution sur le thread actif.</span><span class="sxs-lookup"><span data-stu-id="c56d7-103">Specifies that the Windows identity does not flow across asynchronous points, regardless of the flow settings for the execution context on the current thread.</span></span>  
  
 <span data-ttu-id="c56d7-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="c56d7-104">\<configuration></span></span>  
<span data-ttu-id="c56d7-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="c56d7-105">\<runtime></span></span>  
<span data-ttu-id="c56d7-106">\<legacyImpersonationPolicy ></span><span class="sxs-lookup"><span data-stu-id="c56d7-106">\<legacyImpersonationPolicy></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c56d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c56d7-107">Syntax</span></span>  
  
```xml  
<legacyImpersonationPolicy    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c56d7-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c56d7-108">Attributes and Elements</span></span>  
 <span data-ttu-id="c56d7-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c56d7-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c56d7-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="c56d7-110">Attributes</span></span>  
  
|<span data-ttu-id="c56d7-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="c56d7-111">Attribute</span></span>|<span data-ttu-id="c56d7-112">Description</span><span class="sxs-lookup"><span data-stu-id="c56d7-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="c56d7-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="c56d7-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="c56d7-114">Spécifie que le <xref:System.Security.Principal.WindowsIdentity> n’est pas transmis entre des points asynchrones, quel que soit le <xref:System.Threading.ExecutionContext> de flux de paramètres sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="c56d7-114">Specifies that the <xref:System.Security.Principal.WindowsIdentity> does not flow across asynchronous points, regardless of the <xref:System.Threading.ExecutionContext> flow settings on the current thread.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="c56d7-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="c56d7-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="c56d7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c56d7-116">Value</span></span>|<span data-ttu-id="c56d7-117">Description</span><span class="sxs-lookup"><span data-stu-id="c56d7-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="c56d7-118"><xref:System.Security.Principal.WindowsIdentity> flux entre des points asynchrones en fonction de la <xref:System.Threading.ExecutionContext> de flux de paramètres pour le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="c56d7-118"><xref:System.Security.Principal.WindowsIdentity> flows across asynchronous points depending upon the <xref:System.Threading.ExecutionContext> flow settings for the current thread.</span></span> <span data-ttu-id="c56d7-119">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c56d7-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="c56d7-120"><xref:System.Security.Principal.WindowsIdentity> n’est pas transmis entre des points asynchrones, quel que soit le <xref:System.Threading.ExecutionContext> de flux de paramètres sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="c56d7-120"><xref:System.Security.Principal.WindowsIdentity> does not flow across asynchronous points, regardless of the <xref:System.Threading.ExecutionContext> flow settings on the current thread.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c56d7-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c56d7-121">Child Elements</span></span>  
 <span data-ttu-id="c56d7-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c56d7-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c56d7-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c56d7-123">Parent Elements</span></span>  
  
|<span data-ttu-id="c56d7-124">Élément</span><span class="sxs-lookup"><span data-stu-id="c56d7-124">Element</span></span>|<span data-ttu-id="c56d7-125">Description</span><span class="sxs-lookup"><span data-stu-id="c56d7-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="c56d7-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c56d7-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="c56d7-127">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="c56d7-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c56d7-128">Notes</span><span class="sxs-lookup"><span data-stu-id="c56d7-128">Remarks</span></span>  
 <span data-ttu-id="c56d7-129">Dans les versions du .NET Framework 1.0 et 1.1, la <xref:System.Security.Principal.WindowsIdentity> n’est pas transmis entre des points asynchrones définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c56d7-129">In the .NET Framework versions 1.0 and 1.1, the <xref:System.Security.Principal.WindowsIdentity> does not flow across any user-defined asynchronous points.</span></span> <span data-ttu-id="c56d7-130">À compter de .NET Framework version 2.0, il existe un <xref:System.Threading.ExecutionContext> flux d’objet qui contient des informations sur le thread en cours d’exécution et il entre des points asynchrones dans un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="c56d7-130">Starting with the .NET Framework version 2.0, there is an <xref:System.Threading.ExecutionContext> object that contains information about the currently executing thread, and it flows across asynchronous points within an application domain.</span></span> <span data-ttu-id="c56d7-131">Le <xref:System.Security.Principal.WindowsIdentity> est inclus dans ce contexte d’exécution et donc également transmise entre des points asynchrones, ce qui signifie que si un contexte d’emprunt d’identité existe, il transmet également.</span><span class="sxs-lookup"><span data-stu-id="c56d7-131">The <xref:System.Security.Principal.WindowsIdentity> is included in this execution context and therefore also flows across the asynchronous points, which means that if an impersonation context exists, it will flow as well.</span></span>  
  
 <span data-ttu-id="c56d7-132">À compter de .NET Framework 2.0, vous pouvez utiliser la `<legacyImpersonationPolicy>` élément pour spécifier que <xref:System.Security.Principal.WindowsIdentity> n’est pas transmis entre des points asynchrones.</span><span class="sxs-lookup"><span data-stu-id="c56d7-132">Starting with the .NET Framework 2.0, you can use the `<legacyImpersonationPolicy>` element to specify that  <xref:System.Security.Principal.WindowsIdentity> does not flow across asynchronous points.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c56d7-133">Le common language runtime (CLR) est informé de l’emprunt d’identité opérations effectuées avec uniquement du code managé, pas de l’emprunt d’identité effectuée en dehors du code managé, comme par plate-forme code non managé au code non managé ou via des appels directs aux fonctions Win32.</span><span class="sxs-lookup"><span data-stu-id="c56d7-133">The common language runtime (CLR) is aware of impersonation operations performed using only managed code, not of impersonation performed outside of managed code, such as through platform invoke to unmanaged code or through direct calls to Win32 functions.</span></span> <span data-ttu-id="c56d7-134">Managé <xref:System.Security.Principal.WindowsIdentity> objets peuvent être transmis entre des points asynchrones, à moins que le `alwaysFlowImpersonationPolicy` élément a été défini sur true (`<alwaysFlowImpersonationPolicy enabled="true"/>`).</span><span class="sxs-lookup"><span data-stu-id="c56d7-134">Only managed <xref:System.Security.Principal.WindowsIdentity> objects can flow across asynchronous points, unless the `alwaysFlowImpersonationPolicy` element has been set to true (`<alwaysFlowImpersonationPolicy enabled="true"/>`).</span></span> <span data-ttu-id="c56d7-135">Définition de la `alwaysFlowImpersonationPolicy` élément true spécifie que l’identité Windows est toujours transmise entre des points asynchrones, quelle que soit la façon dont l’emprunt d’identité a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="c56d7-135">Setting the `alwaysFlowImpersonationPolicy` element to true specifies that the Windows identity always flows across asynchronous points, regardless of how impersonation was performed.</span></span> <span data-ttu-id="c56d7-136">Pour plus d’informations sur la transmission non managé à l’emprunt d’identité entre des points asynchrones, consultez [ \<alwaysFlowImpersonationPolicy > élément](../../../../../docs/framework/configure-apps/file-schema/runtime/alwaysflowimpersonationpolicy-element.md).</span><span class="sxs-lookup"><span data-stu-id="c56d7-136">For more information on flowing unmanaged impersonation across asynchronous points, see [\<alwaysFlowImpersonationPolicy> Element](../../../../../docs/framework/configure-apps/file-schema/runtime/alwaysflowimpersonationpolicy-element.md).</span></span>  
  
 <span data-ttu-id="c56d7-137">Vous pouvez modifier ce comportement par défaut de deux manières différentes :</span><span class="sxs-lookup"><span data-stu-id="c56d7-137">You can alter this default behavior in two other ways:</span></span>  
  
1.  <span data-ttu-id="c56d7-138">Dans le code managé sur une base par thread.</span><span class="sxs-lookup"><span data-stu-id="c56d7-138">In managed code on a per-thread basis.</span></span>  
  
     <span data-ttu-id="c56d7-139">Vous pouvez supprimer le flux sur une base par thread en modifiant le <xref:System.Threading.ExecutionContext> et <xref:System.Security.SecurityContext> paramètres à l’aide de la <xref:System.Threading.ExecutionContext.SuppressFlow%2A?displayProperty=nameWithType>, <xref:System.Security.SecurityContext.SuppressFlowWindowsIdentity%2A?displayProperty=nameWithType> ou <xref:System.Security.SecurityContext.SuppressFlow%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="c56d7-139">You can suppress the flow on a per-thread basis by modifying the <xref:System.Threading.ExecutionContext> and <xref:System.Security.SecurityContext> settings by using the <xref:System.Threading.ExecutionContext.SuppressFlow%2A?displayProperty=nameWithType>, <xref:System.Security.SecurityContext.SuppressFlowWindowsIdentity%2A?displayProperty=nameWithType> or <xref:System.Security.SecurityContext.SuppressFlow%2A?displayProperty=nameWithType> method.</span></span>  
  
2.  <span data-ttu-id="c56d7-140">Dans l’appel à l’interface d’hébergement non managée pour charger le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="c56d7-140">In the call to the unmanaged hosting interface to load the common language runtime (CLR).</span></span>  
  
     <span data-ttu-id="c56d7-141">Si une interface d’hébergement non managée (au lieu d’un simple fichier exécutable managé) est utilisée pour charger le CLR, vous pouvez spécifier un indicateur spécial dans l’appel à la [fonction CorBindToRuntimeEx](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="c56d7-141">If an unmanaged hosting interface (instead of a simple managed executable) is used to load the CLR, you can specify a special flag in the call to the [CorBindToRuntimeEx Function](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) function.</span></span> <span data-ttu-id="c56d7-142">Pour activer le mode de compatibilité pour l’ensemble du processus, définissez la `flags` paramètre [fonction CorBindToRuntimeEx](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) valeur STARTUP_LEGACY_IMPERSONATION au.</span><span class="sxs-lookup"><span data-stu-id="c56d7-142">To enable the compatibility mode for the entire process, set the `flags` parameter for [CorBindToRuntimeEx Function](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) to STARTUP_LEGACY_IMPERSONATION.</span></span>  
  
 <span data-ttu-id="c56d7-143">Pour plus d’informations, consultez la [ \<alwaysFlowImpersonationPolicy > élément](../../../../../docs/framework/configure-apps/file-schema/runtime/alwaysflowimpersonationpolicy-element.md).</span><span class="sxs-lookup"><span data-stu-id="c56d7-143">For more information, see the [\<alwaysFlowImpersonationPolicy> Element](../../../../../docs/framework/configure-apps/file-schema/runtime/alwaysflowimpersonationpolicy-element.md).</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="c56d7-144">Fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="c56d7-144">Configuration File</span></span>  
 <span data-ttu-id="c56d7-145">Dans une application .NET Framework, cet élément peut être utilisé uniquement dans le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="c56d7-145">In a .NET Framework application, this element can be used only in the application configuration file.</span></span>  
  
 <span data-ttu-id="c56d7-146">Pour une application ASP.NET, le flux de l’emprunt d’identité peut être configuré dans le fichier aspnet.config trouvé dans le \<dossier Windows > \Microsoft.NET\Framework\vx.x.xxxx active.</span><span class="sxs-lookup"><span data-stu-id="c56d7-146">For an ASP.NET application, the impersonation flow can be configured in the aspnet.config file found in the \<Windows Folder>\Microsoft.NET\Framework\vx.x.xxxx directory.</span></span>  
  
 <span data-ttu-id="c56d7-147">ASP.NET par défaut désactive le flux de l’emprunt d’identité dans le fichier aspnet.config à l’aide de paramètres de configuration suivants :</span><span class="sxs-lookup"><span data-stu-id="c56d7-147">ASP.NET by default disables the impersonation flow in the aspnet.config file by using the following configuration settings:</span></span>  
  
``` xml
<configuration>  
   <runtime>  
      <legacyImpersonationPolicy enabled="true"/>  
      <alwaysFlowImpersonationPolicy enabled="false"/>  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="c56d7-148">Dans ASP.NET, si vous souhaitez autoriser le flux d’emprunt d’identité à la place, vous devez utiliser explicitement les paramètres de configuration suivants :</span><span class="sxs-lookup"><span data-stu-id="c56d7-148">In ASP.NET, if you want to allow the flow of impersonation instead, you must explicitly use the following configuration settings:</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <legacyImpersonationPolicy enabled="false"/>  
      <alwaysFlowImpersonationPolicy enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="example"></a><span data-ttu-id="c56d7-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="c56d7-149">Example</span></span>  
 <span data-ttu-id="c56d7-150">L’exemple suivant montre comment spécifier le comportement hérité qui ne transmet pas l’identité Windows entre des points asynchrones.</span><span class="sxs-lookup"><span data-stu-id="c56d7-150">The following example shows how to specify the legacy behavior that does not flow the Windows identity across asynchronous points.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <legacyImpersonationPolicy enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="c56d7-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c56d7-151">See Also</span></span>  
 [<span data-ttu-id="c56d7-152">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="c56d7-152">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="c56d7-153">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="c56d7-153">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="c56d7-154">\<alwaysFlowImpersonationPolicy > élément</span><span class="sxs-lookup"><span data-stu-id="c56d7-154">\<alwaysFlowImpersonationPolicy> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/alwaysflowimpersonationpolicy-element.md)
