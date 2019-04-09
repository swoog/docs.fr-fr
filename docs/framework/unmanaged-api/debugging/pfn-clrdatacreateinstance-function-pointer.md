---
title: PFN_CLRDataCreateInstance (pointeur fonction)
ms.date: 03/30/2017
api_name:
- PFN_CLRDataCreateInstance
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- PFN_CLRDataCreateInstance
helpviewer_keywords:
- PFN_CLRDataCreateInstance function pointer [.NET Framework debugging]
ms.assetid: 5c66ac57-d751-4de5-af9f-26ceb949af8b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ff2ddb1e98f3455c6915acf8149f528176228425
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59177981"
---
# <a name="pfnclrdatacreateinstance-function-pointer"></a>PFN_CLRDataCreateInstance (pointeur fonction)
Pointe vers une fonction qui crée un objet d’interface pour l’élément cible spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef HRESULT (STDAPICALLTYPE* PFN_CLRDataCreateInstance) (  
    [in]  REFIID           iid,  
    [in]  ICLRDataTarget  *target,  
    [out] void           **iface  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `iid`  
 [in] L’identificateur de l’interface à instancier.  
  
 `target`  
 [in] Un pointeur vers un implémenté par l’utilisateur [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) objet qui représente l’élément cible pour lequel créer l’objet d’interface.  
  
 `iface`  
 [out] Pointeur vers l’adresse de l’objet de l’interface retournée.  
  
## <a name="remarks"></a>Notes  
 Le `ICLRDataTarget` objet est implémenté par le writer de l’application de débogage. L’implémentation varie selon le type d’élément cible qui est représenté. L’élément cible peut être un processus, vidage de mémoire, ordinateur distant et ainsi de suite.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** ClrData.idl  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Fonctions statiques globales du débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
