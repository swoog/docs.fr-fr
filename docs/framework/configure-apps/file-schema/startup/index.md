---
title: Schéma des paramètres de démarrage
ms.date: 03/30/2017
helpviewer_keywords:
- startup settings schema
- schema startup settings
- configuration schema [.NET Framework], startup settings
ms.assetid: 03de6972-442a-4648-9f3e-efa654e3b949
ms.openlocfilehash: e5f9c9af64ff38e7c0f1f26ccab039261b052e30
ms.sourcegitcommit: b351b0781a035616c90c68ccae6dd60aae66a953
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55083416"
---
# <a name="startup-settings-schema"></a>Schéma des paramètres de démarrage

Les paramètres de démarrage spécifient la version du common language runtime qui doit exécuter l’application.  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<requiredRuntime>](requiredruntime-element.md)|Spécifie que l’application prend en charge uniquement la version 1.0 du common language runtime. Les applications générées avec la version 1.1 du runtime doivent utiliser l’élément **\<supportedRuntime>**.|  
|[\<supportedRuntime>](supportedruntime-element.md)|Spécifie quelles versions du Common Language Runtime sont prises en charge par l'application.|  
|[\<startup>](startup-element.md)|Contient les éléments **\<requiredRuntime>** et **\<supportedRuntime>**.|  
  
## <a name="see-also"></a>Voir aussi

- [Schéma des fichiers de configuration](../index.md)
- [Guide pratique pour configurer une application en vue de prendre en charge le .NET Framework 4 ou versions ultérieures](../../../migration-guide/how-to-configure-an-app-to-support-net-framework-4-or-4-5.md)
