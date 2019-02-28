---
title: 'Procédure : Accéder aux éléments d’enfant XML (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- XML axis [Visual Basic], child
- child axis property [Visual Basic]
- XML child axis property [Visual Basic]
- XML [Visual Basic], accessing
ms.assetid: 6689eb36-c471-469f-a82d-099ab8197b25
ms.openlocfilehash: 874c7490e451d64bf50e25934ea43a9b928ddab9
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56980553"
---
# <a name="how-to-access-xml-child-elements-visual-basic"></a><span data-ttu-id="62918-102">Procédure : Accéder aux éléments d’enfant XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="62918-102">How to: Access XML Child Elements (Visual Basic)</span></span>
<span data-ttu-id="62918-103">Cet exemple montre comment utiliser un enfant de propriété d’axe pour accéder à tous les éléments enfants XML qui ont un nom spécifié dans un élément XML.</span><span class="sxs-lookup"><span data-stu-id="62918-103">This example shows how to use a child axis property to access all XML child elements that have a specified name in an XML element.</span></span> <span data-ttu-id="62918-104">En particulier, il utilise le <xref:System.Xml.Linq.XElement.Value%2A> propriété à obtenir la valeur du premier élément dans la collection qui le `name` retourne de propriété d’axe enfant.</span><span class="sxs-lookup"><span data-stu-id="62918-104">In particular, it uses the <xref:System.Xml.Linq.XElement.Value%2A> property to get the value of the first element in the collection that the `name` child axis property returns.</span></span> <span data-ttu-id="62918-105">Le `name` propriété d’axe enfant obtient tous les éléments enfants nommés `phone` dans le `contact` objet.</span><span class="sxs-lookup"><span data-stu-id="62918-105">The `name` child axis property gets all child elements named `phone` in the `contact` object.</span></span> <span data-ttu-id="62918-106">Cet exemple utilise également le `phone` propriété d’axe enfant pour accéder à tous les éléments enfants nommés `phone` qui sont contenus dans le `contact` objet.</span><span class="sxs-lookup"><span data-stu-id="62918-106">This example also uses the `phone` child axis property to access all child elements named `phone` that are contained in the `contact` object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="62918-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="62918-107">Example</span></span>  
 [!code-vb[VbXMLSamples#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples4.vb#10)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="62918-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="62918-108">Compiling the Code</span></span>  
 <span data-ttu-id="62918-109">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="62918-109">This example requires:</span></span>  
  
-   <span data-ttu-id="62918-110">une référence à l'espace de noms <xref:System.Xml.Linq>.</span><span class="sxs-lookup"><span data-stu-id="62918-110">A reference to the <xref:System.Xml.Linq> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62918-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62918-111">See also</span></span>
- <xref:System.Xml.Linq.XContainer.Elements%2A?displayProperty=nameWithType>
- [<span data-ttu-id="62918-112">Propriété d’axe enfant XML</span><span class="sxs-lookup"><span data-stu-id="62918-112">XML Child Axis Property</span></span>](../../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md)
- [<span data-ttu-id="62918-113">Propriété de valeur XML</span><span class="sxs-lookup"><span data-stu-id="62918-113">XML Value Property</span></span>](../../../../visual-basic/language-reference/xml-axis/xml-value-property.md)
- [<span data-ttu-id="62918-114">Accès au code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="62918-114">Accessing XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/accessing-xml.md)
- [<span data-ttu-id="62918-115">XML</span><span class="sxs-lookup"><span data-stu-id="62918-115">XML</span></span>](../../../../visual-basic/programming-guide/language-features/xml/index.md)
