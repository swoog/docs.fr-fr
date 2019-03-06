---
title: ISOSDacInterface::GetMethodDescPtrFromIP (méthode)
ms.date: 02/01/2019
api.name:
- ISOSDacInterface::GetMethodDescPtrFromIP Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescPtrFromIP Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescPtrFromIP Method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 82c4531ac16e8b4bf7ac45bc01eb7128b9507ab5
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57358533"
---
# <a name="isosdacinterfacegetmethoddescptrfromip-method"></a>ISOSDacInterface::GetMethodDescPtrFromIP (méthode)

Récupère le pointeur de la MethodDesc correspondant de la méthode contenant l’adresse d’instruction natif donné.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```
HRESULT GetMethodDescPtrFromIP(
    CLRDATA_ADDRESS ip,
    CLRDATA_ADDRESS * ppMD
);
```

## <a name="parameters"></a>Paramètres

`ip`\
[in] Une adresse dans la méthode lors de l’exécution.

`ppMD`\
[out] L’adresse de le `MethodDesc` pour la méthode particulière.

## <a name="remarks"></a>Notes

La méthode fournie fait partie de la [ `ISOSDacInterface` interface](isosdacinterface-interface.md) et correspond à l’emplacement de la table de la méthode virtuelle de 21.

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.  
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Débogage](index.md)
- [Interface de ISOSDacInterface](isosdacinterface-interface.md)