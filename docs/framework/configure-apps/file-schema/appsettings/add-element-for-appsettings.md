---
title: <add> (élément de <appSettings>)
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/add
helpviewer_keywords:
- add Element
- <add> Element
ms.assetid: 8734efdc-00f6-4a65-bba6-084c5bc65246
author: guardrex
ms.author: mairaw
ms.openlocfilehash: dde773dc722cf75da9d922ccf28af4bf4a09636c
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277470"
---
# <a name="add-element-for-appsettings"></a><span data-ttu-id="eea13-102">\<Ajouter > élément pour \<appSettings ></span><span class="sxs-lookup"><span data-stu-id="eea13-102">\<add> element for \<appSettings></span></span>

<span data-ttu-id="eea13-103">Ajoute un paramètre d’application personnalisé.</span><span class="sxs-lookup"><span data-stu-id="eea13-103">Adds a custom application setting.</span></span>

<span data-ttu-id="eea13-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="eea13-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="eea13-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="eea13-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span></span>  
<span data-ttu-id="eea13-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**</span><span class="sxs-lookup"><span data-stu-id="eea13-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**</span></span>

## <a name="syntax"></a><span data-ttu-id="eea13-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eea13-107">Syntax</span></span>

```xml
<appSettings>
  <add key="Key of custom setting" value="Value of custom setting" />
</appSettings>
```

## <a name="attributes"></a><span data-ttu-id="eea13-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="eea13-108">Attributes</span></span>

|           | <span data-ttu-id="eea13-109">Description</span><span class="sxs-lookup"><span data-stu-id="eea13-109">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="eea13-110">**key**</span><span class="sxs-lookup"><span data-stu-id="eea13-110">**key**</span></span>   | <span data-ttu-id="eea13-111">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="eea13-111">Required attribute.</span></span><br><br><span data-ttu-id="eea13-112">Spécifie le nom de la clé à ajouter.</span><span class="sxs-lookup"><span data-stu-id="eea13-112">Specifies the name of the key to add.</span></span> |
| <span data-ttu-id="eea13-113">**value**</span><span class="sxs-lookup"><span data-stu-id="eea13-113">**value**</span></span> | <span data-ttu-id="eea13-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="eea13-114">Required attribute.</span></span><br><br><span data-ttu-id="eea13-115">Spécifie la valeur de la clé à ajouter.</span><span class="sxs-lookup"><span data-stu-id="eea13-115">Specifies the value of the key to add.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="eea13-116">Élément parent</span><span class="sxs-lookup"><span data-stu-id="eea13-116">Parent element</span></span>

|     | <span data-ttu-id="eea13-117">Description</span><span class="sxs-lookup"><span data-stu-id="eea13-117">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="eea13-118">**\<appSettings>**</span><span class="sxs-lookup"><span data-stu-id="eea13-118">**\<appSettings>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) | <span data-ttu-id="eea13-119">Contient des paramètres d’application personnalisés, tels que des chemins d’accès, des URL de service web XML ou d’autres informations de configuration personnalisée pour une application.</span><span class="sxs-lookup"><span data-stu-id="eea13-119">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="eea13-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eea13-120">Child elements</span></span>

<span data-ttu-id="eea13-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eea13-121">None</span></span>

## <a name="example"></a><span data-ttu-id="eea13-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="eea13-122">Example</span></span>

<span data-ttu-id="eea13-123">L’exemple suivant montre comment ajouter un paramètre de configuration personnalisée pour le nom de l’application :</span><span class="sxs-lookup"><span data-stu-id="eea13-123">The following example shows how to add a custom configuration setting for the application's name:</span></span>

```xml
<appSettings>
  <add key="ApplicationName" value="MyApplication" />
</appSettings>
```

<span data-ttu-id="eea13-124">L’exemple suivant utilise le `<add>` élément pour définir les deux paramètres de compatibilité dans une application ASP.NET :</span><span class="sxs-lookup"><span data-stu-id="eea13-124">The following example uses the `<add>` element to define two compatibility settings in an ASP.NET application:</span></span>

```xml
<appSettings>
  <add key="AppContext.SetSwitch:Switch.System.Globalization.NoAsyncCurrentCulture" value="true" />
  <add key="AppContext.SetSwitch:Switch.System.Uri.DontEnableStrictRFC3986ReservedCharacterSets" value="true" />
</appSettings>
```

## <a name="see-also"></a><span data-ttu-id="eea13-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eea13-125">See also</span></span>

- [<span data-ttu-id="eea13-126">Schéma de fichier de configuration pour le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="eea13-126">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
