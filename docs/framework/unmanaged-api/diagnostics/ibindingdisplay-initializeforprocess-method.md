---
title: IBindingDisplay::InitializeForProcess, méthode
ms.date: 03/30/2017
api_name:
- IBindingDisplay.InitializeForProcess
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- IBindingDisplay::InitializeForProcess
helpviewer_keywords:
- IBindingDisplay::InitializeForProcess method [.NET Framework debugging]
- InitializeForProcess method [.NET Framework debugging]
ms.assetid: 59417acb-4e59-46ad-acfe-d827e6ab6078
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: aabad159b521207fed976636ae8b9e338f09ac42
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57466178"
---
# <a name="ibindingdisplayinitializeforprocess-method"></a>IBindingDisplay::InitializeForProcess, méthode
Initialise le [IBindingDisplay](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-interface.md) objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT InitializeForProcess (  
    [in] ULONG32   pid  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pid`  
 [in] L’identificateur de processus.  
  
## <a name="remarks"></a>Notes  
 Le débogueur appelle la `InitializeForProcess` méthode au moment de la création pour initialiser l’affichage de la liaison. `InitializeForProcess` doit être appelée au moment de la création avant toute autre méthode sur `IBindingDisplay` est appelée.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** BindingDisplay.h  
  
 **Bibliothèque :** BindingDisplay.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IBindingDisplay, interface](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-interface.md)
