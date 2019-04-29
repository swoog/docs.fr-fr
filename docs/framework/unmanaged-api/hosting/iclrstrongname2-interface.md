---
title: ICLRStrongName2, interface
ms.date: 03/30/2017
api_name:
- ICLRStrongName2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName2
helpviewer_keywords:
- ICLRStrongName2 interface [.NET Framework hosting]
ms.assetid: 9f098a74-201e-4628-a468-8dee9ab99b4a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6bf9e3d2df8f507e118b393007c3958358a830cc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763722"
---
# <a name="iclrstrongname2-interface"></a>ICLRStrongName2, interface
Offre la possibilité de créer des noms forts dans le groupe de SHA-2 d’algorithmes de hachage sécurisé (SHA-256, SHA-384 et SHA-512).  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[StrongNameGetPublicKeyEx, méthode](../../../../docs/framework/unmanaged-api/hosting/strongnamegetpublickeyex-method.md)|Obtient la clé publique à partir d’une paire de clés publique/privée et spécifie un algorithme de hachage et un algorithme de signature.|  
|[StrongNameSignatureVerificationEx2, méthode](../../../../docs/framework/unmanaged-api/hosting/strongnamesignatureverificationex2-method.md)|Vérifie la signature d’un assembly de nom fort et fournit un mappage à partir de la clé ECMA à une clé réelle.|  
  
## <a name="remarks"></a>Notes  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]
