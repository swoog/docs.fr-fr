---
title: <clear> élément pour NameValueSectionHandler et DictionarySectionHandler
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName/clear
helpviewer_keywords:
- clear Element
- <clear> Element
ms.assetid: ff2294ec-fb82-4b0c-933e-ae185433fc7b
author: guardrex
ms.author: mairaw
ms.openlocfilehash: ad3ac93b2a7f92cd33787620fc0caa2b632aa072
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55281873"
---
# <a name="clear-element-for-namevaluesectionhandler-and-dictionarysectionhandler"></a><span data-ttu-id="0e782-102">\<Désactivez >, élément pour NameValueSectionHandler et DictionarySectionHandler</span><span class="sxs-lookup"><span data-stu-id="0e782-102">\<clear> element for NameValueSectionHandler and DictionarySectionHandler</span></span>

<span data-ttu-id="0e782-103">Efface tous les paramètres déjà définis dans une section.</span><span class="sxs-lookup"><span data-stu-id="0e782-103">Clears all previously defined settings in a section.</span></span>

<span data-ttu-id="0e782-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="0e782-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="0e782-105">&nbsp;&nbsp;[**\<sectionName>**](~/docs/framework/configure-apps/file-schema/custom-element-2.md) </span><span class="sxs-lookup"><span data-stu-id="0e782-105">&nbsp;&nbsp;[**\<sectionName>**](~/docs/framework/configure-apps/file-schema/custom-element-2.md) </span></span>  
<span data-ttu-id="0e782-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**</span><span class="sxs-lookup"><span data-stu-id="0e782-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**</span></span>

## <a name="syntax"></a><span data-ttu-id="0e782-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e782-107">Syntax</span></span>

```xml
<clear />
```

## <a name="attributes"></a><span data-ttu-id="0e782-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="0e782-108">Attributes</span></span>

<span data-ttu-id="0e782-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0e782-109">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="0e782-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="0e782-110">Parent element</span></span>

|     | <span data-ttu-id="0e782-111">Description</span><span class="sxs-lookup"><span data-stu-id="0e782-111">Description</span></span> |
| --- | ------------|
| [<span data-ttu-id="0e782-112">**\<sectionName>** Element</span><span class="sxs-lookup"><span data-stu-id="0e782-112">**\<sectionName>** Element</span></span>](~/docs/framework/configure-apps/file-schema/custom-element-2.md) | <span data-ttu-id="0e782-113">Définit les paramètres pour les sections de configuration personnalisées qui utilisent le <xref:System.Configuration.NameValueSectionHandler> et <xref:System.Configuration.DictionarySectionHandler> classes.</span><span class="sxs-lookup"><span data-stu-id="0e782-113">Defines settings for custom configuration sections that use the <xref:System.Configuration.NameValueSectionHandler> and <xref:System.Configuration.DictionarySectionHandler> classes.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="0e782-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0e782-114">Child elements</span></span>

<span data-ttu-id="0e782-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0e782-115">None</span></span>

## <a name="remarks"></a><span data-ttu-id="0e782-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0e782-116">Remarks</span></span>

<span data-ttu-id="0e782-117">Vous pouvez utiliser la  **\<Effacer >** élément à supprimer tous les paramètres de votre application qui ont été définies à un niveau supérieur dans la hiérarchie de fichiers de configuration.</span><span class="sxs-lookup"><span data-stu-id="0e782-117">You can use the **\<clear>** element to remove all settings from your application that were defined at a higher level in the configuration file hierarchy.</span></span>

## <a name="example"></a><span data-ttu-id="0e782-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="0e782-118">Example</span></span>

<span data-ttu-id="0e782-119">Cet exemple définit un fichier de configuration d’ordinateur et un fichier de configuration d’application et montre comment utiliser le  **\<Effacer >** élément dans un fichier de configuration d’application pour effacer les sections définies précédemment dans le fichier de configuration machine.</span><span class="sxs-lookup"><span data-stu-id="0e782-119">This example defines a machine configuration file and an application configuration file and shows how to use the **\<clear>** element in an application configuration file to clear sections previously defined in the machine configuration file.</span></span>

<span data-ttu-id="0e782-120">Le code du fichier de configuration machine suivant déclare la section  **\<mySection >**:</span><span class="sxs-lookup"><span data-stu-id="0e782-120">The following machine configuration file code declares the section **\<mySection>**:</span></span>

```xml
<!-- Machine.config file -->
<configuration>
  <configSections>
    <section name="mySection" type="System.Configuration.NameValueSectionHandler,System" />
  </configSections>
  <mySection>
    <add key="key1" value="value1" />
    <add key="key2" value="value2" />
  </mySection>
</configuration>
```

<span data-ttu-id="0e782-121">Le code suivant du fichier de configuration de l’application supprime tous les paramètres à partir de  **\<mySection >**.</span><span class="sxs-lookup"><span data-stu-id="0e782-121">The following application configuration file code removes all settings from **\<mySection>**.</span></span> <span data-ttu-id="0e782-122">L’application ne peut pas récupérer les paramètres qui ont été déclarées dans le dans le  **\<mySection >** section du fichier de configuration machine.</span><span class="sxs-lookup"><span data-stu-id="0e782-122">The application cannot retrieve any of the settings that were declared in the in the **\<mySection>** section of the machine configuration file.</span></span>

```xml
<!-- Application configuration file -->
<configuration>
  <mySection>
    <clear/>
  </mySection>
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="0e782-123">fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="0e782-123">Configuration file</span></span>

<span data-ttu-id="0e782-124">Cet élément peut être utilisé dans le fichier de configuration d’application, fichier de configuration machine (*Machine.config*), et *Web.config* fichiers qui ne sont pas au niveau du répertoire d’application.</span><span class="sxs-lookup"><span data-stu-id="0e782-124">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e782-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e782-125">See also</span></span>

- [<span data-ttu-id="0e782-126">Schéma de fichier de configuration pour le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="0e782-126">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
