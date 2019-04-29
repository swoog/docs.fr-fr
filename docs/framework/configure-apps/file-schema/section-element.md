---
title: <section> d'élément
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections/section
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections/sectionGroup/section
helpviewer_keywords:
- section Element
- <section> Element
ms.assetid: ec7d4110-2403-47ac-8218-499bfe9d5ddb
author: guardrex
ms.author: mairaw
ms.openlocfilehash: 58f823ce0c128f30e361b4a631d41286533b5f0f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61701500"
---
# <a name="section-element"></a><span data-ttu-id="0b483-102">\<section > élément</span><span class="sxs-lookup"><span data-stu-id="0b483-102">\<section> element</span></span>

<span data-ttu-id="0b483-103">Contient une déclaration de section de configuration.</span><span class="sxs-lookup"><span data-stu-id="0b483-103">Contains a configuration section declaration.</span></span>

<span data-ttu-id="0b483-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="0b483-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="0b483-105">&nbsp;&nbsp;[**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="0b483-105">&nbsp;&nbsp;[**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) </span></span>  
<span data-ttu-id="0b483-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<section>**</span><span class="sxs-lookup"><span data-stu-id="0b483-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<section>**</span></span>

<span data-ttu-id="0b483-107">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="0b483-107">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="0b483-108">&nbsp;&nbsp;[**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="0b483-108">&nbsp;&nbsp;[**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) </span></span>  
<span data-ttu-id="0b483-109">&nbsp;&nbsp;&nbsp;&nbsp;[**\<sectionGroup>**](~/docs/framework/configure-apps/file-schema/sectiongroup-element-for-configsections.md) </span><span class="sxs-lookup"><span data-stu-id="0b483-109">&nbsp;&nbsp;&nbsp;&nbsp;[**\<sectionGroup>**](~/docs/framework/configure-apps/file-schema/sectiongroup-element-for-configsections.md) </span></span>  
<span data-ttu-id="0b483-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<section>**</span><span class="sxs-lookup"><span data-stu-id="0b483-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<section>**</span></span>

## <a name="syntax"></a><span data-ttu-id="0b483-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b483-111">Syntax</span></span>

```xml
<section name="section name"
         type="configuration section handler class, assembly"
         allowDefinition="Everywhere|MachineOnly|MachineToApplication" 
         allowLocation="true|false" />
```

## <a name="required-attributes"></a><span data-ttu-id="0b483-112">Attributs requis</span><span class="sxs-lookup"><span data-stu-id="0b483-112">Required attributes</span></span>

|           | <span data-ttu-id="0b483-113">Description</span><span class="sxs-lookup"><span data-stu-id="0b483-113">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="0b483-114">**name**</span><span class="sxs-lookup"><span data-stu-id="0b483-114">**name**</span></span>  | <span data-ttu-id="0b483-115">Spécifie le nom de la section de configuration.</span><span class="sxs-lookup"><span data-stu-id="0b483-115">Specifies the name of the configuration section.</span></span> |
| <span data-ttu-id="0b483-116">**type**</span><span class="sxs-lookup"><span data-stu-id="0b483-116">**type**</span></span>  | <span data-ttu-id="0b483-117">Spécifie le nom de la classe de gestionnaire de section de configuration qui lit la section du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="0b483-117">Specifies the name of the configuration section handler class that reads the section from the configuration file.</span></span> <span data-ttu-id="0b483-118">La valeur de type a la syntaxe « fully-qualified-section-handler-class-name, nom de l’assembly simple ».</span><span class="sxs-lookup"><span data-stu-id="0b483-118">The type value has the syntax "fully-qualified-section-handler-class-name, simple-assembly-name".</span></span> <span data-ttu-id="0b483-119">Le nom d’assembly simple est le nom de fichier racine sans le *.dll* extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="0b483-119">The simple assembly name is the root filename without the *.dll* file extension.</span></span> |

## <a name="optional-attributes"></a><span data-ttu-id="0b483-120">Attributs facultatifs</span><span class="sxs-lookup"><span data-stu-id="0b483-120">Optional attributes</span></span>

<span data-ttu-id="0b483-121">Les attributs suivants sont applicables uniquement pour les applications ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="0b483-121">The following attributes are applicable only for ASP.NET applications.</span></span> <span data-ttu-id="0b483-122">Le système de configuration ignore ces attributs pour les autres types d’application.</span><span class="sxs-lookup"><span data-stu-id="0b483-122">The configuration system ignores these attributes for other application types.</span></span>

|                     | <span data-ttu-id="0b483-123">Description</span><span class="sxs-lookup"><span data-stu-id="0b483-123">Description</span></span> |
| ------------------- | ----------- |
| <span data-ttu-id="0b483-124">**allowDefinition**</span><span class="sxs-lookup"><span data-stu-id="0b483-124">**allowDefinition**</span></span> | <span data-ttu-id="0b483-125">Spécifie la section peut être utilisée dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="0b483-125">Specifies which configuration file the section can be used in.</span></span> <span data-ttu-id="0b483-126">Utilisez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b483-126">Use one of the following values:</span></span><br><br><span data-ttu-id="0b483-127">**Partout**</span><span class="sxs-lookup"><span data-stu-id="0b483-127">**Everywhere**</span></span><br><span data-ttu-id="0b483-128">Permet à la section peut être utilisée dans n’importe quel fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="0b483-128">Allows the section to be used in any configuration file.</span></span> <span data-ttu-id="0b483-129">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0b483-129">This is the default.</span></span><br><span data-ttu-id="0b483-130">**MachineOnly**</span><span class="sxs-lookup"><span data-stu-id="0b483-130">**MachineOnly**</span></span><br><span data-ttu-id="0b483-131">La section peut être utilisé uniquement dans le fichier de configuration de machine (*Machine.config*).</span><span class="sxs-lookup"><span data-stu-id="0b483-131">Allows the section to be used only in the machine configuration file (*Machine.config*).</span></span><br><span data-ttu-id="0b483-132">**MachineToApplication**</span><span class="sxs-lookup"><span data-stu-id="0b483-132">**MachineToApplication**</span></span><br><span data-ttu-id="0b483-133">Permet à la section peut être utilisée dans le fichier de configuration machine ou le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="0b483-133">Allows the section to be used in the machine configuration file or the application configuration file.</span></span> |
| <span data-ttu-id="0b483-134">**allowLocation**</span><span class="sxs-lookup"><span data-stu-id="0b483-134">**allowLocation**</span></span>   | <span data-ttu-id="0b483-135">Détermine si la section peut être utilisée dans le  **\<emplacement >** élément.</span><span class="sxs-lookup"><span data-stu-id="0b483-135">Determines whether the section can be used within the **\<location>** element.</span></span> <span data-ttu-id="0b483-136">Utilisez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b483-136">Use one of the following values:</span></span><br><br><span data-ttu-id="0b483-137">**true**</span><span class="sxs-lookup"><span data-stu-id="0b483-137">**true**</span></span><br><span data-ttu-id="0b483-138">Permet à la section au sein de la  **\<emplacement >** élément.</span><span class="sxs-lookup"><span data-stu-id="0b483-138">Allows the section to be used within the **\<location>** element.</span></span> <span data-ttu-id="0b483-139">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0b483-139">This is the default.</span></span><br><span data-ttu-id="0b483-140">**false**</span><span class="sxs-lookup"><span data-stu-id="0b483-140">**false**</span></span><br><span data-ttu-id="0b483-141">N’autorise pas la section au sein de la  **\<emplacement >** élément.</span><span class="sxs-lookup"><span data-stu-id="0b483-141">Does not allow the section to be used within the **\<location>** element.</span></span> |

## <a name="parent-elements"></a><span data-ttu-id="0b483-142">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0b483-142">Parent elements</span></span>

|     | <span data-ttu-id="0b483-143">Description</span><span class="sxs-lookup"><span data-stu-id="0b483-143">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="0b483-144">**\<configSections >** élément</span><span class="sxs-lookup"><span data-stu-id="0b483-144">**\<configSections>** Element</span></span>](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) | <span data-ttu-id="0b483-145">Contient des déclarations d’espace de noms et de la section de configuration.</span><span class="sxs-lookup"><span data-stu-id="0b483-145">Contains configuration section and namespace declarations.</span></span> |
| [<span data-ttu-id="0b483-146">**\<sectionGroup >** élément</span><span class="sxs-lookup"><span data-stu-id="0b483-146">**\<sectionGroup>** Element</span></span>](~/docs/framework/configure-apps/file-schema/sectiongroup-element-for-configsections.md) | <span data-ttu-id="0b483-147">Définit un espace de noms pour les sections de configuration.</span><span class="sxs-lookup"><span data-stu-id="0b483-147">Defines a namespace for configuration sections.</span></span> |

> [!NOTE]
> <span data-ttu-id="0b483-148">Un  **\<section >** élément est un élément enfant du  **\<configSections >** ou  **\<sectionGroup >** mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="0b483-148">A **\<section>** element is a child element of either **\<configSections>** or **\<sectionGroup>** but not both.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0b483-149">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0b483-149">Child elements</span></span>

<span data-ttu-id="0b483-150">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0b483-150">None</span></span>

## <a name="remarks"></a><span data-ttu-id="0b483-151">Notes</span><span class="sxs-lookup"><span data-stu-id="0b483-151">Remarks</span></span>

<span data-ttu-id="0b483-152">Déclaration essentiellement d’une section de configuration définit un nouvel élément pour le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="0b483-152">Declaring a configuration section essentially defines a new element for the configuration file.</span></span> <span data-ttu-id="0b483-153">Le nouvel élément contient une configuration de gestionnaire de section de paramètres (autrement dit, une classe qui implémente le <xref:System.Configuration.IConfigurationSectionHandler> interface) lit.</span><span class="sxs-lookup"><span data-stu-id="0b483-153">The new element contains settings that a configuration section handler (that is, a class that implements the <xref:System.Configuration.IConfigurationSectionHandler> interface) reads.</span></span> <span data-ttu-id="0b483-154">Les attributs et les éléments enfants d’une section, que vous définissez varient selon le Gestionnaire de section que vous utilisez pour lire vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="0b483-154">The attributes and child elements of a section you define depend on the section handler you use to read your settings.</span></span>

<span data-ttu-id="0b483-155">Déclaration d’un gestionnaire de section de configuration dans le *Machine.config* fichier vous permet d’utiliser la section de configuration dans n’importe quel fichier de configuration d’application sur cet ordinateur, sauf si le **allowDefinition**attribut spécifie autrement.</span><span class="sxs-lookup"><span data-stu-id="0b483-155">Declaring a configuration section handler in the *Machine.config* file enables you to use the configuration section in any application configuration file on that computer, unless the **allowDefinition** attribute specifies otherwise.</span></span>

## <a name="example"></a><span data-ttu-id="0b483-156">Exemple</span><span class="sxs-lookup"><span data-stu-id="0b483-156">Example</span></span>

<span data-ttu-id="0b483-157">L’exemple suivant montre comment définir une section de configuration et de définir les paramètres de cette section :</span><span class="sxs-lookup"><span data-stu-id="0b483-157">The following example shows how to define a configuration section and define settings for that section:</span></span>

```xml
<configuration>
  <configSections>
    <section name="sampleSection"
             type="System.Configuration.SingleTagSectionHandler" 
             allowLocation="false" />
  </configSections>
  <sampleSection setting1="Value1" 
                 setting2="value two" 
                 setting3="third value" />
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="0b483-158">fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="0b483-158">Configuration file</span></span>

<span data-ttu-id="0b483-159">Cet élément peut être utilisé dans le fichier de configuration d’application, fichier de configuration machine (*Machine.config*), et *Web.config* fichiers qui ne sont pas au niveau du répertoire d’application.</span><span class="sxs-lookup"><span data-stu-id="0b483-159">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b483-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b483-160">See also</span></span>

- [<span data-ttu-id="0b483-161">Schéma de fichier de configuration pour le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="0b483-161">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
