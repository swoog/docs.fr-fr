---
title: IXCLRDataProcess::EndEnumModules (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EndEnumModules Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EndEnumModules Method
helpviewer.keywords:
- IXCLRDataProcess::EndEnumModules Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 3b7050e92af6fc58b45837840b2796a5deac955c
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57375335"
---
# <a name="ixclrdataprocessendenummodules-method"></a>IXCLRDataProcess::EndEnumModules (méthode)

Libère les ressources utilisées par les itérateurs internes utilisés pendant l’énumération de module.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe
```
HRESULT EndEnumModules(
    [in] CLRDATA_ENUM handle
);
```

## <a name="parameters"></a>Paramètres

`handle`\
[out] Un handle pour énumérer les modules.

## <a name="remarks"></a>Notes

La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de 26 de la table de la méthode virtuelle.

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).   
**En-tête :** Aucun.   
**Bibliothèque :** Aucun.   
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]   

## <a name="see-also"></a>Voir aussi

- [Débogage](index.md)
- [Interface de IXCLRDataProcess](ixclrdataprocess-interface.md)
