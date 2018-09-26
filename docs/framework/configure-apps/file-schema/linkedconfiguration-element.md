---
title: '&lt;linkedConfiguration&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/assemblyBinding/linkedConfiguration
- http://schemas.microsoft.com/.NetConfiguration/v2.0#linkedConfiguration
helpviewer_keywords:
- configuration files [.NET Framework],linked configuration files
- <linkedConfiguration> element
- including configuration files
- linked configuration files
- linkedConfiguration Element
ms.assetid: 8eb34f3b-427e-4288-a7ff-c73f489deb45
author: mcleblanc
ms.author: markl
ms.openlocfilehash: c5186aa94993ba551252db6fef55853b5b554789
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47200956"
---
# <a name="linkedconfiguration-element"></a><span data-ttu-id="92caf-102">\<linkedConfiguration > élément</span><span class="sxs-lookup"><span data-stu-id="92caf-102">\<linkedConfiguration> element</span></span>

<span data-ttu-id="92caf-103">Spécifie un fichier de configuration à inclure.</span><span class="sxs-lookup"><span data-stu-id="92caf-103">Specifies a configuration file to include.</span></span>

<span data-ttu-id="92caf-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="92caf-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="92caf-105">&nbsp;&nbsp;[**\<assemblyBinding >**](~/docs/framework/configure-apps/file-schema/assemblybinding-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="92caf-105">&nbsp;&nbsp;[**\<assemblyBinding>**](~/docs/framework/configure-apps/file-schema/assemblybinding-element-for-configuration.md) </span></span>  
<span data-ttu-id="92caf-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<linkedConfiguration >**</span><span class="sxs-lookup"><span data-stu-id="92caf-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<linkedConfiguration>**</span></span>

## <a name="syntax"></a><span data-ttu-id="92caf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92caf-107">Syntax</span></span>

```xml
<linkedConfiguration href="URL of linked configuration file" />
```

## <a name="attribute"></a><span data-ttu-id="92caf-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="92caf-108">Attribute</span></span>

|           | <span data-ttu-id="92caf-109">Description</span><span class="sxs-lookup"><span data-stu-id="92caf-109">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="92caf-110">**href**</span><span class="sxs-lookup"><span data-stu-id="92caf-110">**href**</span></span>  | <span data-ttu-id="92caf-111">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="92caf-111">Required attribute.</span></span><br><br><span data-ttu-id="92caf-112">L’URL du fichier de configuration à inclure.</span><span class="sxs-lookup"><span data-stu-id="92caf-112">The URL of the configuration file to include.</span></span> <span data-ttu-id="92caf-113">Le seul format pris en charge pour le **href** attribut est `file://`.</span><span class="sxs-lookup"><span data-stu-id="92caf-113">The only format supported for the **href** attribute is `file://`.</span></span> <span data-ttu-id="92caf-114">Fichiers locaux et les fichiers UNC sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="92caf-114">Local files and UNC files are supported.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="92caf-115">Élément parent</span><span class="sxs-lookup"><span data-stu-id="92caf-115">Parent element</span></span>

|     | <span data-ttu-id="92caf-116">Description</span><span class="sxs-lookup"><span data-stu-id="92caf-116">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="92caf-117">**\<assemblyBinding >** élément</span><span class="sxs-lookup"><span data-stu-id="92caf-117">**\<assemblyBinding>** Element</span></span>](~/docs/framework/configure-apps/file-schema/assemblybinding-element-for-configuration.md) | <span data-ttu-id="92caf-118">Spécifie la stratégie de liaison de l’assembly au niveau de la configuration.</span><span class="sxs-lookup"><span data-stu-id="92caf-118">Specifies assembly binding policy at the configuration level.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="92caf-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="92caf-119">Child elements</span></span>

<span data-ttu-id="92caf-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="92caf-120">None</span></span>

## <a name="remarks"></a><span data-ttu-id="92caf-121">Notes</span><span class="sxs-lookup"><span data-stu-id="92caf-121">Remarks</span></span>

<span data-ttu-id="92caf-122">Le  **\<linkedConfiguration >** élément simplifie la maintenance pour les assemblys de composants.</span><span class="sxs-lookup"><span data-stu-id="92caf-122">The **\<linkedConfiguration>** element simplifies servicing for component assemblies.</span></span> <span data-ttu-id="92caf-123">Si une ou plusieurs applications utilisent un assembly qui a un fichier de configuration qui résident dans un emplacement connu, les fichiers de configuration des applications qui utilisent l’assembly peuvent utiliser le  **\<linkedConfiguration >** élément à inclure le fichier de configuration d’assembly, plutôt que d’y compris les informations de configuration directement.</span><span class="sxs-lookup"><span data-stu-id="92caf-123">If one or more applications use an assembly that has a configuration file residing in a well-known location, the configuration files of the applications that use the assembly can use the **\<linkedConfiguration>** element to include the assembly configuration file, rather than including configuration information directly.</span></span> <span data-ttu-id="92caf-124">Lorsque l’assembly de composant est prise en charge, la mise à jour le fichier de configuration commun fournit des informations de configuration mis à jour à toutes les applications qui utilisent l’assembly.</span><span class="sxs-lookup"><span data-stu-id="92caf-124">When the component assembly is serviced, updating the common configuration file provides updated configuration information to all applications that use the assembly.</span></span>

