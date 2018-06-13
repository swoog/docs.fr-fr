---
title: implicit (référence C#)
ms.date: 07/20/2015
f1_keywords:
- implicit
- implicit_CSharpKeyword
helpviewer_keywords:
- implicit keyword [C#]
ms.assetid: 34db590e-eb3a-4f11-88d0-ffb3cd753dab
ms.openlocfilehash: 160d9f7c0d58abd685bf1d799b53cc96a26aebe8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33215015"
---
# <a name="implicit-c-reference"></a>implicit (référence C#)
Le mot clé `implicit` est utilisé pour déclarer un opérateur de conversion de type implicite défini par l’utilisateur. Utilisez-le pour permettre les conversions implicites entre un type défini par l’utilisateur et un autre type, si la conversion n’est pas susceptible de provoquer une perte de données.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csrefKeywordsConversion#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/implicit_1.cs)]  
  
 En éliminant les casts de type superflus, les conversions implicites peuvent améliorer la lisibilité du code source. Toutefois, étant donné que les conversions implicites ne nécessitent pas que les programmeurs castent explicitement d’un type à un autre, il faut veiller à éviter les résultats inattendus. En général, les opérateurs de conversion implicite ne doivent jamais lever d’exceptions ni perdre d’informations pour pouvoir être utilisés en toute sécurité à l’insu du programmeur. Si un opérateur de conversion ne peut pas répondre à ces critères, il doit être marqué comme `explicit`. Pour plus d’informations, consultez [Utilisation d’opérateurs de conversion](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md).  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
 [explicit](../../../csharp/language-reference/keywords/explicit.md)  
 [operator (référence C#)](../../../csharp/language-reference/keywords/operator.md)  
 [Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs](../../../csharp/programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)
