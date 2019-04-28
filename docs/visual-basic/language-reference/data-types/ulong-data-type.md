---
title: ULong, type de données (Visual Basic)
ms.date: 01/31/2018
f1_keywords:
- vb.ulong
helpviewer_keywords:
- numbers [Visual Basic], whole
- whole numbers
- integral data types [Visual Basic]
- integer numbers
- numbers [Visual Basic], integer
- integers [Visual Basic], data types
- integers [Visual Basic], types
- data types [Visual Basic], integral
- literal type characters [Visual Basic], UL
- ULong data type
- UL literal type characters [Visual Basic]
ms.assetid: 017e0702-774e-44ae-bedc-786b424ca84e
ms.openlocfilehash: 82a2badc1bb22a55f753c9075562db3a5ee0d234
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61747084"
---
# <a name="ulong-data-type-visual-basic"></a>ULong, type de données (Visual Basic)

Contient des entiers 64 bits (8 octets) non signés dont la valeur comprise entre 0 et 18,446,744,073,709,551,615 (plus que 1,84 fois 10 ^ 19).  
  
## <a name="remarks"></a>Notes

Utilisez le `ULong` type de données pour contenir les données binaires trop grandes pour `UInteger`, ou la plus grande possible des valeurs entières non signées.  
  
La valeur par défaut de `ULong` est 0.

## <a name="literal-assignments"></a>Affectations de littéraux

Vous pouvez déclarer et initialiser une `ULong` variable en lui assignant un littéral décimal, un littéral hexadécimal, un littéral octal, ou (à partir de Visual Basic 2017) un littéral binaire. Si le littéral entier est en dehors de la plage de `ULong` (autrement dit, s’il est inférieur à <xref:System.UInt64.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.UInt64.MaxValue?displayProperty=nameWithType>, une erreur de compilation se produit.

Dans l’exemple suivant, les entiers égaux à 7 934 076 125 représentés comme des littéraux décimaux, hexadécimaux et binaires sont assignés aux valeurs `ULong`.
  
[!code-vb[ULong](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#ULong)]

> [!NOTE] 
> Vous utilisez le préfixe `&h` ou `&H` pour désigner un littéral hexadécimal, le préfixe `&b` ou `&B` pour désigner un littéral binaire et le préfixe `&o` ou `&O` pour désigner un littéral octal. Les littéraux décimaux n’ont pas de préfixe.

À partir de Visual Basic 2017, vous pouvez également utiliser le caractère de soulignement, `_`, comme un séparateur numérique pour améliorer la lisibilité, comme dans l’exemple suivant montre.

[!code-vb[ULong](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#LongS)]

À partir de Visual Basic 15.5, vous pouvez également utiliser le caractère de soulignement (`_`) comme séparateur de début entre le préfixe et les chiffres hexadécimaux, binaires ou octaux. Exemple :

```vb
Dim number As ULong = &H_F9AC_0326_1489_D68C
```

[!INCLUDE [supporting-underscores](../../../../includes/vb-separator-langversion.md)]

Littéraux numériques peuvent également inclure le `UL` ou `ul` [caractère de type](../../programming-guide/language-features/data-types/type-characters.md) pour désigner le `ULong` type de données, comme le montre l’exemple suivant.

```vb
Dim number = &H_00_00_0A_96_2F_AC_14_D7ul
```

## <a name="programming-tips"></a>Conseils de programmation
  
- **Nombres négatifs.** Étant donné que `ULong` est un type non signé, il ne peut pas représenter un nombre négatif. Si vous utilisez le moins unaire (`-`) opérateur sur une expression qui correspond au type `ULong`, Visual Basic convertit l’expression à `Decimal` première.  
  
- **Conformité CLS.** Le `ULong` type de données n’est pas dans le cadre de la [Common Language Specification](https://www.ecma-international.org/publications/standards/Ecma-335.htm) (CLS), le code conforme CLS ne peut pas consommer un composant qui l’utilise.  
  
- **Considérations sur l’interopérabilité.** Si vous utilisez des composants non écrits pour le .NET Framework, par exemple des objets Automation ou COM, n’oubliez pas que les types tels que `ulong` peut avoir une largeur de données différente (32 bits) dans d’autres environnements. Si vous passez un argument de 32 bits à un tel composant, déclarez-le en tant que `UInteger` au lieu de `ULong` dans votre code managé de Visual Basic.  
  
     En outre, Automation ne prend pas en charge des entiers 64 bits sur Windows 95, Windows 98, Windows ME ou Windows 2000. Vous ne pouvez pas passer un Visual Basic `ULong` argument à un composant Automation sur ces plateformes.  
  
- **Étendues.** Le `ULong` type de données s’étend à `Decimal`, `Single`, et `Double`. Cela signifie que vous pouvez convertir `ULong` à un de ces types sans rencontrer un <xref:System.OverflowException?displayProperty=nameWithType> erreur.  
  
- **Caractères de type.** Ajout des caractères de type littéral `UL` à un littéral force ce dernier à la `ULong` type de données. `ULong` n’a aucun caractère de type d’identificateur.
  
- **Type de Framework.** Le type correspondant dans le .NET Framework est la structure <xref:System.UInt64?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.UInt64>
- [Types de données](../../../visual-basic/language-reference/data-types/index.md)
- [Fonctions de conversion de types](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [Liste des conversions](../../../visual-basic/language-reference/keywords/conversion-summary.md)
- [Guide pratique pour appeler une fonction Windows qui possède des types non signés](../../../visual-basic/programming-guide/com-interop/how-to-call-a-windows-function-that-takes-unsigned-types.md)
- [Utilisation efficace des types de données](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
