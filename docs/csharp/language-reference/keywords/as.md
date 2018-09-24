---
title: as (référence C#)
ms.date: 07/20/2015
f1_keywords:
- as_CSharpKeyword
- as
helpviewer_keywords:
- type conversion [C#], as keyword
- as keyword [C#]
ms.assetid: a9be126b-cbf4-4990-a70d-d0e1983cad0e
ms.openlocfilehash: aee80b3262ccd9432d7c311dddec47185b66d05f
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46695408"
---
# <a name="as-c-reference"></a>as (référence C#)
Vous pouvez utiliser l’opérateur `as` pour effectuer certains types de conversions entre des types référence ou des [types Nullable](../../../csharp/programming-guide/nullable-types/index.md) compatibles. Le code suivant fournit un exemple.  
  
[!code-csharp[csrefKeywordsOperator#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#1)]
  
## <a name="remarks"></a>Notes  
 L’opérateur `as` est semblable à une opération de cast. Toutefois, si la conversion n’est pas possible, `as` retourne `null` au lieu de lever une exception. Prenons l'exemple suivant :  
  
```csharp  
expression as type  
```  
  
 Le code est équivalent à l’expression suivante, à la différence que la variable `expression` n’est évaluée qu’une seule fois.  
  
```csharp  
expression is type ? (type)expression : (type)null  
```  
  
 Notez que l’opérateur `as` effectue uniquement des conversions de référence, des conversions Nullable et des conversions boxing. L’opérateur `as` ne peut pas effectuer d’autres conversions, telles que les conversions définies par l’utilisateur, qui doivent être effectuées à l’aide d’expressions cast.  
  
## <a name="example"></a>Exemple  

[!code-csharp[csrefKeywordsOperator#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#2)]
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
- [is](../../../csharp/language-reference/keywords/is.md)  
- [?, opérateur](../../../csharp/language-reference/operators/conditional-operator.md)  
- [Mots clés des opérateurs](../../../csharp/language-reference/keywords/operator-keywords.md)
