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
ms.openlocfilehash: c92b112262aa2bede03bddc1396947b5fdfd6286
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65629988"
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

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** None  
**Bibliothèque :** None  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Débogage](index.md)
- [Interface de ISOSDacInterface](isosdacinterface-interface.md)
