---
title: ICorDebugSymbolProvider::GetMethodProps, méthode
ms.date: 03/30/2017
ms.assetid: 8f836b80-b7a5-460b-bf76-5f0e45652aea
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f52d20b9cb717d72d660bb19a0474c3e5b293ab4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422189"
---
# <a name="icordebugsymbolprovidergetmethodprops-method"></a>ICorDebugSymbolProvider::GetMethodProps, méthode
Retourne des informations sur les propriétés de la méthode, telles que le jeton de métadonnées de la méthode et des informations sur ses paramètres génériques, en fonction d'une adresse virtuelle relative (RVA) dans cette méthode.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetMethodProps(  
   [in]  ULONG32 codeRva,  
   [out] mdToken *pMethodToken,  
   [out] ULONG32 *pcGenericParams,  
   [in]  ULONG32 cbSignature,  
   [out] ULONG32 *pcbSignature,  
   [out, size_is(cbSignature), length_is(*pcbSignature)] BYTE signature[]  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `codeRVA`  
 [in] Adresse virtuelle relative dans la méthode sur les informations à récupérer.  
  
 `pMethodToken`  
 [out] Pointeur vers le jeton de métadonnées de la méthode.  
  
 `pcGenericParams`  
 [out] Pointeur vers le nombre de paramètres génériques associés à cette méthode.  
  
 `cbSignature`  
 [in] Taille du tableau `signature`. Consultez la section Notes.  
  
 `pcbSignature`  
 [out] Pointeur vers la taille du tableau `signature` retourné.  
  
 `signature`  
 [out] Mémoire tampon qui conserve les signatures typespec de tous les paramètres génériques.  
  
## <a name="remarks"></a>Notes  
 Pour obtenir la taille requise de la méthode `signature` de tableau, définissez la `cbSignature` argument 0 et `signature` à **null**. Suite au retour de la méthode, `pcbSignature` contient le nombre d'octets requis pour le tableau `signature`.  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [GetTypeProps, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-gettypeprops-method.md)  
 [ICorDebugSymbolProvider, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
