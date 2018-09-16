---
title: '&lt;Directives&gt;, élément (.NET Native)'
ms.date: 03/30/2017
ms.assetid: 444846f3-48d5-4341-a43e-69f7221389eb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8921d2841f9a7b4228ae3b8735d7047453f71bcb
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45676257"
---
# <a name="ltdirectivesgt-element-net-native"></a><span data-ttu-id="d5529-102">&lt;Directives&gt;, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="d5529-102">&lt;Directives&gt; Element (.NET Native)</span></span>
<span data-ttu-id="d5529-103">L’élément racine dans chaque fichier de directives runtime pour .NET Native.</span><span class="sxs-lookup"><span data-stu-id="d5529-103">The root element in every runtime directives file for .NET Native.</span></span>  
  
 `<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">` 
  
## <a name="syntax"></a><span data-ttu-id="d5529-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5529-104">Syntax</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
   <!-- child elements -->   
</Directives>  
```  
  
## <a name="attributes"></a><span data-ttu-id="d5529-105">Attributs</span><span class="sxs-lookup"><span data-stu-id="d5529-105">Attributes</span></span>  
  
|<span data-ttu-id="d5529-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="d5529-106">Attribute</span></span>|<span data-ttu-id="d5529-107">Description</span><span class="sxs-lookup"><span data-stu-id="d5529-107">Description</span></span>|  
|---------------|-----------------|  
|`xmlns`|<span data-ttu-id="d5529-108">Espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="d5529-108">The XML namespace.</span></span> <span data-ttu-id="d5529-109">Sa valeur est toujours **» http://schemas.microsoft.com/netfx/2013/01/metadata»**.</span><span class="sxs-lookup"><span data-stu-id="d5529-109">Its value is always **"http://schemas.microsoft.com/netfx/2013/01/metadata"**.</span></span>|  
  
## <a name="child-elements"></a><span data-ttu-id="d5529-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d5529-110">Child elements</span></span>  
  
|<span data-ttu-id="d5529-111">Élément</span><span class="sxs-lookup"><span data-stu-id="d5529-111">Element</span></span>|<span data-ttu-id="d5529-112">Description</span><span class="sxs-lookup"><span data-stu-id="d5529-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d5529-113">\<Application></span><span class="sxs-lookup"><span data-stu-id="d5529-113">\<Application></span></span>](../../../docs/framework/net-native/application-element-net-native.md)|<span data-ttu-id="d5529-114">Sert de conteneur pour des types à l'échelle de l'application et pour des membres de types dont les métadonnées sont disponibles pour la réflexion.</span><span class="sxs-lookup"><span data-stu-id="d5529-114">Serves as a container for application-wide types and type members whose metadata is available for reflection.</span></span>|  
|[<span data-ttu-id="d5529-115">\<Library></span><span class="sxs-lookup"><span data-stu-id="d5529-115">\<Library></span></span>](../../../docs/framework/net-native/library-element-net-native.md)|<span data-ttu-id="d5529-116">Définit l'assembly dont les types enfants et les membres de type nécessitent des métadonnées au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="d5529-116">Defines the assembly whose child types and type members require metadata at run time.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d5529-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d5529-117">Remarks</span></span>  
 <span data-ttu-id="d5529-118">Chaque fichier de directives runtime ne peut contenir qu'un seul élément `<Directives>`.</span><span class="sxs-lookup"><span data-stu-id="d5529-118">Each runtime directives file can contain only one `<Directives>` element.</span></span>  
  
 <span data-ttu-id="d5529-119">L’élément `<Directives>` peut contenir zéro ou un élément [\<Application>](../../../docs/framework/net-native/application-element-net-native.md), ainsi que zéro, un ou plusieurs éléments [\<Library>](../../../docs/framework/net-native/library-element-net-native.md).</span><span class="sxs-lookup"><span data-stu-id="d5529-119">The `<Directives>` element can contain zero or one [\<Application>](../../../docs/framework/net-native/application-element-net-native.md) element, and zero, one, or more [\<Library>](../../../docs/framework/net-native/library-element-net-native.md) elements.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5529-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5529-120">See Also</span></span>  
 [<span data-ttu-id="d5529-121">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="d5529-121">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)  
 [<span data-ttu-id="d5529-122">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="d5529-122">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
