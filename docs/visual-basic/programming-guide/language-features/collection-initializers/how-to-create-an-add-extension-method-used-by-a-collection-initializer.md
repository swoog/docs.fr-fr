---
title: 'Procédure : Créer une Extension méthode Add utilisée par un initialiseur de Collection (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [Visual Basic]
ms.assetid: f64b52c7-8b11-4410-93a6-cb3aeebcc772
ms.openlocfilehash: 458421da70aca6728f3f03945c28b4c988e44ad7
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56978538"
---
# <a name="how-to-create-an-add-extension-method-used-by-a-collection-initializer-visual-basic"></a>Procédure : Créer une Extension méthode Add utilisée par un initialiseur de Collection (Visual Basic)
Lorsque vous utilisez un initialiseur de collection pour créer une collection, le compilateur Visual Basic cherche un `Add` méthode du type de collection pour laquelle les paramètres pour le `Add` méthode correspondent aux types des valeurs dans l’initialiseur de collection. Cela `Add` méthode est utilisée pour remplir la collection avec les valeurs à partir de l’initialiseur de collection.  
  
 Si aucune correspondance `Add` méthode existe et vous ne pouvez pas modifier le code de la collection, vous pouvez ajouter une méthode d’extension appelée `Add` qui accepte les paramètres qui sont requis par l’initialiseur de collection. Il s’agit généralement ce que vous devez faire lorsque vous utilisez des initialiseurs de collection pour les collections génériques.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment ajouter une méthode d’extension générique <xref:System.Collections.Generic.List%601> tapez afin qu’un initialiseur de collection peut être utilisé pour ajouter des objets de type `Employee`. La méthode d’extension vous permet d’utiliser la syntaxe d’initialiseur de collection abrégée.  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo1#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1/VB/Module1.vb#1)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo1#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1/VB/Module1.vb#2)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo1#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1/VB/Module1.vb#3)]  
  
## <a name="see-also"></a>Voir aussi
- [Initialiseurs de collection](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)
- [Guide pratique pour Créer une Collection utilisée par un initialiseur de Collection](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-a-collection-used-by-a-collection-initializer.md)
