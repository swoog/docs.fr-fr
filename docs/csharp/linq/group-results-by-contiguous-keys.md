---
title: Regrouper des résultats par clés contiguës
description: Comment regrouper des résultats par clés contiguës.
ms.date: 12/1/2016
ms.assetid: cbda9c08-151b-4c9e-82f7-c3d7f3dac66b
ms.openlocfilehash: a8d6ac133932a12154d5b23454065144c7652067
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33281435"
---
# <a name="group-results-by-contiguous-keys"></a>Regrouper des résultats par clés contiguës

L’exemple suivant montre comment regrouper des éléments dans des blocs représentant des sous-séquences de clés contiguës. Par exemple, supposons que vous disposiez de la séquence de paires clé-valeur suivante :  
  
|Touche|Value|  
|---------|-----------|  
|A|Nous|  
|A|pensons|  
|A|que|  
|B|Linq|  
|C|est|  
|A|vraiment|  
|B|chouette|  
|B|!|  
  
 Les groupes suivants seront créés dans cet ordre :  
  
1.  Nous, pensons, que  
  
2.  Linq  
  
3.  est  
  
4.  vraiment  
  
5.  chouette, !  
  
 La solution est implémentée comme une méthode d’extension thread-safe qui retourne ses résultats en continu. En d’autres termes, elle produit ses groupes à mesure qu’elle se déplace dans la séquence source. Contrairement aux opérateurs `group` ou `orderby`, elle peut commencer à retourner des groupes à l’appelant avant que l’intégralité de la séquence ait été lue.  
  
 La cohérence de thread est obtenue en effectuant une copie de chaque groupe ou bloc pendant l’itération de la séquence source, comme expliqué dans les commentaires du code source. Si la séquence source comporte une longue séquence d’éléments contigus, le common language runtime peut lever une <xref:System.OutOfMemoryException>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre la méthode d’extension et le code client qui l’utilise.  
  
 [!code-csharp[cscsrefContiguousGroups#1](../../../samples/snippets/csharp/concepts/linq/how-to-group-results-by-contiguous-keys_1.cs)]  
  
 Pour utiliser la méthode d’extension dans votre projet, copiez la classe statique `MyExtensions` dans un fichier de code source nouveau ou existant et, si nécessaire, ajoutez une directive `using` pour l’espace de noms dans lequel elle se trouve.  
  
## <a name="see-also"></a>Voir aussi  
 [Expressions de requête LINQ](index.md)  
 
