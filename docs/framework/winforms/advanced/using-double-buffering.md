---
title: Utilisation de doubles tampons d'enregistrements
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], double buffering
- double buffering
- flicker [Windows Forms], reducing in Windows Forms
- buffering [Windows Forms], double buffering
ms.assetid: dc484e33-7101-4e4b-ada5-d3c96155fbcd
ms.openlocfilehash: ac6c9b7f2cc1fea86a75eaaf4a2dde1ea60e4f40
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777154"
---
# <a name="using-double-buffering"></a>Utilisation de doubles tampons d'enregistrements
Vous pouvez utiliser des graphiques de double tampon pour réduire le scintillement dans vos applications qui contiennent des opérations de dessin complexes. Le .NET Framework contient une prise en charge intégrée de double tampon, ou vous pouvez gérer et restituer manuellement des graphiques.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Graphiques mis deux fois en mémoire tampon](double-buffered-graphics.md)  
 Introduit la double mise en mémoire tampon concept et les contours .NET Framework prise en charge.  
  
 [Guide pratique pour Réduire le scintillement des graphiques avec Double mise en tampon pour les formulaires et contrôles](how-to-reduce-graphics-flicker-with-double-buffering-for-forms-and-controls.md)  
 Montre comment utiliser la double mise en mémoire tampon de prise en charge dans le .NET Framework de la valeur par défaut.  
  
 [Guide pratique pour Gérer manuellement des graphiques mis en mémoire tampon](how-to-manually-manage-buffered-graphics.md)  
 Montre comment gérer le mécanisme de double tampon dans les applications.  
  
 [Guide pratique pour Restituer manuellement des graphiques mis en mémoire tampon](how-to-manually-render-buffered-graphics.md)  
 Montre comment restituer des graphiques mis en mémoire tampon double.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.Control.SetStyle%2A> ,  
 Méthode de contrôle qui permet la double mise en tampon.  
  
 <xref:System.Drawing.BufferedGraphicsContext> ,  
 Fournit des méthodes pour créer des mémoires tampons de graphiques.  
  
 <xref:System.Drawing.BufferedGraphicsManager>  
 Fournit l’accès au contexte graphique mis en mémoire tampon pour un domaine d’application.
