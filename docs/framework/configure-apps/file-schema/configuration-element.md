---
title: '&lt;configuration&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration
helpviewer_keywords:
- <configuration> element
- configuration element
- container tags, <configuration> element
ms.assetid: 2ec1c9dc-2e5c-4ef0-9958-81670ab88449
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 2a81e422c2e6d8c2d342821163f860c5cb54c083
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54583322"
---
# <a name="configuration-element"></a><span data-ttu-id="58a8d-102">\<configuration > élément</span><span class="sxs-lookup"><span data-stu-id="58a8d-102">\<configuration> element</span></span>

<span data-ttu-id="58a8d-103">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="58a8d-103">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>

<span data-ttu-id="58a8d-104">**\<configuration>**</span><span class="sxs-lookup"><span data-stu-id="58a8d-104">**\<configuration>**</span></span>

## <a name="syntax"></a><span data-ttu-id="58a8d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58a8d-105">Syntax</span></span>

```xml
<configuration>
  <!-- Configuration settings -->
</configuration>
```

## <a name="attributes"></a><span data-ttu-id="58a8d-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="58a8d-106">Attributes</span></span>

<span data-ttu-id="58a8d-107">Aucun.</span><span class="sxs-lookup"><span data-stu-id="58a8d-107">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="58a8d-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="58a8d-108">Parent element</span></span>

<span data-ttu-id="58a8d-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="58a8d-109">None</span></span>

## <a name="child-elements"></a><span data-ttu-id="58a8d-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="58a8d-110">Child elements</span></span>

