---
title: ICeeGen::GetSectionCreate, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionCreate
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionCreate
helpviewer_keywords:
- ICeeGen::GetSectionCreate method [.NET Framework metadata]
- GetSectionCreate method [.NET Framework metadata]
ms.assetid: 154b2460-59ce-4874-a9f2-1b3353486ac5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 93e96e7804a3b5ecc64e9e50ce700435be83b77a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54643362"
---
# <a name="iceegengetsectioncreate-method"></a>ICeeGen::GetSectionCreate, méthode
Génère et obtient une section de code utilisant le nom spécifié et les valeurs d’indicateur.  
  
 Cette méthode est obsolète et ne doit pas être utilisée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetSectionCreate (  
    [in]  const char     *name,  
    [in]  DWORD          flags,  
    [out] HCEESECTION    *section  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `name`  
 [in] Un pointeur vers une chaîne qui spécifie le nom de la section doit être créé.  
  
 `flags`  
 [in] Indicateurs qui spécifient des options.  
  
 `section`  
 [out] Pointeur vers la section de code nouvellement créé.  
  
## <a name="remarks"></a>Notes  
 Appelez `GetSectionCreate` uniquement si vous avez des exigences de section spéciale qui ne sont pas gérées par d’autres méthodes.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICeeGen, interface](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
