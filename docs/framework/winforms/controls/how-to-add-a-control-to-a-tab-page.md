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
ms.openlocfilehash: b42845ab996c0985fe6a48ac588e6d706905faac
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59195850"
---
# <a name="how-to-add-a-control-to-a-tab-page"></a>Procédure : ajouter un contrôle à un onglet
Vous pouvez utiliser les formulaires Windows <xref:System.Windows.Forms.TabControl> pour afficher d’autres contrôles dans une structure organisée. La procédure suivante montre comment ajouter un bouton pour le premier onglet. Pour plus d’informations sur l’ajout d’une icône dans la partie de l’étiquette d’une page d’onglet, consultez [Comment : Modifier l’apparence du contrôle TabControl Windows Forms](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md).  
  
### <a name="to-add-a-control-programmatically"></a>Pour ajouter un contrôle par programmation  
  
1.  Utilisez le <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> méthode de la collection retournée par la <xref:System.Windows.Forms.Control.Controls%2A> propriété du <xref:System.Windows.Forms.TabPage>:  
  
     [!code-cpp[TabPageControlCollectionHowToAdd#1](~/samples/snippets/cpp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cpp/add.cpp#1)]
     [!code-csharp[TabPageControlCollectionHowToAdd#1](~/samples/snippets/csharp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cs/add.cs#1)]
     [!code-vb[TabPageControlCollectionHowToAdd#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/vb/add.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [TabControl, contrôle](tabcontrol-control-windows-forms.md)
- [Vue d’ensemble du contrôle TabControl](tabcontrol-control-overview-windows-forms.md)
- [Procédure : modifier l’aspect du contrôle TabControl Windows Forms](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
- [Procédure : désactiver des onglets](how-to-disable-tab-pages.md)
- [Procédure : ajouter et supprimer des onglets avec le contrôle TabControl de Windows Forms](how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
