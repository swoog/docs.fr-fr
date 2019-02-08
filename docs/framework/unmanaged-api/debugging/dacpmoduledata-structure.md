---
title: DacpModuleData Structure
ms.date: 02/01/2019
api.name:
- DacpModuleData Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpModuleData Structure
helpviewer.keywords:
- DacpModuleData Structure [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: db3fdaa768e3d1b445f08c3964521570631f0965
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828620"
---
# <a name="dacpmoduledata-structure"></a>DacpModuleData Structure

Définit une mémoire tampon de transport pour les informations d’exécution d’un module.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```
struct DacpModuleData
{
    CLRDATA_ADDRESS Address;
    CLRDATA_ADDRESS File; 
    CLRDATA_ADDRESS  ilBase;
    char payLoad[132];
};
```

## <a name="members"></a>Membres

| Membre    | Description                                                             |
| --------- | ----------------------------------------------------------------------- |
| `Address` | Adresse de l’objet de module.                                           |
| `File`    | Pointeur vers le fichier exécutable portable (PE).                       |
| `ilBase`  | L’adresse de l’image chargée de base.                                 |
| `payLoad` | Un tampon de la charge utile pour les informations de module supplémentaire utilisées par le runtime. |


## <a name="remarks"></a>Notes

Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque. Pour l’utiliser, définir la structure comme indiqué ci-dessus.

## <a name="requirements"></a>Spécifications
**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.  
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Structures de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
