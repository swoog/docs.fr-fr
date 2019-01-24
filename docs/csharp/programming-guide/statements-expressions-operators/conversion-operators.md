---
title: Opérateurs de conversion - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, conversion operators
- conversion operators [C#]
- operators [C#], conversion
- user-defined conversions [C#]
ms.assetid: c5ad73a3-d57b-4d2b-b4c9-24e3c2856efc
ms.openlocfilehash: 927640b63773d24be93cc90427668f9568a39652
ms.sourcegitcommit: 542aa405b295955eb055765f33723cb8b588d0d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "54362728"
---
# <a name="conversion-operators-c-programming-guide"></a>Opérateurs de conversion (guide de programmation C#)

C# permet aux programmeurs de déclarer des conversions sur des classes ou structs afin d’autoriser les conversions dans les deux sens entre ces derniers et d’autres classes ou structs, ou des types de base. Les conversions sont définies comme des opérateurs et nommées en fonction du type vers lequel s’effectue l’opération. Soit le type de l’argument à convertir, soit le type du résultat de la conversion, mais pas les deux, doit être le type conteneur.  
  
 [!code-csharp[csProgGuideStatements#10](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/conversion-operators_1.cs)]  
  
## <a name="conversion-operators-overview"></a>Vue d’ensemble des opérateurs de conversion

 Les opérateurs de conversion ont les propriétés suivantes :  
  
-   Les conversions déclarées comme `implicit` se produisent automatiquement selon les besoins.  
  
-   Les conversions déclarées comme `explicit` nécessitent qu’un cast soit appelé.  
  
-   Toutes les conversions doivent être déclarées comme `static`.  
  
## <a name="related-sections"></a>Rubriques connexes

 Pour plus d'informations :  
  
-   [Utilisation d’opérateurs de conversion](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md)  
  
-   [Cast et conversions de types](../../../csharp/programming-guide/types/casting-and-type-conversions.md)  
  
-   [Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs](../../../csharp/programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)  
  
-   [explicit](../../../csharp/language-reference/keywords/explicit.md)  
  
-   [implicit](../../../csharp/language-reference/keywords/implicit.md)  
  
-   [static](../../../csharp/language-reference/keywords/static.md)  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Convert>  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Conversions explicites définies par l’utilisateur chaînées en C#](https://blogs.msdn.microsoft.com/ericlippert/2007/04/16/chained-user-defined-explicit-conversions-in-c/)
