---
title: Fonctions spatiales
ms.date: 03/30/2017
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
ms.openlocfilehash: ad6b722e84aae40354e30434b107752d02352645
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44133952"
---
# <a name="spatial-functions"></a>Fonctions spatiales
Il n'existe aucun format littéral pour les types spatiaux. Toutefois, vous pouvez utiliser des fonctions canoniques Entity Framework que vous appelez à l'aide de chaînes au format texte connu. Par exemple, l'appel de fonction suivant crée un point géométrique :  
  
```  
GeometryFromText('POINT (43 -73)')  
```  
  
 Le [méthodes SpatialEdmFunctions](https://msdn.microsoft.com/library/hh749531.aspx) page répertorie toutes les méthodes canoniques spatiales Entity Framework. Cliquez sur une méthode qui vous intéresse pour afficher les paramètres qui doivent être passés à une fonction.
