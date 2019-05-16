---
title: GetMethod, fonction (référence des API non managées)
description: La fonction GetMethod récupère des informations sur une méthode.
ms.date: 11/06/2017
api_name:
- GetMethod
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetMethod
helpviewer_keywords:
- GetMethod function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 419fb33155cfa91199e52110da29efd44d606f4b
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65636608"
---
# <a name="getmethod-function"></a>GetMethod, fonction

Récupère les informations sur la méthode spécifiée.

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT GetMethod (
   [in] int                vFunc,
   [in] IWbemClassObject*   ptr,
   [in] LPCWSTR             wszName,
   [in] LONG                lFlags,
   [out] IWbemClassObject** ppInSignature,
   [out] IWbemClassObject** ppOutSignature
);
```

## <a name="parameters"></a>Paramètres

`vFunc`\
[in] Ce paramètre n’est pas utilisé.

`ptr`\
[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.

`wszName`\
[in] Le nom de la méthode. Ce paramètre ne peut pas être `null` et doit pointer vers un valide `LPCWSTR`.

`lFlags`\
[in] Réservée. Ce paramètre doit être 0.

`ppInSignature`\
[out] Un pointeur vers l’adresse d’un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance qui décrit les paramètres d’entrée à la méthode. Ce paramètre est ignoré si elle est définie sur `null`.

`ppOutSignature`\
[out] Un pointeur vers l’adresse d’un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance qui décrit les paramètres de sortie à la méthode. Ce paramètre est ignoré si elle est définie sur `null`.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
|`WBEM_E_NOT_FOUND` | 0x80041002 | La propriété spécifiée est introuvable. |
|`WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Mémoire est insuffisante pour terminer l’opération. |
|`WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |

## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemClassObject::GetMethod](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod) (méthode).

Gestion de Windows peut définir le [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointeur vers `null` si la méthode n’a aucun paramètre in.

Dans `ppInSignature` et `ppOutSignature` décrivent respectivement, en tant que propriétés dans les paramètres, in et out un `IWbemClassObject` instance de la classe système [_Parameters](/windows/desktop/WmiSdk/--parameters). Les propriétés dans `ppInSignature` sont nommés `Param` *n*, où *n* correspond à la position du paramètre dans la signature de méthode (tel que `Param1`, `Param2`, etc..). Les propriétés dans `ppOutSignature` sont également appelés `Param` *n*, et la valeur de retour est nommée `ReturnValue`. Pour plus d’informations et un exemple, consultez [IWbemClassObject::GetMethod méthode](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod).

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** WMINet_Utils.idl

**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]

## <a name="see-also"></a>Voir aussi

- [WMI et compteurs de performances (référence des API non managées)](index.md)
