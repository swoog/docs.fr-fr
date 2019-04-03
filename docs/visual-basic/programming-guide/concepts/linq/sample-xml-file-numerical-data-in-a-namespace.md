---
title: 'Exemple de fichier XML : Données numériques dans un espace de noms1'
ms.date: 07/20/2015
ms.assetid: f01cc0a1-fb55-4b42-8380-16f4be47d6f4
ms.openlocfilehash: 09954798615954d238273b3d4ed71b5ff475394f
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58816198"
---
# <a name="sample-xml-file-numerical-data-in-a-namespace"></a><span data-ttu-id="a95ea-102">Exemple de fichier XML : Données numériques dans un espace de noms</span><span class="sxs-lookup"><span data-stu-id="a95ea-102">Sample XML File: Numerical Data in a Namespace</span></span>
<span data-ttu-id="a95ea-103">Le fichier XML suivant est utilisé dans différents exemples dans la documentation [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="a95ea-103">The following XML file is used in various examples in the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] documentation.</span></span> <span data-ttu-id="a95ea-104">Ce fichier contient des données numériques pour effectuer des additions, des moyennes et des regroupements.</span><span class="sxs-lookup"><span data-stu-id="a95ea-104">This file contains numerical data for summing, averaging, and grouping.</span></span> <span data-ttu-id="a95ea-105">Le code XML se trouve dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="a95ea-105">The XML is in a namespace.</span></span>  
  
## <a name="data"></a><span data-ttu-id="a95ea-106">Données</span><span class="sxs-lookup"><span data-stu-id="a95ea-106">Data</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="a95ea-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a95ea-107">See also</span></span>

- [<span data-ttu-id="a95ea-108">Exemples de documents XML (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="a95ea-108">Sample XML Documents (LINQ to XML)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-documents-linq-to-xml.md)
