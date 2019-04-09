---
title: ICeeGen::GetSectionBlock, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionBlock
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionBlock
helpviewer_keywords:
- GetSectionBlock method [.NET Framework metadata]
- ICeeGen::GetSectionBlock method [.NET Framework metadata]
ms.assetid: 05c78aaf-5bbd-497e-9ae2-55f4fae0c5fb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7e600f29a9036bb28031bd7854bc8cbb34c4566a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59200647"
---
# <a name="iceegengetsectionblock-method"></a>ICeeGen::GetSectionBlock, méthode
Obtient un bloc de section de la base de code.  
  
 Cette méthode est obsolète et ne doit pas être utilisée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetSectionBlock (  
    [in]  HCEESECTION    section,     
    [in]  ULONG          len,  
    [in]  ULONG          align     = 1,  
    [out] void           **ppBytes = 0  
);   
```  
  
## <a name="parameters"></a>Paramètres  
 `section`  
 [in] La section à partir de laquelle récupérer un bloc de la base de code.  
  
 `len`  
 [in] La longueur du bloc à récupérer.  
  
 `align`  
 [in] L’octet par rapport au début de la section, avec lequel aligner le premier octet du bloc. Il s’agit de la position du bloc dans la section.  
  
 `ppBytes`  
 [out] Pointeur vers un emplacement qui reçoit l’adresse du bloc récupéré.  
  
## <a name="remarks"></a>Notes  
 Appelez `GetSectionBlock` uniquement si vous avez des exigences de section spéciale qui ne sont pas gérées par d’autres méthodes.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICeeGen, interface](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
