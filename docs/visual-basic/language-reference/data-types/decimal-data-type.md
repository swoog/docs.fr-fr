---
title: Decimal, type de données (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Decimal
helpviewer_keywords:
- literal type characters [Visual Basic], D
- trailing zeros
- real numbers
- trailing 0 characters [Visual Basic]
- Decimal data type
- D literal type character [Visual Basic]
- decimals, Decimal data type
- 0 characters [Visual Basic], trailing
- data types [Visual Basic], assigning
- decimal keyword [Visual Basic]
- numbers [Visual Basic], real
- variable-precision numbers
- zeros, trailing
- '@ identifier type character'
- identifier type characters [Visual Basic], @
ms.assetid: 1d855b45-afe2-45b0-a623-96b6f63a43d5
ms.openlocfilehash: 4d530a8c1f85d2f0045184c05df63849047a8204
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61971767"
---
# <a name="decimal-data-type-visual-basic"></a>Decimal, type de données (Visual Basic)
Contient des valeurs (16 octets) de 128 bits représentant des nombres entier de 96 bits (12 octets) mis à l’échelle par une puissance de 10 variable signés. Le facteur d’échelle spécifie le nombre de chiffres à droite de la virgule décimale ; Il est compris entre 0 et 28. Avec une échelle de 0 (pas de décimales), la plus grande valeur possible est +/-79,228,162,514,264,337,593,543,950,335 (+/-7 9228162514264337593543950335E + 28). La plus grande valeur est +/-7,9228162514264337593543950335 avec 28 décimales, et la plus petite valeur différente de zéro est +/-0,0000000000000000000000000001 (+/-1E-28).  
  
## <a name="remarks"></a>Notes  
 Le `Decimal` type de données fournit le plus grand nombre de chiffres significatifs pour un nombre. Il prend en charge jusqu'à 29 chiffres significatifs et peut représenter des valeurs dépassant 7,9228 x 10 ^ 28. Il est particulièrement adapté aux calculs, tels que financiers, qui nécessitent un grand nombre de chiffres, mais ne peuvent pas tolérer les erreurs d’arrondi.  
  
 La valeur par défaut de `Decimal` est 0.  
  
## <a name="programming-tips"></a>Conseils de programmation  
  
- **Précision.** `Decimal` n’est pas un type de données à virgule flottante. Le `Decimal` structure contient une valeur d’entier binaire, avec un bit de signe et un entier facteur qui spécifie quelle partie de la valeur est une fraction décimale d’échelle. Pour cette raison, `Decimal` nombres ont une représentation plus précise dans la mémoire que les types à virgule flottante (`Single` et `Double`).  
  
- **Performances** Le `Decimal` type de données est le plus lent de tous les types numériques. Vous devez évaluer l’importance de précision par rapport aux performances avant de choisir un type de données.  
  
- **Étendues.** Le `Decimal` type de données s’étend à `Single` ou `Double`. Cela signifie que vous pouvez convertir `Decimal` à un de ces types sans rencontrer un <xref:System.OverflowException?displayProperty=nameWithType> erreur.  
  
- **Les zéros de fin.** Visual Basic ne stocke pas de zéros de fin dans un `Decimal` littéral. Toutefois, un `Decimal` variable conserve les zéros de fin acquis par le calcul. L'exemple suivant illustre ce comportement.  
  
    ```  
    Dim d1, d2, d3, d4 As Decimal  
    d1 = 2.375D  
    d2 = 1.625D  
    d3 = d1 + d2  
    d4 = 4.000D  
    MsgBox("d1 = " & CStr(d1) & ", d2 = " & CStr(d2) &  
          ", d3 = " & CStr(d3) & ", d4 = " & CStr(d4))  
    ```  
  
     La sortie de `MsgBox` dans l’exemple précédent est comme suit :  
  
     d1 = 2.375, d2 = 1.625, d3 = 4.000, d4 = 4  
  
- **Caractères de type.** L'ajout du caractère de type littéral `D` à un littéral force ce dernier en type de données `Decimal`. L'ajout du caractère de type identificateur `@` à un identificateur force ce dernier en type `Decimal`.  
  
- **Type de Framework.** Le type correspondant dans le .NET Framework est la structure <xref:System.Decimal?displayProperty=nameWithType>.  
  
## <a name="range"></a>Plage  
 Vous devrez peut-être utiliser le `D` type caractère à assigner une grande valeur à une `Decimal` variable ou constante. Cette exigence est étant donné que le compilateur interprète un littéral en tant que `Long` , sauf si un caractère de type littéral suit le littéral, comme le montre l’exemple suivant.  
  
```  
Dim bigDec1 As Decimal = 9223372036854775807   ' No overflow.  
Dim bigDec2 As Decimal = 9223372036854775808   ' Overflow.  
Dim bigDec3 As Decimal = 9223372036854775808D  ' No overflow.  
```  
  
 La déclaration pour `bigDec1` ne produit pas un dépassement de capacité, car la valeur qui lui est attribuée se situe dans la plage pour `Long`. Le `Long` valeur peut être assignée à la `Decimal` variable.  
  
 La déclaration pour `bigDec2` génère une erreur de dépassement de capacité, car la valeur qui lui est affectée est trop grande pour `Long`. Étant donné que le littéral numérique ne peut pas tout d’abord être interprété comme un `Long`, il ne peut pas être affecté à la `Decimal` variable.  
  
 Pour `bigDec3`, le caractère de type littéral `D` résout le problème en forçant le compilateur à interpréter le littéral en tant qu’un `Decimal` au lieu de comme un `Long`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Decimal?displayProperty=nameWithType>
- <xref:System.Decimal.%23ctor%2A?displayProperty=nameWithType>
- <xref:System.Math.Round%2A?displayProperty=nameWithType>
- [Types de données](../../../visual-basic/language-reference/data-types/index.md)
- [Single (type de données)](../../../visual-basic/language-reference/data-types/single-data-type.md)
- [Double (type de données)](../../../visual-basic/language-reference/data-types/double-data-type.md)
- [Fonctions de conversion de types](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [Liste des conversions](../../../visual-basic/language-reference/keywords/conversion-summary.md)
- [Utilisation efficace des types de données](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
