---
title: SByte, type de données (Visual Basic)
ms.date: 04/20/2017
f1_keywords:
- vb.sbyte
helpviewer_keywords:
- numbers [Visual Basic], whole
- whole numbers
- integral data types [Visual Basic]
- integer numbers
- numbers [Visual Basic], integer
- integers [Visual Basic], data types
- integers [Visual Basic], types
- data types [Visual Basic], integral
- SByte data type
ms.assetid: 5c38374a-18a1-4cc2-b493-299e3dcaa60f
ms.openlocfilehash: f4e95aacc8e7063cbac8f9ed8e117137836f08bd
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64647031"
---
# <a name="sbyte-data-type-visual-basic"></a>SByte, type de données (Visual Basic)

Contient des entiers 8 bits (1 octet) de valeurs comprises entre -128 et 127 signés.  
  
## <a name="remarks"></a>Notes

Utilisez le `SByte` type de données pour contenir des valeurs entières qui ne nécessitent pas la largeur totale des données de `Integer` ou même de la largeur de la moitié des données de `Short`. Dans certains cas, le common language runtime peut être en mesure de compresser vos `SByte` variables étroitement ensemble et d’enregistrer la consommation de mémoire.

La valeur par défaut de `SByte` est 0.

## <a name="literal-assignments"></a>Affectations de littéraux
  
Vous pouvez déclarer et initialiser une `SByte` variable en lui assignant un littéral décimal, un littéral hexadécimal, un littéral octal, ou (à partir de Visual Basic 2017) un littéral binaire.

Dans l’exemple suivant, les entiers égaux à -102 représentés en tant que séparateur décimal, hexadécimal, et les littéraux binaires sont affectés à `SByte` valeurs. Cet exemple nécessite que vous compilez avec le `/removeintchecks` commutateur de compilateur.

[!code-vb[SByte](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#SByte)]  

> [!NOTE] 
> Vous utilisez le préfixe `&h` ou `&H` pour désigner un littéral hexadécimal, le préfixe `&b` ou `&B` pour désigner un littéral binaire et le préfixe `&o` ou `&O` pour désigner un littéral octal. Les littéraux décimaux n’ont pas de préfixe.

À partir de Visual Basic 2017, vous pouvez également utiliser le caractère de soulignement, `_`, comme un séparateur numérique pour améliorer la lisibilité, comme dans l’exemple suivant montre.

[!code-vb[SByteSeparator](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#SByteS)]  

À partir de Visual Basic 15.5, vous pouvez également utiliser le caractère de soulignement (`_`) comme séparateur de début entre le préfixe et les chiffres hexadécimaux, binaires ou octaux. Exemple :

```vb
Dim number As SByte = &H_F9
```

[!INCLUDE [supporting-underscores](../../../../includes/vb-separator-langversion.md)]

Si le littéral entier est en dehors de la plage de `SByte` (autrement dit, s’il est inférieur à <xref:System.SByte.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.SByte.MaxValue?displayProperty=nameWithType>, une erreur de compilation se produit. Quand un littéral entier n’a aucun suffixe, un [entier](integer-data-type.md) est déduit. Si le littéral entier est en dehors de la plage de la `Integer` type, un [Long](long-data-type.md) est déduit. Cela signifie que, dans les exemples précédents, les littéraux numériques `0x9A` et `0b10011010` sont interprétés comme des entiers signés de 32 bits avec une valeur égale à 156, ce qui dépasse <xref:System.SByte.MaxValue?displayProperty=nameWithType>. Pour compiler le code comme celle-ci, qui affecte un entier décimal non à un `SByte`, vous pouvez effectuer l’une des opérations suivantes :

- Désactive les contrôles de limites d’entier en compilant avec le `/removeintchecks` commutateur de compilateur.

- Utilisez un [caractère de type](../../programming-guide/language-features/data-types/type-characters.md) pour définir explicitement la valeur littérale que vous souhaitez affecter à la `SByte`. L’exemple suivant assigne un littéral négatif `Short` valeur à un `SByte`. Notez que, pour les nombres négatifs, le bit de poids fort du mot de poids fort du littéral numérique doit être défini. Dans le cas de notre exemple, il est de type bit 15 du littéral `Short` valeur.

   [!code-vb[SByteTypeChars](../../../../samples/snippets/visualbasic/language-reference/data-types/sbyte-assignment.vb#1)]

## <a name="programming-tips"></a>Conseils de programmation
  
- **Conformité CLS.** Le `SByte` type de données n’est pas dans le cadre de la [Common Language Specification](https://www.ecma-international.org/publications/standards/Ecma-335.htm) (CLS), le code conforme CLS ne peut pas consommer un composant qui l’utilise.

- **Étendues.** Le `SByte` type de données s’étend à `Short`, `Integer`, `Long`, `Decimal`, `Single`, et `Double`. Cela signifie que vous pouvez convertir `SByte` à un de ces types sans rencontrer un <xref:System.OverflowException?displayProperty=nameWithType> erreur.
  
- **Caractères de type.** `SByte` n’a aucun caractère de type littéral ou un caractère de type identificateur.  
  
- **Type de Framework.** Le type correspondant dans le .NET Framework est la structure <xref:System.SByte?displayProperty=nameWithType>.
  
## <a name="see-also"></a>Voir aussi

- <xref:System.SByte?displayProperty=nameWithType>
- [Types de données](../../../visual-basic/language-reference/data-types/index.md)
- [Fonctions de conversion de types](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [Liste des conversions](../../../visual-basic/language-reference/keywords/conversion-summary.md)
- [Short (type de données)](../../../visual-basic/language-reference/data-types/short-data-type.md)
- [Integer (type de données)](../../../visual-basic/language-reference/data-types/integer-data-type.md)
- [Long (type de données)](../../../visual-basic/language-reference/data-types/long-data-type.md)
- [Utilisation efficace des types de données](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
