---
title: <secureConversationAuthentication> de <serviceCredential>
ms.date: 03/30/2017
ms.assetid: 0bd3fac7-befd-4a45-ba51-c200b33be0fd
ms.openlocfilehash: 13e9312e4c4eade003fec77909a743009aa9bca7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278523"
---
# <a name="secureconversationauthentication-of-servicecredential"></a><span data-ttu-id="7698f-102">\<secureConversationAuthentication > de \<serviceCredential ></span><span class="sxs-lookup"><span data-stu-id="7698f-102">\<secureConversationAuthentication> of \<serviceCredential></span></span>
<span data-ttu-id="7698f-103">Spécifie les paramètres pour un service de conversation sécurisé.</span><span class="sxs-lookup"><span data-stu-id="7698f-103">Specifies the settings for a secure conversation service.</span></span>  
  
 <span data-ttu-id="7698f-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="7698f-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="7698f-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="7698f-105">\<behaviors></span></span>  
<span data-ttu-id="7698f-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="7698f-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="7698f-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="7698f-107">\<behavior></span></span>  
<span data-ttu-id="7698f-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="7698f-108">\<serviceCredentials></span></span>  
<span data-ttu-id="7698f-109">\<secureConversationAuthentication></span><span class="sxs-lookup"><span data-stu-id="7698f-109">\<secureConversationAuthentication></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7698f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7698f-110">Syntax</span></span>  
  
```xml  
<secureConversationAuthentication securityStateEncoderType="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7698f-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7698f-111">Attributes and Elements</span></span>  
 <span data-ttu-id="7698f-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7698f-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7698f-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="7698f-113">Attributes</span></span>  
  
|<span data-ttu-id="7698f-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="7698f-114">Attribute</span></span>|<span data-ttu-id="7698f-115">Description</span><span class="sxs-lookup"><span data-stu-id="7698f-115">Description</span></span>|  
|---------------|-----------------|  
|`securityStateEncoderType`|<span data-ttu-id="7698f-116">Chaîne qui spécifie le type de <xref:System.ServiceModel.Security.SecurityStateEncoder> à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7698f-116">A string that specifies the type of <xref:System.ServiceModel.Security.SecurityStateEncoder> to be used.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7698f-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7698f-117">Child Elements</span></span>  
 <span data-ttu-id="7698f-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7698f-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7698f-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7698f-119">Parent Elements</span></span>  
  
|<span data-ttu-id="7698f-120">Élément</span><span class="sxs-lookup"><span data-stu-id="7698f-120">Element</span></span>|<span data-ttu-id="7698f-121">Description</span><span class="sxs-lookup"><span data-stu-id="7698f-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7698f-122">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="7698f-122">\<serviceCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|<span data-ttu-id="7698f-123">Spécifie les informations d’identification à utiliser pour authentifier le service, ainsi que les paramètres liés à la validation des informations d’identification du client.</span><span class="sxs-lookup"><span data-stu-id="7698f-123">Specifies the credential to be used in authenticating the service, and the client credential validation-related settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7698f-124">Notes</span><span class="sxs-lookup"><span data-stu-id="7698f-124">Remarks</span></span>  
 <span data-ttu-id="7698f-125">Utilisez cet élément de configuration pour spécifier la liste des types de revendication connus pour la sérialisation des cookies SCT (Security Context Token), ainsi qu'un encodeur pour encoder et sécuriser les informations de cookies.</span><span class="sxs-lookup"><span data-stu-id="7698f-125">Use this configuration element to specify a list of known claim types for the Security Context Token (SCT) cookies serialization, as well as an encoder to encode and secure cookies information.</span></span> <span data-ttu-id="7698f-126">Pour plus d'informations sur SCT, consultez <xref:System.ServiceModel.Security.SecureConversationServiceCredential>.</span><span class="sxs-lookup"><span data-stu-id="7698f-126">For more information on SCT, see <xref:System.ServiceModel.Security.SecureConversationServiceCredential>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7698f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7698f-127">See also</span></span>
- <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.SecureConversationAuthentication%2A>
- <xref:System.ServiceModel.Description.ServiceCredentials.SecureConversationAuthentication%2A>
- <xref:System.ServiceModel.Security.SecureConversationServiceCredential>
