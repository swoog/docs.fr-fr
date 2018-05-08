---
title: NukeDownloadedCache, fonction
ms.date: 03/30/2017
api_name:
- NukeDownloadedCache
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- NukeDownloadedCache
helpviewer_keywords:
- NukeDownloadedCache function [.NET Framework fusion]
ms.assetid: fac2b1c6-6fa3-4818-805b-b63972024c86
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f0436991512713c05e60a3c10d6fbdaa17bb378c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="nukedownloadedcache-function"></a>NukeDownloadedCache, fonction
Supprime le cache de téléchargement du common language runtime (CLR).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT NukeDownloadedCache();  
```  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne des codes d’erreur COM standard, tel que défini dans WinError.h.  
  
## <a name="remarks"></a>Notes  
 Le cache de téléchargement CLR est la zone où les assemblys avec nom fort qui sont téléchargés à partir d’une URL sont stockés pour une réutilisation éventuelle.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Bibliothèque :** Fusion.dll et Mscorwks.dll. Utilisez le fichier Fusion.dll plutôt que Mscorwks.dll pour garantir que vous ciblez la version appropriée du .NET Framework.  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [CreateHistoryReader, fonction](../../../../docs/framework/unmanaged-api/fusion/createhistoryreader-function.md)  
 [GetHistoryFileDirectory, fonction](../../../../docs/framework/unmanaged-api/fusion/gethistoryfiledirectory-function.md)  
 [Fonctions statiques globales de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
