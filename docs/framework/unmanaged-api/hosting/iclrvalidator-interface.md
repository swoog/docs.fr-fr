---
title: ICLRValidator, interface
ms.date: 03/30/2017
api_name:
- ICLRValidator
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRValidator
helpviewer_keywords:
- ICLRValidator interface [.NET Framework hosting]
ms.assetid: 2edd0a10-77fb-4173-91eb-f2970cc364d0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6f34a9aac31fe50974a6f88416d0a00cd72aca8e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511928"
---
# <a name="iclrvalidator-interface"></a>ICLRValidator, interface
Fournit des méthodes pour la validation des images (PE) exécutables portables et de signalement des erreurs de validation.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[FormatEventInfo, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrvalidator-formateventinfo-method.md)|Obtient un message détaillé sur l’erreur de validation spécifié.|  
|[Validate, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrvalidator-validate-method.md)|Valide le fichier exécutable portable ou le Microsoft intermediate language (MSIL) dans le fichier spécifié.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** IValidator.idl, IValidator.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICLRErrorReportingManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md)
- [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [CLRRuntimeHost, coclasse](../../../../docs/framework/unmanaged-api/hosting/clrruntimehost-coclass.md)
