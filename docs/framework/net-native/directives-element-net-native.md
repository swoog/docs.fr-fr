---
title: '&lt;Directives&gt;, élément (.NET Native)'
ms.date: 03/30/2017
ms.assetid: 444846f3-48d5-4341-a43e-69f7221389eb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8921d2841f9a7b4228ae3b8735d7047453f71bcb
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44267139"
---
# <a name="ltdirectivesgt-element-net-native"></a><span data-ttu-id="bf168-102">&lt;Directives&gt;, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="bf168-102">&lt;Directives&gt; Element (.NET Native)</span></span>
<span data-ttu-id="bf168-103">L’élément racine dans chaque fichier de directives runtime pour .NET Native.</span><span class="sxs-lookup"><span data-stu-id="bf168-103">The root element in every runtime directives file for .NET Native.</span></span>  
  
 `<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">` 
  
## <a name="syntax"></a><span data-ttu-id="bf168-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf168-104">Syntax</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
   <!-- child elements -->   
</Directives>  
```  
  
## <a name="attributes"></a><span data-ttu-id="bf168-105">Attributs</span><span class="sxs-lookup"><span data-stu-id="bf168-105">Attributes</span></span>  
  
|<span data-ttu-id="bf168-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="bf168-106">Attribute</span></span>|<span data-ttu-id="bf168-107">Description</span><span class="sxs-lookup"><span data-stu-id="bf168-107">Description</span></span>|  
|---------------|-----------------|  
|`xmlns`|<span data-ttu-id="bf168-108">Espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="bf168-108">The XML namespace.</span></span> <span data-ttu-id="bf168-109">Sa valeur est toujours **» http://schemas.microsoft.com/netfx/2013/01/metadata»**.</span><span class="sxs-lookup"><span data-stu-id="bf168-109">Its value is always **"http://schemas.microsoft.com/netfx/2013/01/metadata"**.</span></span>|  
  
## <a name="child-elements"></a><span data-ttu-id="bf168-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bf168-110">Child elements</span></span>  
  
|<span data-ttu-id="bf168-111">Élément</span><span class="sxs-lookup"><span data-stu-id="bf168-111">Element</span></span>|<span data-ttu-id="bf168-112">Description</span><span class="sxs-lookup"><span data-stu-id="bf168-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bf168-113">\<Application></span><span class="sxs-lookup"><span data-stu-id="bf168-113">\<Application></span></span>](../../../docs/framework/net-native/application-element-net-native.md)|<span data-ttu-id="bf168-114">Sert de conteneur pour des types à l'échelle de l'application et pour des membres de types dont les métadonnées sont disponibles pour la réflexion.</span><span class="sxs-lookup"><span data-stu-id="bf168-114">Serves as a container for application-wide types and type members whose metadata is available for reflection.</span></span>|  
|[<span data-ttu-id="bf168-115">\<Library></span><span class="sxs-lookup"><span data-stu-id="bf168-115">\<Library></span></span>](../../../docs/framework/net-native/library-element-net-native.md)|<span data-ttu-id="bf168-116">Définit l'assembly dont les types enfants et les membres de type nécessitent des métadonnées au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="bf168-116">Defines the assembly whose child types and type members require metadata at run time.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bf168-117">Notes</span><span class="sxs-lookup"><span data-stu-id="bf168-117">Remarks</span></span>  
 <span data-ttu-id="bf168-118">Chaque fichier de directives runtime ne peut contenir qu'un seul élément `<Directives>`.</span><span class="sxs-lookup"><span data-stu-id="bf168-118">Each runtime directives file can contain only one `<Directives>` element.</span></span>  
  
 <span data-ttu-id="bf168-119">L’élément `<Directives>` peut contenir zéro ou un élément [\<Application>](../../../docs/framework/net-native/application-element-net-native.md), ainsi que zéro, un ou plusieurs éléments [\<Library>](../../../docs/framework/net-native/library-element-net-native.md).</span><span class="sxs-lookup"><span data-stu-id="bf168-119">The `<Directives>` element can contain zero or one [\<Application>](../../../docs/framework/net-native/application-element-net-native.md) element, and zero, one, or more [\<Library>](../../../docs/framework/net-native/library-element-net-native.md) elements.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf168-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf168-120">See Also</span></span>  
 [<span data-ttu-id="bf168-121">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="bf168-121">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)  
 [<span data-ttu-id="bf168-122">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="bf168-122">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
