---
title: '&lt;windows&gt;, élément de &lt;clientCredentials&gt;'
ms.date: 03/30/2017
ms.assetid: 793e41c2-31ea-4159-abbc-2123bf097233
ms.openlocfilehash: 780d73b747feae5495ad08cb2324e7d8f8de0d7d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147471"
---
# <a name="ltwindowsgt-of-ltclientcredentialsgt-element"></a><span data-ttu-id="fa8dc-102">&lt;windows&gt;, élément de &lt;clientCredentials&gt;</span><span class="sxs-lookup"><span data-stu-id="fa8dc-102">&lt;windows&gt; of &lt;clientCredentials&gt; Element</span></span>
<span data-ttu-id="fa8dc-103">Spécifie les paramètres pour des informations d'identification Windows à utiliser pour représenter le client.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-103">Specifies the settings for a Windows credential to be used to represent the client.</span></span>  
  
 <span data-ttu-id="fa8dc-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="fa8dc-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="fa8dc-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="fa8dc-105">\<behaviors></span></span>  
<span data-ttu-id="fa8dc-106">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="fa8dc-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="fa8dc-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="fa8dc-107">\<behavior></span></span>  
<span data-ttu-id="fa8dc-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="fa8dc-108">\<clientCredentials></span></span>  
<span data-ttu-id="fa8dc-109">\<Windows ></span><span class="sxs-lookup"><span data-stu-id="fa8dc-109">\<windows></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa8dc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa8dc-110">Syntax</span></span>  
  
```xml  
<windows allowedImpersonationLevel="Identification/Impersonation/Delegation/Anonymous/None"
         allowNtlm="Boolean" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fa8dc-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fa8dc-111">Attributes and Elements</span></span>  
 <span data-ttu-id="fa8dc-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fa8dc-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="fa8dc-113">Attributes</span></span>  
  
|<span data-ttu-id="fa8dc-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="fa8dc-114">Attribute</span></span>|<span data-ttu-id="fa8dc-115">Description</span><span class="sxs-lookup"><span data-stu-id="fa8dc-115">Description</span></span>|  
|---------------|-----------------|  
|`allowedImpersonationLevel`|<span data-ttu-id="fa8dc-116">Définit la préférence d'emprunt d'identité que le client communique au serveur.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-116">Sets the impersonation preference that the client communicates to the server.</span></span> <span data-ttu-id="fa8dc-117">Le mode d'emprunt d'identité que le client sélectionne n'est pas appliqué sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-117">The impersonation mode that the client selects is not enforced on the server.</span></span> <span data-ttu-id="fa8dc-118">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa8dc-118">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="fa8dc-119">-Identification : Le serveur peut obtenir l’identité et les privilèges du client, mais ne peut pas représenter le client.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-119">-   Identification: The server can get the identity and privileges of the client, but cannot impersonate the client.</span></span><br /><span data-ttu-id="fa8dc-120">-L’emprunt d’identité : Le serveur peut emprunter l’identité de contexte de sécurité du client sur le système local.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-120">-   Impersonation: The server can impersonate the client's security context on the local system.</span></span><br /><span data-ttu-id="fa8dc-121">-Délégation : Le serveur peut emprunter l’identité de contexte de sécurité du client sur des systèmes distants.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-121">-   Delegation: The server can impersonate the client's security context on remote systems.</span></span><br /><span data-ttu-id="fa8dc-122">-Anonyme : Le serveur ne peut pas emprunter l’identité ou identifier le client.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-122">-   Anonymous: The server cannot impersonate or identify the client.</span></span><br /><span data-ttu-id="fa8dc-123">-None : Un niveau d’emprunt d’identité n’est pas affecté.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-123">-   None: An impersonation level is not assigned.</span></span><br /><br /> <span data-ttu-id="fa8dc-124">La valeur par défaut est Identification.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-124">The default is Identification.</span></span> <span data-ttu-id="fa8dc-125">Cet attribut est de type <xref:System.Security.Principal.TokenImpersonationLevel>.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-125">This attribute is of type <xref:System.Security.Principal.TokenImpersonationLevel>.</span></span>|  
|`allowNtlm`|<span data-ttu-id="fa8dc-126">L'affectation de la valeur `true` à cette propriété permet de rétrograder l'authentification à NTLM si Kerberos n'est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-126">Setting this property to `true` allows authentication to downgrade to NTLM if Kerberos is not available.</span></span><br /><br /> <span data-ttu-id="fa8dc-127">Si cette propriété `false` provoque Windows Communication Foundation (WCF) pour rendre un meilleur effort pour lever une exception si NTLM est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-127">Setting this property to `false` causes Windows Communication Foundation (WCF) to make a best-effort to throw an exception if NTLM is used.</span></span> <span data-ttu-id="fa8dc-128">Notez que l'affectation de la valeur `false` à cette propriété peut ne pas empêcher la transmission des informations d'identification NTLM.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-128">Note that setting this property to `false` may not prevent NTLM credentials from being sent over the wire.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fa8dc-129">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fa8dc-129">Child Elements</span></span>  
 <span data-ttu-id="fa8dc-130">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-130">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fa8dc-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fa8dc-131">Parent Elements</span></span>  
  
|<span data-ttu-id="fa8dc-132">Élément</span><span class="sxs-lookup"><span data-stu-id="fa8dc-132">Element</span></span>|<span data-ttu-id="fa8dc-133">Description</span><span class="sxs-lookup"><span data-stu-id="fa8dc-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fa8dc-134">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="fa8dc-134">\<clientCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|<span data-ttu-id="fa8dc-135">Spécifie les informations d'identification utilisées pour authentifier le client auprès du service.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-135">Specifies the credentials used to authenticate the client to the service.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fa8dc-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-136">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.WindowsClientElement>  
 <xref:System.ServiceModel.Configuration.ClientCredentialsElement>  
 <xref:System.ServiceModel.Description.ClientCredentials>  
 <xref:System.ServiceModel.Configuration.ClientCredentialsElement.Windows%2A>  
 <xref:System.ServiceModel.Description.ClientCredentials>  
 <xref:System.ServiceModel.Description.ClientCredentials.Windows%2A>  
 <xref:System.ServiceModel.Security.WindowsClientCredential>  
 [<span data-ttu-id="fa8dc-137">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="fa8dc-137">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)  
 [<span data-ttu-id="fa8dc-138">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="fa8dc-138">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [<span data-ttu-id="fa8dc-139">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="fa8dc-139">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
