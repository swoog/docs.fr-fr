---
title: Le type sous-jacent <typename> d'Enum n'est pas conforme CLS
ms.date: 07/20/2015
f1_keywords:
- vbc40032
- bc40032
helpviewer_keywords:
- BC40032
ms.assetid: 32bf1949-fd73-456c-a323-bf1ffe1320ed
ms.openlocfilehash: 7d4566637da74726867c55ddf89b965d055e5d14
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65589920"
---
# <a name="underlying-type-typename-of-enum-is-not-cls-compliant"></a>Type sous-jacent \<typename > d’Enum n’est pas conforme CLS
Le type de données spécifié pour cette énumération n’est pas dans le cadre de la [indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md) (CLS). Cela n’est pas une erreur dans votre composant, car le .NET Framework et Visual Basic prennent en charge ce type de données. Toutefois, un autre composant écrit dans un code strictement conforme CLS ne prenne pas en charge ce type de données. Un tel composant n’est peut-être pas en mesure d’interagir correctement avec votre composant.  
  
 Les types de données Visual Basic suivants ne sont pas conformes CLS :  
  
- [SByte (type de données)](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
- [UInteger (type de données)](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
- [ULong (type de données)](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
- [UShort (type de données)](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC40032  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Si votre composant interagit uniquement avec d’autres composants de .NET Framework, ou n’interagit pas avec d’autres composants, il est inutile de modifier quoi que ce soit.  
  
- Si vous utilisez un composant non écrit pour le .NET Framework, vous pourrez déterminer, par réflexion ou à partir de la documentation, si elle prend en charge ce type de données. Dans l’affirmative, il est inutile de modifier quoi que ce soit.  
  
- Si vous utilisez un composant qui ne prend pas en charge ce type de données, vous devez le remplacer par le type conforme CLS le plus proche. Par exemple, vous pouvez utiliser `UInteger` au lieu de `Integer` si vous n’avez pas besoin de la plage de valeurs située au-dessus de 2 147 483 647. Si vous avez besoin de la plage étendue, vous pouvez remplacer `UInteger` par `Long`.  
  
- Si vous utilisez des objets Automation ou COM, n’oubliez pas que certains types ont des largeurs différentes données que dans le .NET Framework. Par exemple, `uint` correspond souvent à 16 bits dans d’autres environnements. Si vous passez un argument de 16 bits à un tel composant, déclarez-le en tant que `UShort` au lieu de `UInteger` dans votre code managé de Visual Basic.  
  
## <a name="see-also"></a>Voir aussi

- [Réflexion (Visual Basic)](../../programming-guide/concepts/reflection.md)
- [Réflexion](../../../framework/reflection-and-codedom/reflection.md)
