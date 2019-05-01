---
title: CorMethodImpl, énumération
ms.date: 03/30/2017
api_name:
- CorMethodImpl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorMethodImpl
helpviewer_keywords:
- CorMethodImpl enumeration [.NET Framework metadata]
ms.assetid: ffbb3caf-20da-4a4b-8983-77376e72b990
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2138dd32cf39db7b7c8989ba5827178d1a1e46c7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62045563"
---
# <a name="cormethodimpl-enumeration"></a>CorMethodImpl, énumération
Contient des valeurs qui décrivent les fonctionnalités d’implémentation d’une méthode.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorMethodImpl {  
  
    miCodeTypeMask      =   0x0003,  
    miIL                =   0x0000,  
    miNative            =   0x0001,  
    miOPTIL             =   0x0002,  
    miRuntime           =   0x0003,  
  
    miManagedMask       =   0x0004,  
    miUnmanaged         =   0x0004,  
    miManaged           =   0x0000,  
  
    miForwardRef        =   0x0010,  
    miPreserveSig       =   0x0080,  
  
    miInternalCall      =   0x1000,  
    miSynchronized      =   0x0020,  
    miNoInlining        =   0x0008,  
    miAggressiveInlining =  0x0100,  
    miNoOptimization     =  0x0040,  
    miMaxMethodImplVal  =   0xffff  
  
} CorMethodImpl;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`miCodeTypeMask`|Indicateurs qui décrivent le type de code.|  
|`miIL`|Spécifie que l’implémentation de méthode est Microsoft intermediate language (MSIL).|  
|`miNative`|Spécifie que l’implémentation de la méthode est native.|  
|`miOPTIL`|Spécifie que l’implémentation de méthode est OPTIL.|  
|`miRuntime`|Spécifie que l’implémentation de méthode est fournie par le common language runtime.|  
|`miManagedMask`|Indicateurs qui indiquent si le code est géré ou non géré.|  
|`miUnmanaged`|Spécifie que l’implémentation de méthode n’est pas gérée.|  
|`miManaged`|Spécifie que l’implémentation de méthode est gérée.|  
|`miForwardRef`|Spécifie que la méthode est définie. Cet indicateur est utilisé principalement dans les scénarios de fusion.|  
|`miPreserveSig`|Spécifie que la signature de méthode ne peut pas être tronquée pour une conversion HRESULT.|  
|`miInternalCall`|Réservé à un usage interne par le common language runtime.|  
|`miSynchronized`|Spécifie que la méthode est à thread unique son corps.|  
|`miNoInlining`|Spécifie que la méthode ne peut pas être inline.|  
|`miAggressiveInlining`|Spécifie que la méthode doit être inline si possible.|  
|`miNoOptimization`|Spécifie que la méthode ne doit pas être optimisée.|  
|`miMaxMethodImplVal`|La valeur valide maximale pour un `CorMethodImpl`.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorHdr.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
