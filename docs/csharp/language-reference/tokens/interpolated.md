---
title: $ - interpolation de chaîne (Référence C#)
description: L’interpolation de chaîne fournit une syntaxe plus lisible et plus pratique pour mettre en forme la sortie de chaîne que la traditionnelle mise en forme composite de chaîne.
ms.date: 03/26/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- $_CSharpKeyword
- $
helpviewer_keywords:
- $ special character [C#]
- $ language element [C#]
- string interpolation [C#]
- interpolated string [C#]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cabb40c9c449780c8c2a504aad3e53938e2ed957
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="---string-interpolation-c-reference"></a>$ - interpolation de chaîne (Référence C#)

Le caractère spécial `$` identifie un littéral de chaîne comme une *chaîne interpolée*. Une chaîne interpolée ressemble à une chaîne de modèle contenant des *expressions interpolées*. Quand la chaîne interpolée est résolue en une chaîne de résultat, les éléments avec des expressions interpolées sont remplacés par les représentations sous forme de chaînes des résultats des expressions. Cette fonctionnalité est disponible dans C# 6 et versions ultérieures.

L’interpolation de chaîne offre une syntaxe plus lisible et plus simple pour créer des chaînes mises en forme que la fonctionnalité de [mise en forme de chaîne composite](../../../standard/base-types/composite-formatting.md). L’exemple suivant utilise les deux fonctionnalités pour produire la même sortie :

[!code-csharp-interactive[compare with composite formatting](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#1)]

> [!NOTE]
> N’ajoutez pas d’espace blanc entre les signes `$` et `"` au début de la chaîne. Cela provoque une erreur de compilation.

La structure d’un élément avec une expression interpolée est comme suit :

```
{<interpolatedExpression>[,<alignment>][:<formatString>]}
```

Les éléments entre crochets sont facultatifs. Le tableau suivant décrit chaque élément.

|Élément|Description|
|-------------|-----------------|
|`interpolatedExpression`|Expression à évaluer pour obtenir la mise en forme d’un résultat. La représentation sous forme de chaîne du résultat `null` est <xref:System.String.Empty?displayProperty=nameWithType>.|
|`alignment`|Expression constante dont la valeur définit le nombre minimal de caractères dans la représentation sous forme de chaîne du résultat de l’expression interpolée. Si le nombre est positif, la représentation sous forme de chaîne est alignée à droite, s’il est négatif, elle est alignée à gauche. Pour plus d'informations, consultez [Composant d’alignement](../../../standard/base-types/composite-formatting.md#alignment-component).|
|`formatString`|Chaîne de format standard ou personnalisé qui est prise en charge par le type de résultat de l’expression. Pour plus d'informations, consultez [Composant de chaîne de format](../../../standard/base-types/composite-formatting.md#format-string-component).|

L’exemple suivant utilise les composants de mise en forme facultatifs décrits ci-dessus :

[!code-csharp-interactive[specify alignment and format string](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#2)]

Pour ajouter une accolade (« { » ou « } ») dans le texte produit par une chaîne interpolée, entrez deux accolades « {{ » ou « }} ». Pour plus d'informations, consultez [Accolades d’échappement](../../../standard/base-types/composite-formatting.md#escaping-braces).

Comme le caractère deux-points (:) a une signification spéciale dans un élément d’expression interpolée, placez l’expression entre parenthèses pour utiliser un [opérateur conditionnel](../operators/conditional-operator.md) dans une expression interpolée.

L’exemple suivant montre comment ajouter une accolade dans la chaîne de résultat et comment utiliser un opérateur conditionnel dans une expression interpolée :

[!code-csharp-interactive[example with ternary conditional operator](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#3)]

Les chaînes interpolées textuelles utilisent le caractère `$` suivi du caractère `@`. Pour plus d'informations sur les chaînes textuelles, consultez la rubrique [string](../keywords/string.md).

> [!NOTE]
> Le jeton `$` doit apparaître avant le jeton `@` dans une chaîne interpolée textuelle.

Trois conversions implicites sont possibles à partir d’une chaîne interpolée :

1. Conversion d’une chaîne interpolée en instance de <xref:System.String> qui est le résultat de la résolution d’une chaîne interpolée avec des éléments d’expression interpolée remplacés par la représentation sous forme de chaîne correctement mise en forme de leurs résultats. Cette conversion utilise la culture actuelle.

1. Conversion d’une chaîne interpolée en instance <xref:System.FormattableString> qui représente une chaîne de format composite avec les résultats d’expression à mettre en forme. Cette conversion vous permet de créer plusieurs chaînes de résultat avec du contenu propre à la culture à partir d’une seule instance de <xref:System.FormattableString>. Pour ce faire, appelez l’une des méthodes suivantes :

      - Une surcharge <xref:System.FormattableString.ToString> qui produit une chaîne de résultat pour <xref:System.Globalization.CultureInfo.CurrentCulture>.
      - Une méthode <xref:System.FormattableString.Invariant%2A> qui produit une chaîne de résultat pour <xref:System.Globalization.CultureInfo.InvariantCulture>.
      - Une méthode <xref:System.FormattableString.ToString(System.IFormatProvider)> qui produit une chaîne de résultat pour une culture spécifiée.

1. Conversion d’une chaîne interpolée en instance <xref:System.IFormattable> qui vous permet aussi de créer plusieurs chaînes de résultat avec du contenu propre à la culture à partir d’une seule instance de <xref:System.IFormattable>.

L’exemple suivant utilise la conversion implicite en <xref:System.FormattableString> pour créer des chaînes de résultat propres à la culture :

[!code-csharp-interactive[create culture-specific result strings](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#4)]

Si vous ne connaissez pas l’interpolation de chaîne, consultez le guide de démarrage rapide [Interpolation de chaîne en C#](../../quick-starts/interpolated-strings.yml). Pour plus d’exemples, consultez le [didacticiel sur l’interpolation de chaîne](../../tutorials/string-interpolation.md).

## <a name="see-also"></a>Voir aussi  
 <xref:System.String.Format%2A?displayProperty=nameWithType>  
 <xref:System.FormattableString?displayProperty=nameWithType>  
 <xref:System.IFormattable?displayProperty=nameWithType>  
 [Mise en forme composite](../../../standard/base-types/composite-formatting.md)  
 [Chaînes](../../../csharp/programming-guide/strings/index.md)  
 [Caractères spéciaux C#](../../../csharp/language-reference/tokens/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Référence C#](../../../csharp/language-reference/index.md)  