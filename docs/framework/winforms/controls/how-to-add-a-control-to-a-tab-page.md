---
title: 'Procédure : ajouter un contrôle à un onglet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TabPage control
- tab controls [Windows Forms], tab order
- tab pages [Windows Forms], adding controls
ms.assetid: b092532e-7346-469f-b9a1-897f9bea4fb7
ms.openlocfilehash: 9806583fda60f1cb8a5ef2d97f42eba158593f61
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59322717"
---
# <a name="how-to-add-a-control-to-a-tab-page"></a>Procédure : ajouter un contrôle à un onglet
Vous pouvez utiliser les formulaires Windows <xref:System.Windows.Forms.TabControl> pour afficher d’autres contrôles dans une structure organisée. La procédure suivante montre comment ajouter un bouton pour le premier onglet. Pour plus d’informations sur l’ajout d’une icône dans la partie de l’étiquette d’une page d’onglet, consultez [Comment : Modifier l’apparence du contrôle TabControl Windows Forms](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md).  
  
### <a name="to-add-a-control-programmatically"></a>Pour ajouter un contrôle par programmation  
  
1. Utilisez le <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> méthode de la collection retournée par la <xref:System.Windows.Forms.Control.Controls%2A> propriété du <xref:System.Windows.Forms.TabPage>:  
  
     [!code-cpp[TabPageControlCollectionHowToAdd#1](~/samples/snippets/cpp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cpp/add.cpp#1)]
     [!code-csharp[TabPageControlCollectionHowToAdd#1](~/samples/snippets/csharp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cs/add.cs#1)]
     [!code-vb[TabPageControlCollectionHowToAdd#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/vb/add.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [TabControl, contrôle](tabcontrol-control-windows-forms.md)
- [Vue d’ensemble du contrôle TabControl](tabcontrol-control-overview-windows-forms.md)
- [Guide pratique pour Modifier l’apparence du contrôle TabControl Windows Forms](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
- [Guide pratique pour Désactiver les Pages d’onglets](how-to-disable-tab-pages.md)
- [Guide pratique pour Ajouter et supprimer des onglets avec le contrôle TabControl de Windows Forms](how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
