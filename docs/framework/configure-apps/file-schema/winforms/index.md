---
title: Section de configuration de Windows Forms
ms.date: 04/07/2017
ms.assetid: 6eb142d5-fc98-40e2-9d90-84733f2a27ba
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bbb2c4157ba702182056c98c959a60569e8c3d1e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61786410"
---
# <a name="windows-forms-configuration-section"></a><span data-ttu-id="f6a33-102">Section de configuration de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f6a33-102">Windows Forms Configuration Section</span></span>
<span data-ttu-id="f6a33-103">Les paramètres de configuration de Windows Forms permettent à une application Windows Forms de stocker et d’extraire des informations sur les paramètres d’application personnalisés, par exemple la prise en charge de plusieurs écrans, la prise en charge de la haute résolution et d’autres paramètres de configuration prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="f6a33-103">Windows Forms configuration settings allow a Windows Forms app to store and retrieve information about customized application settings such as multi-monitor support, high DPI support, and other predefined configuration settings.</span></span>

<span data-ttu-id="f6a33-104">Les paramètres de configuration de l’application Windows Forms sont stockés dans l’élément `System.Windows.Forms.ApplicationConfigurationSection` d’un fichier de configuration de l’application.</span><span class="sxs-lookup"><span data-stu-id="f6a33-104">Windows Forms application configuration settings are stored in an application configuration file's `System.Windows.Forms.ApplicationConfigurationSection` element.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a33-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6a33-105">Syntax</span></span>

```xml
<configuration>
  <System.Windows.Forms.ApplicationConfigurationSection>
  ...
  </System.Windows.Forms.ApplicationConfigurationSection>
</configuration>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f6a33-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f6a33-106">Attributes and elements</span></span>

<span data-ttu-id="f6a33-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f6a33-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="f6a33-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="f6a33-108">Attributes</span></span>

<span data-ttu-id="f6a33-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f6a33-109">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="f6a33-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f6a33-110">Child elements</span></span>

<span data-ttu-id="f6a33-111">Élément</span><span class="sxs-lookup"><span data-stu-id="f6a33-111">Element</span></span>  |<span data-ttu-id="f6a33-112">Description</span><span class="sxs-lookup"><span data-stu-id="f6a33-112">Description</span></span> |
---------|---------|
[`<add>`](../../../../../docs/framework/configure-apps/file-schema/winforms/windows-forms-add-configuration-element.md) | <span data-ttu-id="f6a33-113">Ajoute une clé de paramètre de configuration avec une valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f6a33-113">Adds a configuration setting key with a specified value</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="f6a33-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f6a33-114">Parent elements</span></span>

<span data-ttu-id="f6a33-115">Élément</span><span class="sxs-lookup"><span data-stu-id="f6a33-115">Element</span></span>  |<span data-ttu-id="f6a33-116">Description</span><span class="sxs-lookup"><span data-stu-id="f6a33-116">Description</span></span> |
---------|---------|
[<span data-ttu-id="f6a33-117">\<configuration></span><span class="sxs-lookup"><span data-stu-id="f6a33-117">\<configuration></span></span>](../configuration-element.md) | <span data-ttu-id="f6a33-118">Élément racine de chaque fichier de configuration utilisé par le common language runtime et les applications Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="f6a33-118">The root element in every configuration file used by the common language runtime and Windows Forms applications</span></span> |

## <a name="remarks"></a><span data-ttu-id="f6a33-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f6a33-119">Remarks</span></span>

<span data-ttu-id="f6a33-120">À compter du .NET Framework 4.7, l’élément `<System.Windows.Forms.ApplicationConfigurationSection>` vous permet de configurer des applications Windows Forms pour tirer parti des fonctionnalités ajoutées dans les dernières versions du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f6a33-120">Starting with the .NET Framework 4.7, the `<System.Windows.Forms.ApplicationConfigurationSection>` element allows you to configure Windows Forms applications to take advantage of features added in recent releases of the .NET Framework.</span></span> 

<span data-ttu-id="f6a33-121">L’élément `<System.Windows.Forms.ApplicationConfigurationSection>` peut contenir un ou plusieurs éléments [`<add>`](../../../../../docs/framework/configure-apps/file-schema/winforms/windows-forms-add-configuration-element.md) enfants, dont chacun définit un paramètre de configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="f6a33-121">The `<System.Windows.Forms.ApplicationConfigurationSection>` element can include one or more child [`<add>`](../../../../../docs/framework/configure-apps/file-schema/winforms/windows-forms-add-configuration-element.md) elements, each of which defines a specific configuration setting.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6a33-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6a33-122">See also</span></span>

- [<span data-ttu-id="f6a33-123">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="f6a33-123">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="f6a33-124">Prise en charge de la haute résolution dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f6a33-124">High DPI Support in Windows Forms</span></span>](../../../../../docs/framework/winforms/high-dpi-support-in-windows-forms.md)
