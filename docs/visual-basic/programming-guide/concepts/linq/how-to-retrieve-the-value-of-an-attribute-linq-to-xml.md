---
title: 'Procédure : Récupérer la valeur d’un attribut (LINQ to XML) (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 5f4b3790-c83f-4eb3-a889-e3587edf3ca1
ms.openlocfilehash: 7cdd3e1f3e4c15d99511e944fd9bc2faac17dc5c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58824356"
---
# <a name="how-to-retrieve-the-value-of-an-attribute-linq-to-xml-visual-basic"></a><span data-ttu-id="cab15-102">Procédure : Récupérer la valeur d’un attribut (LINQ to XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cab15-102">How to: Retrieve the Value of an Attribute (LINQ to XML) (Visual Basic)</span></span>
<span data-ttu-id="cab15-103">Cette rubrique montre comment obtenir la valeur d'attributs.</span><span class="sxs-lookup"><span data-stu-id="cab15-103">This topic shows how to obtain the value of attributes.</span></span> <span data-ttu-id="cab15-104">Il existe pour cela deux méthodes : vous pouvez caster un <xref:System.Xml.Linq.XAttribute> en un type souhaité. L’opérateur de conversion explicite convertit alors le contenu de l’élément ou de l’attribut vers le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="cab15-104">There are two main ways: You can cast an <xref:System.Xml.Linq.XAttribute> to the desired type; the explicit conversion operator then converts the contents of the element or attribute to the specified type.</span></span> <span data-ttu-id="cab15-105">En guise d'alternative, vous pouvez utiliser la propriété <xref:System.Xml.Linq.XAttribute.Value%2A>.</span><span class="sxs-lookup"><span data-stu-id="cab15-105">Alternatively, you can use the <xref:System.Xml.Linq.XAttribute.Value%2A> property.</span></span> <span data-ttu-id="cab15-106">Toutefois, la conversion est généralement la meilleure approche.</span><span class="sxs-lookup"><span data-stu-id="cab15-106">However, casting is generally the better approach.</span></span> <span data-ttu-id="cab15-107">Si vous convertissez l'attribut vers un type Nullable, le code est plus simple à écrire lors de la récupération de la valeur d'un attribut qui peut exister ou ne pas exister.</span><span class="sxs-lookup"><span data-stu-id="cab15-107">If you cast the attribute to a nullable type, the code is simpler to write when retrieving the value of an attribute that might or might not exist.</span></span> <span data-ttu-id="cab15-108">Pour obtenir des exemples de cette technique, consultez [Guide pratique pour Récupérer la valeur d’un élément (LINQ to XML) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-retrieve-the-value-of-an-element-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="cab15-108">For examples of this technique, see [How to: Retrieve the Value of an Element (LINQ to XML) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-retrieve-the-value-of-an-element-linq-to-xml.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="cab15-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="cab15-109">Example</span></span>  
 <span data-ttu-id="cab15-110">En Visual Basic, vous pouvez utiliser la propriété d'attribut intégrée pour récupérer la valeur d'un attribut.</span><span class="sxs-lookup"><span data-stu-id="cab15-110">In Visual Basic, you can use the integrated attribute property to retrieve the value of an attribute.</span></span>  
  
```vb  
Dim root As XElement = <Root Attr="abcde"/>  
Console.WriteLine(root)  
Dim str As String = root.@Attr  
Console.WriteLine(str)  
```  
  
 <span data-ttu-id="cab15-111">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="cab15-111">This example produces the following output:</span></span>  
  
```xml  
<Root Attr="abcde" />  
abcde  
```  
  
## <a name="example"></a><span data-ttu-id="cab15-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="cab15-112">Example</span></span>  
 <span data-ttu-id="cab15-113">En Visual Basic, vous pouvez utiliser la propriété d'attribut intégrée pour définir la valeur d'un attribut.</span><span class="sxs-lookup"><span data-stu-id="cab15-113">In Visual Basic, you can use the integrated attribute property to set the value of an attribute.</span></span> <span data-ttu-id="cab15-114">En outre, si vous utilisez la propriété d'attribut intégrée pour définir la valeur d'un attribut qui n'existe pas, l'attribut sera créé.</span><span class="sxs-lookup"><span data-stu-id="cab15-114">Further, if you use the integrated attribute property to set the value of an attribute that does not exist, the attribute will be created.</span></span>  
  
```vb  
Dim root As XElement = <Root Att1="content"/>  
root.@Att1 = "new content"  
root.@Att2 = "new attribute"  
Console.WriteLine(root)  
```  
  
 <span data-ttu-id="cab15-115">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="cab15-115">This example produces the following output:</span></span>  
  
```xml  
<Root Att1="new content" Att2="new attribute" />  
```  
  
## <a name="example"></a><span data-ttu-id="cab15-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="cab15-116">Example</span></span>  
 <span data-ttu-id="cab15-117">L'exemple suivant montre comment récupérer la valeur d'un attribut lorsque celui-ci se trouve dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="cab15-117">The following example shows how to retrieve the value of an attribute where the attribute is in a namespace.</span></span> <span data-ttu-id="cab15-118">Pour plus d’informations, consultez [utilisation des espaces de noms XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="cab15-118">For more information, see [Working with XML Namespaces (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
```vb  
Imports <xmlns:aw="http://www.adventure-works.com">  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = <aw:Root aw:Attr="abcde"/>  
        Dim str As String = root.@aw:Attr  
        Console.WriteLine(str)  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="cab15-119">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="cab15-119">This example produces the following output:</span></span>  
  
```  
abcde  
```  
  
## <a name="see-also"></a><span data-ttu-id="cab15-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cab15-120">See also</span></span>

- [<span data-ttu-id="cab15-121">Axes LINQ to XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cab15-121">LINQ to XML Axes (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-axes.md)
