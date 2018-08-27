---
title: 'Comment : afficher des données liées dans un contrôle DataRepeater (Visual Studio)'
ms.date: 07/20/2015
helpviewer_keywords:
- DataRepeater, data-binding
- DataRepeater, displaying bound controls
ms.assetid: 56a15326-1334-4275-af4e-075cad79e6f7
ms.openlocfilehash: b96fb33a0dcf80a86d1fcb6e219e5f35b1f7351c
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42933404"
---
# <a name="how-to-display-bound-data-in-a-datarepeater-control-visual-studio"></a>Comment : afficher des données liées dans un contrôle DataRepeater (Visual Studio)
L’utilisation la plus courante de la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle consiste à afficher des données liées à partir d’une base de données ou autre source de données.  
  
 En plus de contrôles dépendants, vous souhaiterez ajouter d’autres contrôles, comme une étiquette statique ou une image qui est répétée sur chaque élément dans le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle. Pour plus d’informations, consultez [Comment : afficher les contrôles indépendants dans un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md).  
  
 Vous pouvez également lier à une source de données en cours d’exécution en définissant le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A> propriété `True` et l’affectation d’une source de données pour le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DataSource%2A> propriété. Dans ce cas, vous devrez gérer toutes les interactions avec la source de données. Pour plus d’informations, consultez [Mode virtuel dans le contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/virtual-mode-in-the-datarepeater-control-visual-studio.md).  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-data-bound-datarepeater"></a>Pour créer un contrôle DataRepeater lié aux données  
  
1.  Faites glisser un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle depuis la **Visual Basic PowerPacks** onglet dans le **boîte à outils** à un contrôle de formulaire ou un conteneur.  
  
2.  Faites glisser les poignées de dimensionnement et de position pour dimensionner et positionner le contrôle.  
  
     Notez que le contrôle a les deux régions rectangulaires. Région du haut est la *modèle d’élément*; les contrôles ajoutés au modèle seront répétés dans chaque élément dans le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle au moment de l’exécution. La région inférieure est la *viewport*, où les éléments seront affichés.  
  
     Vous pouvez également dimensionner et positionner le contrôle ou le modèle d’élément en modifiant le **taille** et **Position** propriétés dans la fenêtre Propriétés.  
  
3.  Dans le menu **Données** , cliquez sur **Afficher les sources de données**.  
  
    > [!NOTE]
    >  Si le **des Sources de données** fenêtre est vide, ajoutez une source de données à ce dernier. Pour plus d’informations, consultez [Ajouter de nouvelles sources de données](/visualstudio/data-tools/add-new-data-sources).  
  
4.  Dans le **des Sources de données** fenêtre, sélectionnez le nœud de niveau supérieur pour la table qui contient les données que vous voulez lier.  
  
5.  Modifier le type de déplacement de la table à `Details` en cliquant sur `Details` dans la liste déroulante sur le nœud de la table.  
  
6.  Sélectionnez le nœud de la table et faites-le glisser vers la région du modèle d’élément de la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle.  
  
     Vous pouvez spécifier des types de contrôles sont affichés pour chaque champ. Pour plus d’informations, consultez [définir le contrôle à créer lors du déplacement de la fenêtre Sources de données](/visualstudio/data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>  
 [Introduction au contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)  
 [Guide pratique : afficher les contrôles indépendants dans un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)  
 [Comment : créer un formulaire maître/détail en utilisant deux contrôles DataRepeater (Visual Studio)](../../../visual-basic/developing-apps/windows-forms/how-to-create-a-master-detail-form-by-using-two-datarepeater-controls.md)  
 [Guide pratique : modifier l’apparence d’un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)  
 [Dépannage des problèmes liés au contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
