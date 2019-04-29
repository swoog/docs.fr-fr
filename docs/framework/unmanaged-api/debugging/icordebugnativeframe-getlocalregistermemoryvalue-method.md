---
title: ICorDebugNativeFrame::GetLocalRegisterMemoryValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetLocalRegisterMemoryValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetLocalRegisterMemoryValue
helpviewer_keywords:
- ICorDebugNativeFrame::GetLocalRegisterMemoryValue method [.NET Framework debugging]
- GetLocalRegisterMemoryValue method [.NET Framework debugging]
ms.assetid: d350f69d-9aff-4f5a-8301-daea22dee2da
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 26cd30be591c4167fa6a6e4d19ba9d1c909c6428
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61927307"
---
# <a name="icordebugnativeframegetlocalregistermemoryvalue-method"></a>ICorDebugNativeFrame::GetLocalRegisterMemoryValue, méthode
Obtient la valeur d’un argument ou une variable locale, dont le mot de poids faible et fort sont stockés dans l’emplacement de mémoire et le Registre spécifié, respectivement, pour ce frame natif.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetLocalRegisterMemoryValue (  
    [in] CorDebugRegister   highWordReg,  
    [in] CORDB_ADDRESS      lowWordAddress,  
    [in] ULONG              cbSigBlob,  
    [in] PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue    **ppValue  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `highWordReg`  
 [in] Une valeur de l’énumération « CorDebugRegister » qui spécifie le Registre contenant le mot de poids fort de la valeur.  
  
 `lowWordAddress`  
 [in] Un `CORDB_ADDRESS` valeur qui spécifie l’emplacement de mémoire contenant le mot de poids faible de la valeur.  
  
 `cbSigBlob`  
 [in] Entier qui spécifie la taille de la signature de métadonnées binaires qui est référencée par le `pvSigBlob` paramètre.  
  
 `pvSigBlob`  
 [in] Un `PCCOR_SIGNATURE` valeur pointe vers la signature de métadonnées binaires du type de valeur.  
  
 `ppValue`  
 [out] Pointeur vers l’adresse d’un objet « ICorDebugValue » représentant la valeur récupérée qui est stockée dans l’emplacement de Registre et de mémoire spécifié.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
