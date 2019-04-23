---
title: as - Référence C#
ms.custom: seodec18
ms.date: 10/11/2018
f1_keywords:
- as_CSharpKeyword
- as
helpviewer_keywords:
- type conversion [C#], as keyword
- as keyword [C#]
ms.assetid: a9be126b-cbf4-4990-a70d-d0e1983cad0e
ms.openlocfilehash: b87e75bd4866a191e84465e44d53850e6e2e9723
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59169921"
---
# <a name="as-c-reference"></a>as (référence C#)
Vous pouvez utiliser l’opérateur `as` pour effectuer certains types de conversions entre des types référence ou des [types Nullable](../../../csharp/programming-guide/nullable-types/index.md) compatibles. Le code suivant fournit un exemple.  
  
[!code-csharp[csrefKeywordsOperator#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#1)]

Comme le montre l’exemple, vous devez comparer le résultat de l’expression `as` avec `null` pour vérifier si la conversion a réussi. À partir de C# 7.0, vous pouvez utiliser l’expression [is](is.md) pour effectuer ce test et affecter une variable de manière conditionnelle en cas de réussite. Dans de nombreux scénarios, elle est plus concise que l’opérateur `as`. Pour plus d’informations, voir la section [Modèle de type](is.md#type) de l’article [Opérateur `is`](is.md).
  
## <a name="remarks"></a>Remarques  
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

Pour plus d’informations, consultez [Opérateur as](~/_csharplang/spec/expressions.md#the-as-operator) dans la [spécification du langage C#](../language-specification/index.md). La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.
 
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)
- [is](../../../csharp/language-reference/keywords/is.md)
- [?: Opérateur](../../../csharp/language-reference/operators/conditional-operator.md)
- [Mots clés des opérateurs](../../../csharp/language-reference/keywords/operator-keywords.md)
