---
title: API et bibliothèques de classes supplémentaires
ms.date: 01/29/2018
helpviewer_keywords:
- Additional class libraries
- Additional managed libraries
- .NET Framework out-of-band releases
- out-of-band releases
ms.assetid: cf2d9006-b631-4e5d-81cd-20aab78c60f1
author: mairaw
ms.author: mairaw
ms.topic: conceptual
ms.openlocfilehash: 7659dde4a2cb08fc3257d2f613ce4146522072b6
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46478868"
---
# <a name="additional-class-libraries-and-apis"></a><span data-ttu-id="e6758-102">API et bibliothèques de classes supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e6758-102">Additional class libraries and APIs</span></span>

<span data-ttu-id="e6758-103">Le .NET Framework est en constante évolution.</span><span class="sxs-lookup"><span data-stu-id="e6758-103">The .NET Framework is constantly evolving.</span></span> <span data-ttu-id="e6758-104">Pour améliorer le développement multiplateforme et introduire de nouvelles fonctionnalités très tôt, les nouvelles fonctionnalités sont publiées hors bande (OOB).</span><span class="sxs-lookup"><span data-stu-id="e6758-104">To improve cross-platform development and introduce new functionality early, new features are released out of band (OOB).</span></span> <span data-ttu-id="e6758-105">Cette rubrique répertorie les projets OOB pour lesquels nous fournissons une documentation.</span><span class="sxs-lookup"><span data-stu-id="e6758-105">This topic lists the OOB projects that we provide documentation for.</span></span>  
  
<span data-ttu-id="e6758-106">En outre, certaines bibliothèques ciblent des plateformes ou des implémentations précises du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e6758-106">In addition, some libraries target specific platforms or implementations of the .NET Framework.</span></span> <span data-ttu-id="e6758-107">Par exemple, le <xref:System.Text.CodePagesEncodingProvider> classe rend les codages de page de code disponible pour les applications UWP développées à l’aide de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e6758-107">For example, the <xref:System.Text.CodePagesEncodingProvider> class makes code page encodings available to UWP apps developed using the .NET Framework.</span></span> <span data-ttu-id="e6758-108">Cette rubrique liste également ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="e6758-108">This topic lists these libraries as well.</span></span>  
  
## <a name="oob-projects"></a><span data-ttu-id="e6758-109">Projets OOB</span><span class="sxs-lookup"><span data-stu-id="e6758-109">OOB projects</span></span>
  
