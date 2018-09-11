---
title: global, mot clé contextuel (référence C#)
ms.date: 07/20/2015
f1_keywords:
- global
- global_CSharpKeyword
helpviewer_keywords:
- global keyword [C#]
ms.assetid: 8932c16a-6959-42c2-86e7-2c4221ab788b
ms.openlocfilehash: 837245e31a9a795aa2f13cfc6c33fefb6402801d
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44217450"
---
# <a name="global-c-reference"></a><span data-ttu-id="87825-102">global (Référence C#)</span><span class="sxs-lookup"><span data-stu-id="87825-102">global (C# Reference)</span></span>

<span data-ttu-id="87825-103">Le mot clé contextuel `global`, quand il vient avant l’[opérateur ::](../operators/namespace-alias-qualifer.md), fait référence à l’espace de noms global, qui est l’espace de noms par défaut pour tout programme C# et ne possède pas de nom.</span><span class="sxs-lookup"><span data-stu-id="87825-103">The `global` contextual keyword, when it comes before the [:: operator](../operators/namespace-alias-qualifer.md), refers to the global namespace, which is the default namespace for any C# program and is otherwise unnamed.</span></span> <span data-ttu-id="87825-104">Pour plus d’informations, consultez [Guide pratique pour utiliser l’alias d’espace de noms global](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md).</span><span class="sxs-lookup"><span data-stu-id="87825-104">For more information, see [How to: Use the Global Namespace Alias](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md).</span></span>

## <a name="example"></a><span data-ttu-id="87825-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="87825-105">Example</span></span>

<span data-ttu-id="87825-106">L’exemple suivant indique comment utiliser le mot clé contextuel `global` pour spécifier que la classe `TestApp` est définie dans l’espace de noms global :</span><span class="sxs-lookup"><span data-stu-id="87825-106">The following example shows how to use the `global` contextual keyword to specify that the class `TestApp` is defined in the global namespace:</span></span>

[!code-csharp[csrefKeywordsContextual#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#13)]

## <a name="see-also"></a><span data-ttu-id="87825-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87825-107">See also</span></span>

- [<span data-ttu-id="87825-108">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="87825-108">Namespaces</span></span>](../../programming-guide/namespaces/index.md)