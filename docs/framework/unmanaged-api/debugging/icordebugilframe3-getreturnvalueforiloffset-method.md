---
title: ICorDebugILFrame3::GetReturnValueForILOffset, méthode
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
api_name:
- ICorDebugILFrame3.GetReturnValueForILOffset
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 06522727-5f64-4391-9331-11386883c352
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a01e2fcc7dc00d3a57272abb04ebcecc6d5f74a6
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57467067"
---
# <a name="icordebugilframe3getreturnvalueforiloffset-method"></a>ICorDebugILFrame3::GetReturnValueForILOffset, méthode
Obtient un objet « ICorDebugValue » qui encapsule la valeur de retour d’une fonction.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp
HRESULT GetReturnValueForILOffset(  
    ULONG32 ILoffset,   
    [out] ICorDebugValue **ppReturnValue  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ILOffset`  
 Offset IL. Consultez la section Notes.  
  
 `ppReturnValue`  
 Pointeur vers l’adresse d’un objet d’interface « ICorDebugValue » qui fournit des informations sur la valeur de retour d’un appel de fonction.  
  
## <a name="remarks"></a>Notes  
 Cette méthode est utilisée avec la [ICorDebugCode3::GetReturnValueLiveOffset](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-getreturnvalueliveoffset-method.md) méthode pour obtenir la valeur de retour d’une méthode. Il est particulièrement utile dans le cas des méthodes dont les valeurs de retournés sont ignorées, comme dans les exemples de deux code suivants. Le premier exemple appelle la <xref:System.Int32.TryParse%2A?displayProperty=nameWithType> (méthode), mais ignore la valeur de retour de la méthode.  
  
 [!code-csharp[Unmanaged.Debugging.MRV#1](../../../../samples/snippets/csharp/VS_Snippets_CLR/unmanaged.debugging.mrv/cs/mrv1.cs#1)]
 [!code-vb[Unmanaged.Debugging.MRV#1](../../../../samples/snippets/visualbasic/VS_Snippets_CLR/unmanaged.debugging.mrv/vb/mrv1.vb#1)]  
  
 Le deuxième exemple illustre un problème beaucoup plus courant lors du débogage. Car une méthode est utilisée en tant qu’argument dans un appel de méthode, sa valeur de retour est accessible uniquement lorsque le débogueur parcourt la méthode appelée. Dans de nombreux cas, en particulier lorsque la méthode appelée est définie dans une bibliothèque externe, qui n’est pas possible.  
  
 [!code-csharp[Unmanaged.Debugging.MRV#2](../../../../samples/snippets/csharp/VS_Snippets_CLR/unmanaged.debugging.mrv/cs/mrv2.cs#2)]
 [!code-vb[Unmanaged.Debugging.MRV#2](../../../../samples/snippets/visualbasic/VS_Snippets_CLR/unmanaged.debugging.mrv/vb/mrv2.vb#2)]  
  
 Si vous passez le [ICorDebugCode3::GetReturnValueLiveOffset](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-getreturnvalueliveoffset-method.md) méthode un offset IL à un site d’appel de fonction, elle retourne un ou plusieurs offsets natifs. Le débogueur peut ensuite définir des points d’arrêt sur ces offsets natifs dans la fonction. Lorsque le débogueur atteint un des points d’arrêt, vous pouvez ensuite passer le même offset IL que vous avez passé à cette méthode pour obtenir la valeur de retour. Le débogueur doit ensuite effacer tous les points d’arrêt qu’il a définis.  
  
> [!WARNING]
>  Le [ICorDebugCode3::GetReturnValueLiveOffset Method](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-getreturnvalueliveoffset-method.md) et `ICorDebugILFrame3::GetReturnValueForILOffset` méthodes permettent d’obtenir des informations de valeur de retour pour les types de référence uniquement. Récupération des informations de valeur de retour dans les types valeur (autrement dit, tous les types qui dérivent <xref:System.ValueType>) n’est pas pris en charge.  
  
 L’offset IL spécifié par le `ILOffset` paramètre doivent être sur un site d’appel de fonction, et le programme débogué doit être arrêté par un point d’arrêt défini à l’offset natif retourné par la [ICorDebugCode3::GetReturnValueLiveOffset](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-getreturnvalueliveoffset-method.md) (méthode) pour le même offset IL. Si le programme débogué n’est pas arrêté à l’emplacement correct pour l’offset IL spécifié, l’API échouera.  
  
 Si l’appel de fonction ne retourne aucune valeur, l’API échouera.  
  
 Le `ICorDebugILFrame3::GetReturnValueForILOffset` méthode n’est disponible uniquement sur x86 et les systèmes AMD64.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [GetReturnValueLiveOffset, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-getreturnvalueliveoffset-method.md)
- [ICorDebugILFrame3, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-interface.md)
