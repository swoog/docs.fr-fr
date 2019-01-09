---
title: '&lt;persistableType&gt;'
ms.date: 03/30/2017
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
ms.openlocfilehash: 92c59b3804e22c62340acccc1e12e594203c8e8b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145417"
---
# <a name="ltpersistabletypegt"></a><span data-ttu-id="b203e-102">&lt;persistableType&gt;</span><span class="sxs-lookup"><span data-stu-id="b203e-102">&lt;persistableType&gt;</span></span>
<span data-ttu-id="b203e-103">Spécifie tous les types persistants.</span><span class="sxs-lookup"><span data-stu-id="b203e-103">Specifies all the persistable types.</span></span>  
  
 <span data-ttu-id="b203e-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="b203e-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="b203e-105">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="b203e-105">\<comContracts></span></span>  
<span data-ttu-id="b203e-106">\<comContract ></span><span class="sxs-lookup"><span data-stu-id="b203e-106">\<comContract></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b203e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b203e-107">Syntax</span></span>  
  
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
  
## <a name="type"></a><span data-ttu-id="b203e-108">Type</span><span class="sxs-lookup"><span data-stu-id="b203e-108">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b203e-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b203e-109">Attributes and Elements</span></span>  
 <span data-ttu-id="b203e-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b203e-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b203e-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="b203e-111">Attributes</span></span>  
  
|<span data-ttu-id="b203e-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="b203e-112">Attribute</span></span>|<span data-ttu-id="b203e-113">Description</span><span class="sxs-lookup"><span data-stu-id="b203e-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b203e-114">id</span><span class="sxs-lookup"><span data-stu-id="b203e-114">id</span></span>|<span data-ttu-id="b203e-115">Attribut requis qui contient une chaîne spécifiant un identificateur unique pour un type persistant.</span><span class="sxs-lookup"><span data-stu-id="b203e-115">A required attribute that contains a string that specifies a unique identifier for a persistable type.</span></span>|  
|<span data-ttu-id="b203e-116">name</span><span class="sxs-lookup"><span data-stu-id="b203e-116">name</span></span>|<span data-ttu-id="b203e-117">Attribut facultatif qui contient une chaîne spécifiant le nom du type persistant.</span><span class="sxs-lookup"><span data-stu-id="b203e-117">An optional attribute that contains a string that specifies the name of the persistable type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b203e-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b203e-118">Child Elements</span></span>  
 <span data-ttu-id="b203e-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b203e-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b203e-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b203e-120">Parent Elements</span></span>  
  
|<span data-ttu-id="b203e-121">Élément</span><span class="sxs-lookup"><span data-stu-id="b203e-121">Element</span></span>|<span data-ttu-id="b203e-122">Description</span><span class="sxs-lookup"><span data-stu-id="b203e-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b203e-123">\<persistableTypes></span><span class="sxs-lookup"><span data-stu-id="b203e-123">\<persistableTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)|<span data-ttu-id="b203e-124">Collection d'éléments `persistableType`.</span><span class="sxs-lookup"><span data-stu-id="b203e-124">A collection of `persistableType` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b203e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b203e-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>  
 [<span data-ttu-id="b203e-126">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="b203e-126">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)  
 [<span data-ttu-id="b203e-127">Intégration à des applications COM+</span><span class="sxs-lookup"><span data-stu-id="b203e-127">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)  
 [<span data-ttu-id="b203e-128">Guide pratique pour Configurer les paramètres de Service COM +</span><span class="sxs-lookup"><span data-stu-id="b203e-128">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
