---
title: CorLaunchApplication, fonction
ms.date: 03/30/2017
api_name:
- CorLaunchApplication
api_location:
- mscoree.dll
- clr.dll
api_type:
- COM
f1_keywords:
- CorLaunchApplication
helpviewer_keywords:
- CorLaunchApplication function [.NET Framework hosting]
ms.assetid: 71f362a9-8fe2-47ce-9302-05a645cf3d7d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4c997ab107ba3ceb7773bc9235b9c9dcd4d97df8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59231446"
---
# <a name="corlaunchapplication-function"></a>CorLaunchApplication, fonction
Démarre l’application sur le chemin d’accès réseau spécifié, à l’aide des manifestes spécifiés et autres données d’application.  
  
 Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CorLaunchApplication (  
    [in]  HOST_TYPE                dwClickOnceHost,  
    [in]  LPCWSTR                  pwzAppFullName,  
    [in]  DWORD                    dwManifestPaths,  
    [in]  LPCWSTR                 *ppwzManifestPaths,  
    [in]  DWORD                    dwActivationData,  
    [in]  LPCWSTR                 *ppwzActivationData,  
    [out] LPPROCESS_INFORMATION    lpProcessInformation  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `dwClickOnceHost`  
 [in] Une valeur de la [HOST_TYPE](../../../../docs/framework/unmanaged-api/hosting/host-type-enumeration.md) énumération qui spécifie le type d’hôte qui lance l’application.  
  
 `pwzAppFullName`  
 [in] Le nom complet de l’application qui est lancée.  
  
 `dwManifestPaths`  
 [in] Le nombre de chemins d’accès de manifestes pour l’application.  
  
 `ppwzManifestPaths`  
 [in] Tableau de chaînes, dont chacun spécifie un chemin d’accès à un manifeste d’application qui est lancée.  
  
 `dwActivationData`  
 [in] Le nombre d’éléments de données d’activation pour l’application qui est lancée.  
  
 `ppwzActivationData`  
 [in] Tableau de chaînes, chacune d’elles étant un élément de données d’activation pour l’application qui est lancée.  
  
 `lpProcessInformation`  
 [out] Pointeur vers les informations sur le processus dans lequel l’application a été chargée.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Fonction d'hébergement du CLR déconseillées](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
