---
title: Supprimer (fonction) (référence des API non managées)
description: La fonction de suppression supprime la propriété spécifiée et toutes ses qualificateurs à partir d’une définition de classe CIM.
ms.date: 11/06/2017
api_name:
- Delete
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- Delete
helpviewer_keywords:
- Delete function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 791e75aa60fd651dde1555339e31664a3523e1eb
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46470899"
---
# <a name="delete-function"></a>Supprimer (fonction)
Supprime la propriété spécifiée et toutes ses qualificateurs d’une définition de classe CIM.

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Delete (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LPCWSTR           wszName 
); 
```  

## <a name="parameters"></a>Paramètres

`vFunc`  
[in] Ce paramètre n’est pas utilisé.

`ptr`  
[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.

`wszName`  
[in] Le nom de la propriété à supprimer. `wszName` doit être un pointeur désignant une valide `LPCWSTR`.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
| `WBEM_E_FAILED` | 0 x 80041001 | Une erreur non spécifiée s’est produite. |
| `WBEM_E_INVALID_OPERATION` | 0x80041016 | La propriété ne peut pas être supprimée. |
| `WBEM_E_INVALID_PARAMETER` | 0 x 80041008 | `wszzName` n'est pas valide. |
| `WBEM_E_NOT_FOUND` | 0x80041002 | La propriété spécifiée n’existe pas. |
| `WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Il n’est pas suffisamment de mémoire pour terminer l’opération. |
| `WBEM_E_PROPAGATED_PROPERTY` | 0x8004101c | La propriété est héritée d’une classe de base. |
| `WBEM_E_SYSTEM_PROPERTY` | | La propriété est une propriété système. |
|`WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |
| `WBEM_E_RESET_TO_DEFAULT` | 0x80041030 | La fonction supprimée d’une valeur par défaut de remplacement pour la classe en cours. La valeur par défaut pour cette propriété dans la classe parente a été reactiviated. | 

## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemClassObject::Delete](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-delete) (méthode).

## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[WMI et compteurs de performances (référence des API non managées)](index.md)
