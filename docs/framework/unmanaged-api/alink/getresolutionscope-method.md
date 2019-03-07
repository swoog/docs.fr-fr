---
title: GetResolutionScope, méthode
ms.date: 03/30/2017
api_name:
- IALink.GetResolutionScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetResolutionScope
helpviewer_keywords:
- GetResolutionScope method
ms.assetid: 5b48ca60-dacd-44b2-9979-4a5122f00812
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bfe06c1300a22757b363236454f4f494dab1978a
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57486795"
---
# <a name="getresolutionscope-method"></a>GetResolutionScope, méthode
Récupère l’étendue d’un type donné.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetResolutionScope(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    mdToken     TargetFile,  
    mdToken*    pScope  
) PURE;  
```  
  
## <a name="parameters"></a>Paramètres  
 `AssemblyID`  
 ID de l’assembly.  
  
 `FileToken`  
 Fichier qui a besoin d’une référence.  
  
 `TargetFile`  
 Jeton du fichier dans lequel le type est défini, généralement récupéré avec [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).  
  
 `pScope`  
 Reçoit la référence d’assembly ou module.  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Spécifications  
 Nécessite alink.h.  
  
## <a name="see-also"></a>Voir aussi
- [IALink, interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [IALink2, interface](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [API ALink](../../../../docs/framework/unmanaged-api/alink/index.md)
