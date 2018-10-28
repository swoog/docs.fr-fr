---
title: Schéma des paramètres d’application
ms.date: 05/01/2017
helpviewer_keywords:
- schema app settings
- app settings, schema [Windows Forms]
- Windows Forms, app settings schema
- configuration schema [.NET Framework], app settings
ms.assetid: 99347d62-3ea5-40b6-bfec-c31431011422
author: guardrex
ms.author: mairaw
ms.openlocfilehash: 9bf2568c8c18f8f6d18c445e802cc72df18fb8c4
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50191142"
---
# <a name="app-settings-schema"></a><span data-ttu-id="0f269-102">Schéma des paramètres d’application</span><span class="sxs-lookup"><span data-stu-id="0f269-102">App Settings schema</span></span>

<span data-ttu-id="0f269-103">Contient des paramètres d’application personnalisés, tels que des chemins d’accès, des URL de service web XML ou d’autres informations de configuration personnalisée pour une application.</span><span class="sxs-lookup"><span data-stu-id="0f269-103">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span>

<span data-ttu-id="0f269-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="0f269-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="0f269-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="0f269-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span></span>  
<span data-ttu-id="0f269-106">&nbsp;&nbsp;&nbsp;&nbsp;[**\<add>**](~/docs/framework/configure-apps/file-schema/appsettings/add-element-for-appsettings.md) </span><span class="sxs-lookup"><span data-stu-id="0f269-106">&nbsp;&nbsp;&nbsp;&nbsp;[**\<add>**](~/docs/framework/configure-apps/file-schema/appsettings/add-element-for-appsettings.md) </span></span>  
<span data-ttu-id="0f269-107">&nbsp;&nbsp;&nbsp;&nbsp;[**\<clear>**](~/docs/framework/configure-apps/file-schema/appsettings/clear-element-for-appsettings.md) </span><span class="sxs-lookup"><span data-stu-id="0f269-107">&nbsp;&nbsp;&nbsp;&nbsp;[**\<clear>**](~/docs/framework/configure-apps/file-schema/appsettings/clear-element-for-appsettings.md) </span></span>  
<span data-ttu-id="0f269-108">&nbsp;&nbsp;&nbsp;&nbsp;[**\<remove>**](~/docs/framework/configure-apps/file-schema/appsettings/remove-element-for-appsettings.md)</span><span class="sxs-lookup"><span data-stu-id="0f269-108">&nbsp;&nbsp;&nbsp;&nbsp;[**\<remove>**](~/docs/framework/configure-apps/file-schema/appsettings/remove-element-for-appsettings.md)</span></span>

| <span data-ttu-id="0f269-109">Élément</span><span class="sxs-lookup"><span data-stu-id="0f269-109">Element</span></span> | <span data-ttu-id="0f269-110">Description</span><span class="sxs-lookup"><span data-stu-id="0f269-110">Description</span></span> |
| ------- | ----------- |
| [<span data-ttu-id="0f269-111">**\<appSettings>**</span><span class="sxs-lookup"><span data-stu-id="0f269-111">**\<appSettings>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) | <span data-ttu-id="0f269-112">Contient des balises **\<add>**, **\<clear>** et **\<remove>** pour contrôler les paramètres d’application.</span><span class="sxs-lookup"><span data-stu-id="0f269-112">Contains **\<add>**, **\<clear>**, and **\<remove>** tags to control application settings.</span></span> <span data-ttu-id="0f269-113">A un attribut **file** facultatif.</span><span class="sxs-lookup"><span data-stu-id="0f269-113">Has an optional **file** attribute.</span></span> |
| [<span data-ttu-id="0f269-114">**\<add>**</span><span class="sxs-lookup"><span data-stu-id="0f269-114">**\<add>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/add-element-for-appsettings.md) | <span data-ttu-id="0f269-115">Définit un paramètre.</span><span class="sxs-lookup"><span data-stu-id="0f269-115">Defines a setting.</span></span> <span data-ttu-id="0f269-116">Enfant de **\<appSettings>**.</span><span class="sxs-lookup"><span data-stu-id="0f269-116">Child of **\<appSettings>**.</span></span> <span data-ttu-id="0f269-117">Requiert des attributs **key** et **value**.</span><span class="sxs-lookup"><span data-stu-id="0f269-117">Requires **key** and **value** attributes.</span></span> |
| [<span data-ttu-id="0f269-118">**\<clear>**</span><span class="sxs-lookup"><span data-stu-id="0f269-118">**\<clear>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/clear-element-for-appsettings.md) | <span data-ttu-id="0f269-119">Efface tous les paramètres.</span><span class="sxs-lookup"><span data-stu-id="0f269-119">Clears all settings.</span></span> <span data-ttu-id="0f269-120">Enfant de **\<appSettings>**.</span><span class="sxs-lookup"><span data-stu-id="0f269-120">Child of **\<appSettings>**.</span></span> <span data-ttu-id="0f269-121">N’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0f269-121">Has no attributes.</span></span> |
| [<span data-ttu-id="0f269-122">**\<remove>**</span><span class="sxs-lookup"><span data-stu-id="0f269-122">**\<remove>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/remove-element-for-appsettings.md) | <span data-ttu-id="0f269-123">Supprime un paramètre.</span><span class="sxs-lookup"><span data-stu-id="0f269-123">Removes a setting.</span></span> <span data-ttu-id="0f269-124">Enfant de **\<appSettings>**.</span><span class="sxs-lookup"><span data-stu-id="0f269-124">Child of **\<appSettings>**.</span></span> <span data-ttu-id="0f269-125">Exige un attribut **key**.</span><span class="sxs-lookup"><span data-stu-id="0f269-125">Requires a **key** attribute.</span></span> |