> [!NOTE]
> <span data-ttu-id="92caf-125">Le  **\<linkedConfiguration >** élément n’est pas pris en charge pour les applications avec des manifestes côte à côte de Windows.</span><span class="sxs-lookup"><span data-stu-id="92caf-125">The **\<linkedConfiguration>** element is not supported for applications with Windows side-by-side manifests.</span></span>

<span data-ttu-id="92caf-126">Les règles suivantes régissent l’utilisation de fichiers de configuration liés :</span><span class="sxs-lookup"><span data-stu-id="92caf-126">The following rules govern the use of linked configuration files:</span></span>

- <span data-ttu-id="92caf-127">Les paramètres dans les fichiers de configuration inclus uniquement affectent la stratégie de liaison de chargeur et sont uniquement utilisés par le chargeur.</span><span class="sxs-lookup"><span data-stu-id="92caf-127">The settings in included configuration files only affect loader binding policy and are used only by the loader.</span></span> <span data-ttu-id="92caf-128">Les fichiers de configuration inclus peuvent avoir des paramètres autres que la liaison des stratégies, mais ces paramètres n’ont aucun effet.</span><span class="sxs-lookup"><span data-stu-id="92caf-128">The included configuration files can have settings other than binding policies, but those settings don't have any effect.</span></span>

- <span data-ttu-id="92caf-129">Le seul format pris en charge pour le `href` attribut est `file://`.</span><span class="sxs-lookup"><span data-stu-id="92caf-129">The only format supported for the `href` attribute is `file://`.</span></span> <span data-ttu-id="92caf-130">Fichiers locaux et les fichiers UNC sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="92caf-130">Local files and UNC files are supported.</span></span>

- <span data-ttu-id="92caf-131">Il n’existe aucune contrainte sur le nombre de configurations liées par fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="92caf-131">There is no constraint on the number of linked configurations per configuration file.</span></span>

- <span data-ttu-id="92caf-132">Tous les fichiers de configuration liés sont fusionnées pour former un fichier, semblable au comportement de la `#include` directive en C/C++.</span><span class="sxs-lookup"><span data-stu-id="92caf-132">All linked configuration files are merged to form one file, similar to the behavior of the `#include` directive in C/C++.</span></span>

- <span data-ttu-id="92caf-133">Le  **\<linkedConfiguration >** l’élément est autorisé uniquement dans les fichiers de configuration d’application ; elle est ignorée dans *Machine.config*.</span><span class="sxs-lookup"><span data-stu-id="92caf-133">The **\<linkedConfiguration>** element is allowed only in application configuration files; it's ignored in *Machine.config*.</span></span>

- <span data-ttu-id="92caf-134">Les références circulaires sont détectées et s’est arrêtés.</span><span class="sxs-lookup"><span data-stu-id="92caf-134">Circular references are detected and terminated.</span></span> <span data-ttu-id="92caf-135">Autrement dit, si le  **\<linkedConfiguration >** éléments d’une série de fichiers de configuration forment une boucle, la boucle est détectée et arrêtée.</span><span class="sxs-lookup"><span data-stu-id="92caf-135">That is, if the **\<linkedConfiguration>** elements of a series of configuration files form a loop, the loop is detected and stopped.</span></span>

## <a name="example"></a><span data-ttu-id="92caf-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="92caf-136">Example</span></span>

<span data-ttu-id="92caf-137">L’exemple suivant montre comment inclure le fichier de configuration à partir du disque dur local :</span><span class="sxs-lookup"><span data-stu-id="92caf-137">The following example shows how to include configuration file from the local hard disk:</span></span>

```xml
<configuration>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
    <linkedConfiguration href="file://c:\Program Files\Contoso\sharedConfig.xml"/>
  </assemblyBinding>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="92caf-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92caf-138">See also</span></span>

<span data-ttu-id="92caf-139">[**\<assemblyBinding >** élément](~/docs/framework/configure-apps/file-schema/assemblybinding-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="92caf-139">[**\<assemblyBinding>** Element](~/docs/framework/configure-apps/file-schema/assemblybinding-element-for-configuration.md) </span></span>  
[<span data-ttu-id="92caf-140">Schéma de fichier de configuration pour le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="92caf-140">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
