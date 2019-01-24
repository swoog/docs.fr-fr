---
title: Fonction SaveToHistory (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- SaveToHistory
api_location:
- PresentationHost_v0400.dll
ms.assetid: 6dd101a3-44ad-4143-b228-772156f9b8ff
ms.openlocfilehash: 680c63548482c413a7ceff24a4f38eed589f4682
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745270"
---
# <a name="savetohistory-function-wpf-unmanaged-api-reference"></a>Fonction SaveToHistory (référence des API non managées WPF)
Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.  
  
 Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de windows.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT SaveToHistory(  
   __in_ecount(1) IStream* pHistoryStream  
)  
```  
  
#### <a name="parameters"></a>Paramètres  
 pHistoryStream  
 Un pointeur vers le flux de l’historique.  
  
## <a name="requirements"></a>Spécifications  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [requise du .NET Framework](../../../../docs/framework/get-started/system-requirements.md).  
  
 **DLL :**  
  
 Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll  
  
 Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll  
  
 **Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Référence des API non managées WPF](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
