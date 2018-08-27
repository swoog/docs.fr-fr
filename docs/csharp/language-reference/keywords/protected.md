---
title: protected (référence C#)
ms.date: 07/20/2015
f1_keywords:
- protected
- protected_CSharpKeyword
helpviewer_keywords:
- protected keyword [C#]
ms.assetid: 05ce3794-6675-4025-bddb-eaaa0ec22892
ms.openlocfilehash: 2da8211ac21a5016478e7b881e7f2f9925b49cef
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "43001332"
---
# <a name="protected-c-reference"></a>protected (référence C#)
Le mot clé `protected` est un modificateur d’accès de membre. 

 > Cette page traite de l’accès `protected`. Le mot clé `protected` fait également partie des modificateurs d’accès [`protected internal`](./protected-internal.md) et [`private protected`](./private-protected.md). 

Un membre protégé est accessible dans sa classe et par les instances de la classe dérivée. 

Pour obtenir une comparaison de `protected` et des autres modificateurs d’accès, consultez [Niveaux d’accessibilité](../../../csharp/language-reference/keywords/accessibility-levels.md). 
  
## <a name="example"></a>Exemple  
 Un membre protégé d’une classe de base est accessible dans une classe dérivée uniquement si l’accès s’effectue par le biais du type de la classe dérivée. Prenons l’exemple de l’extrait de code suivant :  
  
 [!code-csharp[csrefKeywordsModifiers#11](../../../csharp/language-reference/keywords/codesnippet/CSharp/protected_1.cs)]  
  
 L’instruction `a.x = 10` génère une erreur, car elle est appelée dans la méthode statique Main, et pas dans une instance de la classe B.  
  
 Les membres de struct ne peuvent pas être protégés, car le struct ne peut pas être hérité.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, la classe `DerivedPoint` est dérivée de `Point`. Vous pouvez donc accéder aux membres protégés de la classe de base directement à partir de la classe dérivée.  
  
 [!code-csharp[csrefKeywordsModifiers#12](../../../csharp/language-reference/keywords/codesnippet/CSharp/protected_2.cs)]  
  
 Si vous changez les niveaux d’accès de `x` et `y` à [private](../../../csharp/language-reference/keywords/private.md), le compilateur affiche les messages d’erreur suivants :  
  
 `'Point.y' is inaccessible due to its protection level.`  
  
 `'Point.x' is inaccessible due to its protection level.`  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## 

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
- [Modificateurs d’accès](../../../csharp/language-reference/keywords/access-modifiers.md)  
- [Niveaux d’accessibilité](../../../csharp/language-reference/keywords/accessibility-levels.md)  
- [Modificateurs](../../../csharp/language-reference/keywords/modifiers.md)  
- [public](../../../csharp/language-reference/keywords/public.md)  
- [private](../../../csharp/language-reference/keywords/private.md)  
- [internal](../../../csharp/language-reference/keywords/internal.md)  
- [Problèmes de sécurité pour les mots clés virtuels internes](https://msdn.microsoft.com/library/heyd8kky(v=vs.110))