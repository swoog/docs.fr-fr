---
title: Fonction CompareTo (référence des API non managées)
description: La fonction CompareTo compare un objet à un autre objet WMI.
ms.date: 11/06/2017
api_name:
- CompareTo
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- CompareTo
helpviewer_keywords:
- CompareTo function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bde25ae7455dd7fe35fe1a0a43bb2a6b560c0e3e
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45969809"
---
# <a name="compareto-function"></a>CompareTo (fonction)
Compare un objet à un autre objet WMI.  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a>Syntaxe  
  
```
HRESULT CompareTo (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LONG              flags,
   [in] IWbemClassObject* pCompareTo 
); 
```  

## <a name="parameters"></a>Paramètres

`vFunc`  
[in] Ce paramètre n’est pas utilisé.

`ptr`  
[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.

`flags`  
[in] Combinaison de bits des indicateurs qui spécifient les caractéristiques des objets à prendre en compte pour la comparaison. Consultez le [notes](#remarks) section pour plus d’informations.

`pCompareTo`  

[in] Objet pour la comparaison. `pcompareTo` doit être un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance ; il ne peut pas être `null`.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_E_FAILED` | 0 x 80041001 | Une erreur non spécifiée s’est produite. |
| `WBEM_E_INVALID_PARAMETER` | 0 x 80041008 | Un paramètre n’est pas valide. |
| `WBEM_E_UNEXPECTED` | 0x8004101d | Un deuxième appel à `BeginEnumeration` a été effectuée sans appel intermédiaire à [ `EndEnumeration` ](endenumeration.md). |
| `WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |
| `WBEM_S_DIFFERENT` | 0x40003 | Les objets sont différents. |
| `WBEM_S_SAME` | 0 | Les objets sont identiques selon les indicateurs de comparaison. |
  
## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemClassObject::CompareTo](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-compareto) (méthode).

Les indicateurs qui peuvent être passés en tant que le `lEnumFlags` argument sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code. Vous pouvez spécifier les caractéristiques individuelles impliquées dans la comparaison en spécifiant une combinaison au niveau du bit des indicateurs suivants :

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_FLAG_IGNORE_OBJECT_SOURCE` | 2 | Ignorer la source (le serveur et l’espace de noms que dont elles sont issues). |
| `WBEM_FLAG_IGNORE_QUALIFIERS` | 1 | Ignorer tous les qualificateurs (y compris **clé** et **dynamique**) |
| `WBEM_FLAG_IGNORE_DEFAULT_VALUES` | 4 | Ignorer les valeurs par défaut des propriétés. Cet indicateur s’applique uniquement à la comparaison des classes. |
| `WBEM_FLAG_IGNORE_FLAVOR` | 0 x 20 | Ignorer les versions de qualificateur. Cet indicateur toujours tienne compte, de qualificateurs mais ignore les distinctions de version telles que les règles de propagation et remplace les restrictions. |
| `WBEM_FLAG_IGNORE_CASE` | 0x10 | Ignorer la casse pour comparer les valeurs de chaîne. Cela s’applique à la fois aux chaînes et aux valeurs de qualificateur. La comparaison des noms de propriété et le qualificateur est toujours la casse, même si cet indicateur est défini. |
| `WBEM_FLAG_IGNORE_CLASS` | 0 x 8 | Supposons que les objets comparés sont des instances de la même classe. Par conséquent, cet indicateur compare uniquement des informations relatives aux instances. Utilisez cette indicateurs pour optimiser les performances. Si les objets ne sont pas de la même classe, les résultats sont indéfinis. |

Ou vous pouvez spécifier un indicateur composite unique comme suit :

|Constante  |Value  |Description  |
|---------|---------|---------|
|`WBEM_COMPARISON_INCLUDE_ALL` | 0 | Prendre en compte toutes les fonctionnalités dans la comparaison. |

## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[WMI et compteurs de performances (référence des API non managées)](index.md)
