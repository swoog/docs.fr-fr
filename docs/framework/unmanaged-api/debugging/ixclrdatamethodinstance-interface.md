---
title: Interface de IXCLRDataMethodInstance
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodInstance Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodInstance Interface
helpviewer.keywords:
- IXCLRDataMethodInstance Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 5bf724bc76591ae59c073b5b9a788ca065f51dc0
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416390"
---
# <a name="ixclrdatamethodinstance-interface"></a>Interface de IXCLRDataMethodInstance

Fournit des méthodes pour obtenir des informations sur une instance de méthode.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a>Méthodes

| Méthode                                                                                                                  | Description                                 |
| ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| [GetILAddressMap](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-getiladdressmap-method.md) | Obtient le langage intermédiaire aux informations de mappage d’adresse. |

## <a name="remarks"></a>Notes

Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque. Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `ECD73800-22CA-4b0d-AB55-E9BA7E6318A5` qui peuvent être obtenues via les mécanismes COM habituels.

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.  
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
