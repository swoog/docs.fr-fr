---
title: 'Procédure : dimensionner un contrôle Label Windows Forms pour qu’il s’ajuste à son contenu'
ms.date: 03/30/2017
helpviewer_keywords:
- captions [Windows Forms], sizing
- sizing controls
- size [Windows Forms], controls
- labels [Windows Forms], sizing to fit contents
- Label control [Windows Forms], sizing to fit contents
ms.assetid: 99648964-63b2-438c-980e-d24103ad602b
ms.openlocfilehash: 110aab0c0826bb4b06e22158afd6af37b5406be4
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59312187"
---
# <a name="how-to-size-a-windows-forms-label-control-to-fit-its-contents"></a>Procédure : dimensionner un contrôle Label Windows Forms pour qu’il s’ajuste à son contenu
Les formulaires Windows <xref:System.Windows.Forms.Label> contrôle peut être une ou plusieurs lignes, et il peut être soit de taille fixe ou que vous pouvez redimensionner automatiquement pour prendre en charge sa légende. Le <xref:System.Windows.Forms.Label.AutoSize%2A> propriété vous permet de dimensionner les contrôles pour s’ajuster à la taille des légendes, ce qui est particulièrement utile si la changer au moment de l’exécution.  
  
### <a name="to-make-a-label-control-resize-dynamically-to-fit-its-contents"></a>Pour rendre un contrôle label redimensionné dynamiquement pour s’ajuster à son contenu  
  
1. Définissez ses <xref:System.Windows.Forms.Label.AutoSize%2A> propriété `true`.  
  
 Si <xref:System.Windows.Forms.Label.AutoSize%2A> a la valeur `false`, les mots spécifiés dans le <xref:System.Windows.Forms.Label.Text%2A> propriété passe à la ligne suivante si possible, mais le contrôle n’augmentera pas.  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : créer des clés d’accès avec les contrôles Label Windows Forms](how-to-create-access-keys-with-windows-forms-label-controls.md)
- [Vue d’ensemble du contrôle Label](label-control-overview-windows-forms.md)
- [Label, contrôle](label-control-windows-forms.md)
