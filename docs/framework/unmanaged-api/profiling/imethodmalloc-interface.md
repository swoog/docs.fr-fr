---
title: IMethodMalloc, interface
ms.date: 03/30/2017
api_name:
- IMethodMalloc
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- IMethodMalloc
helpviewer_keywords:
- IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8c8ab5dc-557c-473a-82f2-6e403eca7dac
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6f5c21d329ed35f82e36c2d88ac911401799e820
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596018"
---
# <a name="imethodmalloc-interface"></a>IMethodMalloc, interface
Fournit une méthode pour allouer de la mémoire pour un nouveau corps de fonction Microsoft intermediate language (MSIL).  
  
> [!NOTE]
>  Le `IMethodMalloc` interface est un allocateur de mémoire simple. Il vous permet d’allocation de mémoire, mais ne pas à libérer.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Alloc, méthode](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-alloc-method.md)|Tente d’allouer une quantité de mémoire spécifiée pour un nouveau corps de fonction MSIL.|  
  
## <a name="remarks"></a>Notes  
 Chaque allocateur est spécifique au module et vous permet de garantir que le corps de fonction à un décalage positif à partir de la base du module. Mémoire au-dessus de la base d’un module peut être précieuse, l’allocateur doit être utilisé pour allouer de la mémoire uniquement pour un corps de fonction.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
