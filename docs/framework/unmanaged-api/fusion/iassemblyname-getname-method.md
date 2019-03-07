---
title: IAssemblyName::GetName, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetName
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetName
helpviewer_keywords:
- GetName method, IAssemblyName interface [.NET Framework debugging]
- IAssemblyName::GetName method [.NET Framework fusion]
ms.assetid: 1dee9781-1cf3-48a9-a376-d18ea1f73280
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fe0b465d0e15fadde48c2278aa367632bda3f9ef
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473822"
---
# <a name="iassemblynamegetname-method"></a>IAssemblyName::GetName, méthode
Obtient le nom simple, non chiffré de l’assembly référencé par ce [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetName (  
    [in, out] LPDWORD lpcwBuffer,  
    [out]     WCHAR *pwzName  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `lpcwBuffer`  
 [in, out] La taille de `pwzName` en caractères larges, y compris le caractère de marque de fin null.  
  
 `pwzName`  
 [out] Une mémoire tampon pour contenir le nom de l’assembly référencé.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IAssemblyName, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
