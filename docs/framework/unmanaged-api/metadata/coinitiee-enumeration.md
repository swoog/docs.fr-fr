---
title: COINITIEE, énumération
ms.date: 03/30/2017
api_name:
- COINITIEE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COINITIEE
helpviewer_keywords:
- COINITIEE enumeration [.NET Framework metadata]
ms.assetid: 64264238-3b68-4bac-a887-36b552426a6c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4a84fdfdba96c58671302c723b8a56848b70eb60
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61984124"
---
# <a name="coinitiee-enumeration"></a>COINITIEE, énumération
Spécifie les constantes utilisées par [CoInitializeEE](../../../../docs/framework/unmanaged-api/hosting/coinitializeee-function.md) lors de l’initialisation du common language runtime.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum tagCOINITEE {  
   COINITEE_DEFAULT = 0x0,  
   COINITEE_DLL     = 0x1,  
   COINITEE_MAIN    = 0x2  
} COINITIEE;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`COINITEE_DEFAULT`|Mode d’initialisation par défaut. Initialise l’exécution et crée la valeur par défaut <xref:System.AppDomain>.|  
|`COINITEE_DLL`|Initialise l’exécution d’une DLL managée.|  
|`COINITEE_MAIN`|Initialise l’exécution d’un EXE managé. Cela initialise le runtime, mais ne crée pas la valeur par défaut <xref:System.AppDomain>, qui est créé après avoir entré la routine principale de l’EXE.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
