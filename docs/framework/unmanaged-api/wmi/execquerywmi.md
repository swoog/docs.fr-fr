---
title: Execquerywmi, fonction (référence des API non managées)
description: Execquerywmi, de la fonction exécute une requête pour récupérer des objets.
ms.date: 11/06/2017
api_name:
- ExecQueryWmi
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- ExecQueryWmi
helpviewer_keywords:
- ExecQueryWmi function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 402bbcb9ad5e462a55c5ec2716417f512f03ee19
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57373216"
---
# <a name="execquerywmi-function"></a>Execquerywmi, fonction

Exécute une requête pour récupérer des objets.

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT ExecQueryWmi (
   [in] BSTR                    strQueryLanguage,
   [in] BSTR                    strQuery,
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

`strQueryLanguage`\
[in] Chaîne avec le langage de requête valide pris en charge par la gestion de Windows. Il doit être « WQL », l’acronyme de langage de requête WMI.

`strQuery`\
[in] Le texte de la requête. Ce paramètre ne peut pas être `null`.

`lFlags`\
[in] Combinaison d’indicateurs qui affectent le comportement de cette fonction. Les valeurs suivantes sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

| Constante | Value  | Description  |
|---------|---------|---------|
| `WBEM_FLAG_USE_AMENDED_QUALIFIERS` | 0x20000 | Si l’ensemble, la fonction récupère les qualificateurs stockées dans l’espace de noms localisé des paramètres régionaux de la connexion actuelle. <br/> Si ce n’est pas le cas, ensemble, la fonction récupère uniquement les qualificateurs stockées dans l’espace de noms immédiate. |
| `WBEM_FLAG_RETURN_IMMEDIATELY` | 0x10 | L’indicateur provoque un appel semi-synchrone. |
| `WBEM_FLAG_FORWARD_ONLY` | 0x20 | La fonction retourne un énumérateur avant uniquement. En règle générale, les énumérateurs avant uniquement sont plus rapides et utilisent moins de mémoire que les énumérateurs classiques, mais ils ne permettent pas d’appels à [Clone](clone.md). |
| `WBEM_FLAG_BIDIRECTIONAL` | 0 | WMI conserve les pointeurs vers les objets dans l’énumération jusqu'à ce qu’ils sont libérés. |
| `WBEM_FLAG_ENSURE_LOCATABLE` | 0x100 | Permet de s’assurer que les objets retournés ont suffisamment d’informations dans leur par conséquent, ces propriétés système, telles que **__PATH**, **__RELPATH**, et **__SERVER**, ne sont pas `null`. |
| `WBEM_FLAG_PROTOTYPE` | 2 | Cet indicateur est utilisé pour le prototypage. Il ne s’exécute pas la requête et retourne à la place un objet qui ressemble à un objet de résultat par défaut. |
| `WBEM_FLAG_DIRECT_READ` | 0x200 | Entraîne un accès direct au fournisseur pour la classe spécifiée sans tenir compte de sa classe parente ou n’importe quelles sous-classes. |

Les indicateurs recommandées sont `WBEM_FLAG_RETURN_IMMEDIATELY` et `WBEM_FLAG_FORWARD_ONLY` pour de meilleures performances.

`pCtx`\
[in] En règle générale, cette valeur est `null`. Sinon, il est un pointeur vers un [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) instance qui peut être utilisé par le fournisseur qui fournit les classes demandées.

`ppEnum`\
[out] Si aucune erreur ne se produit, reçoit le pointeur vers l’énumérateur qui permet à l’appelant récupérer les instances dans le jeu de résultats de la requête. La requête peut avoir un jeu de résultats avec zéro instances. Consultez le [notes](#remarks) section pour plus d’informations.

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
| `WBEM_E_ACCESS_DENIED` | 0x80041003 | L’utilisateur n’a pas l’autorisation d’afficher un ou plusieurs des classes qui la fonction peut retourner. |
| `WBEM_E_FAILED` | 0x80041001 | Une erreur non spécifiée s’est produite. |
| `WBEM_E_INVALID_PARAMETER` | 0x80041008 | Un paramètre n’est pas valide. |
| `WBEM_E_INVALID_QUERY` | 0x80041017 | La requête a dû à une erreur de syntaxe. |
| `WBEM_E_INVALID_QUERY_TYPE` | 0x80041018 | Le langage de requête demandé n’est pas pris en charge. |
| `WBEM_E_QUOTA_VIOLATION` | 0x8004106c | La requête est trop complexe. |
| `WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Mémoire est insuffisante pour terminer l’opération. |
| `WBEM_E_SHUTTING_DOWN` | 0x80041033 | WMI s’est probablement arrêté et redémarrage. Appelez [ConnectServerWmi](connectserverwmi.md) à nouveau. |
| `WBEM_E_TRANSPORT_FAILURE` | 0x80041015 | Le lien remote procedure call (RPC) entre les processus en cours et WMI a échoué. |
| `WBEM_E_NOT_FOUND` | 0x80041002 | La requête spécifie une classe qui n’existe pas. |
| `WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |

## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemServices::ExecQuery](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery) (méthode).

Cette fonction traite la requête spécifiée dans le `strQuery` paramètre et crée un énumérateur par le biais duquel l’appelant peut accéder les résultats de requête. L’énumérateur est un pointeur vers un [IEnumWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject) interface ; la requête résultats sont des instances d’objets de classe accessibles via le [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) interface.

Il existe des limites au nombre de `AND` et `OR` mots clés qui peuvent être utilisées dans les requêtes WQL. Grand nombre de mots clés WQL utilisés dans une requête complexe peut provoquer de WMI retourner le `WBEM_E_QUOTA_VIOLATION` (ou 0x8004106c) code d’erreur comme un `HRESULT` valeur. La limite des mots clés WQL dépend de la complexité de la requête est.

Si l’appel de fonction échoue, vous pouvez obtenir des informations d’erreur supplémentaires en appelant le [GetErrorInfo](geterrorinfo.md) (fonction).

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** WMINet_Utils.idl

**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]

## <a name="see-also"></a>Voir aussi

- [WMI et compteurs de performances (référence des API non managées)](index.md)