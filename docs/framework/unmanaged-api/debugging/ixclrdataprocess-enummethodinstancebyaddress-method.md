---
title: IXCLRDataProcess::EnumMethodInstanceByAddress (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: a51c709b0b331127b74d98c4dc42e2772fd7f2db
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775464"
---
# <a name="ixclrdataprocessenummethodinstancebyaddress-method"></a>IXCLRDataProcess::EnumMethodInstanceByAddress (méthode)

Énumère les instances de la méthode de ce processus, en commençant à un offset d’adresse.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```
HRESULT EnumMethodInstanceByAddress(
    [in] CLRDATA_ENUM              *handle,
    [out] IXCLRDataMethodInstance **method
);
```

## <a name="parameters"></a>Paramètres

`handle`\
[in] Un handle pour énumérer les instances de la méthode.

`mod`\
[out] L’instance de la méthode énumérée.

## <a name="remarks"></a>Notes

La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 28.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).   
**En-tête :** Aucun.   
**Bibliothèque :** Aucun.   
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]   
 
## <a name="see-also"></a>Voir aussi

- [Énumération de CLRDataSourceType](clrdatasourcetype-enumeration.md)
- [Débogage](index.md)
- [Interface de IXCLRDataProcess](ixclrdataprocess-interface.md)
