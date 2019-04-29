---
title: Énumération de CLRDataSourceType
ms.date: 01/16/2019
api.name:
- CLRDataSourceType Enumeration
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDataSourceType Enumeration
helpviewer.keywords:
- CLRDataSourceType Enumeration [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: c8b3f338659e2784db8deca3e1776e7926c30c32
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61609678"
---
# <a name="clrdatasourcetype-enumeration"></a>Énumération de CLRDataSourceType

Fournit des valeurs qui sont utilisées par la structure CLRDATA_IL_ADDRESS_MAP.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```
typedef enum
{
    CLRDATA_SOURCE_TYPE_INVALID        = 0x00, // To indicate that nothing else applies
} CLRDataSourceType;
```

## <a name="members"></a>Membres

| Membre                        | Description                           |
| ----------------------------- | ------------------------------------- |
| `CLRDATA_SOURCE_TYPE_INVALID` | Pour indiquer que rien d’autre ne s’applique. |

## <a name="remarks"></a>Notes

Cette énumération réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque. Pour l’utiliser, définir une énumération comme indiqué ci-dessus dans votre code. Il s’agit également d’un alias à `CLRDATA_ENUM` comme indiqué dans [des Types de données courants](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.  
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Énumérations de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
