---
title: ICLRDataTarget2::AllocVirtual, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2.AllocVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2::AllocVirtual
helpviewer_keywords:
- ICLRDataTarget2::AllocVirtual method [.NET Framework debugging]
- AllocVirtual method [.NET Framework debugging]
ms.assetid: e3226230-964b-47fb-9f53-d6fdbeda1e9e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7ba9200419d6b6fef467ae02bd74101414e125da
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61698003"
---
# <a name="iclrdatatarget2allocvirtual-method"></a>ICLRDataTarget2::AllocVirtual, méthode
Appelé par les services d’accès aux données du common language runtime (CLR) d’allocation de mémoire dans l’espace d’adressage de ce processus cible.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT AllocVirtual(  
    [in] CLRDATA_ADDRESS addr,  
    [in] ULONG32 size,  
    [in] ULONG32 typeFlags,  
    [in] ULONG32 protectFlags,  
    [out] CLRDATA_ADDRESS* virt  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `addr`  
 [in] Un `CLRDATA_ADDRESS` valeur qui spécifie l’adresse de départ demandée de la mémoire à allouer.  
  
 `size`  
 [in] La taille, en octets, de la mémoire à allouer.  
  
 `typeFlags`  
 [in] Indicateurs qui contrôlent l’allocation de mémoire. Consultez Win32 `VirtualAlloc` (fonction).  
  
 `protectFlags`  
 [in] Attributs de protection de la mémoire allouée. Consultez Win32 `VirtualAlloc` (fonction).  
  
 `virt`  
 [out] Un pointeur vers un `CLRDATA_ADDRESS` valeur qui spécifie l’adresse de départ réelle de la mémoire allouée.  
  
## <a name="remarks"></a>Notes  
 Le `AllocVirtual` méthode sert de wrapper logique pour Win32 `VirtualAlloc` (fonction).  
  
 Cette méthode est implémentée par le writer de l'application de débogage.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** ClrData.idl, ClrData.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRDataTarget2, interface](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)
- [FreeVirtual, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-freevirtual-method.md)
