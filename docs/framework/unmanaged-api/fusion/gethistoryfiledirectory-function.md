---
title: GetHistoryFileDirectory, fonction
ms.date: 03/30/2017
api_name:
- GetHistoryFileDirectory
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- GetHistoryFileDirectory
helpviewer_keywords:
- GetHistoryFileDirectory function [.NET Framework fusion]
ms.assetid: 93232222-926e-42ac-b85d-8a6d33977672
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 21742881c5aef7384be318297aa3432411c3d57c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57479279"
---
# <a name="gethistoryfiledirectory-function"></a>GetHistoryFileDirectory, fonction
Récupère le chemin d’accès du répertoire de l’historique de l’application.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetHistoryFileDirectory (  
    [in]      LPWSTR      wzDir,  
    [in,out]  LPCWSTR  *pdwsize,  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `wzDir`  
 [out] Une mémoire tampon pour contenir le chemin d’accès au répertoire de l’historique de l’application.  
  
 `pdwSize`  
 [in, out] La longueur de la mémoire tampon.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne des codes d’erreur COM standards, tel que défini dans le fichier WinError.h, en plus des valeurs suivantes.  
  
|Code de retour|Description|  
|-----------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|E_INVALIDARG|`wzDir` ou `pdwSize` est null, ou la version de chaîne est incorrecte.|  
  
## <a name="remarks"></a>Notes  
 Opération réussie, le `pdwSize` argument est défini sur la longueur de la chaîne de chemin d’accès.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Bibliothèque :** Le fichier fusion.dll et Mscorwks.dll. Utilisez le fichier Fusion.dll plutôt que Mscorwks.dll pour vous assurer que vous ciblez la version correcte du .NET Framework.  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [CreateHistoryReader, fonction](../../../../docs/framework/unmanaged-api/fusion/createhistoryreader-function.md)
- [NukeDownloadedCache, fonction](../../../../docs/framework/unmanaged-api/fusion/nukedownloadedcache-function.md)
- [Fonctions statiques globales de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
