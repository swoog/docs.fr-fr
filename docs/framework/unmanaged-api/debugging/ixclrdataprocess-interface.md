---
title: IXCLRDataProcess, interface
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess Interface
helpviewer.keywords:
- IXCLRDataProcess Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: ff74a7acb5cc84c177f083c19402cd78977aeab5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775243"
---
# <a name="ixclrdataprocess-interface"></a>IXCLRDataProcess, interface

Fournit des méthodes pour obtenir des informations relatives à un processus.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a>Méthodes

| Méthode                                                                                                                                               | Description                                                                                     |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [GetAppDomainByUniqueId](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-getappdomainbyuniqueid-method.md)                       | Obtient un `AppDomain` dans un processus par son id unique.                                              |
| [StartEnumModules](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-startenummodules-method.md)                                   | Fournit un handle pour énumérer les modules d’un processus.                                        |
| [EnumModule](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-enummodule-method.md)                                               | Énumère les modules de ce processus.                                                         |
| [EndEnumModules](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-endenummodules-method.md)                                       | Libère les ressources utilisées par les itérateurs internes utilisés pendant l’énumération de module.               |
| [StartEnumMethodInstancesByAddress](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-startenummethodinstancesbyaddress-method.md) | Fournit un handle pour énumérer les instances de la méthode de `AppDomain` en commençant à une adresse donnée. |
| [EnumMethodInstanceByAddress](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-enummethodinstancebyaddress-method.md)             | Énumère les instances de la méthode de ce processus, en commençant à un offset d’adresse.                  |
| [EndEnumMethodInstancesByAddress](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-endenummethodinstancesbyaddress-method.md)     | Libère les ressources utilisées par les itérateurs internes utilisés pendant l’énumération de l’instance.             |

## <a name="remarks"></a>Notes

Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque. Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `5c552ab6-fc09-4cb3-8e36-22fa03c798b7` qui peuvent être obtenues via les mécanismes COM habituels.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).   
**En-tête :** Aucun.  
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
