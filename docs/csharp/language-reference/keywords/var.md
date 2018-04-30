---
title: var (référence C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- var
- var_CSharpKeyword
helpviewer_keywords:
- var keyword [C#]
ms.assetid: 0777850a-2691-4e3e-927f-0c850f5efe15
caps.latest.revision: 13
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: e0df25eb46bb769214412646d0ac3a7a576b3b73
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
---
# <a name="var-c-reference"></a>var (référence C#)
Depuis Visual C# 3.0, les variables déclarées à la portée de la méthode peuvent avoir un type implicite `var`. Une variable locale implicitement typée est fortement typée comme si vous aviez déclaré vous-même le type, alors que c’est le compilateur qui détermine le type. Les deux déclarations suivantes d’`i` sont équivalentes fonctionnellement :  
  
```  
var i = 10; // implicitly typed  
int i = 10; //explicitly typed  
```  
  
 Pour plus d’informations, consultez [Variables locales implicitement typées](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md) et [Relations des types dans des opérations de requête LINQ](../../../csharp/programming-guide/concepts/linq/type-relationships-in-linq-query-operations.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant présente deux expressions de requête. Dans la première expression, l’utilisation de `var` est autorisée, mais n’est pas obligatoire parce que le type du résultat de la requête peut être déclaré explicitement en tant que `IEnumerable<string>`. Toutefois, dans la deuxième expression où `var` est utilisé, le résultat peut être une collection de types anonymes, et le nom de ce type n’est pas accessible sauf par le compilateur. Si vous utilisez `var`, vous n’avez pas besoin de créer une classe pour le résultat. Notez que, dans le deuxième exemple, la variable d’itération `foreach` `item` doit également être implicitement typée.  
  
 [!code-csharp[csrefKeywordsTypes#18](../../../csharp/language-reference/keywords/codesnippet/CSharp/var_1.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Variables locales implicitement typées](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md)
