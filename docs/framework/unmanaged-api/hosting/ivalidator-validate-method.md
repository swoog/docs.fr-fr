---
title: IValidator::Validate, méthode
ms.date: 03/30/2017
api_name:
- IValidator.Validate
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- Validate
helpviewer_keywords:
- IValidator::Validate method [.NET Framework hosting]
- Validate method, IValidator interface [.NET Framework hosting]
ms.assetid: 7d68666a-fb73-4455-bebd-908d49a16abc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3c362b41d842fb9d35cc7ae9293e2e305b2af281
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57500432"
---
# <a name="ivalidatorvalidate-method"></a>IValidator::Validate, méthode
Valide le spécifié exécutable portable (PE) ou un fichier Microsoft intermediate language (MSIL).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Validate (  
    [in] IVEHandler            *veh,  
    [in] IUnknown              *pAppDomain,  
    [in] unsigned long          ulFlags,  
    [in] unsigned long          ulMaxError,  
    [in] unsigned long          token,  
    [in] LPWSTR                 fileName,  
    [in, size_is(ulSize)] BYTE *pe,  
    [in] unsigned long          ulSize  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `veh`  
 [in] Un pointeur vers un `IVEHandler` instance qui gère les erreurs de validation.  
  
 `pAppDomain`  
 [in] Pointeur vers le domaine d’application dans lequel le fichier est chargé.  
  
 `ulFlags`  
 [in] Une combinaison au niveau du bit de [ValidatorFlags](../../../../docs/framework/unmanaged-api/hosting/validatorflags-enumeration.md) valeurs indiquant les validations qui doivent être effectuées.  
  
 `ulMaxError`  
 [in] Le nombre maximal d’erreurs autorisées avant de quitter la validation.  
  
 `token`  
 [in] Non utilisé.  
  
 `fileName`  
 [in] Chaîne qui spécifie le nom du fichier à valider.  
  
 `pe`  
 [in] Pointeur vers la mémoire tampon dans lequel le fichier est stocké.  
  
 `ulSize`  
 [in] La taille, en octets, du fichier à valider.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** IValidator.idl, IValidator.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

