---
title: IAssemblyName::IsEqual, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyName.IsEqual
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::IsEqual
helpviewer_keywords:
- IsEqual method [.NET Framework fusion]
- IAssemblyName::IsEqual method [.NET Framework fusion]
ms.assetid: 6dfc220f-d0d4-45b3-bfce-5829f817766f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 80402234d9374fa4f16e1f8bb315536a9bdfb2c2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697210"
---
# <a name="iassemblynameisequal-method"></a>IAssemblyName::IsEqual, méthode
Détermine si une certaine [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) objet est égal à ce `IAssemblyName`, selon les indicateurs de comparaison spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsEqual (  
    [in] IAssemblyName  *pName,  
    [in] DWORD          dwCmpFlags  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pName`  
 [in] Le `IAssemblyName` objet auquel comparer cette `IAssemblyName`.  
  
 `dwCmpFlags`  
 [in] Une combinaison au niveau du bit de [ASM_CMP_FLAGS pour](../../../../docs/framework/unmanaged-api/fusion/asm-cmp-flags-enumeration.md) valeurs influencer la comparaison.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IAssemblyName, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
- [Énumérations de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-enumerations.md)
