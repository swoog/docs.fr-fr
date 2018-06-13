---
title: 'Exemple de fichier XML : Données numériques dans un espace de noms3'
ms.date: 07/20/2015
ms.assetid: 51750cab-3c66-4511-90fb-b9d211308d31
ms.openlocfilehash: 5a752f477d17cee50b98bc88bd39cabda2bd3bf6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33329002"
---
# <a name="sample-xml-file-numerical-data-in-a-namespace"></a><span data-ttu-id="449ae-102">Exemple de fichier XML : Données numériques dans un espace de noms</span><span class="sxs-lookup"><span data-stu-id="449ae-102">Sample XML File: Numerical Data in a Namespace</span></span>
<span data-ttu-id="449ae-103">Le fichier XML suivant est utilisé dans différents exemples dans la documentation [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="449ae-103">The following XML file is used in various examples in the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] documentation.</span></span> <span data-ttu-id="449ae-104">Ce fichier contient des données numériques pour effectuer des additions, des moyennes et des regroupements.</span><span class="sxs-lookup"><span data-stu-id="449ae-104">This file contains numerical data for summing, averaging, and grouping.</span></span> <span data-ttu-id="449ae-105">Le code XML se trouve dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="449ae-105">The XML is in a namespace.</span></span>  
  
## <a name="data"></a><span data-ttu-id="449ae-106">Données</span><span class="sxs-lookup"><span data-stu-id="449ae-106">Data</span></span>  
  
```xml  
<Root xmlns='http://www.adatum.com'>  
  <TaxRate>7.25</TaxRate>  
  <Data>  
    <Category>A</Category>  
    <Quantity>3</Quantity>  
    <Price>24.50</Price>  
  </Data>  
  <Data>  
    <Category>B</Category>  
    <Quantity>1</Quantity>  
    <Price>89.99</Price>  
  </Data>  
  <Data>  
    <Category>A</Category>  
    <Quantity>5</Quantity>  
    <Price>4.95</Price>  
  </Data>  
  <Data>  
    <Category>A</Category>  
    <Quantity>3</Quantity>  
    <Price>66.00</Price>  
  </Data>  
  <Data>  
    <Category>B</Category>  
    <Quantity>10</Quantity>  
    <Price>.99</Price>  
  </Data>  
  <Data>  
    <Category>A</Category>  
    <Quantity>15</Quantity>  
    <Price>29.00</Price>  
  </Data>  
  <Data>  
    <Category>B</Category>  
    <Quantity>8</Quantity>  
    <Price>6.99</Price>  
  </Data>  
</Root>  
```  
  
## <a name="see-also"></a><span data-ttu-id="449ae-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="449ae-107">See Also</span></span>  
 [<span data-ttu-id="449ae-108">Exemples de documents XML (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="449ae-108">Sample XML Documents (LINQ to XML)</span></span>](../../../../csharp/programming-guide/concepts/linq/sample-xml-documents-linq-to-xml.md)
