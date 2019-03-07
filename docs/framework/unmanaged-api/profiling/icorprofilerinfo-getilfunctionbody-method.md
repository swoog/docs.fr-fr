---
title: ICorProfilerInfo::GetILFunctionBody, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetILFunctionBody
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetILFunctionBody
helpviewer_keywords:
- GetILFunctionBody method [.NET Framework profiling]
- ICorProfilerInfo::GetILFunctionBody method [.NET Framework profiling]
ms.assetid: e29b46bc-5fdc-4894-b0c2-619df4b65ded
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8e98ee26da2d78278435d90d6d04ef9771f41104
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57489447"
---
# <a name="icorprofilerinfogetilfunctionbody-method"></a>ICorProfilerInfo::GetILFunctionBody, méthode
Obtient un pointeur vers le corps d’une méthode dans le code Microsoft intermediate language (MSIL), en commençant à son en-tête.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetILFunctionBody(  
    [in]  ModuleID    moduleId,  
    [in]  mdMethodDef methodId,  
    [out] LPCBYTE     *ppMethodHeader,  
    [out] ULONG       *pcbMethodSize);  
```  
  
## <a name="parameters"></a>Paramètres  
 `moduleId`  
 [in] L’ID du module dans lequel la fonction réside.  
  
 `methodId`  
 [in] Le jeton de métadonnées pour la méthode.  
  
 `ppMethodHeader`  
 [out] Pointeur vers l’en-tête de la méthode.  
  
 `pcbMethodSize`  
 [out] Entier qui spécifie la taille de la méthode.  
  
## <a name="remarks"></a>Notes  
 Une méthode est limitée par le module dans lequel il réside. Étant donné que le `GetILFunctionBody` méthode est conçue pour donner un accès au code MSIL avant qu’il a été chargé par le common language runtime (CLR), il utilise le jeton de métadonnées de la méthode pour rechercher l’instance souhaitée.  
  
 `GetILFunctionBody` peut retourner un HRESULT de CORPROF_E_FUNCTION_NOT_IL si le `methodId` pointe vers une méthode sans code MSIL (comme une méthode abstraite ou une plateforme (méthode) (PInvoke)).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
