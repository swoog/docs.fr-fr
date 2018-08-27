---
title: typeof (référence C#)
ms.date: 07/20/2015
f1_keywords:
- typeof
- typeof_CSharpKeyword
helpviewer_keywords:
- typeof keyword [C#]
ms.assetid: 0c08d880-515e-46bb-8cd2-48b8dd62c08d
ms.openlocfilehash: 4203b597d7045a13ffed9e61ddbbde57e2113c23
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2018
ms.locfileid: "42908028"
---
# <a name="typeof-c-reference"></a>typeof (référence C#)
Permet d’obtenir l’objet `System.Type` pour un type. Une expression `typeof` prend la forme suivante :  
  
```csharp  
System.Type type = typeof(int);  
```  
  
## <a name="remarks"></a>Notes  
 Pour obtenir le type au moment de l’exécution d’une expression, vous pouvez utiliser la méthode <xref:System.Object.GetType%2A> du .NET Framework, comme dans l’exemple suivant :  
  
```csharp  
int i = 0;  
System.Type type = i.GetType();  
```  
  
 L’opérateur `typeof` ne peut pas être surchargé.  
  
 L’opérateur `typeof` peut également être utilisé sur les types génériques ouverts. Les types avec plusieurs paramètres de type doivent avoir le nombre approprié de virgules dans la spécification. L’exemple suivant montre comment déterminer si le type de retour d’une méthode est un <xref:System.Collections.Generic.IEnumerable%601> générique. Supposons que la méthode est une instance d’un type MethodInfo :  
  
```csharp  
string s = method.ReturnType.GetInterface  
    (typeof(System.Collections.Generic.IEnumerable<>).FullName);  
```  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csrefKeywordsOperator#12](../../../csharp/language-reference/keywords/codesnippet/CSharp/typeof_1.cs)]  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Object.GetType%2A> pour déterminer le type utilisé pour contenir le résultat d’un calcul numérique. Cela dépend des besoins de stockage du nombre résultant.  
  
 [!code-csharp[csrefKeywordsOperator#13](../../../csharp/language-reference/keywords/codesnippet/CSharp/typeof_2.cs)]  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Type?displayProperty=nameWithType>  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
 [is](../../../csharp/language-reference/keywords/is.md)  
 [Mots clés des opérateurs](../../../csharp/language-reference/keywords/operator-keywords.md)
