---
title: ICorProfilerInfo3::GetRuntimeInformation, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetRuntimeInformation Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetRuntimeInformation
helpviewer_keywords:
- GetRuntimeInformation method [.NET Framework profiling]
- ICorProfilerInfo3::GetRuntimeInformation method [.NET Framework profiling]
ms.assetid: 4400fb8c-0407-4791-8557-f011fd2aee51
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a13e3e525c7f019e7dc49111b88ac374345830af
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59164929"
---
# <a name="icorprofilerinfo3getruntimeinformation-method"></a>ICorProfilerInfo3::GetRuntimeInformation, méthode
Fournit des informations de version sur le common language runtime (CLR) qui est en cours de profilage.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetRuntimeInformation(  
       [out] USHORT *pClrInstanceId,  
       [out] COR_PRF_RUNTIME_TYPE *pRuntimeType,  
       [out] USHORT *pMajorVersion,  
       [out] USHORT *pMinorVersion,  
       [out] USHORT *pBuildNumber,  
       [out] USHORT *pQFEVersion,  
       [in]  ULONG  cchVersionString,  
       [out] ULONG  *pcchVersionString,  
       [out, size_is(cchVersionString), length_is(*pcchVersionString)]  
                   WCHAR  szVersionString[]);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pClrInstanceId`  
 [out] ID représentatif d’une instance CLR en cours d’exécution dans un processus. Ceci est le même que le `ClrInstanceID` que le suivi d’événements pour l’événement de démarrage de Windows (ETW) signale.  
  
 `pRuntimeType`  
 [out] Le type de runtime. Ce paramètre retourne `COR_PRF_DESKTOP_CLR` pour la version de bureau du CLR, ou `COR_PRF_CORE_CLR` pour la version principale du CLR utilisée dans Silverlight.  
  
 `pMajorVersion`  
 [out] Numéro de version principale du CLR.  
  
 `pMinorVersion`  
 [out] Numéro de version mineure du CLR.  
  
 `pBuildVersion`  
 [out] Le numéro de build du CLR.  
  
 `pQFEVersion`  
 [out] Le numéro de version du CLR qui est associé à une mise à jour logicielle.  
  
 `cchVersionString`  
 [in] La longueur, en caractères, de la mémoire tampon qui `szVersionString` pointe vers.  
  
 `pcchVersionString`  
 [out] La longueur, en caractères, de `szVersionString`.  
  
 `szVersionString`  
 [out] La chaîne de version CLR.  
  
## <a name="remarks"></a>Notes  
 Vous pouvez passer null pour n’importe quel paramètre. Toutefois, `pcchVersionString` ne peut pas être null, sauf si `szVersionString` a également la valeur null.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerInfo3, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [Profilage](../../../../docs/framework/unmanaged-api/profiling/index.md)
