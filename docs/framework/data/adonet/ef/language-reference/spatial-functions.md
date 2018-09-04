---
title: Fonctions spatiales
ms.date: 03/30/2017
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
ms.openlocfilehash: ad6b722e84aae40354e30434b107752d02352645
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43559515"
---
# <a name="spatial-functions"></a><span data-ttu-id="11162-102">Fonctions spatiales</span><span class="sxs-lookup"><span data-stu-id="11162-102">Spatial Functions</span></span>
<span data-ttu-id="11162-103">Il n'existe aucun format littéral pour les types spatiaux.</span><span class="sxs-lookup"><span data-stu-id="11162-103">There is no literal format for spatial types.</span></span> <span data-ttu-id="11162-104">Toutefois, vous pouvez utiliser des fonctions canoniques Entity Framework que vous appelez à l'aide de chaînes au format texte connu.</span><span class="sxs-lookup"><span data-stu-id="11162-104">However, you can use canonical Entity Framework functions that you call using strings in Well-Known Text format.</span></span> <span data-ttu-id="11162-105">Par exemple, l'appel de fonction suivant crée un point géométrique :</span><span class="sxs-lookup"><span data-stu-id="11162-105">For example, the following function call creates a geometry point:</span></span>  
  
```  
GeometryFromText('POINT (43 -73)')  
```  
  
 <span data-ttu-id="11162-106">Le [méthodes SpatialEdmFunctions](https://msdn.microsoft.com/library/hh749531.aspx) page répertorie toutes les méthodes canoniques spatiales Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="11162-106">The [SpatialEdmFunctions Methods](https://msdn.microsoft.com/library/hh749531.aspx) page lists all spatial canonical Entity Framework methods.</span></span> <span data-ttu-id="11162-107">Cliquez sur une méthode qui vous intéresse pour afficher les paramètres qui doivent être passés à une fonction.</span><span class="sxs-lookup"><span data-stu-id="11162-107">Click on a method of interest to see what parameters should be passed to a function.</span></span>
