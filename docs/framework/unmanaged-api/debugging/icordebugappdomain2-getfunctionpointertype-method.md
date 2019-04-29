---
title: ICorDebugAppDomain2::GetFunctionPointerType, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain2.GetFunctionPointerType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain2::GetFunctionPointerType
helpviewer_keywords:
- ICorDebugAppDomain2::GetFunctionPointerType method [.NET Framework debugging]
- GetFunctionPointerType method [.NET Framework debugging]
ms.assetid: 0aba6096-5b38-435c-a72a-86d35db4daef
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ec1a9968dbec10783c6f1383fb523e95ff79561e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61683909"
---
# <a name="icordebugappdomain2getfunctionpointertype-method"></a>ICorDebugAppDomain2::GetFunctionPointerType, méthode
Obtient un pointeur vers une fonction qui a une signature donnée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetFunctionPointerType (  
    [in] ULONG32                             nTypeArgs,  
    [in, size_is(nTypeArgs)] ICorDebugType   *ppTypeArgs[],  
    [out] ICorDebugType                      **ppType  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `nTypeArgs`  
 [in] Le nombre d’arguments de type pour la fonction.  
  
 `ppTypeArgs`  
 [in] Tableau de pointeurs, chacun pointant vers un objet de ICorDebugType qui représente un argument de type de la fonction. Le premier élément est le type de retour ; chacun des autres éléments est un type de paramètre.  
  
 `ppType`  
 [out] Un pointeur vers l’adresse d’un `ICorDebugType` objet qui représente le pointeur vers la fonction.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
