---
title: Fonction CreateIDispatchSTAForwarder (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CreateIDispatchSTAForwarder
api_location:
- PresentationHost_v0400.dll
ms.assetid: 57a02dfa-f091-4ace-9c06-1f4ab52b3527
ms.openlocfilehash: c4da322bf779e084f12529d0da6949ef6ada5cf3
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57379651"
---
# <a name="createidispatchstaforwarder-function-wpf-unmanaged-api-reference"></a>Fonction CreateIDispatchSTAForwarder (référence des API non managées WPF)
Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.  
  
 Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de thread et de windows.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT CreateIDispatchSTAForwarder(  
   __in IDispatch *pDispatchDelegate,   
   __deref_out IDispatch **ppForwarder  
)  
```  
  
#### <a name="parameters"></a>Paramètres  
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de retour  
 pDispatchDelegate  
 Un pointeur vers un `IDispatch` interface.  
  
 ppForwarder  
 Un pointeur vers l’adresse d’un `IDispatch` interface.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).  
  
 **DLL :**  
  
 Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll  
  
 Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll  
  
 **Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Référence des API non managées WPF](wpf-unmanaged-api-reference.md)