## <a name="appsettings-element"></a><span data-ttu-id="0f269-126">\<appSettings>, élément</span><span class="sxs-lookup"><span data-stu-id="0f269-126">\<appSettings> element</span></span>

<span data-ttu-id="0f269-127">Cet élément contient des balises **\<add>**, **\<clear>** et **\<remove>** pour contrôler les paramètres d’application.</span><span class="sxs-lookup"><span data-stu-id="0f269-127">This element contains **\<add>**, **\<clear>**, and **\<remove>** tags to control application settings.</span></span> <span data-ttu-id="0f269-128">Il définit un attribut facultatif pour **file**.</span><span class="sxs-lookup"><span data-stu-id="0f269-128">It defines an optional attribute for **file**.</span></span>

## <a name="add-element"></a><span data-ttu-id="0f269-129">\<add>, élément</span><span class="sxs-lookup"><span data-stu-id="0f269-129">\<add> element</span></span>

<span data-ttu-id="0f269-130">Ajoute un paramètre d’application personnalisé en tant que paire nom/valeur à la collection de paramètres d’application.</span><span class="sxs-lookup"><span data-stu-id="0f269-130">Adds a custom application setting as a name/value pair to the application settings collection.</span></span> <span data-ttu-id="0f269-131">Il définit les attributs pour **key** et **value**.</span><span class="sxs-lookup"><span data-stu-id="0f269-131">It defines attributes for **key** and **value**.</span></span>

## <a name="clear-element"></a><span data-ttu-id="0f269-132">\<clear>, élément</span><span class="sxs-lookup"><span data-stu-id="0f269-132">\<clear> element</span></span>

<span data-ttu-id="0f269-133">Supprime toutes les références aux paramètres d’application personnalisés hérités et autorise uniquement les références ajoutées par les éléments **\<add>** suivant l’élément **\<clear>**.</span><span class="sxs-lookup"><span data-stu-id="0f269-133">Removes all references to inherited custom application settings and allows only the references that are added by **\<add>** elements following the **\<clear>** element.</span></span> <span data-ttu-id="0f269-134">Il ne définit aucun attribut.</span><span class="sxs-lookup"><span data-stu-id="0f269-134">It defines no attributes.</span></span>

## <a name="remove-element"></a><span data-ttu-id="0f269-135">\<remove>, élément</span><span class="sxs-lookup"><span data-stu-id="0f269-135">\<remove> element</span></span>

<span data-ttu-id="0f269-136">Supprime une référence à un paramètre d’application personnalisé hérité de la collection de paramètres d’application.</span><span class="sxs-lookup"><span data-stu-id="0f269-136">Removes a reference to an inherited custom application setting from the application settings collection.</span></span> <span data-ttu-id="0f269-137">Il définit un attribut pour **key**.</span><span class="sxs-lookup"><span data-stu-id="0f269-137">It defines an attribute for **key**.</span></span>

## <a name="example"></a><span data-ttu-id="0f269-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="0f269-138">Example</span></span>

<span data-ttu-id="0f269-139">L’exemple suivant montre un fichier de paramètres d’application externe (*custom.config*) qui définit un paramètre d’application personnalisé :</span><span class="sxs-lookup"><span data-stu-id="0f269-139">The following example shows an external application settings file (*custom.config*) that defines a custom application setting:</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<appSettings>
  <add key="MyCustomSetting" value="MyCustomSettingValue" />
</appSettings>
```

<span data-ttu-id="0f269-140">L’exemple suivant montre un fichier de configuration d’application qui consomme le paramètre dans le fichier de paramètres externes et définit un paramètre d’application qui lui est propre :</span><span class="sxs-lookup"><span data-stu-id="0f269-140">The following example shows an application configuration file that consumes the setting in the external settings file and sets an application setting of its own:</span></span>

```xml
<configuration>
  <appSettings file="custom.config">
    <add key="ApplicationName" value="MyApplication" />
  </appSettings>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="0f269-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f269-141">See also</span></span>

- [<span data-ttu-id="0f269-142">Vue d'ensemble des paramètres d'application</span><span class="sxs-lookup"><span data-stu-id="0f269-142">Application Settings Overview</span></span>](~/docs/framework/winforms/advanced/application-settings-overview.md)   
- [<span data-ttu-id="0f269-143">Architecture des paramètres d'application</span><span class="sxs-lookup"><span data-stu-id="0f269-143">Application Settings Architecture</span></span>](~/docs/framework/winforms/advanced/application-settings-architecture.md)
