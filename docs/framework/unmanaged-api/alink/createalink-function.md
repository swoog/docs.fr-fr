---
title: CreateALink, fonction
ms.date: 03/30/2017
api_name:
- CreateALink
api_location:
- alink.dll
api_type:
- DLLExport
f1_keywords:
- CreateALink
helpviewer_keywords:
- CreateALink function
- Alink API, CreateALink function
ms.assetid: fc73bcb9-6af6-44d8-bc39-2f4400325dae
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f809395de68b596f769f9396da8668bf296b1aa2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54675039"
---
# <a name="createalink-function"></a>CreateALink, fonction
Crée une instance de l’utilitaire Assembly Linker et définit un pointeur vers l’interface spécifiée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CreateALink (  
   REFIID riid,  
   IUnknown **ppInterface  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
  
|Paramètre|Description|  
|---------------|-----------------|  
|`riid`|Le nom physique d’une des interfaces Assembly Linker.|  
|`ppInterface`|L’emplacement qui réussit, contient un pointeur vers le `riid` interface.|  
  
## <a name="requirements"></a>Spécifications  
 **Bibliothèque**: alink.dll  
  
## <a name="see-also"></a>Voir aussi
- [Al.exe (Assembly Linker)](../../../../docs/framework/tools/al-exe-assembly-linker.md)
