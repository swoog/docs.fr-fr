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
ms.openlocfilehash: 4e549e13c0d51e4aa708a674a2224168ab66f8ad
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59178163"
---
# <a name="nukedownloadedcache-function"></a>NukeDownloadedCache, fonction
Supprime le cache de téléchargement du common language runtime (CLR).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT NukeDownloadedCache();  
```  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne des codes d’erreur COM standards, tel que défini dans WinError.h.  
  
## <a name="remarks"></a>Notes  
 Le cache de téléchargement CLR est la zone où les assemblys avec nom fort qui sont téléchargés à partir d’une URL sont stockés pour une réutilisation éventuelle.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Bibliothèque :** Le fichier fusion.dll et Mscorwks.dll. Utilisez le fichier Fusion.dll plutôt que Mscorwks.dll pour vous assurer que vous ciblez la version correcte du .NET Framework.  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [CreateHistoryReader, fonction](../../../../docs/framework/unmanaged-api/fusion/createhistoryreader-function.md)
- [GetHistoryFileDirectory, fonction](../../../../docs/framework/unmanaged-api/fusion/gethistoryfiledirectory-function.md)
- [Fonctions statiques globales de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
