---
title: CoInitializeCor, fonction
ms.date: 03/30/2017
api_name:
- CoInitializeCor
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoInitializeCor
helpviewer_keywords:
- CoInitializeCor function [.NET Framework hosting]
ms.assetid: 9b9079fb-579e-4141-b3f0-791072dd40dc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 556d26ac7e4fb8847f132d19bd2e749aff345abf
ms.sourcegitcommit: 79066169e93d9d65203028b21983574ad9dcf6b4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57211843"
---
# <a name="coinitializecor-function"></a>CoInitializeCor, fonction
`CoInitializeCor` est obsolète.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
STDAPI CoInitializeCor (  
    DWORD fFlags  
);  
```  
  
## <a name="remarks"></a>Notes  
 Pour initialiser le common language runtime, utilisez soit [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) ou [CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md).  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** Cor.h  
  
## <a name="see-also"></a>Voir aussi
- [Fonctions statiques globales des métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
