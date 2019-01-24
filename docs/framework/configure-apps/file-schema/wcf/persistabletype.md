---
title: '&lt;persistableType&gt;'
ms.date: 03/30/2017
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
ms.openlocfilehash: b9d61a736a2f8650c543433931d57e156d115018
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706850"
---
# <a name="ltpersistabletypegt"></a><span data-ttu-id="dbd5c-102">&lt;persistableType&gt;</span><span class="sxs-lookup"><span data-stu-id="dbd5c-102">&lt;persistableType&gt;</span></span>
<span data-ttu-id="dbd5c-103">Spécifie tous les types persistants.</span><span class="sxs-lookup"><span data-stu-id="dbd5c-103">Specifies all the persistable types.</span></span>  
  
 <span data-ttu-id="dbd5c-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="dbd5c-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="dbd5c-105">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="dbd5c-105">\<comContracts></span></span>  
<span data-ttu-id="dbd5c-106">\<comContract></span><span class="sxs-lookup"><span data-stu-id="dbd5c-106">\<comContract></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dbd5c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbd5c-107">Syntax</span></span>  
  
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
  
## <a name="type"></a><span data-ttu-id="dbd5c-108">Type</span><span class="sxs-lookup"><span data-stu-id="dbd5c-108">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dbd5c-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="dbd5c-109">Attributes and Elements</span></span>  
 <span data-ttu-id="dbd5c-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="dbd5c-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dbd5c-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="dbd5c-111">Attributes</span></span>  
  
|<span data-ttu-id="dbd5c-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="dbd5c-112">Attribute</span></span>|<span data-ttu-id="dbd5c-113">Description</span><span class="sxs-lookup"><span data-stu-id="dbd5c-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="dbd5c-114">id</span><span class="sxs-lookup"><span data-stu-id="dbd5c-114">id</span></span>|<span data-ttu-id="dbd5c-115">Attribut requis qui contient une chaîne spécifiant un identificateur unique pour un type persistant.</span><span class="sxs-lookup"><span data-stu-id="dbd5c-115">A required attribute that contains a string that specifies a unique identifier for a persistable type.</span></span>|  
|<span data-ttu-id="dbd5c-116">name</span><span class="sxs-lookup"><span data-stu-id="dbd5c-116">name</span></span>|<span data-ttu-id="dbd5c-117">Attribut facultatif qui contient une chaîne spécifiant le nom du type persistant.</span><span class="sxs-lookup"><span data-stu-id="dbd5c-117">An optional attribute that contains a string that specifies the name of the persistable type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dbd5c-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dbd5c-118">Child Elements</span></span>  
 <span data-ttu-id="dbd5c-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dbd5c-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dbd5c-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dbd5c-120">Parent Elements</span></span>  
  
|<span data-ttu-id="dbd5c-121">Élément</span><span class="sxs-lookup"><span data-stu-id="dbd5c-121">Element</span></span>|<span data-ttu-id="dbd5c-122">Description</span><span class="sxs-lookup"><span data-stu-id="dbd5c-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dbd5c-123">\<persistableTypes></span><span class="sxs-lookup"><span data-stu-id="dbd5c-123">\<persistableTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)|<span data-ttu-id="dbd5c-124">Collection d'éléments `persistableType`.</span><span class="sxs-lookup"><span data-stu-id="dbd5c-124">A collection of `persistableType` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dbd5c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbd5c-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>
- [<span data-ttu-id="dbd5c-126">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="dbd5c-126">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)
- [<span data-ttu-id="dbd5c-127">Intégration à des applications COM+</span><span class="sxs-lookup"><span data-stu-id="dbd5c-127">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="dbd5c-128">Guide pratique pour Configurer les paramètres de Service COM +</span><span class="sxs-lookup"><span data-stu-id="dbd5c-128">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
