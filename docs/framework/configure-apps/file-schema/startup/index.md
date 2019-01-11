---
title: Schéma des paramètres de démarrage
ms.date: 03/30/2017
helpviewer_keywords:
- startup settings schema
- schema startup settings
- configuration schema [.NET Framework], startup settings
ms.assetid: 03de6972-442a-4648-9f3e-efa654e3b949
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 0a03438968f487f574606f415fb9d43223030038
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222153"
---
# <a name="startup-settings-schema"></a><span data-ttu-id="0f463-102">Schéma des paramètres de démarrage</span><span class="sxs-lookup"><span data-stu-id="0f463-102">Startup settings schema</span></span>

<span data-ttu-id="0f463-103">Les paramètres de démarrage spécifient la version du common language runtime qui doit exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="0f463-103">Startup settings specify the version of the common language runtime that should run the application.</span></span>  
  
|<span data-ttu-id="0f463-104">Élément</span><span class="sxs-lookup"><span data-stu-id="0f463-104">Element</span></span>|<span data-ttu-id="0f463-105">Description</span><span class="sxs-lookup"><span data-stu-id="0f463-105">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0f463-106">\<requiredRuntime></span><span class="sxs-lookup"><span data-stu-id="0f463-106">\<requiredRuntime></span></span>](requiredruntime-element.md)|<span data-ttu-id="0f463-107">Spécifie que l’application prend en charge uniquement la version 1.0 du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="0f463-107">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="0f463-108">Les applications générées avec la version 1.1 du runtime doivent utiliser l’élément **\<supportedRuntime>**.</span><span class="sxs-lookup"><span data-stu-id="0f463-108">Applications built with runtime version 1.1 should use the **\<supportedRuntime>** element.</span></span>|  
|[<span data-ttu-id="0f463-109">\<supportedRuntime></span><span class="sxs-lookup"><span data-stu-id="0f463-109">\<supportedRuntime></span></span>](supportedruntime-element.md)|<span data-ttu-id="0f463-110">Spécifie quelles versions du Common Language Runtime sont prises en charge par l'application.</span><span class="sxs-lookup"><span data-stu-id="0f463-110">Specifies which versions of the common language runtime the application supports.</span></span>|  
|[<span data-ttu-id="0f463-111">\<startup></span><span class="sxs-lookup"><span data-stu-id="0f463-111">\<startup></span></span>](startup-element.md)|<span data-ttu-id="0f463-112">Contient les éléments **\<requiredRuntime>** et **\<supportedRuntime>**.</span><span class="sxs-lookup"><span data-stu-id="0f463-112">Contains the **\<requiredRuntime>** and **\<supportedRuntime>** elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0f463-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f463-113">See also</span></span>

- [<span data-ttu-id="0f463-114">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="0f463-114">Configuration File Schema</span></span>](../index.md)  
- [<span data-ttu-id="0f463-115">Guide pratique pour Configurer une application pour prendre en charge de .NET Framework 4 ou versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f463-115">How to: Configure an app to support .NET Framework 4 or later versions</span></span>](../../../migration-guide/how-to-configure-an-app-to-support-net-framework-4-or-4-5.md)