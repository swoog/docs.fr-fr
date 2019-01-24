---
title: IMethodMalloc::Alloc, méthode
ms.date: 03/30/2017
api_name:
- IMethodMalloc.Alloc
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- IMethodMalloc::Alloc
helpviewer_keywords:
- IMethodMalloc::Alloc method [.NET Framework profiling]
- Alloc method, IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8653bd4c-2290-43d2-a3e1-cbbd50033f4f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 54c38f9a9abc9a02ba4d84c9a41b2ef6b1f7cb69
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528561"
---
# <a name="imethodmallocalloc-method"></a>IMethodMalloc::Alloc, méthode
Tente d’allouer une quantité de mémoire spécifiée pour un nouveau corps de fonction Microsoft intermediate language (MSIL).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
PVOID Alloc (  
    [in] ULONG   cb  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `cb`  
 [in] Le nombre d’octets à allouer pour le corps de méthode.  
  
## <a name="remarks"></a>Notes  
 La mémoire allouée commencera à une adresse supérieure à l’adresse de base du module qui est associé à cet allocateur. En d’autres termes, chaque allocateur est créé pour un module particulier et tentera d’allouer de mémoire à un décalage positif à partir de son adresse de base. Si `Alloc` ne parvient pas à allouer le nombre requis d’octets à une adresse supérieure à l’adresse de base du module, il retourne E_OUTOFMEMORY, quelle que soit la quantité réelle d’espace mémoire disponible.  
  
 Le `Alloc` méthode doit être utilisée conjointement avec la [ICorProfilerInfo::SetILFunctionBody](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setilfunctionbody-method.md) (méthode).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** WindSee [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMethodMalloc, interface](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-interface.md)
