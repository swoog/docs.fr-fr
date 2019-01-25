---
title: Coordonnées Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms coordinates
- screen coordinates
- client coordinates
- coordinates [Windows Forms], Windows Forms
ms.assetid: cc06e61f-43b6-4408-a676-2542dcfcd96e
ms.openlocfilehash: a6f082eb57a9cfe1af0d4207cbf5226637191c90
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54556049"
---
# <a name="windows-forms-coordinates"></a>Coordonnées Windows Forms
Le système de coordonnées d’un formulaire Windows est basé sur les coordonnées de périphérique, et l’unité de mesure lors du dessin dans les Windows Forms de base est l’unité de périphérique (en règle générale, le pixel). Points à l’écran sont décrits par des paires de coordonnées x et y, avec les coordonnées x qui augmentent vers la droite et les coordonnées y augmentant de haut en bas. L’emplacement de l’origine, par rapport à l’écran, varie selon que vous spécifiez les coordonnées d’écran ou client.  
  
## <a name="screen-coordinates"></a>Coordonnées d’écran  
 Une application Windows Forms spécifie la position d’une fenêtre sur l’écran en coordonnées d’écran. Pour les coordonnées d’écran, l’origine est l’angle supérieur gauche de l’écran. La position complète d’une fenêtre est souvent décrite par un <xref:System.Drawing.Rectangle> structure contenant les coordonnées d’écran de deux points qui définissent les angles supérieur gauche et inférieur droit de la fenêtre.  
  
## <a name="client-coordinates"></a>Coordonnées clientes  
 Une application Windows Forms spécifie la position des points dans un formulaire ou d’un contrôle à l’aide de coordonnées clientes. L’origine de coordonnées clientes est l’angle supérieur gauche de la zone cliente du formulaire ou contrôle. Les coordonnées clientes garantissent qu’une application peut utiliser les valeurs des coordonnées cohérents pendant que vous dessinez dans un formulaire ou contrôle, quelle que soit la position du formulaire ou contrôle sur l’écran.  
  
 Les dimensions de la zone cliente sont également décrites par un <xref:System.Drawing.Rectangle> structure qui contient les coordonnées clientes pour la zone. Dans tous les cas, la coordonnée supérieure gauche du rectangle est incluse dans la zone cliente, tandis que la coordonnée inférieure droite est exclue. Opérations graphiques n’incluent pas les bords droit et inférieurs d’une zone cliente. Par exemple le <xref:System.Drawing.Graphics.FillRectangle%2A> méthode remplira jusqu’au bord droit et inférieur du rectangle spécifié, mais n’inclura pas ces bords.  
  
## <a name="mapping-from-one-type-of-coordinate-to-another"></a>Mappage d’un Type de coordonnée à un autre  
 Parfois, vous devrez peut-être mapper à partir des coordonnées d’écran en coordonnées clientes. Vous pouvez le faire facilement en utilisant le <xref:System.Windows.Forms.Control.PointToClient%2A> et <xref:System.Windows.Forms.Control.PointToScreen%2A> méthodes disponibles dans le <xref:System.Windows.Forms.Control> classe. Par exemple, le <xref:System.Windows.Forms.Control.MousePosition%2A> propriété du <xref:System.Windows.Forms.Control> est signalée en coordonnées d’écran, mais vous pouvez convertir celles-ci en coordonnées clientes.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.Control.PointToClient%2A>
- <xref:System.Windows.Forms.Control.PointToScreen%2A>
