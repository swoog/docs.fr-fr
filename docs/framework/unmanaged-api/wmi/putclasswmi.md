---
title: PutClassWmi (fonction) (référence des API non managées)
description: La fonction PutClassWmi crée une nouvelle classe ou mettre à jour.
ms.date: 11/06/2017
api_name:
- PutClassWmi
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- PutClassWmi
helpviewer_keywords:
- PutClassWmi function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: de08662a825a84f19a40863cf73481d89364ebd0
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43258543"
---
# <a name="putclasswmi-function"></a>PutClassWmi (fonction)
Crée une nouvelle classe ou mettre à jour.  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT PutClassWmi (
   [in] IWbemClassObject*    pObject,
   [in] long                 lFlags,
   [in] IWbemContext*        pCtx,
   [out] IWbemCallResult**   ppCallResult
); 
```  

## <a name="parameters"></a>Paramètres

`pObject`    
[in] Pointeur vers une définition de classe valide. Il doit être initialisé correctement avec toutes les valeurs de propriété requise.

`lFlags`   
[in] Combinaison d’indicateurs qui affectent le comportement de cette fonction. Les valeurs suivantes sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code : 

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_FLAG_USE_AMENDED_QUALIFIERS` | 0 x 20000 | Si le jeu, WMI ne stocke pas les qualificateurs avec la version modifiée. </br> Si ce n’est pas ensemble, il est supposé que cet objet n’est pas localisé, et tous les qualificateurs sont storedwith cette instance. |
| `WBEM_FLAG_CREATE_OR_UPDATE` | 0 | Créer la classe si elle n’existe pas, ou remplacer si elle existe déjà. |
| `WBEM_FLAG_UPDATE_ONLY` | 1 | Mettre à jour de la classe. La classe doit exister pour l’appel réussisse. |
| `WBEM_FLAG_CREATE_ONLY` | 2 | Créer la classe. L’appel échoue si la classe existe déjà. |
| `WBEM_FLAG_RETURN_IMMEDIATELY` | 0x10 | L’indicateur provoque un appel semi-synchrone. |
| `WBEM_FLAG_OWNER_UPDATE` | 0 x 10000 | Fournisseurs de push doivent spécifier cet indicateur lors de l’appel `PutClassWmi` pour indiquer que cette classe a changé. |
| `WBEM_FLAG_UPDATE_COMPATIBLE` | 0 | Permet à une classe à mettre à jour s’il existe aucune classe dérivée et aucune instance de cette classe. Autorise également les mises à jour dans tous les cas si la modification consiste simplement à des qualificateurs sans importance, telles que le qualificateur de Description. Si la classe a des instances ou les modifications doivent qualificateurs importants, la mise à jour échoue. |
| `WBEM_FLAG_UPDATE_SAFE_MODE` | 0 x 20 | Permet des mises à jour des classes même s’il existe des classes enfants tant que la modification n’entraîne pas de tous les conflits avec les classes enfants. Par exemple, cet indicateur permet une nouvelle propriété à ajouter à la classe de base qui n’a pas été précédemment mentionnée dans les classes enfants. Si la classe a des instances, la mise à jour échoue. |
| `WBEM_FLAG_UPDATE_FORCE_MODE` | 0 x 40 | force les mises à jour des classes lorsque les classes enfants en conflit existent. Par exemple, cet indicateur de force une mise à jour si un qualificateur de classe est défini dans une classe enfant et la classe de base essaie d’ajouter le même qualificateur qui est en conflit avec thte un existant. En mode de force, conflit de tis est résolu par la suppression du qualificateur dans la classe enfant. |

`pCtx`  
[in] En règle générale, cette valeur est `null`. Sinon, il est un pointeur vers un [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) instance qui peut être utilisé par le fournisseur qui fournit les classes demandées. 

`ppCallResult`  
[out] Si `null`, ce paramètre n’est pas utilisé. Si `lFlags` contient `WBEM_FLAG_RETURN_IMMEDIATELY`, la fonction retourne immédiatement avec `WBEM_S_NO_ERROR`. Le `ppCallResult` paramètre reçoit un pointeur vers un nouveau [IWbemCallResult](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult) objet.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_E_ACCESS_DENIED` | 0 x 80041003 | L’utilisateur n’a pas d’autorisation pour créer ou modifier des classes. |
| `WBEM_E_FAILED` | 0 x 80041001 | Une erreur non spécifiée s’est produite. |
| `WBEM_E_INVALID_CLASS` | 0 x 80041010 | La classe spécifiée n’est pas valide. En règle générale, cela indique que `pObject` spécifie un objet d’instance. |
| `WBEM_E_INVALID_PARAMETER` | 0 x 80041008 | Un paramètre n’est pas valide. |
| `WBEM_E_INVALID OPERATION` | 0x80041016 | Le nom de la classe spécifiée n’est pas valid. |
| `WBEM_E_CLASS_HAS_CHILDREN` | 0x80041025 | Une tentative a été effectuée pour apporter une modification qui invaliderait une sous-classe. |
| `WBEM_E_ALREADY_EXISTS` | 0x80041019 | Le `WBEM_FLAG_CREATE_ONLY` indicateur a été spécifié, mais la classe existe déjà. |
| `WBEM_E_NOT_FOUND` | 0x80041002 | `WBEM_FLAG_UPDATE_ONLY` a été spécifié dans `lFlags`, et la classe est introuvable. |
| `WBEM_E_INCOMPLETE_CLASS` | 0x80041020 | Les propriétés requises pour les classes ont pas toutes été définies. |
| `WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Mémoire est insuffisante pour terminer l’opération. |
| `WBEM_E_SHUTTING_DOWN` | 0x80041033 | WMI s’est probablement arrêté et redémarrage. Appelez [ConnectServerWmi](connectserverwmi.md) à nouveau. |
| `WBEM_E_TRANSPORT_FAILURE` | 0x80041015 | Le lien remote procedure call (RPC) entre les processus en cours et WMI a échoué. |
| `WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |
  
## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemServices::PutClass](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass) (méthode).

L’utilisateur ne peut pas créer les classes dont les noms commencent ou finir par un trait de soulignement chacater

Si l’appel de fonction échoue, vous pouvez obtenir des informations d’erreur supplémentaires en appelant le [GetErrorInfo](geterrorinfo.md) (fonction).

## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[WMI et compteurs de performances (référence des API non managées)](index.md)
