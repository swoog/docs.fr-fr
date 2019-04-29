---
title: CorSymVarFlag, énumération
ms.date: 03/30/2017
api_name:
- CorSymVarFlag
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSymVarFlag
helpviewer_keywords:
- CorSymVarFlag enumeration [.NET Framework debugging]
ms.assetid: c3f7d307-4047-4f9a-be8c-f152fca42fd0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0c797378f5e13f39c1c786237a3a7b9cf577fccc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763648"
---
# <a name="corsymvarflag-enumeration"></a>CorSymVarFlag, énumération
Indique si une variable est générée par le compilateur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorSymVarFlag   
{  
    VAR_IS_COMP_GEN = 1  
} CorSymVarFlag;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`VAR_IS_COMP_GEN`|Indique que la variable donnée est généré par le compilateur.|  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-enumerations.md)
