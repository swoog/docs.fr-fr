---
title: 'Comment : créer un formulaire maître / détail en utilisant deux contrôles DataRepeater (Visual Studio)'
ms.date: 07/20/2015
helpviewer_keywords:
- DataRepeater, master/detail tables
ms.assetid: eec43ae3-05d8-45a1-8d41-3803c6359dbe
ms.openlocfilehash: 84639a5d49a3fa4a8c6845793c39fc8a67c31e02
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-create-a-masterdetail-form-by-using-two-datarepeater-controls-visual-studio"></a>Comment : créer un formulaire maître/détail en utilisant deux contrôles DataRepeater (Visual Studio)
Vous pouvez afficher les données associées à l’aide de deux ou plusieurs <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôles pour créer un formulaire maître/détail. Par exemple, vous souhaiterez peut-être afficher une liste de clients dans un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>et lorsque l’utilisateur sélectionne un client, afficher la liste des commandes de ce client dans un deuxième <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>.  
  
 Vous pouvez afficher les données associées en faisant glisser des éléments de détail qui partagent le même nœud de la table principale à partir de la **des Sources de données** fenêtre sur un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle. Par exemple, si vous avez une source de données qui possède une table Customers et une table connexe Orders, vous voyez les deux tables en tant que nœuds de niveau supérieur dans l’arborescence de la **des Sources de données** fenêtre. Développez le nœud de clients afin que vous puissiez voir les colonnes. Notez que la dernière colonne dans la liste est un nœud extensible qui représente la table Orders. Ce nœud représente les commandes connexes d’un client.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-display-related-data-in-two-datarepeater-controls"></a>Pour afficher les données associées dans deux contrôles DataRepeater  
  
1.  Faites glisser deux <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> des contrôles de la **Visual Basic PowerPacks** onglet dans le **boîte à outils** à un contrôle de formulaire ou un conteneur.  
  
2.  Faites glisser les poignées de dimensionnement et de déplacement pour redimensionner les contrôles et les positionner côte-à-côte.  
  
3.  Dans le menu **Données** , cliquez sur **Afficher les sources de données**.  
  
    > [!NOTE]
    >  Si le **des Sources de données** fenêtre est vide, ajoutez une source de données à ce dernier. Pour plus d’informations, consultez [Ajouter de nouvelles sources de données](/visualstudio/data-tools/add-new-data-sources).  
  
4.  Dans le **des Sources de données** fenêtre, sélectionnez le nœud de niveau supérieur pour la table principale.  
  
5.  Modifier le type de déplacement de la table principale vers les détails en cliquant sur **détails** dans la liste déroulante du nœud table.  
  
6.  Faites glisser le nœud de la table principale sur la région de modèle d’élément du premier <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle.  
  
7.  Développez le nœud de la table principale et sélectionnez le nœud secondaire de la table associée.  
  
8.  Modifier le type de déplacement de la table de détail détails en cliquant sur **détails** dans la liste déroulante du nœud table.  
  
9. Sélectionnez ce nœud table et faites-le glisser sur la région de modèle d’élément de la seconde <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>  
 [Introduction au contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)  
 [Guide pratique : afficher des données liées dans un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-display-bound-data-in-a-datarepeater-control-visual-studio.md)  
 [Guide pratique pour afficher des données connexes dans une application Windows Forms](/visualstudio/data-tools/bind-windows-forms-controls-to-data-in-visual-studio)  
 [Guide pratique : modifier l’apparence d’un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)  
 [Dépannage des problèmes liés au contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
