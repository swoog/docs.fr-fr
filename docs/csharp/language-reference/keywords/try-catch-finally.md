---
title: try-catch-finally (référence C#)
ms.date: 07/20/2015
f1_keywords:
- catch-finally_CSharpKeyword
- catch-finally
helpviewer_keywords:
- finally blocks [C#]
- try-catch statement [C#]
ms.assetid: a1b443b0-ff7a-43ab-b835-0cc9bfbd15ca
ms.openlocfilehash: 18625838bd36d9d32079b7c72ded7ed660b8cf3a
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53130661"
---
# <a name="try-catch-finally-c-reference"></a>try-catch-finally (référence C#)

`catch` et `finally` sont souvent utilisés ensemble pour obtenir et utiliser des ressources dans un bloc `try`, pour traiter des circonstances exceptionnelles dans un bloc `catch` et pour libérer les ressources dans le bloc `finally`.

 Pour plus d’informations et des exemples sur la génération répétée d’exceptions, consultez [try-catch](try-catch.md) et [Génération d’exceptions](../../../standard/exceptions/index.md). Pour plus d’informations sur le bloc `finally`, consultez [try-finally](try-finally.md).

## <a name="example"></a>Exemple

[!code-csharp[csrefKeywordsExceptions#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsExceptions/CS/csrefKeywordsExceptions.cs#1)]  

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Instructions try, throw et catch (C++)](/cpp/cpp/try-throw-and-catch-statements-cpp)
- [Instructions de gestion des exceptions](exception-handling-statements.md)
- [throw](throw.md)
- [Guide pratique pour lever explicitement des exceptions](../../../standard/exceptions/how-to-explicitly-throw-exceptions.md)
- [using, instruction](using-statement.md)