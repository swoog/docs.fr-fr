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
ms.openlocfilehash: de30384b4c12c4fcac3eafe580484685f8a43fa4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775425"
---
# <a name="ixclrdataprocessendenummodules-method"></a>IXCLRDataProcess::EndEnumModules (méthode)

Libère les ressources utilisées par les itérateurs internes utilisés pendant l’énumération de module.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT EndEnumModules(
    [in] CLRDATA_ENUM handle
);
```

## <a name="parameters"></a>Paramètres

`handle`\
[out] Un handle pour énumérer les modules.

## <a name="remarks"></a>Notes

La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de 26 de la table de la méthode virtuelle.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).
**En-tête :** Aucun **bibliothèque :** Aucun **Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]

## <a name="see-also"></a>Voir aussi

- [Débogage](index.md)
- [Interface de IXCLRDataProcess](ixclrdataprocess-interface.md)
