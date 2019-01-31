---
title: <system.identityModel>
ms.date: 03/30/2017
ms.assetid: 210ce7e9-d07b-400c-800f-5f525dcf95e8
author: BrucePerlerMS
ms.openlocfilehash: fd17c0318480f5e157c8c9114116735b82bbfcef
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55257497"
---
# <a name="systemidentitymodel"></a><span data-ttu-id="8d4a4-102">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="8d4a4-102">\<system.identityModel></span></span>
<span data-ttu-id="8d4a4-103">Fournit la configuration permettant d’activer les options de Windows Identity Foundation (WIF) dans les applications.</span><span class="sxs-lookup"><span data-stu-id="8d4a4-103">Provides configuration for enabling Windows Identity Foundation (WIF) options in applications.</span></span>  
  
 <span data-ttu-id="8d4a4-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="8d4a4-104">\<system.identityModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8d4a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d4a4-105">Syntax</span></span>  
  
```xml  
<system.identityModel>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8d4a4-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="8d4a4-106">Attributes and Elements</span></span>  
 <span data-ttu-id="8d4a4-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="8d4a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8d4a4-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="8d4a4-108">Attributes</span></span>  
 <span data-ttu-id="8d4a4-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8d4a4-109">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="8d4a4-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8d4a4-110">Child Elements</span></span>  
  
|<span data-ttu-id="8d4a4-111">Élément</span><span class="sxs-lookup"><span data-stu-id="8d4a4-111">Element</span></span>|<span data-ttu-id="8d4a4-112">Description</span><span class="sxs-lookup"><span data-stu-id="8d4a4-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8d4a4-113">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="8d4a4-113">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="8d4a4-114">Spécifie les paramètres de l’identité de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="8d4a4-114">Specifies service-level identity settings.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8d4a4-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8d4a4-115">Parent Elements</span></span>  
  
|<span data-ttu-id="8d4a4-116">Élément</span><span class="sxs-lookup"><span data-stu-id="8d4a4-116">Element</span></span>|<span data-ttu-id="8d4a4-117">Description</span><span class="sxs-lookup"><span data-stu-id="8d4a4-117">Description</span></span>|  
|-------------|-----------------|  
|`<configuration>`|<span data-ttu-id="8d4a4-118">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8d4a4-118">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8d4a4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8d4a4-119">Remarks</span></span>  
 <span data-ttu-id="8d4a4-120">Ajouter un `<system.identityModel>` section au fichier de configuration pour configurer un service ou une application à utiliser Windows Identity Foundation (WIF).</span><span class="sxs-lookup"><span data-stu-id="8d4a4-120">Add a `<system.identityModel>` section to the configuration file to configure a service or application to use Windows Identity Foundation (WIF).</span></span> <span data-ttu-id="8d4a4-121">Le `<system.identityModel>` élément est représenté par la <xref:System.IdentityModel.Configuration.SystemIdentityModelSection> classe.</span><span class="sxs-lookup"><span data-stu-id="8d4a4-121">The `<system.identityModel>` element is represented by the <xref:System.IdentityModel.Configuration.SystemIdentityModelSection> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8d4a4-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="8d4a4-122">Example</span></span>  
 <span data-ttu-id="8d4a4-123">L’exemple suivant montre comment ajouter un `<system.identityModel>` section dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="8d4a4-123">The following example shows how to add a `<system.identityModel>` section to a configuration file.</span></span> <span data-ttu-id="8d4a4-124">Vous devez d’abord ajouter la déclaration d’espace de noms et de la section configuration sous la `<configSections>` élément.</span><span class="sxs-lookup"><span data-stu-id="8d4a4-124">You must first add the configuration section and namespace declaration under the `<configSections>` element.</span></span> <span data-ttu-id="8d4a4-125">Vous pouvez ensuite ajouter le `<system.IdentityModel>` élément à votre fichier de configuration pour spécifier une ou plusieurs configurations d’identité.</span><span class="sxs-lookup"><span data-stu-id="8d4a4-125">Then you can add the `<system.IdentityModel>` element to your configuration file to specify one or more identity configurations.</span></span>  
  
```xml  
<configuration>  
  <configSections>  
    <!--WIF 4.5 sections -->  
    <section name="system.identityModel" type="System.IdentityModel.Configuration.SystemIdentityModelSection, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089"/>  
    <section name="system.identityModel.services" type="System.IdentityModel.Services.Configuration.SystemIdentityModelServicesSection, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089"/>  
  </configSections>  
  
  ...  
  
  <system.identityModel>  
    <identityConfiguration>  
      <audienceUris>  
        <add value="http://localhost/WebApplication1/" />  
      </audienceUris>  
      <issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089">  
        <trustedIssuers>  
          <add thumbprint="313D3B … 9106A9EC" name="SelfSTS" />  
        </trustedIssuers>  
      </issuerNameRegistry>  
      <certificateValidation certificateValidationMode="None"/>  
    </identityConfiguration>  
  </system.identityModel>  
  
  ...  
  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8d4a4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d4a4-126">See also</span></span>
- <xref:System.IdentityModel.Configuration.SystemIdentityModelSection>
