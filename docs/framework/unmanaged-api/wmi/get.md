---
title: Get, fonction (référence des API non managées)
description: La fonction Get récupère la valeur de propriété spécifiée.
ms.date: 11/06/2017
api_name:
- Get
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- Get
helpviewer_keywords:
- Get function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cb7475623961fe2ee5fc821c5f237f0a2acfae1a
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42933331"
---
# <a name="get-function"></a>Get, fonction
Récupère la valeur de propriété spécifiée si elle existe.

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Get (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LPCWSTR           wszName,
   [in] LONG              lFlags,
   [out] VARIANT*         pVal,
   [out] CIMTYPE*         pvtType,
   [out] LONG*            plFlavor
); 
```  

## <a name="parameters"></a>Paramètres

`vFunc`  
[in] Ce paramètre n’est pas utilisé.

`ptr`  
[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.

`wszName`  
[in] Le nom de la propriété.

`lFlags` [in] Réservé. Ce paramètre doit être 0.

`pVal` [out] Si la fonction a été retournée avec succès, contient la valeur de la `wszName` propriété. Le `pval` argument reçoit le type correct et la valeur du qualificateur.

`pvtType` [out] Si la fonction a été retournée avec succès, contient un [constante de type CIM](/windows/desktop/api/wbemcli/ne-wbemcli-tag_cimtype_enumeration) qui indique le type de propriété. Sa valeur peut également être `null`. 

`plFlavor` [out] Si la fonction a été retournée avec succès, reçoit des informations sur l’origine de la propriété. Sa valeur peut être `null`, ou l’une des constantes WBEM_FLAVOR_TYPE suivantes définies dans le *WbemCli.h* fichier d’en-tête : 

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_FLAVOR_ORIGIN_SYSTEM` | 0 x 40 | La propriété est une propriété système standard. |
| `WBEM_FLAVOR_ORIGIN_PROPAGATED` | 0 x 20 | Pour une classe : la propriété est héritée de la classe parente. </br> Pour une instance : la propriété, tandis que héritée de la classe parente, n'a pas été modifiée par l’instance.  |
| `WBEM_FLAVOR_ORIGIN_LOCAL` | 0 | Pour une classe : la propriété appartient à la classe dérivée. </br> Pour une instance : cette propriété est modifiée par l’instance ; Autrement dit, une valeur a été fournie, ou un qualificateur a été ajouté ou modifié. |

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
|`WBEM_E_FAILED` | 0 x 80041001 | Il y a eu une défaillance générale. |
|`WBEM_E_INVALID_PARAMETER` | 0 x 80041008 | Un ou plusieurs paramètres ne sont pas valides. |
|`WBEM_E_NOT_FOUND` | 0x80041002 | La propriété spécifiée est introuvable. |
|`WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Mémoire est insuffisante pour terminer l’opération. |
|`WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |
  
## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemClassObject::Get](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get) (méthode).

Le `Get` fonction peut également retourner les propriétés système.

Le `pVal` argument reçoit le type correct et la valeur pour le qualificateur et le modèle COM [VariantInit](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) (fonction)

## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[WMI et compteurs de performances (référence des API non managées)](index.md)
