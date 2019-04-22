---
title: Dimensions du tableau dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- dimensions, arrays
- arrays [Visual Basic], dimensions
- arrays [Visual Basic], rectangular
- arrays [Visual Basic], rank
- rectangular arrays
- ranking, arrays
ms.assetid: 385e911b-18c1-4e98-9924-c6d279101dd9
ms.openlocfilehash: 0b4e7c9e253f94e1e28700c8669d28799ab69d91
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58836933"
---
# <a name="array-dimensions-in-visual-basic"></a>Dimensions du tableau dans Visual Basic
Un *dimension* est une direction dans laquelle vous pouvez modifier la spécification d’éléments d’un tableau. Un tableau qui contient les ventes total pour chaque jour du mois possède une dimension (le jour du mois). Un tableau qui concerne les ventes total par service pour chaque jour du mois possède deux dimensions (le numéro de service et le jour du mois). Le nombre de dimensions que possède un tableau est appelé son *rang*.  
  
> [!NOTE]
>  Vous pouvez utiliser le <xref:System.Array.Rank%2A> propriété pour déterminer le nombre de dimensions d’un tableau.  
  
## <a name="working-with-dimensions"></a>Utilisation des Dimensions  
 Vous spécifiez un élément d’un tableau en fournissant un *index* ou *indice* pour chacune de ses dimensions. Les éléments sont contigus pour chaque dimension de l’index 0 jusqu'à l’index le plus élevé pour cette dimension.  
  
 Les illustrations suivantes montrent la structure conceptuelle de tableaux avec des classements différents. Chaque élément dans les illustrations affiche les valeurs d’index qui y accèdent. Par exemple, vous pouvez accéder le premier élément de la deuxième ligne du tableau à deux dimensions en spécifiant l’index `(1, 0)`.  
  
 ![Diagramme illustrant un tableau unidimensionnel.](./media/array-dimensions/one-dimensional-array.gif)  
  
 ![Diagramme illustrant un tableau à deux dimensions.](./media/array-dimensions/two-dimensional-array.gif)  
  
 ![Diagramme illustrant un tableau tridimensionnel.](./media/array-dimensions/three-dimensional-array.gif)  
  
### <a name="one-dimension"></a>Une Dimension  
 De nombreux groupes ont une seule dimension, telles que le nombre de personnes chaque âge. La seule exigence pour spécifier un élément est l’âge pour lequel cet élément conserve le nombre. Par conséquent, un tel tableau utilise un seul index. L’exemple suivant déclare une variable qui doit contenir un *tableau unidimensionnel* d’âge du nombre d’âges 0 à 120.  
  
```  
Dim ageCounts(120) As UInteger  
```  
  
### <a name="two-dimensions"></a>Deux Dimensions  
 Certains tableaux ont deux dimensions, telles que le nombre de bureaux à chaque étage de chaque bâtiment d’un campus. La spécification d’un élément requiert le numéro du bâtiment et le plancher, et chaque élément contient le nombre pour cette combinaison de bâtiment et étage. Par conséquent, un tel tableau utilise deux index. L’exemple suivant déclare une variable qui doit contenir un *tableau à deux dimensions* de comptes de bureau, pour les bâtiments 0 à 40 et les étages de 0 à 5.  
  
```  
Dim officeCounts(40, 5) As Byte  
```  
  
 Un tableau à deux dimensions est également appelé un *tableau rectangulaire*.  
  
### <a name="three-dimensions"></a>Trois Dimensions  
 Certains tableaux ont trois dimensions, telles que les valeurs dans un espace tridimensionnel. Ce type de tableau utilise trois index, qui dans ce cas représentent le x, y et les coordonnées z de l’espace physique. L’exemple suivant déclare une variable qui doit contenir un *tableau tridimensionnel* de température à différents points dans un volume en trois dimensions.  
  
```  
Dim airTemperatures(99, 99, 24) As Single  
```  
  
### <a name="more-than-three-dimensions"></a>Plus de trois Dimensions  
 Bien qu’un tableau peut avoir jusqu'à 32 dimensions, il est rare d’avoir plus de trois.  
  
> [!NOTE]
>  Lorsque vous ajoutez des dimensions à un tableau, le stockage total nécessaire pour le tableau augmente considérablement, c’est le cas des tableaux multidimensionnels utiliser avec précaution.  
  
## <a name="using-different-dimensions"></a>À l’aide de différentes Dimensions  
 Supposons que vous souhaitez effectuer le suivi des montants des ventes pour tous les jours du mois en cours. Vous pouvez déclarer un tableau unidimensionnel avec 31 éléments, un pour chaque jour du mois, comme dans l’exemple suivant montre.  
  
```  
Dim salesAmounts(30) As Double  
```  
  
 Maintenant Supposons que vous souhaitez suivre les mêmes informations non seulement pour tous les jours du mois, mais également pour chaque mois de l’année. Vous pouvez déclarer un tableau à deux dimensions avec 12 lignes (pour les mois) et 31 colonnes (pour les jours), comme le montre l’exemple suivant.  
  
```  
Dim salesAmounts(11, 30) As Double  
```  
  
 Maintenant Supposons que vous voulez que votre tableau contiennent des informations pour plusieurs années. Si vous souhaitez effectuer le suivi des montants des ventes pendant 5 ans, vous pouvez déclarer un tableau tridimensionnel avec 5 couches, 12 lignes et 31 colonnes, comme le montre l’exemple suivant.  
  
```  
Dim salesAmounts(4, 11, 30) As Double  
```  
  
 Notez que, étant donné que chaque index varie de 0 à sa valeur maximale, chaque dimension du `salesAmounts` est déclaré comme un de moins que la longueur requise pour cette dimension. Notez également que la taille du tableau augmente avec chaque nouvelle dimension. Les trois tailles dans les exemples précédents sont respectivement 31, 372 et 1 860 éléments.  
  
> [!NOTE]
>  Vous pouvez créer un tableau sans utiliser le `Dim` instruction ou le `New` clause. Par exemple, vous pouvez appeler la <xref:System.Array.CreateInstance%2A> (méthode), ou un autre composant peut passer à votre code un tableau créé de cette manière. Un tel tableau peut avoir une limite inférieure différente de 0. Vous pouvez toujours tester la limite inférieure d’une dimension à l’aide de la <xref:System.Array.GetLowerBound%2A> méthode ou le `LBound` (fonction).  
  
## <a name="see-also"></a>Voir aussi

- [Tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [Dépannage des tableaux](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)
