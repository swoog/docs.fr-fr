---
title: Fonctions d'assistance de Tlbexp (Informations de référence sur les API non managées)
ms.date: 03/30/2017
helpviewer_keywords:
- exporter tool [.NET Framework]
- TlbRef.dll
- Tlbexp.exe
- Type Library Exporter
ms.assetid: 5c0a3d14-5f26-4267-94a9-82c30f8db09a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9f41a233e9b5338bdb0a324ff9af267a97821d4e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61967698"
---
# <a name="tlbexp-helper-functions-unmanaged-api-reference"></a>Fonctions d'assistance de Tlbexp (Informations de référence sur les API non managées)
L’[outil Type Library Exporter](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md) (Tlbexp.exe) charge une bibliothèque de liens dynamiques nommée TlbRef.dll. Cette DLL contient deux fonctions d’assistance et une interface que l’outil exportateur utilise pendant le processus de conversion de l’assembly à la bibliothèque de types.  
  
## <a name="in-this-section"></a>Dans cette section  
 [GetTypeLibInfo, fonction](../../../../docs/framework/unmanaged-api/tlbexp/gettypelibinfo-function.md)  
 Fournit des informations sur la localisation et le système d’exploitation pour une bibliothèque de types.  
  
 [LoadTypeLibWithResolver, fonction](../../../../docs/framework/unmanaged-api/tlbexp/loadtypelibwithresolver-function.md)  
 Charge une bibliothèque de types à l’aide d’une implémentation de l’[interface ITypeLibResolver](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md) pour résoudre tous les types de bibliothèques référencés.  
  
 [ITypeLibResolver, interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md)  
 Fournit la [méthode ResolveTypeLib](../../../../docs/framework/unmanaged-api/tlbexp/resolvetypelib-method.md), qui retourne le chemin d’accès complet d’une bibliothèque de types.
