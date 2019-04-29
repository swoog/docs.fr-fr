---
title: <remove>, élément de bypasslist (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist/remove
- http://schemas.microsoft.com/.NetConfiguration/v2.0#remove
helpviewer_keywords:
- <bypasslist>, remove element
- remove element, bypasslist
- bypasslist, remove element
- remove element, bypasslist
ms.assetid: 61dcfb4a-e3d9-4abf-a2cd-7d685fe2f64b
ms.openlocfilehash: a04cca3e57af5cc422776c5b2444a140e86f98b9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674465"
---
# <a name="remove-element-for-bypasslist-network-settings"></a><span data-ttu-id="9d6b7-102">\<Supprimer >, élément de bypasslist (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="9d6b7-102">\<remove> Element for bypasslist (Network Settings)</span></span>

<span data-ttu-id="9d6b7-103">Supprime une adresse IP ou le nom DNS de la liste de contournement proxy.</span><span class="sxs-lookup"><span data-stu-id="9d6b7-103">Removes an IP address or DNS name from the proxy bypass list.</span></span>

<span data-ttu-id="9d6b7-104">\<configuration>\\</span><span class="sxs-lookup"><span data-stu-id="9d6b7-104">\<configuration>\\</span></span>
<span data-ttu-id="9d6b7-105">\<system.net>\\</span><span class="sxs-lookup"><span data-stu-id="9d6b7-105">\<system.net>\\</span></span>
<span data-ttu-id="9d6b7-106">\<defaultProxy>\\</span><span class="sxs-lookup"><span data-stu-id="9d6b7-106">\<defaultProxy>\\</span></span>
<span data-ttu-id="9d6b7-107">\<BypassList > \\</span><span class="sxs-lookup"><span data-stu-id="9d6b7-107">\<bypasslist>\\</span></span>
<span data-ttu-id="9d6b7-108">\<remove></span><span class="sxs-lookup"><span data-stu-id="9d6b7-108">\<remove></span></span>

## <a name="syntax"></a><span data-ttu-id="9d6b7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d6b7-109">Syntax</span></span>

```xml
<remove
  address="regular expression"
/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="9d6b7-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9d6b7-110">Attributes and Elements</span></span>

<span data-ttu-id="9d6b7-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9d6b7-111">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="9d6b7-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="9d6b7-112">Attributes</span></span>

|<span data-ttu-id="9d6b7-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9d6b7-113">**Attribute**</span></span>|<span data-ttu-id="9d6b7-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="9d6b7-114">**Description**</span></span>|
|-------------------|---------------------|
|`address`|<span data-ttu-id="9d6b7-115">Une expression régulière décrivant une adresse IP ou un nom DNS.</span><span class="sxs-lookup"><span data-stu-id="9d6b7-115">A regular expression describing an IP address or DNS name.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="9d6b7-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9d6b7-116">Child Elements</span></span>

<span data-ttu-id="9d6b7-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9d6b7-117">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="9d6b7-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9d6b7-118">Parent Elements</span></span>

|<span data-ttu-id="9d6b7-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9d6b7-119">**Element**</span></span>|<span data-ttu-id="9d6b7-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="9d6b7-120">**Description**</span></span>|
|-----------------|---------------------|
|[<span data-ttu-id="9d6b7-121">bypasslist</span><span class="sxs-lookup"><span data-stu-id="9d6b7-121">bypasslist</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/bypasslist-element-network-settings.md)|<span data-ttu-id="9d6b7-122">Fournit un ensemble d’expressions régulières décrivant les adresses qui n’utilisent pas un proxy.</span><span class="sxs-lookup"><span data-stu-id="9d6b7-122">Provides a set of regular expressions that describe addresses that do not use a proxy.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9d6b7-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9d6b7-123">Remarks</span></span>

<span data-ttu-id="9d6b7-124">Le `remove` élément supprime des expressions régulières décrivant les adresses IP ou des noms de serveur DNS dans la liste des adresses qui contournent un serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="9d6b7-124">The `remove` element removes regular expressions describing IP addresses or DNS server names from the list of addresses that bypass a proxy server.</span></span> <span data-ttu-id="9d6b7-125">Les adresses ont été définis précédemment dans le fichier de configuration ou à un niveau supérieur dans la hiérarchie de configuration.</span><span class="sxs-lookup"><span data-stu-id="9d6b7-125">The addresses were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>

<span data-ttu-id="9d6b7-126">La valeur de la `address` attribut doit être une expression régulière qui décrit un ensemble d’adresses IP ou noms d’hôte.</span><span class="sxs-lookup"><span data-stu-id="9d6b7-126">The value for the `address` attribute should be a regular expression that describes a set of IP addresses or host names.</span></span>

<span data-ttu-id="9d6b7-127">Pour plus d’informations sur les expressions régulières, consultez. [Expressions régulières .NET framework](../../../../../docs/standard/base-types/regular-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="9d6b7-127">For more information about regular expressions, see .[.NET Framework Regular Expressions](../../../../../docs/standard/base-types/regular-expressions.md).</span></span>

## <a name="configuration-files"></a><span data-ttu-id="9d6b7-128">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="9d6b7-128">Configuration Files</span></span>

<span data-ttu-id="9d6b7-129">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="9d6b7-129">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>

## <a name="example"></a><span data-ttu-id="9d6b7-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="9d6b7-130">Example</span></span>

<span data-ttu-id="9d6b7-131">L’exemple suivant supprime toute définition précédente pour le domaine adventure-works.com, puis ajoute le domaine contoso.com à la liste de contournement.</span><span class="sxs-lookup"><span data-stu-id="9d6b7-131">The following example removes any previous definition for the adventure-works.com domain, and then adds the contoso.com domain to the bypass list.</span></span>

```xml
<configuration>
  <system.net>
    <defaultProxy>
      <bypasslist>
        <remove address="[a-z]+\.adventure-works\.com$" />
        <add address="[a-z]+\.contoso\.com$" />
      </bypasslist>
    </defaultProxy>
  </system.net>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="9d6b7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d6b7-132">See also</span></span>

- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [<span data-ttu-id="9d6b7-133">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="9d6b7-133">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
