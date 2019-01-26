---
title: '&lt;assemblyBinding&gt; élément pour &lt;configuration&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/assemblyBinding
helpviewer_keywords:
- assemblyBinding Element
- <assemblyBinding> Element
ms.assetid: 6cc55983-b894-449b-8e26-b258e53939cd
ms.openlocfilehash: 12065d8bc484f7bbf77ae18c67df1de0845167b2
ms.sourcegitcommit: b351b0781a035616c90c68ccae6dd60aae66a953
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55083897"
---
# <a name="assemblybinding-element-for-configuration"></a><span data-ttu-id="1b2d6-102">\<assemblyBinding >, élément pour \<configuration ></span><span class="sxs-lookup"><span data-stu-id="1b2d6-102">\<assemblyBinding> element for \<configuration></span></span>

<span data-ttu-id="1b2d6-103">Spécifie la stratégie de liaison de l’assembly au niveau de la configuration.</span><span class="sxs-lookup"><span data-stu-id="1b2d6-103">Specifies assembly binding policy at the configuration level.</span></span>

<span data-ttu-id="1b2d6-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="1b2d6-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="1b2d6-105">&nbsp;&nbsp;**\<assemblyBinding>**</span><span class="sxs-lookup"><span data-stu-id="1b2d6-105">&nbsp;&nbsp;**\<assemblyBinding>**</span></span>

## <a name="syntax"></a><span data-ttu-id="1b2d6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b2d6-106">Syntax</span></span>

```xml
<assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
  <!-- Configuration files to include. -->
</assemblyBinding>
```

## <a name="attribute"></a><span data-ttu-id="1b2d6-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="1b2d6-107">Attribute</span></span>

|           | <span data-ttu-id="1b2d6-108">Description</span><span class="sxs-lookup"><span data-stu-id="1b2d6-108">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="1b2d6-109">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="1b2d6-109">**xmlns**</span></span> | <span data-ttu-id="1b2d6-110">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="1b2d6-110">Required attribute.</span></span><br><br><span data-ttu-id="1b2d6-111">Spécifie l'espace de noms XML requis pour la liaison d'assembly.</span><span class="sxs-lookup"><span data-stu-id="1b2d6-111">Specifies the XML namespace required for assembly binding.</span></span> <span data-ttu-id="1b2d6-112">Utilisez la chaîne « urn:schemas-microsoft-com:asm.v1 » comme valeur.</span><span class="sxs-lookup"><span data-stu-id="1b2d6-112">Use the string "urn:schemas-microsoft-com:asm.v1" as the value.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="1b2d6-113">Élément parent</span><span class="sxs-lookup"><span data-stu-id="1b2d6-113">Parent element</span></span>

|     | <span data-ttu-id="1b2d6-114">Description</span><span class="sxs-lookup"><span data-stu-id="1b2d6-114">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="1b2d6-115">**\<configuration>**</span><span class="sxs-lookup"><span data-stu-id="1b2d6-115">**\<configuration>**</span></span>](~/docs/framework/configure-apps/file-schema/configuration-element.md) | <span data-ttu-id="1b2d6-116">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="1b2d6-116">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |

## <a name="child-element"></a><span data-ttu-id="1b2d6-117">Élément enfant</span><span class="sxs-lookup"><span data-stu-id="1b2d6-117">Child element</span></span>

|     | <span data-ttu-id="1b2d6-118">Description</span><span class="sxs-lookup"><span data-stu-id="1b2d6-118">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="1b2d6-119">**\<linkedConfiguration>**</span><span class="sxs-lookup"><span data-stu-id="1b2d6-119">**\<linkedConfiguration>**</span></span>](~/docs/framework/configure-apps/file-schema/linkedconfiguration-element.md) | <span data-ttu-id="1b2d6-120">Spécifie un fichier de configuration à inclure.</span><span class="sxs-lookup"><span data-stu-id="1b2d6-120">Specifies a configuration file to include.</span></span> |

## <a name="remarks"></a><span data-ttu-id="1b2d6-121">Notes</span><span class="sxs-lookup"><span data-stu-id="1b2d6-121">Remarks</span></span>

<span data-ttu-id="1b2d6-122">Le [  **\<linkedConfiguration >** ](~/docs/framework/configure-apps/file-schema/linkedconfiguration-element.md) élément simplifie la gestion des assemblys de composant en permettant aux fichiers de configuration d’application pour inclure l’assembly dans les fichiers de configuration emplacements bien connus, plutôt que les paramètres de configuration assembly duplication.</span><span class="sxs-lookup"><span data-stu-id="1b2d6-122">The [**\<linkedConfiguration>**](~/docs/framework/configure-apps/file-schema/linkedconfiguration-element.md) element simplifies the management of component assemblies by allowing application configuration files to include assembly configuration files in well-known locations, rather than duplicating assembly configuration settings.</span></span>

> [!NOTE]
> <span data-ttu-id="1b2d6-123">Le  **\<linkedConfiguration >** élément n’est pas pris en charge pour les applications avec des manifestes côte à côte de Windows.</span><span class="sxs-lookup"><span data-stu-id="1b2d6-123">The **\<linkedConfiguration>** element is not supported for applications with Windows side-by-side manifests.</span></span>

## <a name="example"></a><span data-ttu-id="1b2d6-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="1b2d6-124">Example</span></span>

<span data-ttu-id="1b2d6-125">L’exemple suivant montre comment inclure un fichier de configuration sur le disque dur local :</span><span class="sxs-lookup"><span data-stu-id="1b2d6-125">The following example shows how to include a configuration file on the local hard disk:</span></span>

```xml
<configuration>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
    <linkedConfiguration href="file://c:\Program Files\Contoso\sharedConfig.xml" />
  </assemblyBinding>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="1b2d6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b2d6-126">See also</span></span>

- [<span data-ttu-id="1b2d6-127">Schéma de fichier de configuration pour le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="1b2d6-127">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
