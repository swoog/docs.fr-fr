---
title: 'Procédure : Créer une Collection utilisée par un initialiseur de Collection (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [Visual Basic]
ms.assetid: c858db10-424d-47e0-92cd-e08087cc5ebc
ms.openlocfilehash: aaa367e5a1739f26e9b0458d8f2fc44462b73b7b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631722"
---
# <a name="how-to-create-a-collection-used-by-a-collection-initializer-visual-basic"></a>Procédure : Créer une Collection utilisée par un initialiseur de Collection (Visual Basic)
Lorsque vous utilisez un initialiseur de collection pour créer une collection, le compilateur Visual Basic cherche un `Add` méthode du type de collection pour laquelle les paramètres pour le `Add` méthode correspondent aux types des valeurs dans l’initialiseur de collection. Cela `Add` méthode est utilisée pour remplir la collection avec les valeurs à partir de l’initialiseur de collection.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre un `OrderCollection` collection qui contient un public `Add` méthode un initialiseur de collection peut utiliser pour ajouter des objets de type `Order`. Le `Add` méthode vous permet d’utiliser la syntaxe d’initialiseur de collection abrégée.  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#4](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_1.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#1](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_2.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#2](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_3.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#3](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_4.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Initialiseurs de collection](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)
- [Guide pratique pour Créer une méthode d’Extension utilisée par un initialiseur de Collection Add](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-an-add-extension-method-used-by-a-collection-initializer.md)
