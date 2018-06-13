---
title: ICorDebugThread::EnumerateChains, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread.EnumerateChains
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::EnumerateChains
helpviewer_keywords:
- EnumerateChains method [.NET Framework debugging]
- ICorDebugThread::EnumerateChains method [.NET Framework debugging]
ms.assetid: ec00bc21-117e-4acd-9301-2cfafd5be8d3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: caeb60c33580f7171a6959c3046cf7312868851b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420552"
---
# <a name="icordebugthreadenumeratechains-method"></a>ICorDebugThread::EnumerateChains, méthode
Obtient un pointeur d’interface vers un énumérateur ICorDebugChainEnum qui contient toutes les chaînes de pile dans cet objet ICorDebugThread.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumerateChains (  
    [out] ICorDebugChainEnum **ppChains  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppChains`  
 [out] Un pointeur vers l’adresse d’un `ICorDebugChainEnum` objet qui permet l’énumération de la pile de toutes les chaînes dans ce thread, en commençant par la chaîne active (c'est-à-dire, la plus récente).  
  
## <a name="remarks"></a>Notes  
 La chaîne de pile représente la pile des appels physique pour le thread. Les circonstances suivantes créer une limite de chaîne de pile :  
  
-   Une transition managé à managé ou non managé à managé.  
  
-   Un changement de contexte.  
  
-   Un blocage d’un thread de l’utilisateur du débogueur.  
  
 Dans le cas simple d’un thread qui exécute du code managé uniquement dans un contexte unique, une correspondance existera entre les threads et les chaînes de pile.  
  
 Un débogueur peut être amené à réorganiser les piles des appels physiques de tous les threads dans les piles d’appels logiques. Cela implique le tri de chaînes de tous les threads par leurs relations appelant/appelé et le regroupement.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