|     | <span data-ttu-id="58a8d-111">Description</span><span class="sxs-lookup"><span data-stu-id="58a8d-111">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="58a8d-112">**\<assemblyBinding>**</span><span class="sxs-lookup"><span data-stu-id="58a8d-112">**\<assemblyBinding>**</span></span>](~/docs/framework/configure-apps/file-schema/assemblybinding-element-for-configuration.md) | <span data-ttu-id="58a8d-113">Spécifie la stratégie de liaison de l’assembly au niveau de la configuration.</span><span class="sxs-lookup"><span data-stu-id="58a8d-113">Specifies assembly binding policy at the configuration level.</span></span>|
| [<span data-ttu-id="58a8d-114">**\<démarrage >** schéma des paramètres</span><span class="sxs-lookup"><span data-stu-id="58a8d-114">**\<startup>** Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/startup/index.md) | <span data-ttu-id="58a8d-115">Tous les éléments du schéma des paramètres de démarrage.</span><span class="sxs-lookup"><span data-stu-id="58a8d-115">All elements in the startup settings schema.</span></span> |
| [<span data-ttu-id="58a8d-116">**\<runtime >** schéma des paramètres</span><span class="sxs-lookup"><span data-stu-id="58a8d-116">**\<runtime>** Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/runtime/index.md) | <span data-ttu-id="58a8d-117">Tous les éléments dans le schéma des paramètres d’exécution.</span><span class="sxs-lookup"><span data-stu-id="58a8d-117">All elements in the runtime settings schema.</span></span> |
| [<span data-ttu-id="58a8d-118">**\<system.runtime.remoting>** Settings Schema</span><span class="sxs-lookup"><span data-stu-id="58a8d-118">**\<system.runtime.remoting>** Settings Schema</span></span>](https://msdn.microsoft.com/dc2d1e62-9af7-4ca1-99fd-98b93bb4db9e) | <span data-ttu-id="58a8d-119">Tous les éléments dans le schéma de paramètres de communication à distance.</span><span class="sxs-lookup"><span data-stu-id="58a8d-119">All elements in the remoting settings schema.</span></span> |
| [<span data-ttu-id="58a8d-120">**\<system.Net >** schéma des paramètres</span><span class="sxs-lookup"><span data-stu-id="58a8d-120">**\<system.Net>** Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/network/index.md) | <span data-ttu-id="58a8d-121">Tous les éléments du schéma des paramètres réseau.</span><span class="sxs-lookup"><span data-stu-id="58a8d-121">All elements in the network settings schema.</span></span> |
| [<span data-ttu-id="58a8d-122">**\<cryptographySettings >** schéma des paramètres</span><span class="sxs-lookup"><span data-stu-id="58a8d-122">**\<cryptographySettings>** Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/cryptography/index.md) | <span data-ttu-id="58a8d-123">Tous les éléments du schéma des paramètres de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="58a8d-123">All elements in the crypto settings schema.</span></span> |
| [<span data-ttu-id="58a8d-124">**\<configuration >** schéma des Sections</span><span class="sxs-lookup"><span data-stu-id="58a8d-124">**\<configuration>** Sections Schema</span></span>](~/docs/framework/configure-apps/file-schema/configuration-sections-schema.md) | <span data-ttu-id="58a8d-125">Tous les éléments dans le schéma de paramètres de section de configuration.</span><span class="sxs-lookup"><span data-stu-id="58a8d-125">All elements in the configuration section settings schema.</span></span> |
| [<span data-ttu-id="58a8d-126">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="58a8d-126">Trace and Debug Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/trace-debug/index.md) | <span data-ttu-id="58a8d-127">Tous les éléments du schéma des paramètres de trace et debug.</span><span class="sxs-lookup"><span data-stu-id="58a8d-127">All elements in the trace and debug settings schema.</span></span> |
| <span data-ttu-id="58a8d-128">[Schéma de paramètres de Configuration ASP.NET](https://msdn.microsoft.com/library/b5ysx397(v=vs.100).aspx)</span><span class="sxs-lookup"><span data-stu-id="58a8d-128">[ASP.NET Configuration Settings Schema](https://msdn.microsoft.com/library/b5ysx397(v=vs.100).aspx)</span></span> | <span data-ttu-id="58a8d-129">Tous les éléments dans le schéma de configuration ASP.NET, qui inclut des éléments de configuration des applications et sites Web ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="58a8d-129">All elements in the ASP.NET configuration schema, which includes elements for configuring ASP.NET Web sites and applications.</span></span> <span data-ttu-id="58a8d-130">Utilisé dans *Web.config* fichiers.</span><span class="sxs-lookup"><span data-stu-id="58a8d-130">Used in *Web.config* files.</span></span> |
| [<span data-ttu-id="58a8d-131">**\<webServices>** Settings Schema</span><span class="sxs-lookup"><span data-stu-id="58a8d-131">**\<webServices>** Settings Schema</span></span>](https://msdn.microsoft.com/f84d6d55-1add-4eb7-ae46-33df5833ea2e) | <span data-ttu-id="58a8d-132">Tous les éléments du schéma des paramètres Web services.</span><span class="sxs-lookup"><span data-stu-id="58a8d-132">All elements in the Web services settings schema.</span></span> |
| [<span data-ttu-id="58a8d-133">Schéma des paramètres web</span><span class="sxs-lookup"><span data-stu-id="58a8d-133">Web Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/web/index.md) | <span data-ttu-id="58a8d-134">Tous les éléments du schéma des paramètres Web, qui inclut des éléments pour la configuration d'ASP.NET en vue d'une utilisation avec une application hôte telle qu'IIS.</span><span class="sxs-lookup"><span data-stu-id="58a8d-134">All elements in the Web settings schema, which includes elements for configuring how ASP.NET works with a host application such as IIS.</span></span> <span data-ttu-id="58a8d-135">Utilisé dans *aspnet.config* fichiers.</span><span class="sxs-lookup"><span data-stu-id="58a8d-135">Used in *aspnet.config* files.</span></span> |

## <a name="remarks"></a><span data-ttu-id="58a8d-136">Notes</span><span class="sxs-lookup"><span data-stu-id="58a8d-136">Remarks</span></span>

<span data-ttu-id="58a8d-137">Chaque fichier de configuration doit contenir exactement un  **\<configuration >** élément.</span><span class="sxs-lookup"><span data-stu-id="58a8d-137">Each configuration file must contain exactly one **\<configuration>** element.</span></span>

## <a name="see-also"></a><span data-ttu-id="58a8d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58a8d-138">See also</span></span>

- [<span data-ttu-id="58a8d-139">Schéma de fichier de configuration pour le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="58a8d-139">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
