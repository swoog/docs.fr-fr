---
title: 'Procédure : Créer une Extension méthode Add utilisée par un initialiseur de Collection (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [Visual Basic]
ms.assetid: f64b52c7-8b11-4410-93a6-cb3aeebcc772
ms.openlocfilehash: 3a1db8ede8162b329d546c0e712ef1c2df7d7883
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54661670"
---
# <a name="how-to-create-an-add-extension-method-used-by-a-collection-initializer-visual-basic"></a><span data-ttu-id="bba8e-102">Procédure : Créer une Extension méthode Add utilisée par un initialiseur de Collection (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bba8e-102">How to: Create an Add Extension Method Used by a Collection Initializer (Visual Basic)</span></span>
<span data-ttu-id="bba8e-103">Lorsque vous utilisez un initialiseur de collection pour créer une collection, le compilateur Visual Basic cherche un `Add` méthode du type de collection pour laquelle les paramètres pour le `Add` méthode correspondent aux types des valeurs dans l’initialiseur de collection.</span><span class="sxs-lookup"><span data-stu-id="bba8e-103">When you use a collection initializer to create a collection, the Visual Basic compiler searches for an `Add` method of the collection type for which the parameters for the `Add` method match the types of the values in the collection initializer.</span></span> <span data-ttu-id="bba8e-104">Cela `Add` méthode est utilisée pour remplir la collection avec les valeurs à partir de l’initialiseur de collection.</span><span class="sxs-lookup"><span data-stu-id="bba8e-104">This `Add` method is used to populate the collection with the values from the collection initializer.</span></span>  
  
 <span data-ttu-id="bba8e-105">Si aucune correspondance `Add` méthode existe et vous ne pouvez pas modifier le code de la collection, vous pouvez ajouter une méthode d’extension appelée `Add` qui accepte les paramètres qui sont requis par l’initialiseur de collection.</span><span class="sxs-lookup"><span data-stu-id="bba8e-105">If no matching `Add` method exists and you cannot modify the code for the collection, you can add an extension method called `Add` that takes the parameters that are required by the collection initializer.</span></span> <span data-ttu-id="bba8e-106">Il s’agit généralement ce que vous devez faire lorsque vous utilisez des initialiseurs de collection pour les collections génériques.</span><span class="sxs-lookup"><span data-stu-id="bba8e-106">This is typically what you need to do when you use collection initializers for generic collections.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bba8e-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="bba8e-107">Example</span></span>  
 <span data-ttu-id="bba8e-108">L’exemple suivant montre comment ajouter une méthode d’extension générique <xref:System.Collections.Generic.List%601> tapez afin qu’un initialiseur de collection peut être utilisé pour ajouter des objets de type `Employee`.</span><span class="sxs-lookup"><span data-stu-id="bba8e-108">The following example shows how to add an extension method to the generic <xref:System.Collections.Generic.List%601> type so that a collection initializer can be used to add objects of type `Employee`.</span></span> <span data-ttu-id="bba8e-109">La méthode d’extension vous permet d’utiliser la syntaxe d’initialiseur de collection abrégée.</span><span class="sxs-lookup"><span data-stu-id="bba8e-109">The extension method enables you to use the shortened collection initializer syntax.</span></span>  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo1#1](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-an-add-extension-method-used-by-a-collection-initializer_1.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo1#2](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-an-add-extension-method-used-by-a-collection-initializer_2.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo1#3](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-an-add-extension-method-used-by-a-collection-initializer_3.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="bba8e-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bba8e-110">See also</span></span>
- [<span data-ttu-id="bba8e-111">Initialiseurs de collection</span><span class="sxs-lookup"><span data-stu-id="bba8e-111">Collection Initializers</span></span>](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)
- [<span data-ttu-id="bba8e-112">Guide pratique pour Créer une Collection utilisée par un initialiseur de Collection</span><span class="sxs-lookup"><span data-stu-id="bba8e-112">How to: Create a Collection Used by a Collection Initializer</span></span>](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-a-collection-used-by-a-collection-initializer.md)
