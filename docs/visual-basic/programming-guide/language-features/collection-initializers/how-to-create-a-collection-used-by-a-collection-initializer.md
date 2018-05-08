---
title: 'Comment : créer une collection utilisée par un initialiseur de collection (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [Visual Basic]
ms.assetid: c858db10-424d-47e0-92cd-e08087cc5ebc
ms.openlocfilehash: 6158b6f02d95260e2955e77d732fae8b8d9d5e04
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-create-a-collection-used-by-a-collection-initializer-visual-basic"></a>Comment : créer une collection utilisée par un initialiseur de collection (Visual Basic)
Lorsque vous utilisez un initialiseur de collection pour créer une collection, le compilateur Visual Basic cherche un `Add` méthode du type de collection pour laquelle les paramètres de la `Add` méthode correspondent aux types des valeurs dans l’initialiseur de collection. Cela `Add` méthode est utilisée pour remplir la collection avec les valeurs de l’initialiseur de collection.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre une `OrderCollection` collection qui contient un public `Add` méthode qu’un initialiseur de collection peut utiliser pour ajouter des objets de type `Order`. Le `Add` méthode vous permet d’utiliser la syntaxe d’initialiseur de collection raccourcie.  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#4](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_1.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#1](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_2.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#2](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_3.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#3](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_4.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Initialiseurs de collection](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)  
 [Guide pratique : créer une méthode d’extension Add utilisée par un initialiseur de collection](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-an-add-extension-method-used-by-a-collection-initializer.md)
