---
title: Fonctions spatiales
ms.date: 03/30/2017
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
ms.openlocfilehash: 09402633c5e7f591a534992fc92655e6a2d1d88d
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55904471"
---
# <a name="spatial-functions"></a>Fonctions spatiales
Il n'existe aucun format littéral pour les types spatiaux. Toutefois, vous pouvez utiliser des fonctions canoniques Entity Framework que vous appelez à l'aide de chaînes au format texte connu. Par exemple, l'appel de fonction suivant crée un point géométrique :  
  
```  
GeometryFromText('POINT (43 -73)')  
```  
  
 Le <xref:System.Data.Common.CommandTrees.ExpressionBuilder.Spatial.SpatialEdmFunctions> méthodes ont toutes les méthodes canoniques spatiales Entity Framework. Cliquez sur une méthode qui vous intéresse pour afficher les paramètres qui doivent être passés à une fonction.
