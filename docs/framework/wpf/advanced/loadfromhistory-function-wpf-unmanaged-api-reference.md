---
title: Fonction LoadFromHistory (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- LoadFromHistory
api_location:
- PresentationHost_v0400.dll
ms.assetid: d037c062-a911-4949-b251-ccd3e48b1d17
ms.openlocfilehash: 155b83b8b904350bd6faf73ea21d1db4f83085b7
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57376128"
---
# <a name="loadfromhistory-function-wpf-unmanaged-api-reference"></a>Fonction LoadFromHistory (référence des API non managées WPF)
Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.  
  
 Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de windows.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT LoadFromHistory_export(  
        IStream* pHistoryStream,   
        IBindCtx* pBindCtx  
)  
```  
  
#### <a name="parameters"></a>Paramètres  
 pHistoryStream  
 Pointeur vers un flux d’informations d’historique.  
  
 pBindCtx  
 Pointeur vers un contexte de liaison.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).  
  
 **DLL :**  
  
 Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll  
  
 Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll  
  
 **Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Référence des API non managées WPF](wpf-unmanaged-api-reference.md)
