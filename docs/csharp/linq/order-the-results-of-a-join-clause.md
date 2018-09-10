---
title: Classer les résultats d'une clause join (LINQ en C#)
description: Découvrez comment classer les résultats d'une clause join LINQ en C#.
ms.date: 12/1/2016
ms.assetid: a7458901-1201-4c25-b8d9-c04ca52e0eb9
ms.openlocfilehash: 13cd6cb202cf67def17310db6d98e368ce837646
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43516984"
---
# <a name="order-the-results-of-a-join-clause"></a>Classer les résultats d’une clause join

Cet exemple montre comment classer les résultats d’une opération de jointure. Notez que le classement est effectué après la jointure. Vous pouvez utiliser une clause `orderby` avec une ou plusieurs séquences sources avant la jointure, mais cette pratique est généralement déconseillée. Certains fournisseurs LINQ ne conservent pas ce classement après la jointure.

## <a name="example"></a>Exemple

Cette requête crée une jointure groupée, puis trie les groupes en fonction de l’élément de catégorie, qui est encore dans la portée. À l’intérieur de l’initialiseur de type anonyme, une sous-requête classe tous les éléments correspondants de la séquence de produits.

[!code-csharp[csProgGuideLINQ#81](~/samples/snippets/csharp/concepts/linq/how-to-order-the-results-of-a-join-clause_1.cs)]

## <a name="see-also"></a>Voir aussi

- [LINQ (Language Integrated Query)](index.md)  
- [orderby, clause](../language-reference/keywords/orderby-clause.md)  
- [join, clause](../language-reference/keywords/join-clause.md)  