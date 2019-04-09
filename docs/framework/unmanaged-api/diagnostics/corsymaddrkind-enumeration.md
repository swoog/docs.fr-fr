---
title: CorSymAddrKind, énumération
ms.date: 03/30/2017
api_name:
- CorSymAddrKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSymAddrKind
helpviewer_keywords:
- CorSymAddrKind enumeration [.NET Framework debugging]
ms.assetid: 3ef841c2-cade-42ee-ba34-2ef91d6d0879
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: adef1010d08561c0a0fe38480fe0d2f519a80b49
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59133521"
---
# <a name="corsymaddrkind-enumeration"></a>CorSymAddrKind, énumération
Indique le type d’adresse de mémoire.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorSymAddrKind  
{  
    ADDR_IL_OFFSET          = 1,  
    ADDR_NATIVE_RVA         = 2,  
    ADDR_NATIVE_REGISTER    = 3,  
    ADDR_NATIVE_REGREL      = 4,  
    ADDR_NATIVE_OFFSET      = 5,  
    ADDR_NATIVE_REGREG      = 6,  
    ADDR_NATIVE_REGSTK      = 7,  
    ADDR_NATIVE_STKREG      = 8,  
    ADDR_BITFIELD           = 9,  
    ADDR_NATIVE_ISECTOFFSET = 10  
} CorSymAddrKind;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`ADDR_IL_OFFSET`|Indique un index Microsoft intermediate language (MSIL) local variable ou un paramètre.|  
|`ADDR_NATIVE_RVA`|Indique une adresse virtuelle relative dans un module.|  
|`ADDR_NATIVE_REGISTER`|Indique un Registre du processeur.|  
|`ADDR_NATIVE_REGREL`|Indique que la première adresse est un Registre et la deuxième adresse est un décalage.|  
|`ADDR_NATIVE_OFFSET`|Indique un décalage à partir d’une adresse de base.|  
|`ADDR_NATIVE_REGREG`|Indique que la première adresse est la partie basse d’un Registre, et la deuxième adresse est la partie haute.|  
|`ADDR_NATIVE_REGSTK`|Indique que la première adresse est la partie basse d’un Registre, la seconde est la partie haute, et le troisième est un décalage.|  
|`ADDR_NATIVE_STKREG`|Indique que la première adresse est un Registre, le second est un décalage, et le troisième est la partie haute du Registre.|  
|`ADDR_BITFIELD`|Indique que la première adresse est le début d’un champ et la deuxième adresse est la longueur de champ.|  
|`ADDR_NATIVE_ISECTOFFSET`|Indique que la première adresse est la section et la deuxième adresse est un décalage.|  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-enumerations.md)
