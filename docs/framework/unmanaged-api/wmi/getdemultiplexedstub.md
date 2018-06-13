---
title: GetDemultiplexedStub (fonction) (référence des API non managées)
description: La fonction GetDemultiplexedStub crée un récepteur de redirecteur d’objet pour aider un client lors de la réception des appels asynchrones de la gestion de Windows.
ms.date: 11/06/2017
api_name:
- GetDemultiplexedStub
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetDemultiplexedStub
helpviewer_keywords:
- GetDemultiplexedStub function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6b195d3a512c537ca409bd2039add9e69abaf4df
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33456360"
---
# <a name="getdemultiplexedstub-function"></a>GetDemultiplexedStub (fonction)
Crée un récepteur de redirecteur d’objet pour aider un client lors de la réception des appels asynchrones de la gestion de Windows.
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetDemultiplexedStub (
   [in] IUnknown*    pObject, 
   [in] boolean      isLocal, 
   [out] IUnknown**  ppObject
); 
```  

## <a name="parameters"></a>Paramètres

`pObject`  
[in] Un pointeur à l’implémentation du client dans le processus de [IWbemObjectSink](https://msdn.microsoft.com/library/aa391787(v=vs.85).aspx).

`isLocal`  
[in] Un indicateur qui indique si l’événement est locale (`true`) ; sinon, `false`.

`ppObject`  
[out] Un récepteur de redirecteur objet pour aider un client lors de la réception des appels asynchrones de la gestion de Windows.

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est `S_OK` (0).

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro. Pour obtenir des informations d’erreur plus complètes, appelez le [GetErrorInfo](geterrorinfo.md) (fonction).
    
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[WMI et les compteurs de Performance (référence des API non managées)](index.md)
