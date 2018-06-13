---
title: Utilisation de conteneurs graphiques
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], using containers
- graphics containers
- examples [Windows Forms], graphics containers
ms.assetid: 74632f91-cefa-4f51-ab7c-f9ac91942caf
ms.openlocfilehash: 8755a95434d3fed06a55cfca0f71d86e5521cb39
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33525019"
---
# <a name="using-graphics-containers"></a>Utilisation de conteneurs graphiques
A <xref:System.Drawing.Graphics> objet fournit des méthodes telles que <xref:System.Drawing.Graphics.DrawLine%2A>, <xref:System.Drawing.Graphics.DrawImage%2A>, et <xref:System.Drawing.Graphics.DrawString%2A> pour l’affichage des images vectorielles, des images raster et texte. A <xref:System.Drawing.Graphics> objet possède également plusieurs propriétés qui influencent la qualité et l’orientation des éléments qui sont dessinées. Par exemple, la propriété du mode de lissage détermine si l’anticrénelage est appliquée à des lignes et des courbes, et la propriété de transformation universelle influence sur la position et la rotation des éléments qui sont dessinées.  
  
 A <xref:System.Drawing.Graphics> objet est associé à un périphérique d’affichage particulier. Lorsque vous utilisez un <xref:System.Drawing.Graphics> objet à dessiner dans une fenêtre, le <xref:System.Drawing.Graphics> objet est également associé à cette fenêtre particulière.  
  
 A <xref:System.Drawing.Graphics> objet peut être considéré comme un conteneur car il conserve un jeu de propriétés qui influencent le dessin et il est lié à des informations spécifiques au périphérique. Vous pouvez créer un conteneur secondaire dans un fichier <xref:System.Drawing.Graphics> objet en appelant le <xref:System.Drawing.Graphics.BeginContainer%2A> méthode qui <xref:System.Drawing.Graphics> objet.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Gestion de l'état d'un objet graphique](../../../../docs/framework/winforms/advanced/managing-the-state-of-a-graphics-object.md)  
 Décrit comment gérer les paramètres de qualité, zone de découpage et les transformations d’une <xref:System.Drawing.Graphics> objet.  
  
 [Utilisation de conteneurs graphiques imbriqués](../../../../docs/framework/winforms/advanced/using-nested-graphics-containers.md)  
 Montre comment utiliser des conteneurs pour contrôler l’état de la <xref:System.Drawing.Graphics> objet.
