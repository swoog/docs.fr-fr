---
title: DacpGetModuleAddress::Request (méthode)
ms.date: 01/16/2019
api.name:
- DacpGetModuleAddress::Request Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpGetModuleAddress::Request Method
helpviewer.keywords:
- DacpGetModuleAddress::Request Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 86a51605ad8ea8b394c5b8a5961f32e96baf9e58
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416426"
---
# <a name="dacpgetmoduleaddressrequest-method"></a>DacpGetModuleAddress::Request (méthode)

Exécute une requête pour remplir la structure à partir de la structure de runtime donné.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```
HRESULT Request(
    [in] IXCLRDataModule* pDataModule
);
```

### <a name="parameters"></a>Paramètres

`pDataModule` [in] Pointeur vers le module de données de valeur initiale.

## <a name="remarks"></a>Notes

Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque. Pour l’utiliser, le moyen le plus simple est d’imiter l’implémentation :

- Retourne la valeur obtenue en appelant le `Request` méthode sur le `IXCLRDataModule*` paramètre avec les paramètres suivants : `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`


## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.     
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [DacpGetModuleAddress Interface](../../../../docs/framework/unmanaged-api/debugging/dacpgetmoduleaddress-structure.md)