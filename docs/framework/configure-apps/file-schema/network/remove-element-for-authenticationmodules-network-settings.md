---
title: '&lt;supprimer&gt; , élément d’authenticationModules (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules/remove
- http://schemas.microsoft.com/.NetConfiguration/v2.0#remove
helpviewer_keywords:
- remove element, authenticationModules
- <authenticationModules>, remove element
- <remove> element, authenticationModules
- authenticationModules, remove element
ms.assetid: abf79949-b05c-465a-b51c-bbeda9a74173
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 332f8eb4fb1a5a02df76c5745522037b029a2407
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48028535"
---
# <a name="ltremovegt-element-for-authenticationmodules-network-settings"></a><span data-ttu-id="5af3f-102">&lt;supprimer&gt; , élément d’authenticationModules (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="5af3f-102">&lt;remove&gt; Element for authenticationModules (Network Settings)</span></span>
<span data-ttu-id="5af3f-103">Supprime un module d’authentification de l’application.</span><span class="sxs-lookup"><span data-stu-id="5af3f-103">Removes an authentication module from the application.</span></span>  
  
 <span data-ttu-id="5af3f-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="5af3f-104">\<configuration></span></span>  
<span data-ttu-id="5af3f-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="5af3f-105">\<system.net></span></span>  
<span data-ttu-id="5af3f-106">\<authenticationModules ></span><span class="sxs-lookup"><span data-stu-id="5af3f-106">\<authenticationModules></span></span>  
<span data-ttu-id="5af3f-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="5af3f-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5af3f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5af3f-108">Syntax</span></span>  
  
```xml  
<remove   
   type="authentication module name"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5af3f-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5af3f-109">Attributes and Elements</span></span>  
 <span data-ttu-id="5af3f-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5af3f-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5af3f-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="5af3f-111">Attributes</span></span>  
  
|<span data-ttu-id="5af3f-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5af3f-112">**Attribute**</span></span>|<span data-ttu-id="5af3f-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="5af3f-113">**Description**</span></span>|  
|-------------------|---------------------|  
|<span data-ttu-id="5af3f-114">**type**</span><span class="sxs-lookup"><span data-stu-id="5af3f-114">**type**</span></span>|<span data-ttu-id="5af3f-115">Le nom du module d’authentification à supprimer.</span><span class="sxs-lookup"><span data-stu-id="5af3f-115">The name of the authentication module to remove.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5af3f-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5af3f-116">Child Elements</span></span>  
 <span data-ttu-id="5af3f-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5af3f-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5af3f-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5af3f-118">Parent Elements</span></span>  
  
|<span data-ttu-id="5af3f-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5af3f-119">**Element**</span></span>|<span data-ttu-id="5af3f-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="5af3f-120">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="5af3f-121">authenticationModules</span><span class="sxs-lookup"><span data-stu-id="5af3f-121">authenticationModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/authenticationmodules-element-network-settings.md)|<span data-ttu-id="5af3f-122">Spécifie les modules utilisés pour authentifier les demandes du réseau.</span><span class="sxs-lookup"><span data-stu-id="5af3f-122">Specifies modules used to authenticate network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5af3f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="5af3f-123">Remarks</span></span>  
 <span data-ttu-id="5af3f-124">Le `remove` élément supprime les modules d’authentification qui ont été définis précédemment dans le fichier de configuration ou à un niveau supérieur dans la hiérarchie de configuration.</span><span class="sxs-lookup"><span data-stu-id="5af3f-124">The `remove` element removes authentication modules that were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>  
  
 <span data-ttu-id="5af3f-125">La valeur de la `type` attribut doit être un nom de classe valide.</span><span class="sxs-lookup"><span data-stu-id="5af3f-125">The value for the `type` attribute should be a valid class name.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="5af3f-126">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="5af3f-126">Configuration Files</span></span>  
 <span data-ttu-id="5af3f-127">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="5af3f-127">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5af3f-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="5af3f-128">Example</span></span>  
 <span data-ttu-id="5af3f-129">L’exemple suivant supprime un module d’authentification.</span><span class="sxs-lookup"><span data-stu-id="5af3f-129">The following example removes an authentication module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <remove type="System.Net.NtlmClient" />  
    </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="5af3f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5af3f-130">See Also</span></span>  
 <xref:System.Net.IAuthenticationModule>  
 <xref:System.Net.AuthenticationManager>  
 [<span data-ttu-id="5af3f-131">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="5af3f-131">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
