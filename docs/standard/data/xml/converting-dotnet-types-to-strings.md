---
title: Conversion de types .NET Framework en chaînes
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: dc2e2b65-f623-4dc3-938b-d2a054d6832c
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 59e288a756a022763bae2235964a8b25a9d72bd1
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44196231"
---
# <a name="converting-net-framework-types-to-strings"></a><span data-ttu-id="2c6db-102">Conversion de types .NET Framework en chaînes</span><span class="sxs-lookup"><span data-stu-id="2c6db-102">Converting .NET Framework Types to Strings</span></span>
<span data-ttu-id="2c6db-103">Si vous voulez convertir un type .NET Framework en chaîne, utilisez la méthode **ToString**.</span><span class="sxs-lookup"><span data-stu-id="2c6db-103">If you want to convert a .NET Framework type to a string, use the **ToString** method.</span></span> <span data-ttu-id="2c6db-104">La méthode **ToString** retourne une représentation sous forme de chaîne du type passé.</span><span class="sxs-lookup"><span data-stu-id="2c6db-104">The **ToString** method returns a string representation of the type passed in.</span></span> <span data-ttu-id="2c6db-105">Le tableau suivant répertorie les types .NET Framework qui retournent une chaîne dans un format qui mappe aux spécifications de schéma XML (XSD).</span><span class="sxs-lookup"><span data-stu-id="2c6db-105">The following table lists the .NET Framework types that return a string in a format that maps to the XML Schema (XSD) specifications.</span></span>  
  
|<span data-ttu-id="2c6db-106">Type .NET Framework</span><span class="sxs-lookup"><span data-stu-id="2c6db-106">.NET Framework type</span></span>|<span data-ttu-id="2c6db-107">Type de chaîne de retour</span><span class="sxs-lookup"><span data-stu-id="2c6db-107">String type returned</span></span>|  
|-------------------------|--------------------------|  
|<span data-ttu-id="2c6db-108">Booléen</span><span class="sxs-lookup"><span data-stu-id="2c6db-108">Boolean</span></span>|<span data-ttu-id="2c6db-109">"true", "false"</span><span class="sxs-lookup"><span data-stu-id="2c6db-109">"true", "false"</span></span>|  
|<span data-ttu-id="2c6db-110">Single.PositiveInfinity</span><span class="sxs-lookup"><span data-stu-id="2c6db-110">Single.PositiveInfinity</span></span>|<span data-ttu-id="2c6db-111">"INF"</span><span class="sxs-lookup"><span data-stu-id="2c6db-111">"INF"</span></span>|  
|<span data-ttu-id="2c6db-112">Single.NegativeInfinity</span><span class="sxs-lookup"><span data-stu-id="2c6db-112">Single.NegativeInfinity</span></span>|<span data-ttu-id="2c6db-113">"-INF"</span><span class="sxs-lookup"><span data-stu-id="2c6db-113">"-INF"</span></span>|  
|<span data-ttu-id="2c6db-114">Double.PositiveInfinity</span><span class="sxs-lookup"><span data-stu-id="2c6db-114">Double.PositiveInfinity</span></span>|<span data-ttu-id="2c6db-115">"INF"</span><span class="sxs-lookup"><span data-stu-id="2c6db-115">"INF"</span></span>|  
|<span data-ttu-id="2c6db-116">Double.NegativeInfinity</span><span class="sxs-lookup"><span data-stu-id="2c6db-116">Double.NegativeInfinity</span></span>|<span data-ttu-id="2c6db-117">"-INF"</span><span class="sxs-lookup"><span data-stu-id="2c6db-117">"-INF"</span></span>|  
|<span data-ttu-id="2c6db-118">DateTime</span><span class="sxs-lookup"><span data-stu-id="2c6db-118">DateTime</span></span>|<span data-ttu-id="2c6db-119">Le format est yyyy-MM-ddTHH:mm:sszzzzzz et ses sous-ensembles.</span><span class="sxs-lookup"><span data-stu-id="2c6db-119">Format is yyyy-MM-ddTHH:mm:sszzzzzz and its subsets.</span></span>|  
|<span data-ttu-id="2c6db-120">TimeSpan</span><span class="sxs-lookup"><span data-stu-id="2c6db-120">Timespan</span></span>|<span data-ttu-id="2c6db-121">Le format est PnYnMnTnHnMnS. Par exemple, `P2Y10M15DT10H30M20S` est la durée de 2 années, 10 mois, 15 jours, 10 heures, 30 minutes et 20 secondes.</span><span class="sxs-lookup"><span data-stu-id="2c6db-121">Format is PnYnMnTnHnMnS, for example, `P2Y10M15DT10H30M20S` is a duration of 2 years, 10 months, 15 days, 10hours, 30 minutes and 20 seconds.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2c6db-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c6db-122">See also</span></span>

- [<span data-ttu-id="2c6db-123">Conversion des types de données XML</span><span class="sxs-lookup"><span data-stu-id="2c6db-123">Conversion of XML Data Types</span></span>](../../../../docs/standard/data/xml/conversion-of-xml-data-types.md)  
- [<span data-ttu-id="2c6db-124">Conversion de chaînes en types de données .NET Framework</span><span class="sxs-lookup"><span data-stu-id="2c6db-124">Converting Strings to .NET Framework Data Types</span></span>](../../../../docs/standard/data/xml/converting-strings-to-dotnet-data-types.md)
