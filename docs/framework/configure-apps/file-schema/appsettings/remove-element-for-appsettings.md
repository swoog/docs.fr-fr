---
title: <remove>, élément de <appSettings>
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/remove
helpviewer_keywords:
- remove Element
- <remove> Element
ms.assetid: 218c4464-e007-4539-803f-7c8b0a909fd8
author: guardrex
ms.author: mairaw
ms.openlocfilehash: cf9a34e47b70aaff12b29b9c5cf944d5bb15fee9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61705387"
---
# <a name="remove-element-for-appsettings"></a><span data-ttu-id="8d31c-102">\<Supprimer >, élément pour \<appSettings ></span><span class="sxs-lookup"><span data-stu-id="8d31c-102">\<remove> element for \<appSettings></span></span>

<span data-ttu-id="8d31c-103">Supprime les paramètres d’application personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8d31c-103">Removes custom application settings.</span></span>

<span data-ttu-id="8d31c-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="8d31c-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="8d31c-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="8d31c-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span></span>  
<span data-ttu-id="8d31c-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**</span><span class="sxs-lookup"><span data-stu-id="8d31c-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**</span></span>

## <a name="syntax"></a><span data-ttu-id="8d31c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d31c-107">Syntax</span></span>

```xml
<appSettings>
  <remove key="Key of custom setting" />
</appSettings>
```

### <a name="attribute"></a><span data-ttu-id="8d31c-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="8d31c-108">Attribute</span></span>

|         | <span data-ttu-id="8d31c-109">Description</span><span class="sxs-lookup"><span data-stu-id="8d31c-109">Description</span></span> |
| ------- | ----------- |
| <span data-ttu-id="8d31c-110">**key**</span><span class="sxs-lookup"><span data-stu-id="8d31c-110">**key**</span></span> | <span data-ttu-id="8d31c-111">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="8d31c-111">Required attribute.</span></span><br><br><span data-ttu-id="8d31c-112">Spécifie le nom de la clé à supprimer.</span><span class="sxs-lookup"><span data-stu-id="8d31c-112">Specifies the name of the key to remove.</span></span> |

### <a name="parent-element"></a><span data-ttu-id="8d31c-113">Élément parent</span><span class="sxs-lookup"><span data-stu-id="8d31c-113">Parent element</span></span>

|     | <span data-ttu-id="8d31c-114">Description</span><span class="sxs-lookup"><span data-stu-id="8d31c-114">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="8d31c-115">**\<appSettings>**</span><span class="sxs-lookup"><span data-stu-id="8d31c-115">**\<appSettings>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) | <span data-ttu-id="8d31c-116">Contient des paramètres d’application personnalisés, tels que des chemins d’accès, des URL de service web XML ou d’autres informations de configuration personnalisée pour une application.</span><span class="sxs-lookup"><span data-stu-id="8d31c-116">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="8d31c-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8d31c-117">Child elements</span></span>

<span data-ttu-id="8d31c-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8d31c-118">None</span></span>

## <a name="example"></a><span data-ttu-id="8d31c-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="8d31c-119">Example</span></span>

<span data-ttu-id="8d31c-120">L’exemple suivant montre comment supprimer un paramètre de configuration personnalisée pour `ApplicationName`:</span><span class="sxs-lookup"><span data-stu-id="8d31c-120">The following example shows how to remove a custom configuration setting for `ApplicationName`:</span></span>

```xml
<appSettings>
  <remove key="ApplicationName" />
</appSettings>
```

## <a name="see-also"></a><span data-ttu-id="8d31c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d31c-121">See also</span></span>

- [<span data-ttu-id="8d31c-122">Schéma de fichier de configuration pour le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="8d31c-122">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
