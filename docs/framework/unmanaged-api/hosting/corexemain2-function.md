---
title: _CorExeMain2, fonction
ms.date: 03/30/2017
api_name:
- _CorExeMain2
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- _CorExeMain2
helpviewer_keywords:
- _CorExeMain2 function [.NET Framework hosting]
ms.assetid: 72ea68b4-689f-4733-9416-9664b75e8892
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 573336b32040f44ff1b59fcbb75b59aa00976b5c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33430177"
---
# <a name="corexemain2-function"></a>_CorExeMain2, fonction
Exécute le point d’entrée dans le code mappé en mémoire spécifié. Cette fonction est appelée par le chargeur du système d’exploitation.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
__int32 STDMETHODCALLTYPE _CorExeMain2 (  
   [in] PBYTE           pUnmappedPE,  
   [in] DWORD           cUnmappedPE,  
   [in] __in LPWSTR     pImageNameIn,  
   [in] __in LPWSTR     pLoadersFileName,  
   [in] __in LPWSTR     pCmdLine  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pUnmappedPE`  
 [in] Pointeur vers le code mappé en mémoire.  
  
 `cUnmappedPE`  
 [in] Le nombre d’éléments `pUnmappedPE` peut contenir.  
  
 `pImageNameIn`  
 [in] Pointeur vers le nom de l’image exécutable.  
  
 `pLoadersFileName`  
 [in] Le nom du fichier de chargeur.  
  
 `pCmdLine`  
 [in] Paramètres de ligne de commande, le cas échéant.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Fonctions statiques globales des métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
