---
title: IXCLRDataModule::GetVersionId (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::GetVersionId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::GetVersionId Method
helpviewer.keywords:
- IXCLRDataModule::GetVersionId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: ac4111abdf6a471aca1eca72a86e33698debbff6
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416402"
---
# <a name="ixclrdatamodulegetversionid-method"></a>IXCLRDataModule::GetVersionId (méthode)

Obtient l’identificateur de version du module.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```
HRESULT GetVersionId(
    [out] GUID* vid
);
```

### <a name="parameters"></a>Paramètres

`vid` [out] Identificateur de version du module.

## <a name="remarks"></a>Notes

La méthode fournie fait partie de la `IXCLRDataModule` interface et correspond à l’emplacement 40E de la table de la méthode virtuelle.

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.  
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Interface de IXCLRDataModule](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
