---
title: Interroger une collection d’objets
description: Comment interroger les collections.
ms.date: 11/30/2016
ms.assetid: 87a76f8a-0b58-4791-90ea-2fe0a30416c9
ms.openlocfilehash: c690da2ae59d2a9b34a5bd403bc54797c4e95fa0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="query-a-collection-of-objects"></a>Interroger une collection d’objets
Cet exemple montre comment effectuer une requête simple sur une liste d’objets `Student`. Chaque objet `Student` contient des informations de base sur l’étudiant et une liste qui représente les notes de l’étudiant lors de quatre examens.  
  
 Cette application sert de cadre pour de nombreux autres exemples dans cette section qui utilisent la même source de données `students`.  
  
## <a name="example"></a>Exemple  
 La requête suivante retourne les étudiants qui ont reçu une note supérieure ou égale à 90 lors de leur premier examen.  
  
 [!code-csharp[csProgGuideLINQ#15](../../../samples/snippets/csharp/concepts/linq/how-to-query-a-collection-of-objects_1.cs)]  
  
 Cette requête est volontairement simple pour vous permettre de faire des essais. Par exemple, vous pouvez essayer plus de conditions dans la clause `where` ou utiliser une clause `orderby` pour trier les résultats.  
  

## <a name="see-also"></a>Voir aussi  
 [Expressions de requête LINQ](index.md)  
 [Interpolation de chaîne](../language-reference/tokens/interpolated.md)
