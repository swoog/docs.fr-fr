---
title: Fonction ForwardTranslateAccelerator (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ForwardTranslateAccelerator
api_location:
- PresentationHost_v0400.dll
ms.assetid: fff47a86-9d9f-4176-9530-10e1876e393f
ms.openlocfilehash: 78031ed80fe83b736a351886457f9200534f470b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54591511"
---
# <a name="forwardtranslateaccelerator-function-wpf-unmanaged-api-reference"></a>Fonction ForwardTranslateAccelerator (référence des API non managées WPF)
Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.  
  
 Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de windows.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT ForwardTranslateAccelerator(  
   MSG* pMsg,   
   VARIANT_BOOL appUnhandled  
)  
```  
  
#### <a name="parameters"></a>Paramètres  
 pMsg  
 Pointeur vers un message.  
  
 appUnhandled  
 `true` Lorsque l’application a déjà reçue une chance de traiter le message d’entrée, mais n’a pas gérée Sinon, `false`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [requise du .NET Framework](../../../../docs/framework/get-started/system-requirements.md).  
  
 **DLL :**  
  
 Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll  
  
 Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll  
  
 **Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Référence des API non managées WPF](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
