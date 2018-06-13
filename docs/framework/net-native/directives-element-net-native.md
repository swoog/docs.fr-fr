---
title: '&lt;Directives&gt;, élément (.NET Native)'
ms.date: 03/30/2017
ms.assetid: 444846f3-48d5-4341-a43e-69f7221389eb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bd571255f924c9f3878c00a2bc01397d63e6d777
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33394444"
---
# <a name="ltdirectivesgt-element-net-native"></a><span data-ttu-id="a8461-102">&lt;Directives&gt;, élément (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="a8461-102">&lt;Directives&gt; Element (.NET Native)</span></span>
<span data-ttu-id="a8461-103">Élément racine de chaque fichier de directives runtime pour [!INCLUDE[net_native](../../../includes/net-native-md.md)].</span><span class="sxs-lookup"><span data-stu-id="a8461-103">The root element in every runtime directives file for [!INCLUDE[net_native](../../../includes/net-native-md.md)].</span></span>  
  
 <span data-ttu-id="a8461-104">**\<Directives xmlns = »http://schemas.microsoft.com/netfx/2013/01/metadata« >**</span><span class="sxs-lookup"><span data-stu-id="a8461-104">**\<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">**</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8461-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8461-105">Syntax</span></span>  
  
```xml  
      <Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
   <!-- child elements -->   
</Directives>  
```  
  
## <a name="attributes"></a><span data-ttu-id="a8461-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="a8461-106">Attributes</span></span>  
  
|<span data-ttu-id="a8461-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="a8461-107">Attribute</span></span>|<span data-ttu-id="a8461-108">Description</span><span class="sxs-lookup"><span data-stu-id="a8461-108">Description</span></span>|  
|---------------|-----------------|  
|`xmlns`|<span data-ttu-id="a8461-109">Espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="a8461-109">The XML namespace.</span></span> <span data-ttu-id="a8461-110">Sa valeur est toujours **»http://schemas.microsoft.com/netfx/2013/01/metadata»**.</span><span class="sxs-lookup"><span data-stu-id="a8461-110">Its value is always **"http://schemas.microsoft.com/netfx/2013/01/metadata"**.</span></span>|  
  
## <a name="child-elements"></a><span data-ttu-id="a8461-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a8461-111">Child elements</span></span>  
  
|<span data-ttu-id="a8461-112">Élément</span><span class="sxs-lookup"><span data-stu-id="a8461-112">Element</span></span>|<span data-ttu-id="a8461-113">Description</span><span class="sxs-lookup"><span data-stu-id="a8461-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a8461-114">\<Application></span><span class="sxs-lookup"><span data-stu-id="a8461-114">\<Application></span></span>](../../../docs/framework/net-native/application-element-net-native.md)|<span data-ttu-id="a8461-115">Sert de conteneur pour des types à l'échelle de l'application et pour des membres de types dont les métadonnées sont disponibles pour la réflexion.</span><span class="sxs-lookup"><span data-stu-id="a8461-115">Serves as a container for application-wide types and type members whose metadata is available for reflection.</span></span>|  
|[<span data-ttu-id="a8461-116">\<Library></span><span class="sxs-lookup"><span data-stu-id="a8461-116">\<Library></span></span>](../../../docs/framework/net-native/library-element-net-native.md)|<span data-ttu-id="a8461-117">Définit l'assembly dont les types enfants et les membres de type nécessitent des métadonnées au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="a8461-117">Defines the assembly whose child types and type members require metadata at run time.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a8461-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a8461-118">Remarks</span></span>  
 <span data-ttu-id="a8461-119">Chaque fichier de directives runtime ne peut contenir qu'un seul élément `<Directives>`.</span><span class="sxs-lookup"><span data-stu-id="a8461-119">Each runtime directives file can contain only one `<Directives>` element.</span></span>  
  
 <span data-ttu-id="a8461-120">L’élément `<Directives>` peut contenir zéro ou un élément [\<Application>](../../../docs/framework/net-native/application-element-net-native.md), ainsi que zéro, un ou plusieurs éléments [\<Library>](../../../docs/framework/net-native/library-element-net-native.md).</span><span class="sxs-lookup"><span data-stu-id="a8461-120">The `<Directives>` element can contain zero or one [\<Application>](../../../docs/framework/net-native/application-element-net-native.md) element, and zero, one, or more [\<Library>](../../../docs/framework/net-native/library-element-net-native.md) elements.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8461-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8461-121">See Also</span></span>  
 [<span data-ttu-id="a8461-122">Guide de référence du fichier de configuration des directives runtime (rd.xml)</span><span class="sxs-lookup"><span data-stu-id="a8461-122">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)  
 [<span data-ttu-id="a8461-123">Éléments de directive runtime</span><span class="sxs-lookup"><span data-stu-id="a8461-123">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
