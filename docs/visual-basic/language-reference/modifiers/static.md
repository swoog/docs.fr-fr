---
title: Static (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Static
helpviewer_keywords:
- static modifier
- Static keyword [Visual Basic]
ms.assetid: 19013910-4658-47b6-a22e-1744b527979e
ms.openlocfilehash: de4f67fc5b60de48383a8ca886cff02b03830318
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781184"
---
# <a name="static-visual-basic"></a>Static (Visual Basic)
Spécifie qu’une ou plusieurs variables locales déclarées doivent continuer à exister et conservent leurs valeurs les plus récentes après l’arrêt de la procédure dans laquelle elles sont déclarées.  
  
## <a name="remarks"></a>Notes  
 Normalement, une variable locale dans une procédure cesse d’exister dès que la procédure s’arrête. Une variable statique continue d’exister et conserve sa valeur la plus récente. La prochaine fois que votre code appelle la procédure, la variable n’est pas réinitialisée, et elle contient toujours la valeur la plus récente que vous avez attribué à ce dernier. Une variable statique continue d’exister pour la durée de vie de la classe ou le module qui est défini dans.  
  
## <a name="rules"></a>Règles  
  
- **Contexte de déclaration.** Vous pouvez utiliser `Static` uniquement sur les variables locales. Cela signifie que le contexte de déclaration pour un `Static` variable doit être une procédure ou un bloc dans une procédure, et il ne peut pas être un fichier source, un espace de noms, une classe, une structure ou un module.  
  
     Vous ne pouvez pas utiliser `Static` à l’intérieur d’une procédure de structure.  
  
- Les types de données de `Static` variables locales ne peut pas être déduits. Pour plus d’informations, consultez [l’inférence de Type Local](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md).  
  
- **Modificateurs combinés.** Vous ne pouvez pas spécifier `Static` avec `ReadOnly`, `Shadows`, ou `Shared` dans la même déclaration.  
  
## <a name="behavior"></a>Comportement  
 Lorsque vous déclarez une variable statique dans un `Shared` procédure, qu’une seule copie de la variable statique est disponible pour l’application entière. Vous appelez un `Shared` nom de la procédure à l’aide de la classe, pas une variable qui pointe vers une instance de la classe.  
  
 Lorsque vous déclarez une variable statique dans une procédure qui n’est pas `Shared`, seule une copie de la variable est disponible pour chaque instance de la classe. Vous appelez une procédure non partagée à l’aide d’une variable qui pointe vers une instance spécifique de la classe.  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre l'utilisation de `Static`.  
  
 [!code-vb[VbVbalrKeywords#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class1.vb#5)]  
  
 Le `Static` variable `totalSales` est initialisée à 0 qu’une seule fois. Chaque fois que vous entrez `updateSales`, `totalSales` a toujours la valeur la plus récente que vous avez calculé pour lui.  
  
 Le `Static` modificateur peut être utilisé dans ce contexte :  
  
 [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
## <a name="see-also"></a>Voir aussi

- [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md)
- [Shared](../../../visual-basic/language-reference/modifiers/shared.md)
- [Durée de vie en Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md)
- [Déclaration de variable](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [Structures](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [Inférence de type local](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [Objets et classes](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
