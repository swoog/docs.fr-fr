---
title: '&lt;securityTokenHandlerConfiguration&gt;'
ms.date: 03/30/2017
ms.assetid: 28724cc6-020c-4a06-9a1f-d7594f315019
author: BrucePerlerMS
ms.openlocfilehash: d66771ec7ed52ace52df6bb3bfafdcf9cce989b5
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48029322"
---
# <a name="ltsecuritytokenhandlerconfigurationgt"></a><span data-ttu-id="8c388-102">&lt;securityTokenHandlerConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="8c388-102">&lt;securityTokenHandlerConfiguration&gt;</span></span>
<span data-ttu-id="8c388-103">Fournit la configuration de la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="8c388-103">Provides configuration for the collection of token handlers.</span></span>  
  
 <span data-ttu-id="8c388-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="8c388-104">\<system.identityModel></span></span>  
<span data-ttu-id="8c388-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="8c388-105">\<identityConfiguration></span></span>  
<span data-ttu-id="8c388-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="8c388-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="8c388-107">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="8c388-107">\<securityTokenHandlerConfiguration></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8c388-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c388-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration saveBootstrapContext=xs:boolean  
          maximumClockSkew=TimeSpan>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8c388-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="8c388-109">Attributes and Elements</span></span>  
 <span data-ttu-id="8c388-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="8c388-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8c388-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="8c388-111">Attributes</span></span>  
  
