---
title: ICorDebugAppDomain2::GetArrayOrPointerType, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain2.GetArrayOrPointerType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain2::GetArrayOrPointerType
helpviewer_keywords:
- GetArrayOrPointerType method [.NET Framework debugging]
- ICorDebugAppDomain2::GetArrayOrPointerType method [.NET Framework debugging]
ms.assetid: 97e493f5-3a62-4ec7-b42f-4af57bf71f57
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cb3f0ca6d930b22f30fe9bbc5b5a04bf1e034f34
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405823"
---
# <a name="icordebugappdomain2getarrayorpointertype-method"></a>ICorDebugAppDomain2::GetArrayOrPointerType, méthode
Obtient un tableau du type spécifié, ou un pointeur ou une référence au type spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetArrayOrPointerType (  
    [in]  CorElementType    elementType,  
    [in]  ULONG32           nRank,  
    [in]  ICorDebugType     *pTypeArg,  
    [out] ICorDebugType     **ppType  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `elementType`  
 [in] Valeur de l’énumération CorElementType qui spécifie le type natif sous-jacent (tableau, pointeur ou référence) à créer.  
  
 `nRank`  
 [in] Le rang (autrement dit, le nombre de dimensions) du tableau. Cette valeur doit être 0 si `elementType` spécifie un pointeur ou type référence.  
  
 `pTypeArg`  
 [in] Un pointeur vers un objet ICorDebugType qui représente le type de tableau, pointeur ou référence à créer.  
  
 `ppType`  
 [out] Un pointeur vers l’adresse d’un `ICorDebugType` type d’objet qui représente le tableau construit, type pointeur ou référence.  
  
## <a name="remarks"></a>Notes  
 La valeur de *elementType* doit être une des opérations suivantes :  
  
-   ELEMENT_TYPE_PTR  
  
-   ELEMENT_TYPE_BYREF  
  
-   ELEMENT_TYPE_ARRAY ou ELEMENT_TYPE_SZARRAY  
  
 Si la valeur de *elementType* est ELEMENT_TYPE_PTR ou ELEMENT_TYPE_BYREF, *nRank* doit être égal à zéro.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
