---
title: Fonctions de chaînes canoniques au niveau du bit
ms.date: 03/30/2017
ms.assetid: 993868ca-16e3-47b6-9915-c29cd63b0a21
ms.openlocfilehash: df3b81a47b8e1202884a5c38f55c7061279b245f
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32761192"
---
# <a name="bitwise-canonical-functions"></a>Fonctions de chaînes canoniques au niveau du bit
[!INCLUDE[esql](../../../../../../includes/esql-md.md)] inclut des fonctions canoniques au niveau du bit.  
  
## <a name="remarks"></a>Notes  
 Le tableau suivant présente les autres fonctions canoniques [!INCLUDE[esql](../../../../../../includes/esql-md.md)] au niveau du bit. Ces fonctions retournent `Null` si `Null` entrée est fournie. Le type de retour des fonctions est le même que le ou les types d’arguments. Les arguments doivent être du même type si la fonction prend plusieurs arguments. Pour effectuer des opérations au niveau du bit sur différents types, vous devez effectuer un cast explicite vers le même type.  
  
|Fonction|Description|  
|--------------|-----------------|  
|`BitWiseAnd (` `value1` `,`  `value2` `)`|Retourne la conjonction au niveau du bit de `value1` et de `value2` comme type de `value1` et de `value2`.<br /><br /> **Arguments**<br /><br /> A `Byte`, `Int16`, `Int32`, et `Int64`.<br /><br /> **Exemple**<br /><br /> `-- The following example returns 1.`<br /><br /> `BitWiseAnd(1,3)`|  
|`BitWiseNot (` `value` `)`|Retourne la négation au niveau du bit de `value`.<br /><br /> **Arguments**<br /><br /> A `Byte`, `Int16`, `Int32`, et `Int64`.<br /><br /> **Exemple**<br /><br /> `-- The following example returns -4.`<br /><br /> `BitWiseNot(3)`|  
|`BitWiseOr (` `value1` `,`  `value2` `)`|Retourne la disjonction au niveau du bit de `value1` et de `value2` comme type de `value1` et de `value2`.<br /><br /> **Arguments**<br /><br /> A `Byte`, `Int16`, `Int32` et `Int64`.<br /><br /> **Exemple**<br /><br /> `-- The following example returns 3.`<br /><br /> `BitWiseOr(1,3)`|  
|`BitWiseXor (` `value1` `,`  `value2` `)`|Retourne la disjonction exclusive au niveau du bit de `value1` et de `value2` comme type de `value1` et de `value2`.<br /><br /> **Arguments**<br /><br /> A `Byte`, `Int16`, `Int32` et `Int64`.<br /><br /> **Exemple**<br /><br /> `-- The following example returns 2.`<br /><br /> `BitWiseXor (1,3)`|  
  
## <a name="see-also"></a>Voir aussi  
 [Fonctions canoniques](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
