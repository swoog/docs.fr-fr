---
title: 'Procédure : Récupérer un seul attribut (LINQ to XML) (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 11b938d7-c011-4048-900e-8b9183c41c94
ms.openlocfilehash: f56bdf86e4b63bc952c1d139aac9ee619b5a5f6c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58837125"
---
# <a name="how-to-retrieve-a-single-attribute-linq-to-xml-visual-basic"></a><span data-ttu-id="726da-102">Procédure : Récupérer un seul attribut (LINQ to XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="726da-102">How to: Retrieve a Single Attribute (LINQ to XML) (Visual Basic)</span></span>
<span data-ttu-id="726da-103">Cette rubrique explique comment récupérer un seul attribut d'un élément, étant donné le nom de l'attribut.</span><span class="sxs-lookup"><span data-stu-id="726da-103">This topic explains how to retrieve a single attribute of an element, given the attribute name.</span></span> <span data-ttu-id="726da-104">Ceci est utile pour écrire des expressions de requête où vous souhaitez rechercher un élément qui possède un attribut particulier.</span><span class="sxs-lookup"><span data-stu-id="726da-104">This is useful for writing query expressions where you want to find an element that has a particular attribute.</span></span>  
  
 <span data-ttu-id="726da-105">La méthode <xref:System.Xml.Linq.XElement.Attribute%2A> de la classe <xref:System.Xml.Linq.XElement> retourne l'objet <xref:System.Xml.Linq.XAttribute> avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="726da-105">The <xref:System.Xml.Linq.XElement.Attribute%2A> method of the <xref:System.Xml.Linq.XElement> class returns the <xref:System.Xml.Linq.XAttribute> with the specified name.</span></span>  
  
## <a name="example"></a><span data-ttu-id="726da-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="726da-106">Example</span></span>  
 <span data-ttu-id="726da-107">L'exemple suivant utilise la méthode <xref:System.Xml.Linq.XElement.Attribute%2A>.</span><span class="sxs-lookup"><span data-stu-id="726da-107">The following example uses the <xref:System.Xml.Linq.XElement.Attribute%2A> method.</span></span>  
  
```vb  
Dim cust As XElement = <PhoneNumbers>  
                           <Phone type="home">555-555-5555</Phone>  
                           <Phone type="work">555-555-6666</Phone>  
                       </PhoneNumbers>  
Dim elList = From el In cust...<Phone>  
For Each e As XElement In elList  
    Console.WriteLine(e.@type)  
Next  
```  
  
 <span data-ttu-id="726da-108">Cet exemple recherche tous les descendants dans l'arborescence nommés `Phone`, puis recherche l'attribut nommé `type`.</span><span class="sxs-lookup"><span data-stu-id="726da-108">This example finds all the descendants in the tree named `Phone`, and then finds the attribute named `type`.</span></span>  
  
 <span data-ttu-id="726da-109">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="726da-109">This code produces the following output:</span></span>  
  
```  
home  
work  
```  
  
## <a name="example"></a><span data-ttu-id="726da-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="726da-110">Example</span></span>  
 <span data-ttu-id="726da-111">Si vous souhaitez récupérer la valeur de l'attribut vous pouvez le convertir, comme vous le feriez avec des objets <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="726da-111">If you want to retrieve the value of the attribute, you can cast it, just as you do for with <xref:System.Xml.Linq.XElement> objects.</span></span> <span data-ttu-id="726da-112">Cela est illustré par l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="726da-112">The following example demonstrates this.</span></span>  
  
```vb  
Dim cust As XElement = <PhoneNumbers>  
                           <Phone type="home">555-555-5555</Phone>  
                           <Phone type="work">555-555-6666</Phone>  
                       </PhoneNumbers>  
Dim elList As IEnumerable(Of XElement) = _  
    From el In cust...<Phone> _  
    Select el  
For Each el As XElement In elList  
    Console.WriteLine(el.@type)  
Next  
```  
  
 <span data-ttu-id="726da-113">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="726da-113">This code produces the following output:</span></span>  
  
```  
home  
work  
```  
  
 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] <span data-ttu-id="726da-114">fournit des opérateurs de conversion explicites pour la classe <xref:System.Xml.Linq.XAttribute> vers `string`, `bool`, `bool?`, `int`, `int?`, `uint`, `uint?`, `long`, `long?`, `ulong`, `ulong?`, `float`, `float?`, `double`, `double?`, `decimal`, `decimal?`, `DateTime`, `DateTime?`, `TimeSpan`, `TimeSpan?`, `GUID` et `GUID?`.</span><span class="sxs-lookup"><span data-stu-id="726da-114">provides explicit cast operators for the <xref:System.Xml.Linq.XAttribute> class to `string`, `bool`, `bool?`, `int`, `int?`, `uint`, `uint?`, `long`, `long?`, `ulong`, `ulong?`, `float`, `float?`, `double`, `double?`, `decimal`, `decimal?`, `DateTime`, `DateTime?`, `TimeSpan`, `TimeSpan?`, `GUID`, and `GUID?`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="726da-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="726da-115">Example</span></span>  
 <span data-ttu-id="726da-116">L'exemple suivant illustre le même code pour un attribut qui est dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="726da-116">The following example shows the same code for an attribute that is in a namespace.</span></span> <span data-ttu-id="726da-117">Pour plus d’informations, consultez [utilisation des espaces de noms XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="726da-117">For more information, see [Working with XML Namespaces (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
```vb  
Imports <xmlns:aw="http://www.adventure-works.com">  
  
Module Module1  
    Sub Main()  
        Dim cust As XElement = _  
            <aw:PhoneNumbers>  
                <aw:Phone aw:type="home">555-555-5555</aw:Phone>  
                <aw:Phone aw:type="work">555-555-6666</aw:Phone>  
            </aw:PhoneNumbers>  
        Dim elList As IEnumerable(Of XElement) = _  
            From el In cust...<aw:Phone> _  
            Select el  
        For Each el As XElement In elList  
            Console.WriteLine(el.@aw:type)  
        Next  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="726da-118">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="726da-118">This code produces the following output:</span></span>  
  
```  
home  
work  
```  
  
## <a name="see-also"></a><span data-ttu-id="726da-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="726da-119">See also</span></span>

- [<span data-ttu-id="726da-120">Axes LINQ to XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="726da-120">LINQ to XML Axes (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-axes.md)
