---
title: IXCLRDataProcess::EnumModule (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumModule Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumModule Method
helpviewer.keywords:
- IXCLRDataProcess::EnumModule Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: a0398d18f9568754231082d63b4c6a2c865d8c6f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775263"
---
# <a name="ixclrdataprocessenummodule-method"></a>IXCLRDataProcess::EnumModule (méthode)

Énumère les modules de ce processus.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```
HRESULT EnumModule(
    [in, out] CLRDATA_ENUM  *handle,
    [out] IXCLRDataModule  **mod
);
```

## <a name="parameters"></a>Paramètres

`handle`\
[in, out] Un handle pour énumérer les modules.

`mod`\
[out] Le module énuméré.

## <a name="remarks"></a>Notes

La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 25.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.  
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Énumération de CLRDataSourceType](clrdatasourcetype-enumeration.md)
- [Débogage](index.md)
- [Interface de IXCLRDataModule](ixclrdatamodule-interface.md)
- [Interface de IXCLRDataProcess](ixclrdataprocess-interface.md)