|<span data-ttu-id="8c388-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="8c388-112">Attribute</span></span>|<span data-ttu-id="8c388-113">Description</span><span class="sxs-lookup"><span data-stu-id="8c388-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8c388-114">saveBootstrapContext</span><span class="sxs-lookup"><span data-stu-id="8c388-114">saveBootstrapContext</span></span>|<span data-ttu-id="8c388-115">Spécifie si les jetons de démarrage doivent être inclus dans le jeton de session.</span><span class="sxs-lookup"><span data-stu-id="8c388-115">Specifies whether bootstrap tokens should be included in the session token.</span></span> <span data-ttu-id="8c388-116">La valeur peut également être définie sur une collection de gestionnaires de jetons en définissant le `saveBootstrapContext` d’attribut sur le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément.</span><span class="sxs-lookup"><span data-stu-id="8c388-116">The value may also be set on a token handler collection by setting the `saveBootstrapContext` attribute on the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element.</span></span> <span data-ttu-id="8c388-117">Une valeur définie sur la collection de gestionnaires de jetons substitue à la valeur définie sur le service.</span><span class="sxs-lookup"><span data-stu-id="8c388-117">A value set on the token handler collection overrides the value set on the service.</span></span>|  
|<span data-ttu-id="8c388-118">maximumClockSkew</span><span class="sxs-lookup"><span data-stu-id="8c388-118">maximumClockSkew</span></span>|<span data-ttu-id="8c388-119">Un <xref:System.TimeSpan> qui spécifie le décalage d’horloge maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="8c388-119">A <xref:System.TimeSpan> that specifies the maximum allowed clock skew.</span></span> <span data-ttu-id="8c388-120">Contrôle le décalage d’horloge maximale autorisée lorsque vous effectuez des opérations de contrainte de temps, telles que la validation de l’heure d’expiration d’une session de connexion.</span><span class="sxs-lookup"><span data-stu-id="8c388-120">Controls the maximum allowed clock skew when performing time-sensitive operations, such as validating the expiration time of a sign-in session.</span></span> <span data-ttu-id="8c388-121">La valeur par défaut est 5 minutes, « 00 : 05:00 ».</span><span class="sxs-lookup"><span data-stu-id="8c388-121">The default is 5 minutes, "00:05:00".</span></span> <span data-ttu-id="8c388-122">Pour plus d’informations sur la spécification <xref:System.TimeSpan> valeurs, consultez [valeurs Timespan](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span><span class="sxs-lookup"><span data-stu-id="8c388-122">For more information about how to specify <xref:System.TimeSpan> values, see [Timespan Values](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span> <span data-ttu-id="8c388-123">Le décalage d’horloge maximale peut également être défini au niveau du service en définissant le `maximumClockSkew` d’attribut sur le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément.</span><span class="sxs-lookup"><span data-stu-id="8c388-123">The maximum clock skew may also be set at the service level by setting the `maximumClockSkew` attribute on the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element.</span></span> <span data-ttu-id="8c388-124">Une valeur définie sur la collection de gestionnaires de jetons substitue à la valeur définie sur le service.</span><span class="sxs-lookup"><span data-stu-id="8c388-124">A value set on the token handler collection overrides the value set on the service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8c388-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8c388-125">Child Elements</span></span>  
  
|<span data-ttu-id="8c388-126">Élément</span><span class="sxs-lookup"><span data-stu-id="8c388-126">Element</span></span>|<span data-ttu-id="8c388-127">Description</span><span class="sxs-lookup"><span data-stu-id="8c388-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8c388-128">\<audienceUris ></span><span class="sxs-lookup"><span data-stu-id="8c388-128">\<audienceUris></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/audienceuris.md)|<span data-ttu-id="8c388-129">Spécifie le jeu d’URI qui sont des identificateurs acceptables de cette partie de confiance.</span><span class="sxs-lookup"><span data-stu-id="8c388-129">Specifies the set of URIs that are acceptable identifiers of this relying party.</span></span> <span data-ttu-id="8c388-130">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8c388-130">Optional.</span></span>|  
|[<span data-ttu-id="8c388-131">\<met en cache ></span><span class="sxs-lookup"><span data-stu-id="8c388-131">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="8c388-132">Inscrit les caches utilisés pour la détection de relecture de jetons et de jetons de session.</span><span class="sxs-lookup"><span data-stu-id="8c388-132">Registers the caches used for session tokens and token replay detection.</span></span> <span data-ttu-id="8c388-133">Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8c388-133">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="8c388-134">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8c388-134">Optional.</span></span>|  
|[<span data-ttu-id="8c388-135">\<certificateValidation ></span><span class="sxs-lookup"><span data-stu-id="8c388-135">\<certificateValidation></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)|<span data-ttu-id="8c388-136">Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats.</span><span class="sxs-lookup"><span data-stu-id="8c388-136">Controls the settings that token handlers use to validate certificates.</span></span> <span data-ttu-id="8c388-137">Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8c388-137">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="8c388-138">Ces paramètres sont remplacés si un gestionnaire spécifique est configuré avec son propre validateur.</span><span class="sxs-lookup"><span data-stu-id="8c388-138">These settings are overridden if a specific handler is configured with its own validator.</span></span> <span data-ttu-id="8c388-139">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8c388-139">Optional.</span></span>|  
|[<span data-ttu-id="8c388-140">\<issuerNameRegistry ></span><span class="sxs-lookup"><span data-stu-id="8c388-140">\<issuerNameRegistry></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuernameregistry.md)|<span data-ttu-id="8c388-141">Configure le Registre de nom de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="8c388-141">Configures the issuer name registry that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="8c388-142">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8c388-142">Optional.</span></span>|  
|[<span data-ttu-id="8c388-143">\<issuerTokenResolver ></span><span class="sxs-lookup"><span data-stu-id="8c388-143">\<issuerTokenResolver></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuertokenresolver.md)|<span data-ttu-id="8c388-144">Inscrit le résolveur de jeton de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="8c388-144">Registers the issuer token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="8c388-145">Le programme de résolution de jeton de l’émetteur est utilisé pour résoudre le jeton de signature sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="8c388-145">The issuer token resolver is used to resolve the signing token on incoming tokens and messages.</span></span> <span data-ttu-id="8c388-146">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8c388-146">Optional.</span></span>|  
|[<span data-ttu-id="8c388-147">\<serviceTokenResolver ></span><span class="sxs-lookup"><span data-stu-id="8c388-147">\<serviceTokenResolver></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/servicetokenresolver.md)|<span data-ttu-id="8c388-148">Inscrit le résolveur de jeton de service qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="8c388-148">Registers the service token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="8c388-149">Le programme de résolution de jeton de service est utilisé pour résoudre le jeton de chiffrement sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="8c388-149">The service token resolver is used to resolve the encryption token on incoming tokens and messages.</span></span> <span data-ttu-id="8c388-150">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8c388-150">Optional.</span></span>|  
|[<span data-ttu-id="8c388-151">\<tokenReplayDetection ></span><span class="sxs-lookup"><span data-stu-id="8c388-151">\<tokenReplayDetection></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md)|<span data-ttu-id="8c388-152">Active la détection de relecture de jetons et spécifie le délai d’expiration pour les jetons.</span><span class="sxs-lookup"><span data-stu-id="8c388-152">Enables token replay detection and specifies the expiration time for tokens.</span></span> <span data-ttu-id="8c388-153">Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8c388-153">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="8c388-154">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8c388-154">Optional.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8c388-155">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8c388-155">Parent Elements</span></span>  
  
|<span data-ttu-id="8c388-156">Élément</span><span class="sxs-lookup"><span data-stu-id="8c388-156">Element</span></span>|<span data-ttu-id="8c388-157">Description</span><span class="sxs-lookup"><span data-stu-id="8c388-157">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8c388-158">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="8c388-158">\<securityTokenHandlers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|<span data-ttu-id="8c388-159">Spécifie une collection de gestionnaires de jetons de sécurité qui sont inscrits avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="8c388-159">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8c388-160">Notes</span><span class="sxs-lookup"><span data-stu-id="8c388-160">Remarks</span></span>  
 <span data-ttu-id="8c388-161">Cette section fournit des valeurs de propriété pour un <xref:System.IdentityModel.Tokens.SecurityTokenHandlerConfiguration> objet.</span><span class="sxs-lookup"><span data-stu-id="8c388-161">This section provides property values for a <xref:System.IdentityModel.Tokens.SecurityTokenHandlerConfiguration> object.</span></span> <span data-ttu-id="8c388-162">Paramètres configurés dans cette section remplacent ceux configurés sur le service.</span><span class="sxs-lookup"><span data-stu-id="8c388-162">Settings configured in this section override those configured on the service.</span></span> <span data-ttu-id="8c388-163">Certains de ces paramètres peuvent, à son tour, être substituée par les paramètres qui sont spécifiés lors de l’ajout d’un gestionnaire à la collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8c388-163">Some of these settings can, in turn, be overridden by settings that are specified when a handler is added to the security token handler collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8c388-164">Exemple</span><span class="sxs-lookup"><span data-stu-id="8c388-164">Example</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>   
      <securityTokenHandlerConfiguration>  
  
        <audienceUris>  
          <clear/>  
          <add value="http://www.example.com/myapp/" />  
        </audienceUris>  
  
        <issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel">  
          <trustedIssuers>  
            <add thumbprint="97249e1a … 4c9158de" name="contoso.com" />  
          </trustedIssuers>  
        </issuerNameRegistry>  
  
        <issuerTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
  
        <serviceTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```
