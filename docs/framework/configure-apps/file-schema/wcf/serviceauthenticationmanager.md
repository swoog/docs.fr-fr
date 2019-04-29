---
title: <serviceAuthenticationManager>
ms.date: 03/30/2017
ms.assetid: 5d69e64f-f325-4d55-8e2d-0fb30f222dda
ms.openlocfilehash: 0940248364488bb38a329c5e461d72463c574e74
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670376"
---
# <a name="serviceauthenticationmanager"></a><span data-ttu-id="6adcc-101">\<serviceAuthenticationManager></span><span class="sxs-lookup"><span data-stu-id="6adcc-101">\<serviceAuthenticationManager></span></span>
<span data-ttu-id="6adcc-102">Fournit un élément de configuration de flux de travail qui établit au niveau du service la validité d'une transmission, d'un message ou d'un donneur d'ordre.</span><span class="sxs-lookup"><span data-stu-id="6adcc-102">Provides a workflow configuration element that establishes at the service level the validity of a transmission, message, or originator.</span></span>  
  
<span data-ttu-id="6adcc-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="6adcc-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="6adcc-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="6adcc-104">\<behaviors></span></span>  
<span data-ttu-id="6adcc-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="6adcc-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="6adcc-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="6adcc-106">\<behavior></span></span>  
<span data-ttu-id="6adcc-107">\<serviceAuthenticationManager></span><span class="sxs-lookup"><span data-stu-id="6adcc-107">\<serviceAuthenticationManager></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6adcc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6adcc-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <serviceAuthenticationManager serviceAuthenticationManagerType="String" />
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6adcc-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6adcc-109">Attributes and Elements</span></span>  
 <span data-ttu-id="6adcc-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6adcc-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6adcc-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="6adcc-111">Attributes</span></span>  
  
|<span data-ttu-id="6adcc-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="6adcc-112">Attribute</span></span>|<span data-ttu-id="6adcc-113">Description</span><span class="sxs-lookup"><span data-stu-id="6adcc-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6adcc-114">serviceAuthenticationManagerType</span><span class="sxs-lookup"><span data-stu-id="6adcc-114">serviceAuthenticationManagerType</span></span>|<span data-ttu-id="6adcc-115">Chaîne qui spécifie le type de la stratégie d'authentification pour le comportement actuel.</span><span class="sxs-lookup"><span data-stu-id="6adcc-115">A string that specifies the type of the authentication policy for the current behavior.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6adcc-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6adcc-116">Child Elements</span></span>  
 <span data-ttu-id="6adcc-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6adcc-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6adcc-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6adcc-118">Parent Elements</span></span>  
  
|<span data-ttu-id="6adcc-119">Élément</span><span class="sxs-lookup"><span data-stu-id="6adcc-119">Element</span></span>|<span data-ttu-id="6adcc-120">Description</span><span class="sxs-lookup"><span data-stu-id="6adcc-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6adcc-121">\<behavior></span><span class="sxs-lookup"><span data-stu-id="6adcc-121">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="6adcc-122">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="6adcc-122">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6adcc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6adcc-123">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceAuthenticationElement>
