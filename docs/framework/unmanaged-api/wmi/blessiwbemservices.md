---
title: Blessiwbemservices, fonction (référence des API non managées)
description: Blessiwbemservices, de la fonction indique si les informations d’identification utilisateur autorisent l’accès à une classe IWbemServices.
ms.date: 11/06/2017
api_name:
- BlessIWbemServices
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- BlessIWbemServices
helpviewer_keywords:
- BlessIWbemServices function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a65c3c14507b2520c69875a1bc101ce826ace7ba
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42934302"
---
# <a name="blessiwbemservices-function"></a>Blessiwbemservices, fonction
Indique si les informations d’identification autorisent l’accès spécifié [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) classe.   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT BlessIWbemServices (
   [in] IWbemServices* pIWbemServices,
   [in] BSTR strUser, 
   [in] BSTR strPassword, 
   [in] BSTR strAuthority, 
   [in] DWORD impLevel, 
   [in] DWORD authnLevel
);
```  

## <a name="parameters"></a>Paramètres

`pIWbemServices`  
[in] Un pointeur vers le [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) objet pour lequel les autorisations sont requises.

`strUser`  
[in] Le nom d’utilisateur.

`strPassword`  
[in] Le mot de passe associé `strUser`.

`strAuthority` [in] Le nom de domaine de l’utilisateur. Consultez le [ConnectServerWmi](connectserverwmi.md) (fonction) pour plus d’informations.

`impLevel` [in] Le niveau d’emprunt d’identité.

`authnLevel` [in] Le niveau d’autorisation.

## <a name="return-value"></a>Valeur de retour

Les valeurs suivantes est retournées par cette fonction sont définies dans le *WinError.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :

|Constante  |Value  |Description  |
|---------|---------|---------|
| `E_INVALIDARG` | 0 x 80070057 | Un ou plusieurs arguments ne sont pas valides. |
| `E_POINTER` | 0 x 80004003 | `pIWbemServices` a la valeur `null`. | 
| `E_FAIL` | 0x80000008 | Une erreur non spécifiée s’est produite. |
| `E_OUTOFMEMORY` | 0x80000002 | Mémoire disponible est insuffisante pour effectuer l’opération. | 
| `S_OK` | 0 | L’appel de fonction a réussi. | 

## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[WMI et compteurs de performances (référence des API non managées)](index.md)
