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
ms.openlocfilehash: cf2c343db459879ca95372e104aee68b22dee6b0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33440614"
---
# <a name="ivalidatorvalidate-method"></a>IValidator::Validate, méthode
Valide le spécifié fichier exécutable portable (PE) ou un fichier Microsoft intermediate language (MSIL).  
  
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
  
#### <a name="parameters"></a>Paramètres  
 `veh`  
 [in] Un pointeur vers un `IVEHandler` instance qui gère les erreurs de validation.  
  
 `pAppDomain`  
 [in] Pointeur vers le domaine d’application dans lequel le fichier est chargé.  
  
 `ulFlags`  
 [in] Une combinaison d’opérations de [ValidatorFlags](../../../../docs/framework/unmanaged-api/hosting/validatorflags-enumeration.md) valeurs indiquant les validations qui doivent être effectuées.  
  
 `ulMaxError`  
 [in] Le nombre maximal d’erreurs autorisées avant de quitter la validation.  
  
 `token`  
 [in] Non utilisé.  
  
 `fileName`  
 [in] Chaîne qui spécifie le nom du fichier à valider.  
  
 `pe`  
 [in] Pointeur vers la mémoire tampon dans laquelle le fichier est stocké.  
  
 `ulSize`  
 [in] La taille, en octets, du fichier à valider.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** IValidator.idl, IValidator.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 
