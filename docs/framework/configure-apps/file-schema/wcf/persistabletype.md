---
title: <persistableType>
ms.date: 03/30/2017
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
ms.openlocfilehash: 3ea99d360ceb1e3fe6e97cbf9c8827dd7c853f63
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55256522"
---
# <a name="persistabletype"></a><span data-ttu-id="0f6ec-101">\<persistableType></span><span class="sxs-lookup"><span data-stu-id="0f6ec-101">\<persistableType></span></span>
<span data-ttu-id="0f6ec-102">Spécifie tous les types persistants.</span><span class="sxs-lookup"><span data-stu-id="0f6ec-102">Specifies all the persistable types.</span></span>  
  
 <span data-ttu-id="0f6ec-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0f6ec-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="0f6ec-104">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="0f6ec-104">\<comContracts></span></span>  
<span data-ttu-id="0f6ec-105">\<comContract></span><span class="sxs-lookup"><span data-stu-id="0f6ec-105">\<comContract></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f6ec-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f6ec-106">Syntax</span></span>  
  
```xml  
<comContracts>
  <comContract>
    <persistableTypes>
      <persistableType id="String"
                       name="String">
      </persistableType>
    </persistableTypes>
  </comContract>
</comContracts>
```  
  
## <a name="type"></a><span data-ttu-id="0f6ec-107">Type</span><span class="sxs-lookup"><span data-stu-id="0f6ec-107">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0f6ec-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0f6ec-108">Attributes and Elements</span></span>  
 <span data-ttu-id="0f6ec-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0f6ec-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0f6ec-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="0f6ec-110">Attributes</span></span>  
  
|<span data-ttu-id="0f6ec-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="0f6ec-111">Attribute</span></span>|<span data-ttu-id="0f6ec-112">Description</span><span class="sxs-lookup"><span data-stu-id="0f6ec-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0f6ec-113">id</span><span class="sxs-lookup"><span data-stu-id="0f6ec-113">id</span></span>|<span data-ttu-id="0f6ec-114">Attribut requis qui contient une chaîne spécifiant un identificateur unique pour un type persistant.</span><span class="sxs-lookup"><span data-stu-id="0f6ec-114">A required attribute that contains a string that specifies a unique identifier for a persistable type.</span></span>|  
|<span data-ttu-id="0f6ec-115">name</span><span class="sxs-lookup"><span data-stu-id="0f6ec-115">name</span></span>|<span data-ttu-id="0f6ec-116">Attribut facultatif qui contient une chaîne spécifiant le nom du type persistant.</span><span class="sxs-lookup"><span data-stu-id="0f6ec-116">An optional attribute that contains a string that specifies the name of the persistable type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0f6ec-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f6ec-117">Child Elements</span></span>  
 <span data-ttu-id="0f6ec-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0f6ec-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0f6ec-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0f6ec-119">Parent Elements</span></span>  
  
|<span data-ttu-id="0f6ec-120">Élément</span><span class="sxs-lookup"><span data-stu-id="0f6ec-120">Element</span></span>|<span data-ttu-id="0f6ec-121">Description</span><span class="sxs-lookup"><span data-stu-id="0f6ec-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0f6ec-122">\<persistableTypes></span><span class="sxs-lookup"><span data-stu-id="0f6ec-122">\<persistableTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)|<span data-ttu-id="0f6ec-123">Collection d'éléments `persistableType`.</span><span class="sxs-lookup"><span data-stu-id="0f6ec-123">A collection of `persistableType` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0f6ec-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f6ec-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>
- [<span data-ttu-id="0f6ec-125">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="0f6ec-125">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)
- [<span data-ttu-id="0f6ec-126">Intégration à des applications COM+</span><span class="sxs-lookup"><span data-stu-id="0f6ec-126">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="0f6ec-127">Guide pratique pour Configurer les paramètres de Service COM +</span><span class="sxs-lookup"><span data-stu-id="0f6ec-127">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
