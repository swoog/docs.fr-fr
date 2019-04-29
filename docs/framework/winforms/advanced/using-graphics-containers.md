---
title: Utilisation de conteneurs graphiques
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], using containers
- graphics containers
- examples [Windows Forms], graphics containers
ms.assetid: 74632f91-cefa-4f51-ab7c-f9ac91942caf
ms.openlocfilehash: cfad7254057a31ea8268784cd4b6849850f3e2aa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61766153"
---
# <a name="using-graphics-containers"></a>Utilisation de conteneurs graphiques
Un <xref:System.Drawing.Graphics> objet fournit des méthodes telles que <xref:System.Drawing.Graphics.DrawLine%2A>, <xref:System.Drawing.Graphics.DrawImage%2A>, et <xref:System.Drawing.Graphics.DrawString%2A> pour l’affichage des images vectorielles, des images raster et texte. Un <xref:System.Drawing.Graphics> objet possède également plusieurs propriétés qui influencent la qualité et l’orientation des éléments qui sont dessinées. Par exemple, la propriété de mode de lissage détermine si l’anticrénelage est appliquée à des lignes et des courbes, et la propriété de transformation world influence la position et la rotation des éléments qui sont dessinées.  
  
 Un <xref:System.Drawing.Graphics> objet est associé à un périphérique d’affichage particulier. Lorsque vous utilisez un <xref:System.Drawing.Graphics> objet à dessiner dans une fenêtre, le <xref:System.Drawing.Graphics> objet est également associé à cette fenêtre particulière.  
  
 Un <xref:System.Drawing.Graphics> objet peut être imaginée comme un conteneur, car il conserve un jeu de propriétés qui influencent le dessin et il est lié à des informations spécifiques au périphérique. Vous pouvez créer un conteneur secondaire dans une existante <xref:System.Drawing.Graphics> objet en appelant le <xref:System.Drawing.Graphics.BeginContainer%2A> méthode cela <xref:System.Drawing.Graphics> objet.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Gestion de l'état d'un objet graphique](managing-the-state-of-a-graphics-object.md)  
 Décrit comment gérer les paramètres de qualité, de zone de découpage et de transformations d’un <xref:System.Drawing.Graphics> objet.  
  
 [Utilisation de conteneurs graphiques imbriqués](using-nested-graphics-containers.md)  
 Montre comment utiliser des conteneurs pour contrôler l’état de la <xref:System.Drawing.Graphics> objet.
