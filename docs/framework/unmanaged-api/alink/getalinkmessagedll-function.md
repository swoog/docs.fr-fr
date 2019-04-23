---
title: GetALinkMessageDll, fonction
ms.date: 03/30/2017
api_name:
- GetALinkMessageDll
api_location:
- alink.dll
api_type:
- DLLExport
f1_keywords:
- GetALinkMessageDll
helpviewer_keywords:
- Alink API, GetALinkMessageDll function
- GetALinkMessageDll function
ms.assetid: 67985a22-88a2-4c54-8d99-4bcde9d6213e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: edd83e62b08aa7892c01577cd8c46f9d965c0894
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59163018"
---
# <a name="getalinkmessagedll-function"></a>GetALinkMessageDll, fonction
Recherche et charge la DLL de message. Retourne 0 si Impossible de trouver ou de charger la DLL de message. La DLL de message doit être dans un sous-répertoire dont le nom est un ID de langue, ou dans le répertoire actif.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HINSTANCE WINAPI GetALinkMessageDll();  
```  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** alink.h  
  
 **Bibliothèque**: alink.dll  
  
## <a name="see-also"></a>Voir aussi

- [Al.exe (Assembly Linker)](../../../../docs/framework/tools/al-exe-assembly-linker.md)
