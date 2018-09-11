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
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44273331"
---
# <a name="global-c-reference"></a>global (Référence C#)

Le mot clé contextuel `global`, quand il vient avant l’[opérateur ::](../operators/namespace-alias-qualifer.md), fait référence à l’espace de noms global, qui est l’espace de noms par défaut pour tout programme C# et ne possède pas de nom. Pour plus d’informations, consultez [Guide pratique pour utiliser l’alias d’espace de noms global](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md).

## <a name="example"></a>Exemple

L’exemple suivant indique comment utiliser le mot clé contextuel `global` pour spécifier que la classe `TestApp` est définie dans l’espace de noms global :

[!code-csharp[csrefKeywordsContextual#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#13)]

## <a name="see-also"></a>Voir aussi

- [Espaces de noms](../../programming-guide/namespaces/index.md)