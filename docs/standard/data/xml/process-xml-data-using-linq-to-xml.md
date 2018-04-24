---
title: Traitement des données XML à l'aide de LINQ to XML
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology: dotnet-standard
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 059d6b9d-63f7-4011-9ba8-8406f0bbae7d
caps.latest.revision: 2
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 4b3d9b53992cfa1c638266883f1298954f5a529c
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="process-xml-data-using-linq-to-xml"></a><span data-ttu-id="fa29a-102">Traitement des données XML à l'aide de LINQ to XML</span><span class="sxs-lookup"><span data-stu-id="fa29a-102">Process XML Data Using LINQ to XML</span></span>
<span data-ttu-id="fa29a-103">LINQ to XML est le nouveau modèle du .NET Framework version 3.5 pour le traitement des données XML.</span><span class="sxs-lookup"><span data-stu-id="fa29a-103">LINQ to XML is the new model in the .NET Framework version 3.5 for processing XML data.</span></span> <span data-ttu-id="fa29a-104">LINQ to XML permet aux développeurs d'effectuer toutes les opérations qu'ils souhaitent avec les données XML : interrogation, modification, création et sérialisation de documents XML,</span><span class="sxs-lookup"><span data-stu-id="fa29a-104">LINQ to XML allows developers to do everything they would expect with XML data: querying, modifying, creating, saving, and serializing XML documents.</span></span> <span data-ttu-id="fa29a-105">mais les avantages réels se situe dans les fonctions de requête et de création.</span><span class="sxs-lookup"><span data-stu-id="fa29a-105">The real advantages lie in the query and creation capabilities.</span></span>  
  
 <span data-ttu-id="fa29a-106">À la fois succinctes et expressives, les requêtes en LINQ to XML se basent sur une syntaxe qui se rapproche davantage du langage SQL que de Xpath ou XQuery.</span><span class="sxs-lookup"><span data-stu-id="fa29a-106">Queries in LINQ to XML are succinct and expressive, using syntax more similar to SQL than to XPath or XQuery.</span></span> <span data-ttu-id="fa29a-107">Parce que les résultats de requête peuvent être retournés en tant que collections d'éléments ou d'attributs et utilisés comme paramètres pour les objets XElement, les arborescences XML peuvent être facilement transformées d'une forme à l'autre.</span><span class="sxs-lookup"><span data-stu-id="fa29a-107">Because query results can be returned as collections of elements or attributes and can be used as parameters for XElement objects, XML trees can be easily transformed from one shape to another.</span></span>  
  
 <span data-ttu-id="fa29a-108">LINQ to XML se base sur la technologie LINQ (Langage-Integrated Query) du .NET Framework version 3.5.</span><span class="sxs-lookup"><span data-stu-id="fa29a-108">LINQ to XML leverages the language-integrated query (LINQ) technology in the .NET Framework version 3.5.</span></span> <span data-ttu-id="fa29a-109">LINQ étend la syntaxe des langages C# et Visual Basic pour fournir de puissantes capacités de requête qui peuvent être potentiellement étendues à n'importe quel magasin de données.</span><span class="sxs-lookup"><span data-stu-id="fa29a-109">LINQ extends the language syntax of C# and Visual Basic to provide powerful query capabilities that can be extended to potentially any data store.</span></span>  
  
 <span data-ttu-id="fa29a-110">Consultez [LINQ to XLM](https://msdn.microsoft.com/library/f0fe21e9-ee43-4a55-b91a-0800e5782c13) pour une présentation détaillée de son utilisation et [LINQ (Language-Integrated Query](https://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d) pour une vue d'ensemble de l'infrastructure LINQ.</span><span class="sxs-lookup"><span data-stu-id="fa29a-110">See [LINQ to XML](https://msdn.microsoft.com/library/f0fe21e9-ee43-4a55-b91a-0800e5782c13) for a detailed discussion of its use, and see [LINQ (Language-Integrated Query)](https://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d) for an overview of the LINQ framework.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa29a-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa29a-111">See Also</span></span>  
 <xref:System.Xml.Linq>  
 <xref:System.Linq>  
 [<span data-ttu-id="fa29a-112">LINQ to XML, différences par rapport à DOM</span><span class="sxs-lookup"><span data-stu-id="fa29a-112">LINQ to XML vs. DOM</span></span>](https://msdn.microsoft.com/library/19b5ed02-feb2-455a-8897-f7f0fd76aca3)  
 [<span data-ttu-id="fa29a-113">LINQ to XML, différences par rapport à d’autres technologies XML</span><span class="sxs-lookup"><span data-stu-id="fa29a-113">LINQ to XML vs. Other XML Technologies</span></span>](https://msdn.microsoft.com/library/7ba1eecf-f09a-42de-bc80-22ca5b2e42d3)