| <span data-ttu-id="e6758-110">Projet</span><span class="sxs-lookup"><span data-stu-id="e6758-110">Project</span></span> | <span data-ttu-id="e6758-111">Description</span><span class="sxs-lookup"><span data-stu-id="e6758-111">Description</span></span> |  
| ------- | ----------- |  
| <xref:System.Collections.Immutable> | <span data-ttu-id="e6758-112">Fournit des collections thread-safe dont le contenu est assuré de ne jamais changer.</span><span class="sxs-lookup"><span data-stu-id="e6758-112">Provides collections that are thread safe and guaranteed to never change their contents.</span></span> |
| <xref:System.Net.Http.WinHttpHandler> | <span data-ttu-id="e6758-113">Fournit un gestionnaire de messages pour <xref:System.Net.Http.HttpClient> basé sur l’interface WinHTTP de Windows.</span><span class="sxs-lookup"><span data-stu-id="e6758-113">Provides a message handler for <xref:System.Net.Http.HttpClient> based on the WinHTTP interface of Windows.</span></span> |
| [<span data-ttu-id="e6758-114">System.Numerics.Vectors</span><span class="sxs-lookup"><span data-stu-id="e6758-114">System.Numerics.Vectors</span></span>](https://msdn.microsoft.com/library/mt452176.aspx) | <span data-ttu-id="e6758-115">Fournit une bibliothèque de types de vecteurs qui peuvent tirer parti de l’accélération matérielle SIMD.</span><span class="sxs-lookup"><span data-stu-id="e6758-115">Provides a library of vector types that can take advantage of SIMD hardware-based acceleration.</span></span>| 
| <xref:System.Threading.Tasks.Dataflow> | <span data-ttu-id="e6758-116">La bibliothèque de flux de données TPL fournit des composants de flux de données destinés à accroître la robustesse des applications prenant en charge l’accès concurrentiel.</span><span class="sxs-lookup"><span data-stu-id="e6758-116">The TPL Dataflow Library provides dataflow components to help increase the robustness of concurrency-enabled applications.</span></span> |  

## <a name="platform-specific-libraries"></a><span data-ttu-id="e6758-117">Bibliothèques propres à une plateforme</span><span class="sxs-lookup"><span data-stu-id="e6758-117">Platform-specific libraries</span></span>
  
| <span data-ttu-id="e6758-118">Projet</span><span class="sxs-lookup"><span data-stu-id="e6758-118">Project</span></span> | <span data-ttu-id="e6758-119">Description</span><span class="sxs-lookup"><span data-stu-id="e6758-119">Description</span></span> |  
| ------- | ----------- |  
| <xref:System.Text.CodePagesEncodingProvider> | <span data-ttu-id="e6758-120">Étend la <xref:System.Text.EncodingProvider> classe pour rendre les codages de page de code disponibles pour les applications qui ciblent la plateforme Windows universelle.</span><span class="sxs-lookup"><span data-stu-id="e6758-120">Extends the <xref:System.Text.EncodingProvider> class to make code page encodings available to apps that target the Universal Windows Platform.</span></span> |  
  
## <a name="private-apis"></a><span data-ttu-id="e6758-121">API privées</span><span class="sxs-lookup"><span data-stu-id="e6758-121">Private APIs</span></span>  

<span data-ttu-id="e6758-122">Ces API prennent en charge l'infrastructure du produit et ne sont ni utilisables ni destinées à être utilisées directement à partir du code.</span><span class="sxs-lookup"><span data-stu-id="e6758-122">These APIs support the product infrastructure and are not intended/supported to be used directly from your code.</span></span>  
  
| <span data-ttu-id="e6758-123">Nom de l'API</span><span class="sxs-lookup"><span data-stu-id="e6758-123">API Name</span></span> |
| -------- |
| [<span data-ttu-id="e6758-124">Classe de System.Net.Connection</span><span class="sxs-lookup"><span data-stu-id="e6758-124">System.Net.Connection Class</span></span>](../../../docs/framework/additional-apis/connection.md) |
| [<span data-ttu-id="e6758-125">System.Net.Connection.m\_WriteList champ</span><span class="sxs-lookup"><span data-stu-id="e6758-125">System.Net.Connection.m\_WriteList Field</span></span>](../../../docs/framework/additional-apis/m_writelist.md) |
| [<span data-ttu-id="e6758-126">Classe de System.Net.ConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="e6758-126">System.Net.ConnectionGroup Class</span></span>](../../../docs/framework/additional-apis/connectiongroup.md) |
| [<span data-ttu-id="e6758-127">System.Net.ConnectionGroup.m\_ConnectionList champ</span><span class="sxs-lookup"><span data-stu-id="e6758-127">System.Net.ConnectionGroup.m\_ConnectionList Field</span></span>](../../../docs/framework/additional-apis/m_connectionlist.md) |
| [<span data-ttu-id="e6758-128">Classe de System.Net.CoreResponseData</span><span class="sxs-lookup"><span data-stu-id="e6758-128">System.Net.CoreResponseData Class</span></span>](../../../docs/framework/additional-apis/coreresponsedata.md) |
| [<span data-ttu-id="e6758-129">System.Net.CoreResponseData.m\_ResponseHeaders champ</span><span class="sxs-lookup"><span data-stu-id="e6758-129">System.Net.CoreResponseData.m\_ResponseHeaders Field</span></span>](../../../docs/framework/additional-apis/coreresponsedata_m_responseheaders.md) |
| [<span data-ttu-id="e6758-130">System.Net.CoreResponseData.m\_champ StatusCode</span><span class="sxs-lookup"><span data-stu-id="e6758-130">System.Net.CoreResponseData.m\_StatusCode Field</span></span>](../../../docs/framework/additional-apis/coreresponsedata_m_statuscode.md) |
| [<span data-ttu-id="e6758-131">System.Net.HttpWebRequest. \_AutoRedirects champ</span><span class="sxs-lookup"><span data-stu-id="e6758-131">System.Net.HttpWebRequest.\_AutoRedirects Field</span></span>](../../../docs/framework/additional-apis/_autoredirects.md) |
| [<span data-ttu-id="e6758-132">System.Net.HttpWebRequest. \_CoreResponse champ</span><span class="sxs-lookup"><span data-stu-id="e6758-132">System.Net.HttpWebRequest.\_CoreResponse Field</span></span>](../../../docs/framework/additional-apis/httpwebrequest__coreresponse.md) |
| [<span data-ttu-id="e6758-133">System.Net.HttpWebRequest. \_HttpResponse champ</span><span class="sxs-lookup"><span data-stu-id="e6758-133">System.Net.HttpWebRequest.\_HttpResponse Field</span></span>](../../../docs/framework/additional-apis/_httpresponse.md) |
| [<span data-ttu-id="e6758-134">System.Net.ServicePoint.m\_ConnectionGroupList champ</span><span class="sxs-lookup"><span data-stu-id="e6758-134">System.Net.ServicePoint.m\_ConnectionGroupList Field</span></span>](../../../docs/framework/additional-apis/m_connectiongrouplist.md) |
| [<span data-ttu-id="e6758-135">System.Net.ServicePointManager.s\_ServicePointTable champ</span><span class="sxs-lookup"><span data-stu-id="e6758-135">System.Net.ServicePointManager.s\_ServicePointTable Field</span></span>](../../../docs/framework/additional-apis/s_servicepointtable.md) |
| [<span data-ttu-id="e6758-136">System.Windows.Diagnostics.VisualDiagnostics.s\_isDebuggerCheckDisabledForTestPurposes Field</span><span class="sxs-lookup"><span data-stu-id="e6758-136">System.Windows.Diagnostics.VisualDiagnostics.s\_isDebuggerCheckDisabledForTestPurposes Field</span></span>](../../../docs/framework/additional-apis/s-isdebuggercheckdisabledfortestpurposes-field.md) |
| [<span data-ttu-id="e6758-137">Classe de System.Windows.Forms.Design.DataMemberFieldEditor</span><span class="sxs-lookup"><span data-stu-id="e6758-137">System.Windows.Forms.Design.DataMemberFieldEditor Class</span></span>](../../../docs/framework/additional-apis/datamemberfieldeditor-class.md) |
| [<span data-ttu-id="e6758-138">Classe de System.Windows.Forms.Design.DataMemberListEditor</span><span class="sxs-lookup"><span data-stu-id="e6758-138">System.Windows.Forms.Design.DataMemberListEditor Class</span></span>](../../../docs/framework/additional-apis/datamemberlisteditor-class.md) |
  
## <a name="see-also"></a><span data-ttu-id="e6758-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6758-139">See also</span></span>

[<span data-ttu-id="e6758-140">Versions finales hors plage de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="e6758-140">The .NET Framework and Out-of-Band Releases</span></span>](../../../docs/framework/get-started/the-net-framework-and-out-of-band-releases.md)
