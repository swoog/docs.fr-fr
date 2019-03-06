---
title: EndEnumeration, fonction (référence des API non managées)
description: La fonction EndEnumeration met fin à une énumération.
ms.date: 11/06/2017
api_name:
- EndEnumeration
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- EndEnumeration
helpviewer_keywords:
- EndEnumeration function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 65904da9efea90d31960d71ae0da8c81dffeccf1
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57351396"
---
# <a name="endenumeration-function"></a>EndEnumeration, fonction

Met fin à une séquence d’énumération démarrée avec un appel à la [BeginEnumeration, fonction](beginenumeration.md).

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT EndEnumeration (
   [in] int               vFunc,
   [in] IWbemClassObject* ptr
);
```

## <a name="parameters"></a>Paramètres

`vFunc`\
[in] Ce paramètre n’est pas utilisé.

`ptr`\
[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
|`WBEM_E_FAILED` | 0x80041001 | Il y a eu une défaillance générale. |
|`WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |

## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemClassObject::EndEnumeration](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) (méthode).

Un appel à la `EndEnumeration` fonction n’est pas obligatoire, mais il est recommandé car il libère les ressources associées à l’énumération. Toutefois, les ressources sont libérées automatiquement lors de l’énumération suivante est démarrée ou l’objet est libéré.

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** WMINet_Utils.idl

**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]

## <a name="see-also"></a>Voir aussi

- [WMI et compteurs de performances (référence des API non managées)](index.md)