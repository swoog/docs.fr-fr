---
title: SYMLINEDELTA, structure
ms.date: 03/30/2017
api_name:
- SYMLINEDELTA
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- SYMLINEDELTA
helpviewer_keywords:
- SYMLINEDELTA structure [.NET Framework debugging]
ms.assetid: 9634e995-d46d-4397-ab66-cc5781d11e4e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fabc8f77b12865d0d971b5934d7de27b52f3e813
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61914639"
---
# <a name="symlinedelta-structure"></a>SYMLINEDELTA, structure
Fournit des informations pour le Gestionnaire de symboles sur les méthodes qui ont été déplacées à la suite de modifications.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct _SYMLINEDELTA  
    {  
        mdMethodDef  mdMethod;  
        INT32        delta;  
    } SYMLINEDELTA;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`mdMethod`|Jeton de métadonnées de la méthode.|  
|`delta`|Le nombre de lignes de que la méthode a été déplacée.|  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl  
  
## <a name="see-also"></a>Voir aussi

- [Structures du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)
