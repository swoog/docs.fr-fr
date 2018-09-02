---
title: ConnectServerWmi (fonction) (référence des API non managées)
description: La fonction ConnectServerWmi utilise DCOM pour créer une connexion à un espace de noms WMI.
ms.date: 11/06/2017
api_name:
- ConnectServerWmi
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- ConnectServerWmi
helpviewer_keywords:
- ConnectServerWmi function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 163e61eef8a753b5b6470285e5e3ce63789e25a4
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43416135"
---
# <a name="connectserverwmi-function"></a>ConnectServerWmi (fonction)
Crée une connexion via DCOM à un espace de noms WMI sur un ordinateur spécifié.  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ConnectServerWmi (
   [in] BSTR               strNetworkResource,
   [in] BSTR               strUser,
   [in] BSTR               strPassword,
   [in] BSTR               strLocale,
   [in] long               lSecurityFlags,
   [in] BSTR               strAuthority,
   [in] IWbemContext*      pCtx,
   [out] IWbemServices**   ppNamespace,
   [in] DWORD              impLevel, 
   [in] DWORD              authLevel
);
```  
## <a name="parameters"></a>Paramètres

`strNetworkResource` [in] Pointeur vers un valide `BSTR` qui contient le chemin d’accès de l’objet de l’espace de noms WMI. Consultez le [notes](#remarks) section pour plus d’informations.

`strUser` [in] Un pointeur vers une valide `BSTR` qui contient le nom d’utilisateur. Un `null` valeur indique le contexte de sécurité actuel. Si l’utilisateur provient d’un autre domaine que celui en cours, `strUser` peut également contenir le nom de domaine et d’utilisateur séparés par une barre oblique inverse. `strUser` peut également être utilisateur principaux (UPN) mettre en forme, suhc comme *userName@domainName*. Consultez le [notes](#remarks) section pour plus d’informations.

`strPassword` [in] Un pointeur vers une valide `BSTR` qui contient le mot de passe. Un `null` indique le contexte de sécurité actuel. Une chaîne vide (« ») indique un mot de passe vide.

`strLocale` [in] Un pointeur vers une valide `BSTR` qui indique les paramètres régionaux corrects pour la récupération d’informations. Pour les identificateurs de paramètres régionaux Microsoft, le format de la chaîne est « MS\_*xxx*», où *xxx* est une chaîne au format hexadécimal qui indique l’identificateur de paramètres régionaux (LCID). Si une variable locale non valide est spécifié, la méthode retourne `WBEM_E_INVALID_PARAMETER` sauf sur Windows 7, où les paramètres régionaux par défaut du serveur sont utilisé à la place. Si « null1, les paramètres régionaux est utilisé. 
 
`lSecurityFlags` [in] Indicateurs à passer à la `ConnectServerWmi` (méthode). Une valeur de zéro (0) pour ce paramètre entraîne l’appel à `ConnectServerWmi` retourner uniquement une fois une connexion au serveur est établie. Cela peut entraîner une application ne répond ne pas indéfiniment si le serveur est rompu. Les autres valeurs valides sont :

| Constante  | Value  | Description  |
|---------|---------|---------|
| `CONNECT_REPOSITORY_ONLY` | 0 x 40 | Réservé à un usage interne. Ne pas utiliser. |
| `WBEM_FLAG_CONNECT_USE_MAX_WAIT` | 0 x 80 | `ConnectServerWmi` retourne en deux minutes ou moins. |

`strAuthority` [in] Le nom de domaine de l’utilisateur. Il peut afficher les valeurs suivantes :

| Value | Description |
|---------|---------|
| vide | L’authentification NTLM est utilisée et le domaine NTLM de l’utilisateur actuel est utilisé. Si `strUser` Spécifie le domaine (l’emplacement recommandé), il ne doit pas être spécifié ici. La fonction retourne `WBEM_E_INVALID_PARAMETER` si vous spécifiez le domaine dans les deux paramètres. |
| Kerberos :*nom principal* | L’authentification Kerberos est utilisée, et ce paramètre contient un nom principal Kerberos. |
| Valeur NTLMDOMAIN :*nom de domaine* | L’authentification NT LAN Manager est utilisée, et ce paramètre contient un nom de domaine NTLM. |

`pCtx`   
[in] En règle générale, ce paramètre est `null`. Sinon, il est un pointeur vers un [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) objet requis par un ou plusieurs fournisseurs de la classe dynamique. 

`ppNamespace`  
[out] Lorsque la fonction retourne, reçoit un pointeur vers un [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) objet lié à l’espace de noms spécifié. Il est défini pour pointer vers `null` lorsqu’il existe une erreur.

`impLevel`  
[in] Le niveau d’emprunt d’identité.

`authLevel`  
[in] Le niveau d’autorisation.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_E_FAILED` | 0 x 80041001 | Il y a eu une défaillance générale. |
| `WBEM_E_INVALID_PARAMETER` | 0 x 80041008 | Un paramètre n’est pas valide. |
| `WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Mémoire est insuffisante pour terminer l’opération. |
| `WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |
  
## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemLocator::ConnectServer](https://msdn.microsoft.com/libraryaa391769%28v=vs.85%29.aspx) (méthode).

 Pour un accès local à l’espace de noms par défaut, `strNetworkResource` peut être un chemin d’accès de l’objet simple : « root\default » ou «\\.\root\default ». Pour accéder à l’espace de noms par défaut sur un ordinateur distant à l’aide de la mise en réseau COM ou compatible avec Microsoft, incluent le nom d’ordinateur : «\\myserver\root\default ». Le nom d’ordinateur peut être une adresse IP ou nom DNS. Le `ConnectServerWmi` fonction peut également se connecter avec les ordinateurs qui exécutent IPv6 à l’aide d’une adresse IPv6.

`strUser` ne peut pas être une chaîne vide. Si le domaine est spécifié dans `strAuthority`, il ne doit pas également figurer dans `strUser`, ou la fonction retourne `WBEM_E_INVALID_PARAMETER`.


## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[WMI et compteurs de performances (référence des API non managées)](index.md)
