---
title: IXCLRDataModule Interface
ms.date: 01/16/2019
api.name:
- IXCLRDataModule Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule Interface
helpviewer.keywords:
- IXCLRDataModule Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: e306834166051ae48fd283d51f18d9458091578f
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416449"
---
# <a name="ixclrdatamodule-interface"></a>IXCLRDataModule Interface

Fournit des méthodes pour obtenir des informations sur un module chargé.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a>Méthodes

| Méthode                                                                                                                                | Description                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [GetMethodDefinitionByToken](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getmethoddefinitionbytoken-method.md) | Obtient la définition de méthode correspondant à un jeton de métadonnées donné. |
| [Requête](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-request-method.md)                                       | Demandes pour remplir la mémoire tampon spécifiée avec les données du module.       |
| [GetVersionId](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getversionid-method.md)                             | Obtient l’ID de version. du module                                       |

## <a name="remarks"></a>Notes

Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque. Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` qui peuvent être obtenues via les mécanismes COM habituels.

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.  
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
