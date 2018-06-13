---
title: GetRequestedRuntimeVersion, fonction
ms.date: 03/30/2017
api_name:
- GetRequestedRuntimeVersion
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- GetRequestedRuntimeVersion
helpviewer_keywords:
- GetRequestedRuntimeVersion function [.NET Framework hosting]
ms.assetid: 82f596a4-483d-4509-b0c5-a84c53c3da1b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 977f63b58ccbc709fb9383acf64686fc92808da4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433300"
---
# <a name="getrequestedruntimeversion-function"></a>GetRequestedRuntimeVersion, fonction
Obtient le numéro de version du common language runtime (CLR) demandé par l’application spécifiée. Si cette version n’est pas installée, obtient la version la plus récente qui est installée avant la version demandée.  
  
 Cette fonction est déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetRequestedRuntimeVersion (  
    [in]  LPWSTR  pExe,   
    [out] LPWSTR  pVersion,   
    [in]  DWORD   cchBuffer,   
    [out] DWORD  *pdwLength  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pExe`  
 [in] Le nom de l’application.  
  
 `pVersion`  
 [out] Une mémoire tampon qui contient la chaîne de numéro de version en cas de réussite.  
  
 `cchBuffer`  
 [in] La longueur de la mémoire tampon de version.  
  
 `pdwLength`  
 [out] Pointeur vers la longueur de la chaîne de numéro de version.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne des codes d’erreur de modèle COM (Component Object) standard, tel que défini dans WinError.h, en plus des valeurs suivantes.  
  
|Code de retour|Description|  
|-----------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|ERROR_INSUFFICIENT_BUFFER|Le tampon de version n’est pas suffisamment grand pour stocker la chaîne de version.|  
|E_POINTER|`pdwLength` a la valeur null.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [GetRequestedRuntimeInfo, fonction](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md)  
 [GetVersionFromProcess, fonction](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md)  
 [Fonctions d’hébergement CLR dépréciées](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
