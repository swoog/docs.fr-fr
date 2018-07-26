---
title: Guide pratique pour intercepter les erreurs d’analyse (C#)
ms.date: 07/20/2015
ms.assetid: bfb612d4-5605-48ef-8c93-915cf9d5dcfb
ms.openlocfilehash: 037e490fa7b0600b906ec310201e5d33c2f55baa
ms.sourcegitcommit: 2d8b7488d94101b534ca3e9780b1c1e840233405
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2018
ms.locfileid: "39198471"
---
# <a name="how-to-catch-parsing-errors-c"></a><span data-ttu-id="78c9b-102">Guide pratique pour intercepter les erreurs d’analyse (C#)</span><span class="sxs-lookup"><span data-stu-id="78c9b-102">How to: Catch Parsing Errors (C#)</span></span>
<span data-ttu-id="78c9b-103">Cette rubrique montre comment détecter du code XML incorrect ou non valide.</span><span class="sxs-lookup"><span data-stu-id="78c9b-103">This topic shows how to detect badly formed or invalid XML.</span></span>  
  
 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]<span data-ttu-id="78c9b-104"> est implémenté avec <xref:System.Xml.XmlReader>.</span><span class="sxs-lookup"><span data-stu-id="78c9b-104"> is implemented using <xref:System.Xml.XmlReader>.</span></span> <span data-ttu-id="78c9b-105">Si du code XML incorrect ou non valide est passé à [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)], la classe sous-jacente <xref:System.Xml.XmlReader> ève une exception.</span><span class="sxs-lookup"><span data-stu-id="78c9b-105">If badly formed or invalid XML is passed to [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)], the underlying <xref:System.Xml.XmlReader> class will throw an exception.</span></span> <span data-ttu-id="78c9b-106">Les différentes méthodes qui analysent le code XML, telles que <xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=nameWithType>, n’interceptent pas l’exception. Celle-ci peut donc être interceptée par votre application.</span><span class="sxs-lookup"><span data-stu-id="78c9b-106">The various methods that parse XML, such as <xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=nameWithType>, do not catch the exception; the exception can then be caught by your application.</span></span>  
  
## <a name="example"></a><span data-ttu-id="78c9b-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="78c9b-107">Example</span></span>  
 <span data-ttu-id="78c9b-108">Le code suivant tente d'analyser du code XML non valide :</span><span class="sxs-lookup"><span data-stu-id="78c9b-108">The following code tries to parse invalid XML:</span></span>  
  
```csharp  
try {  
    XElement contacts = XElement.Parse(  
        @"<Contacts>  
            <Contact>  
                <Name>Jim Wilson</Name>  
            </Contact>  
          </Contcts>");  
  
    Console.WriteLine(contacts);  
}  
catch (System.Xml.XmlException e)  
{  
    Console.WriteLine(e.Message);  
}  
```  
  
 <span data-ttu-id="78c9b-109">Lorsque vous exécutez ce code, l'exception suivante est levée :</span><span class="sxs-lookup"><span data-stu-id="78c9b-109">When you run this code, it throws the following exception:</span></span>  
  
```  
The 'Contacts' start tag on line 1 does not match the end tag of 'Contcts'. Line 5, position 13.  
```  
  
 <span data-ttu-id="78c9b-110">Pour plus d'informations sur les exceptions que les méthodes <xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=nameWithType>, <xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=nameWithType>, <xref:System.Xml.Linq.XElement.Load%2A?displayProperty=nameWithType> et <xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=nameWithType> peuvent lever, consultez la documentation <xref:System.Xml.XmlReader>.</span><span class="sxs-lookup"><span data-stu-id="78c9b-110">For information about the exceptions that you can expect the <xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=nameWithType>, <xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=nameWithType>, <xref:System.Xml.Linq.XElement.Load%2A?displayProperty=nameWithType>, and <xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=nameWithType> methods to throw, see the <xref:System.Xml.XmlReader> documentation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="78c9b-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78c9b-111">See Also</span></span>  
 [<span data-ttu-id="78c9b-112">Analyse de code XML (C#)</span><span class="sxs-lookup"><span data-stu-id="78c9b-112">Parsing XML (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/parsing-xml.md)
