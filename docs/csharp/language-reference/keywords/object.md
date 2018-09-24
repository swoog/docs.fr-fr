---
title: object (référence C#)
ms.date: 07/20/2015
f1_keywords:
- object_CSharpKeyword
- object
helpviewer_keywords:
- object keyword [C#]
ms.assetid: 93f60c0b-e17a-40a9-9362-cca5fb77b0e7
ms.openlocfilehash: b36703828e6027a89297ac88edaf2b55ec18f42e
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46579603"
---
# <a name="object-c-reference"></a>object (référence C#)

Le type `object` est un alias de <xref:System.Object> dans .NET. Dans le système de type unifié de C#, tous les types (les types référence et valeur, prédéfinis ou définis par l’utilisateur) héritent directement ou indirectement du type <xref:System.Object>. Vous pouvez assigner des valeurs de tout type aux variables de type `object`. Quand une variable d’un type valeur est convertie en type objet, elle est dite *boxed*. Quand une variable de type objet est convertie en type valeur, elle est dite *unboxed*. Pour plus d’informations, consultez [Boxing et unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).

## <a name="example"></a>Exemple

L’exemple suivant montre comment les variables de type `object` acceptent des valeurs de tout type de données et comment les variables de type `object` utilisent des méthodes d’<xref:System.Object> du .NET Framework.

[!code-csharp[csrefKeywordsTypes#16](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#16)]

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Types référence](reference-types.md)
- [Types valeur](value-types.md)