---
title: QualifierSet_BeginEnumeration (fonction) (référence des API non managées)
description: La fonction QualifierSet_BeginEnumeration réinitialise un énumérateur des qualificateurs d’un objet.
ms.date: 11/06/2017
api_name:
- QualifierSet_BeginEnumeration
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- QualifierSet_BeginEnumeration
helpviewer_keywords:
- QualifierSet_BeginEnumeration function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2d20701237501834c611c4e498c39597cf275176
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43407032"
---
# <a name="qualifiersetbeginenumeration-function"></a>QualifierSet_BeginEnumeration (fonction)
Réinitialise un énumérateur des qualificateurs d’un objet au début de l’énumération.  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT QualifierSet_BeginEnumeration (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LONG                 lFlags
); 
```  

## <a name="parameters"></a>Paramètres

`vFunc`   
[in] Ce paramètre n’est pas utilisé.

`ptr`   
[in] Un pointeur vers un [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.

`lFlags`   
[in] Une combinaison au niveau du bit des indicateurs ou des valeurs décrites dans le [notes](#remarks) section qui spécifie les qualificateurs à inclure dans l’énumération.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | 0 x 80041008 | Le `lFlags` paramètre n’est pas valide. |
|`WBEM_E_UNEXPECTED` | 0x8004101d | Un deuxième appel à `QualifierSet_BeginEnumeration` a été effectuée sans appel intermédiaire à [ `QualifierSet_EndEnumeration` ](qualifierset-endenumeration.md). |
|`WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Pas assez de mémoire est disponible pour commencer une nouvelle énumération. |
|`WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |
  
## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemQualifierSet::BeginEnumeration](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-beginenumeration) (méthode).

Pour énumérer tous les qualificateurs sur un objet, cette méthode doit être appelée avant le premier appel à [QualifierSet_Next](qualifierset-next.md). L’ordre dans lequel les qualificateurs sont énumérés est garanti être indifférente pour une énumération donnée.

Les indicateurs qui peuvent être passés en tant que le `lEnumFlags` argument sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code.   

|Constante  |Value  |Description  |
|---------|---------|---------|
|  | 0 | Retourner les noms de tous les qualificateurs. |
| `WBEM_FLAG_LOCAL_ONLY` | 0x10 | Retourner uniquement les noms des qualificateurs spécifiques à l’objet ou la propriété actuelle. <br/> Pour une propriété : retourner uniquement les qualificateurs spécifiques à la propriété (y compris les substitutions), et pas ces qualificateurs propagés à partir de la définition de classe. <br/> Pour une instance : retourner uniquement les noms d’un qualificateur de nom spécifique à l’instance. <br/> Pour une classe : retourner uniquement des qualificateurs spécifiques à la beiong de classe dérivée.
|`WBEM_FLAG_PROPAGATED_ONLY` | 0 x 20 | Retour uniquement les noms des qualificateurs propagés à partir d’un autre objet. <br/> Pour une propriété : retour uniquement les qualificateurs propagées à cette propriété à partir de la définition de classe et non celles de la propriété proprement dite. <br/> Pour une instance : retour uniquement ces qualificateurs propagés à partir de la définition de classe. <br/> Pour une classe : retour uniquement les noms de qualificateur héritées des classes parentes. |

## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[WMI et compteurs de performances (référence des API non managées)](index.md)
