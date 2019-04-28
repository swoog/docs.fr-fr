---
title: Élément personnalisé pour SingleTagSectionHandler
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName
helpviewer_keywords:
- custom element
ms.assetid: e62056c6-b351-40eb-afc0-cc13fc44e45e
author: guardrex
ms.author: mairaw
ms.openlocfilehash: bfc2a916e37ac27d45746eb268912b3752f4d80f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61705296"
---
# <a name="custom-element-for-singletagsectionhandler"></a><span data-ttu-id="cc06a-102">Élément personnalisé pour SingleTagSectionHandler</span><span class="sxs-lookup"><span data-stu-id="cc06a-102">Custom element for SingleTagSectionHandler</span></span>

<span data-ttu-id="cc06a-103">Définit les paramètres dans une section de configuration personnalisée qui est définie par un \<section > élément et utilise le <xref:System.Configuration.SingleTagSectionHandler> classe.</span><span class="sxs-lookup"><span data-stu-id="cc06a-103">Defines settings in a custom configuration section that is defined by a \<section> element and uses the <xref:System.Configuration.SingleTagSectionHandler> class.</span></span>

<span data-ttu-id="cc06a-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="cc06a-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="cc06a-105">&nbsp;&nbsp;*\<sectionName>*</span><span class="sxs-lookup"><span data-stu-id="cc06a-105">&nbsp;&nbsp;*\<sectionName>*</span></span>

## <a name="syntax"></a><span data-ttu-id="cc06a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc06a-106">Syntax</span></span>

```xml
<sectionName key="value" key2="value2" ... />
```

## <a name="attributes"></a><span data-ttu-id="cc06a-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="cc06a-107">Attributes</span></span>

<span data-ttu-id="cc06a-108">Attributs et valeurs d’attribut sont définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cc06a-108">Attributes and attribute values are user defined.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cc06a-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="cc06a-109">Parent element</span></span>

|     | <span data-ttu-id="cc06a-110">Description</span><span class="sxs-lookup"><span data-stu-id="cc06a-110">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="cc06a-111">**\<configuration>**</span><span class="sxs-lookup"><span data-stu-id="cc06a-111">**\<configuration>**</span></span>](~/docs/framework/configure-apps/file-schema/configuration-element.md) | <span data-ttu-id="cc06a-112">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="cc06a-112">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="cc06a-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cc06a-113">Child elements</span></span>

<span data-ttu-id="cc06a-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cc06a-114">None</span></span>

## <a name="remarks"></a><span data-ttu-id="cc06a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="cc06a-115">Remarks</span></span>

<span data-ttu-id="cc06a-116">Le  **\<sectionName >** est un élément personnalisé défini par un [  **\<section >** ](~/docs/framework/configure-apps/file-schema/section-element.md) balise dans le [  **\<configSections >** ](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) élément.</span><span class="sxs-lookup"><span data-stu-id="cc06a-116">The **\<sectionName>** element is a custom element defined by a [**\<section>**](~/docs/framework/configure-apps/file-schema/section-element.md) tag in the [**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) element.</span></span> <span data-ttu-id="cc06a-117">Le système de configuration retourne un <xref:System.Collections.IDictionary> lorsque vous appelez l’objet <xref:System.Configuration.Configuration.GetSection(System.String)?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="cc06a-117">The configuration system returns a <xref:System.Collections.IDictionary> object when you call <xref:System.Configuration.Configuration.GetSection(System.String)?displayProperty=nameWithType>.</span></span>

## <a name="example"></a><span data-ttu-id="cc06a-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="cc06a-118">Example</span></span>

<span data-ttu-id="cc06a-119">L’exemple suivant déclare un élément personnalisé appelé  **\<sampleSection >** qui contient les paramètres lus par le <xref:System.Configuration.SingleTagSectionHandler> classe :</span><span class="sxs-lookup"><span data-stu-id="cc06a-119">The following example declares a custom element called **\<sampleSection>** that contains settings read by the <xref:System.Configuration.SingleTagSectionHandler> class:</span></span>

```xml
<configuration>
  <configSections>
    <section name="sampleSection" 
             type="System.Configuration.SingleTagSectionHandler" />
  </configSections>
  <sampleSection setting1="Value1" 
                 setting2="value two" 
                 setting3="third value" />
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="cc06a-120">fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="cc06a-120">Configuration file</span></span>

<span data-ttu-id="cc06a-121">Cet élément peut être utilisé dans le fichier de configuration d’application, fichier de configuration machine (*Machine.config*), et *Web.config* fichiers qui ne sont pas au niveau du répertoire d’application.</span><span class="sxs-lookup"><span data-stu-id="cc06a-121">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc06a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc06a-122">See also</span></span>

- [<span data-ttu-id="cc06a-123">Schéma de fichier de configuration pour le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="cc06a-123">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
