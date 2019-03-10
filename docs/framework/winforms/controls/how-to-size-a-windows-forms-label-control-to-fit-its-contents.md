---
title: 'Procédure : Taille d’un contrôle d’étiquette Windows Forms pour s’ajuster à son contenu'
ms.date: 03/30/2017
helpviewer_keywords:
- captions [Windows Forms], sizing
- sizing controls
- size [Windows Forms], controls
- labels [Windows Forms], sizing to fit contents
- Label control [Windows Forms], sizing to fit contents
ms.assetid: 99648964-63b2-438c-980e-d24103ad602b
ms.openlocfilehash: 5771b232d77e3e5a792b179ebffd3fa0edda7c9b
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57702192"
---
# <a name="how-to-size-a-windows-forms-label-control-to-fit-its-contents"></a>Procédure : Taille d’un contrôle d’étiquette Windows Forms pour s’ajuster à son contenu
Les formulaires Windows <xref:System.Windows.Forms.Label> contrôle peut être une ou plusieurs lignes, et il peut être soit de taille fixe ou que vous pouvez redimensionner automatiquement pour prendre en charge sa légende. Le <xref:System.Windows.Forms.Label.AutoSize%2A> propriété vous permet de dimensionner les contrôles pour s’ajuster à la taille des légendes, ce qui est particulièrement utile si la changer au moment de l’exécution.  
  
### <a name="to-make-a-label-control-resize-dynamically-to-fit-its-contents"></a>Pour rendre un contrôle label redimensionné dynamiquement pour s’ajuster à son contenu  
  
1.  Définissez ses <xref:System.Windows.Forms.Label.AutoSize%2A> propriété `true`.  
  
 Si <xref:System.Windows.Forms.Label.AutoSize%2A> a la valeur `false`, les mots spécifiés dans le <xref:System.Windows.Forms.Label.Text%2A> propriété passe à la ligne suivante si possible, mais le contrôle n’augmentera pas.  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Créer des clés d’accès avec les contrôles Label Windows Forms](how-to-create-access-keys-with-windows-forms-label-controls.md)
- [Vue d'ensemble du contrôle Label](label-control-overview-windows-forms.md)
- [Label, contrôle](label-control-windows-forms.md)
