---
title: Short, type de données (Visual Basic)
ms.date: 01/31/2018
f1_keywords:
- vb.Short
helpviewer_keywords:
- numbers [Visual Basic], whole
- whole numbers
- integral data types [Visual Basic]
- integer numbers
- numbers [Visual Basic], integer
- integers [Visual Basic], data types
- integers [Visual Basic], types
- data types [Visual Basic], integral
- S literal type character [Visual Basic]
- Short data type
- literal type characters [Visual Basic], S
ms.assetid: 65fcbcf3-a841-400e-885e-301497729a8b
ms.openlocfilehash: dce345e049a1b89b85a340b8e9078f39882a45fb
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53148504"
---
# <a name="short-data-type-visual-basic"></a>Type de données de type short (Visual Basic)
Contient des entiers 16 bits (2 octets) de valeurs comprises entre-32 768 à 32 767 signés.  
  
## <a name="remarks"></a>Notes  
 Utilisez le `Short` type de données pour contenir des valeurs entières qui ne nécessitent pas la largeur totale des données de `Integer`. Dans certains cas, le common language runtime peut regrouper votre `Short` variables étroitement ensemble et d’enregistrer la consommation de mémoire.  
  
 La valeur par défaut de `Short` est 0.  
  
## <a name="literal-assignments"></a>Affectations de littéraux

Vous pouvez déclarer et initialiser une `Short` variable en lui assignant un littéral décimal, un littéral hexadécimal, un littéral octal, ou (à partir de Visual Basic 2017) un littéral binaire. Si le littéral entier est en dehors de la plage de `Short` (autrement dit, s’il est inférieur à <xref:System.Int16.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.Int16.MaxValue?displayProperty=nameWithType>, une erreur de compilation se produit.

Dans l’exemple suivant, les entiers égaux à 1 034 représentés comme séparateur décimal, hexadécimal, et les littéraux binaires sont implicitement convertis à partir de [entier](integer-data-type.md) à `Short` valeurs.

[!code-vb[Short](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#Short)]

> [!NOTE]
> Vous utilisez le préfixe `&h` ou `&H` pour désigner un littéral hexadécimal, le préfixe `&b` ou `&B` pour désigner un littéral binaire et le préfixe `&o` ou `&O` pour désigner un littéral octal. Les littéraux décimaux n’ont pas de préfixe.

À partir de Visual Basic 2017, vous pouvez également utiliser le caractère de soulignement, `_`, comme un séparateur numérique pour améliorer la lisibilité, comme dans l’exemple suivant montre.

[!code-vb[Short](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#ShortS)]

À partir de Visual Basic 15.5, vous pouvez également utiliser le caractère de soulignement (`_`) comme séparateur de début entre le préfixe et les chiffres hexadécimaux, binaires ou octaux. Exemple :

```vb
Dim number As Short = &H_3264
```

[!INCLUDE [supporting-underscores](../../../../includes/vb-separator-langversion.md)]

Littéraux numériques peuvent également inclure le `S` [caractère de type](../../programming-guide/language-features/data-types/type-characters.md) pour désigner le `Short` type de données, comme le montre l’exemple suivant.

```vb
Dim number = &H_3264S
```

## <a name="programming-tips"></a>Conseils de programmation

-   **Étendues.** Le `Short` type de données s’étend à `Integer`, `Long`, `Decimal`, `Single`, ou `Double`. Cela signifie que vous pouvez convertir `Short` en l'un de ces types sans rencontrer d'erreur <xref:System.OverflowException?displayProperty=nameWithType>.  
  
-   **Caractères de type.** L'ajout du caractère de type littéral `S` à un littéral force ce dernier en type de données `Short`. `Short` n’a aucun caractère de type d’identificateur.  
  
-   **Type de Framework.** Le type correspondant dans le .NET Framework est la structure <xref:System.Int16?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi

 <xref:System.Int16?displayProperty=nameWithType>  
 [Types de données](../../../visual-basic/language-reference/data-types/index.md)  
 [Fonctions de conversion de types](../../../visual-basic/language-reference/functions/type-conversion-functions.md)  
 [Liste des conversions](../../../visual-basic/language-reference/keywords/conversion-summary.md)  
 [Integer (type de données)](../../../visual-basic/language-reference/data-types/integer-data-type.md)  
 [Long (type de données)](../../../visual-basic/language-reference/data-types/long-data-type.md)  
 [Utilisation efficace des types de données](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
