---
title: Getpropertyorigin, fonction (référence des API Unmnaged)
description: Getpropertyorigin, de la fonction détermine la classe dans laquelle une propriété est déclarée.
ms.date: 11/06/2017
api_name:
- GetPropertyOrigin
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetPropertyOrigin
helpviewer_keywords:
- GetPropertyOrigin function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 86c512f25c40f201d818b6789c6410bfb095b878
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43488116"
---
# <a name="getpropertyorigin-function"></a>Getpropertyorigin, fonction
Détermine la classe dans laquelle une propriété est déclarée.

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetPropertyOrigin (
   [in] int                 vFunc, 
   [in] IWbemClassObject*   ptr, 
   [in] LPCWSTR             wszMethodName,
   [out] BSTR*              pstrClassName
); 
```  

## <a name="parameters"></a>Paramètres

`vFunc`  
[in] Ce paramètre n’est pas utilisé.

`ptr`  
[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.

`wszMethodName`  
[in] Le nom de la propriété de l’objet dont la classe propriétaire est demandée. 

`pstrClassName`  
[out] Reçoit le nom de la classe qui possède la propriété.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
|`WBEM_E_FAILED` | 0 x 80041001 | Il y a eu une défaillance générale. |
|`WBEM_E_NOT_FOUND` | 0x80041002 | La propriété spécifiée est introuvable. |
|`WBEM_E_INVALID_PARAMETER` | 0 x 80041008 | Un paramètre n’est pas valide. |
|`WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Mémoire est insuffisante pour terminer l’opération. |
|`WBEM_S_NO_ERROR` | 0 | L’appel de fonction a réussi.  |
  
## <a name="remarks"></a>Notes

Cette fonction encapsule un appel à la [IWbemClassObject::GetPropertyOrigin](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getpropertyorigin) (méthode).

Car une classe peut hériter des propriétés d’une ou plusieurs classes de base, les développeurs souhaitent souvent de déterminer la propriété dans lequel une méthode donnée est définie.

Le `pstrClassName` paramètre ne doit pas pointer vers un valide `BSTR` avant que la fonction est appelée, car il s’agit d’un `out` paramètre ; ce pointeur n’est pas libéré une fois que la fonction retourne.

## <a name="requirements"></a>Configuration requise  
**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[WMI et compteurs de performances (référence des API non managées)](index.md)
