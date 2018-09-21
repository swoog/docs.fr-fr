---
title: PutInstanceWmi (fonction) (référence des API non managées)
description: La fonction PutInstanceWmi crée ou met à jour une instance d’une classe existante.
ms.date: 11/06/2017
api_name:
- PutInstanceWmi
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- PutInstanceWmi
helpviewer_keywords:
- PutInstanceWmi function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 67abf017040b9e6bbe9b10e560c8d57c124ae84e
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46526807"
---
# <a name="putinstancewmi-function"></a>PutInstanceWmi (fonction)
Crée ou met à jour une instance d’une classe existante. L’instance est écrite dans le référentiel WMI. 

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT PutInstanceWmi (
   [in] IWbemClassObject*    pInst,
   [in] long                 lFlags,
   [in] IWbemContext*        pCtx,
   [out] IWbemCallResult**   ppCallResult
); 
```  

## <a name="parameters"></a>Paramètres

`pInst`    
[in] Pointeur vers l’instance soit écrit.

`lFlags`   
[in] Combinaison d’indicateurs qui affectent le comportement de cette fonction. Les valeurs suivantes sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code : 

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_FLAG_USE_AMENDED_QUALIFIERS` | 0 x 20000 | Si la valeur, WMI ne stocke pas les qualificateurs avec le **modifié** flavor. </br> Si ce n’est pas ensemble, il est supposé que cet objet n’est pas localisé, et tous les qualificateurs sont storedwith cette instance. |
| `WBEM_FLAG_CREATE_OR_UPDATE` | 0 | Créer l’instance s’il n’existe pas, ou remplacer si elle existe déjà. |
| `WBEM_FLAG_UPDATE_ONLY` | 1 | Mettre à jour l’instance. L’instance doit exister pour l’appel réussisse. |
| `WBEM_FLAG_CREATE_ONLY` | 2 | Créer l’instance. L’appel échoue si l’instance existe déjà. |
| `WBEM_FLAG_RETURN_IMMEDIATELY` | 0x10 | L’indicateur provoque un appel semi-synchrone. |

`pCtx`  
[in] En règle générale, cette valeur est `null`. Sinon, il est un pointeur vers un [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) instance qui peut être utilisé par le fournisseur qui fournit les classes demandées. 

`ppCallResult`  
[out] Si `null`, ce paramètre n’est pas utilisé. Si `lFlags` contient `WBEM_FLAG_RETURN_IMMEDIATELY`, la fonction retourne immédiatement avec `WBEM_S_NO_ERROR`. Le `ppCallResult` paramètre reçoit un pointeur vers un nouveau [IWbemCallResult](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult) objet.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_E_ACCESS_DENIED` | 0 x 80041003 | L’utilisateur n’a pas autorisé à mettre à jour une instance de la classe spécifiée. |
| `WBEM_E_FAILED` | 0 x 80041001 | Une erreur non spécifiée s’est produite. |
| `WBEM_E_INVALID_CLASS` | 0 x 80041010 | La classe de prise en charge de cette instance n’est pas valide. |
| `WBEM_E_ILLEGAL_NULL` | 0x80041028 | un `null` a été spécifié pour une propriété qui ne peut pas être `null`, tel que celui qui est marquée par un **indexé** ou **Not_Null** qualificateur. |
| `WBEM_E_INVALID_OBJECT` | 0x8004100f | L’instance spécifiée n’est pas valide. (Par exemple, l’appel `PutInstanceWmi` avec une classe retourne cette valeur.) |
| `WBEM_E_INVALID_PARAMETER` | 0 x 80041008 | Un paramètre n’est pas valide. |
| `WBEM_E_ALREADY_EXISTS` | 0x80041019 | Le `WBEM_FLAG_CREATE_ONLY` indicateur a été spécifié, mais l’instance existe déjà. |
| `WBEM_E_NOT_FOUND` | 0x80041002 | `WBEM_FLAG_UPDATE_ONLY` a été spécifié dans `lFlags`, mais l’instance n’existe pas. |
| `WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Mémoire est insuffisante pour terminer l’opération. |
| `WBEM_E_SHUTTING_DOWN` | 0x80041033 | WMI s’est probablement arrêté et redémarrage. Appelez [ConnectServerWmi](connectserverwmi.md) à nouveau. |
| `WBEM_E_TRANSPORT_FAILURE` | 0x80041015 | Le lien remote procedure call (RPC) entre les processus en cours et WMI a échoué. |
| `WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi. |
  
## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemServices::PutInstance](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) (méthode).

Le `PutInstanceWmi` fonction prend en charge la création d’instances et la mise à jour des instances de classes existantes uniquement.  Selon la façon dont le `pCtx` paramètre est défini, certaines ou toutes les propriétés de l’instance sont mis à jour. 

Lorsque l’instance vers laquelle pointe `pInst` appartient à une sous-classe, la gestion de Windows appelle tous les fournisseurs de responsables pour les classes dont dérive la sous-classe. Tous ces fournisseurs doivent réussir pour que l’original `PutInstanceWmi` demande réussisse. Le fournisseur de prise en charge de la classe plus haut dans la hiérarchie est appelé en premier. L’ordre d’appel continue avec la sous-classe de la classe au premier plan et se poursuit à partir de haut en bas jusqu'à ce que Windows Management atteigne le fournisseur pour la classe qui possède l’instance vers laquelle pointé `pInst`.
Gestion de Windows n’appelle pas les fournisseurs pour les classes enfants d’une instance. 

Lorsqu’une application doit mettre à jour une instance qui appartient à une hiérarchie de classes, le `pInst` paramètre doit pointer vers l’instance qui contient les propriétés à modifier. Autrement dit, prenons un exemple de cible qui appartient à **ClassB**. Le **ClassB** instance dérive **ClassA**, et **ClassA** définit la propriété **PropA**. Si une application souhaite apporter une modification à la valeur de **PropA** dans le **ClassB** instance, elle doit définir `pInst` à cette instance, plutôt qu’à une instance de **ClassA** .

Appel de `PutInstanceWmi` sur une instance d’une classe abstraite n’est pas autorisée.

Si l’appel de fonction échoue, vous pouvez obtenir des informations d’erreur supplémentaires en appelant le [GetErrorInfo](geterrorinfo.md) (fonction).

## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[WMI et compteurs de performances (référence des API non managées)](index.md)
