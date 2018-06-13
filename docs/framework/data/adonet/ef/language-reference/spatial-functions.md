---
title: Fonctions spatiales
ms.date: 03/30/2017
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
ms.openlocfilehash: 7b78cbf4dc53ba1bc4148fa0077615e43cc8f9f9
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32763928"
---
# <a name="spatial-functions"></a><span data-ttu-id="921fb-102">Fonctions spatiales</span><span class="sxs-lookup"><span data-stu-id="921fb-102">Spatial Functions</span></span>
<span data-ttu-id="921fb-103">Il n'existe aucun format littéral pour les types spatiaux.</span><span class="sxs-lookup"><span data-stu-id="921fb-103">There is no literal format for spatial types.</span></span> <span data-ttu-id="921fb-104">Toutefois, vous pouvez utiliser des fonctions canoniques Entity Framework que vous appelez à l'aide de chaînes au format texte connu.</span><span class="sxs-lookup"><span data-stu-id="921fb-104">However, you can use canonical Entity Framework functions that you call using strings in Well-Known Text format.</span></span> <span data-ttu-id="921fb-105">Par exemple, l'appel de fonction suivant crée un point géométrique :</span><span class="sxs-lookup"><span data-stu-id="921fb-105">For example, the following function call creates a geometry point:</span></span>  
  
```  
GeometryFromText('POINT (43 -73)')  
```  
  
 <span data-ttu-id="921fb-106">Le [spatialedmfunctions, méthodes](http://msdn.microsoft.com/library/hh749531.aspx) page répertorie toutes les méthodes canoniques spatiales Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="921fb-106">The [SpatialEdmFunctions Methods](http://msdn.microsoft.com/library/hh749531.aspx) page lists all spatial canonical Entity Framework methods.</span></span> <span data-ttu-id="921fb-107">Cliquez sur une méthode qui vous intéresse pour afficher les paramètres qui doivent être passés à une fonction.</span><span class="sxs-lookup"><span data-stu-id="921fb-107">Click on a method of interest to see what parameters should be passed to a function.</span></span>
