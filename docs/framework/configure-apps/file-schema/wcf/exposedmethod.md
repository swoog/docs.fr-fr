---
title: <exposedMethod>
ms.date: 03/30/2017
ms.assetid: 61c938cd-4ee9-4b06-ab28-922ef491ab11
ms.openlocfilehash: 91eafa46aa73b5e6d359fcbe48f098f9f8a4d0f0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61644297"
---
# <a name="exposedmethod"></a><span data-ttu-id="06f6e-101">\<exposedMethod></span><span class="sxs-lookup"><span data-stu-id="06f6e-101">\<exposedMethod></span></span>
<span data-ttu-id="06f6e-102">Représente une méthode COM+ exposée lorsque l'interface sur un composant COM+ est exposée en tant que service Web.</span><span class="sxs-lookup"><span data-stu-id="06f6e-102">Represents a COM+ method that is exposed when the interface on a COM+ component is exposed as a Web service.</span></span>  
  
 <span data-ttu-id="06f6e-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="06f6e-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="06f6e-104">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="06f6e-104">\<comContracts></span></span>  
<span data-ttu-id="06f6e-105">\<comContract></span><span class="sxs-lookup"><span data-stu-id="06f6e-105">\<comContract></span></span>  
<span data-ttu-id="06f6e-106">\<methods></span><span class="sxs-lookup"><span data-stu-id="06f6e-106">\<methods></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06f6e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06f6e-107">Syntax</span></span>  
  
```xml  
<comContracts>
  <comContract>
    <exposedMethods>
      <exposedMethod name="String" />
    </exposedMethods>
  </comContract>
</comContracts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="06f6e-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="06f6e-108">Attributes and Elements</span></span>  
 <span data-ttu-id="06f6e-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="06f6e-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="06f6e-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="06f6e-110">Attributes</span></span>  
  
|<span data-ttu-id="06f6e-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="06f6e-111">Attribute</span></span>|<span data-ttu-id="06f6e-112">Description</span><span class="sxs-lookup"><span data-stu-id="06f6e-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="06f6e-113">name</span><span class="sxs-lookup"><span data-stu-id="06f6e-113">name</span></span>|<span data-ttu-id="06f6e-114">Chaîne qui contient la méthode COM+ exposée lorsque l'interface sur un composant COM+ est exposée comme un service Web.</span><span class="sxs-lookup"><span data-stu-id="06f6e-114">A string that contains the COM+ method that is exposed when the interface on a COM+ component is exposed as a Web service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="06f6e-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="06f6e-115">Child Elements</span></span>  
 <span data-ttu-id="06f6e-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="06f6e-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="06f6e-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="06f6e-117">Parent Elements</span></span>  
  
|<span data-ttu-id="06f6e-118">Élément</span><span class="sxs-lookup"><span data-stu-id="06f6e-118">Element</span></span>|<span data-ttu-id="06f6e-119">Description</span><span class="sxs-lookup"><span data-stu-id="06f6e-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="06f6e-120">\<exposedMethods></span><span class="sxs-lookup"><span data-stu-id="06f6e-120">\<exposedMethods></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethods.md)|<span data-ttu-id="06f6e-121">Une collection de [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) éléments.</span><span class="sxs-lookup"><span data-stu-id="06f6e-121">A collection of [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="06f6e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="06f6e-122">Remarks</span></span>  
 <span data-ttu-id="06f6e-123">Il est possible d'utiliser l'outil de configuration d'intégration COM+ (ComSvcConfig.exe) pour ajouter des méthodes spécifiques issues d'une interface COM afin qu'elles apparaissent sur le contrat de service généré.</span><span class="sxs-lookup"><span data-stu-id="06f6e-123">The COM+ integration configuration tool (ComSvcConfig.exe) can be used to add specific methods from a COM interface to appear on the generated service contract.</span></span>  
  
 <span data-ttu-id="06f6e-124">Par exemple, vous pouvez utiliser la commande suivante pour ajouter les trois méthodes nommées issues de l'interface COM `IFinances` sur le composant financier `ItemOrders` au contrat de service généré.</span><span class="sxs-lookup"><span data-stu-id="06f6e-124">For example, you can use the following command to add the three named methods from the `IFinances` COM interface on the `ItemOrders`.Financial component, to the generated service contract.</span></span>  
  
 `ComSvcConfig.exe /i /application:OnlineStore /contract:ItemOrders.Financial,IFinances.{TransferFunds,AddFunds,RemoveFunds} /hosting:complus`  
  
 <span data-ttu-id="06f6e-125">Lorsque vous exécutez également ComSvcConfig.exe, il génère le contrat de service suivant qui répertorie les méthodes mentionnées précédemment comme [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) éléments.</span><span class="sxs-lookup"><span data-stu-id="06f6e-125">When you also run the ComSvcConfig.exe, it then generates the following service contract listing the previously mentioned methods as [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span>  
  
```xml  
<comContract contractType="{C551FBA9-E3AA-4272-8C2A-84BD8D290AC7}"
             name="IFinances"
             namespace="http://contoso.com/services/financial">
  <exposedMethod name="TransferFunds"/>
  <exposedMethod name="AddFunds"/>
  <exposedMethod name="RemoveFunds"/>
</comContract>
```  
  
 <span data-ttu-id="06f6e-126">Au moment de l’initialisation du service, le runtime tente de générer un contrat de service en reflétant sur et en ajoutant uniquement les méthodes incluses dans la liste des [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) éléments.</span><span class="sxs-lookup"><span data-stu-id="06f6e-126">At service initialization time, the runtime attempts to generate a service contract by reflecting over and adding only the methods included in the list of [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span> <span data-ttu-id="06f6e-127">Une trace est produite pour chaque méthode d'interface qui n'est pas incluse sur le contrat de service.</span><span class="sxs-lookup"><span data-stu-id="06f6e-127">A trace is produced for every interface method that is not included on the service contract.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06f6e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06f6e-128">See also</span></span>

- <xref:System.ServiceModel.Configuration.ComMethodElementCollection>
- <xref:System.ServiceModel.Configuration.ComMethodElement>
- [<span data-ttu-id="06f6e-129">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="06f6e-129">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)
- [<span data-ttu-id="06f6e-130">Intégration à des applications COM+</span><span class="sxs-lookup"><span data-stu-id="06f6e-130">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="06f6e-131">Guide pratique pour Configurer les paramètres de Service COM +</span><span class="sxs-lookup"><span data-stu-id="06f6e-131">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
