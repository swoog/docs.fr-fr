---
title: '#elif - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#elif'
helpviewer_keywords:
- '#elif directive [C#]'
ms.assetid: 731d78df-08e0-4d51-b8c8-f193c27de13f
ms.openlocfilehash: 00a9298be6ecd6f5e775d930190ddb6e227e4711
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587227"
---
# <a name="elif-c-reference"></a>#elif (référence C#)
`#elif` vous permet de créer une directive conditionnelle composée. L’expression `#elif` est évaluée si ni l’expression [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) précédente ni une expression de directive `#elif` facultative précédente n’est évaluée à `true`. Si une expression `#elif` est évaluée à `true`, le compilateur évalue l’ensemble du code situé entre `#elif` et la directive conditionnelle suivante. Par exemple :  
  
```csharp
#define VC7  
//...  
#if debug  
    Console.WriteLine("Debug build");  
#elif VC7  
    Console.WriteLine("Visual Studio 7");  
#endif  
```  
  
 Vous pouvez utiliser les opérateurs `==` (égalité), `!=` (inégalité) `&&` (et) et `||` (ou) pour évaluer plusieurs symboles. Vous pouvez également regrouper des symboles et des opérateurs à l’aide de parenthèses.  
  
## <a name="remarks"></a>Notes  
 `#elif` revient à utiliser :  
  
```csharp
#else  
#if  
```  
  
 `#elif` est plus simple à utiliser, car chaque expression `#if` a besoin d’une expression [#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md), alors qu’une expression `#elif` peut être utilisée sans expression `#endif` correspondante.  
  
 Consultez [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) pour obtenir un exemple d’utilisation de `#elif`.  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Directives de préprocesseur C#](../../../csharp/language-reference/preprocessor-directives/index.md)
