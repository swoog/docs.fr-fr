---
title: CreateInstanceEnumWmi (fonction) (référence des API non managées)
description: La fonction CreateInstanceEnumWmi retourne un énumérateur qui contient les instances d’une classe spécifiée qui répondent aux critères de sélection.
ms.date: 11/06/2017
api_name:
- CreateInstanceEnumWmi
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- CreateInstanceEnumWmi
helpviewer_keywords:
- CreateInstanceEnumWmi function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8a1d082cae19bd83c90e063d841a0c9e4602bc40
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57373047"
---
# <a name="createinstanceenumwmi-function"></a>CreateInstanceEnumWmi (fonction)

Retourne un énumérateur qui retourne les instances d’une classe spécifiée qui répondent aux critères de sélection spécifiés.

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT CreateInstanceEnumWmi (
   [in] BSTR                    strFilter,
   [in] long                    lFlags,
   [in] IWbemContext*           pCtx,
   [out] IEnumWbemClassObject** ppEnum,
   [in] DWORD                   authLevel,
   [in] DWORD                   impLevel,
   [in] IWbemServices*          pCurrentNamespace,
   [in] BSTR                    strUser,
   [in] BSTR                    strPassword,
   [in] BSTR                    strAuthority
);
```

## <a name="parameters"></a>Paramètres

`strFilter`\
[in] Le nom de la classe pour laquelle des instances sont souhaitées. Ce paramètre ne peut pas être `null`.

`lFlags`\
[in] Combinaison d’indicateurs qui affectent le comportement de cette fonction. Les valeurs suivantes sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_FLAG_USE_AMENDED_QUALIFIERS` | 0x20000 | Si l’ensemble, la fonction récupère les qualificateurs stockées dans l’espace de noms localisé des paramètres régionaux de la connexion actuelle. <br/> Si ce n’est pas le cas, ensemble, la fonction récupère uniquement les qualificateurs stockées dans l’espace de noms immédiate. |
| `WBEM_FLAG_DEEP` | 0 | L’énumération inclut ce et toutes les sous-classes de la hiérarchie. |
| `WBEM_FLAG_SHALLOW` | 1 | L’énumération inclut uniquement les instances pures de cette classe et exclut toutes les instances de sous-classes qui fournissent des propriétés qui que se trouvent ne pas dans cette classe. |
| `WBEM_FLAG_RETURN_IMMEDIATELY` | 0x10 | L’indicateur provoque un appel semi-synchrone. |
| `WBEM_FLAG_FORWARD_ONLY` | 0x20 | La fonction retourne un énumérateur avant uniquement. En règle générale, les énumérateurs avant uniquement sont plus rapides et utilisent moins de mémoire que les énumérateurs classiques, mais ils ne permettent pas d’appels à [Clone](clone.md). |
| `WBEM_FLAG_BIDIRECTIONAL` | 0 | WMI conserve les pointeurs vers les objets dans l’énumération jusqu'à ce qu’ils sont libérés. |

Les indicateurs recommandées sont `WBEM_FLAG_RETURN_IMMEDIATELY` et `WBEM_FLAG_FORWARD_ONLY` pour de meilleures performances.

`pCtx`\
[in] En règle générale, cette valeur est `null`. Sinon, il est un pointeur vers un [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) instance qui peut être utilisé par le fournisseur qui fournit les instances demandées.

`ppEnum`\
[out] Reçoit le pointeur vers l’énumérateur.

`authLevel`\
[in] Le niveau d’autorisation.

`impLevel`\
[in] Le niveau d’emprunt d’identité.

`pCurrentNamespace`\
[in] Un pointeur vers un [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) objet qui représente l’espace de noms actuel.

`strUser`\
[in] Le nom d’utilisateur. Consultez le [ConnectServerWmi](connectserverwmi.md) (fonction) pour plus d’informations.

`strPassword`\
[in] Le mot de passe. Consultez le [ConnectServerWmi](connectserverwmi.md) (fonction) pour plus d’informations.

`strAuthority`\
[in] Le nom de domaine de l’utilisateur. Consultez le [ConnectServerWmi](connectserverwmi.md) (fonction) pour plus d’informations.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_E_ACCESS_DENIED` | 0x80041003 | L’utilisateur n’a pas l’autorisation d’afficher les instances de la classe spécifiée. |
| `WBEM_E_FAILED` | 0x80041001 | Une erreur non spécifiée s’est produite. |
| `WBEM_E_INVALID_CLASS` | 0x80041010 | `strFilter` n’existe pas. |
| `WBEM_E_INVALID_PARAMETER` | 0x80041008 | Un paramètre n’est pas valide. |
| `WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Mémoire est insuffisante pour terminer l’opération. |
| `WBEM_E_SHUTTING_DOWN` | 0x80041033 | WMI s’est probablement arrêté et redémarrage. Appelez [ConnectServerWmi](connectserverwmi.md) à nouveau. |
| `WBEM_E_TRANSPORT_FAILURE` | 0x80041015 | Le lien remote procedure call (RPC) entre les processus en cours et WMI a échoué. |
|`WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |

## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemServices::CreateClassEnum](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum) (méthode).

Notez que l’énumérateur retourné peut avoir zéro élément.

Si l’appel de fonction échoue, vous pouvez obtenir des informations d’erreur supplémentaires en appelant le [GetErrorInfo](geterrorinfo.md) (fonction).

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** WMINet_Utils.idl

**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]

## <a name="see-also"></a>Voir aussi

- [WMI et compteurs de performances (référence des API non managées)](index.md)