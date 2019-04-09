---
title: CorExitProcess, fonction
ms.date: 03/30/2017
api_name:
- CorExitProcess
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CorExitProcess
helpviewer_keywords:
- CorExitProcess function [.NET Framework hosting]
ms.assetid: a5cab4c6-990e-47f3-8798-cf422b791015
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b95625cfe17b36c0244e6780a08dcf50ce50763d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59201856"
---
# <a name="corexitprocess-function"></a>CorExitProcess, fonction
Arrête le processus non managé en cours.  
  
 Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)]. Utilisez le [ICLRMetaHost::ExitProcess](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-exitprocess-method.md) méthode à la place.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
void STDMETHODCALLTYPE CorExitProcess (   
  int  exitCode  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `exitCode`  
 Entier qui spécifie le code de sortie.  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Compter les [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], `CorExitProcess` quitte chaque exécution commencée dans le processus, pas uniquement le runtime auquel les API héritées ont été liés.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Fonction d'hébergement du CLR déconseillées](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
