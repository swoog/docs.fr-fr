---
title: 'Procédure : Rechercher des données dans un contrôle DataRepeater (Visual Studio)'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, implementing search
- DataRepeater, searching data
ms.assetid: a8ab5d17-b94f-43c4-8dd7-d0450226d73f
ms.openlocfilehash: 514e72afc9570071f57e385574456ff7d716bad7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654384"
---
# <a name="how-to-search-data-in-a-datarepeater-control-visual-studio"></a>Procédure : Rechercher des données dans un contrôle DataRepeater (Visual Studio)
Lorsque vous utilisez un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle qui contient de nombreux enregistrements, vous souhaiterez peut-être permettre aux utilisateurs, recherchez un enregistrement spécifique. Au lieu de rechercher les données dans le contrôle lui-même, vous pouvez implémenter une recherche en interrogeant sous-jacent <xref:System.Windows.Forms.BindingSource>. Si l’élément est trouvé, vous pouvez ensuite utiliser le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CurrentItemIndex%2A> propriété pour sélectionner l’élément et de faire défiler dans la vue.  
  
### <a name="to-implement-search"></a>Pour implémenter la recherche  
  
1.  Faites glisser un contrôle <xref:System.Windows.Forms.TextBox> de la **Boîte à outils** vers le formulaire qui contient le contrôle <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> .  
  
2.  Dans la fenêtre Propriétés, attribuez à la propriété **Name** la valeur **SearchTextBox**.  
  
3.  Faites glisser un contrôle <xref:System.Windows.Forms.Button> de la **Boîte à outils** vers le formulaire qui contient le contrôle <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> .  
  
4.  Dans la fenêtre Propriétés, attribuez à la propriété **Name** la valeur **SearchButton**. Affectez à la propriété **Text** la valeur **Search**.  
  
5.  Double-cliquez sur le contrôle <xref:System.Windows.Forms.Button> pour ouvrir l’éditeur de code et ajoutez le code suivant au gestionnaire d’événements `SearchButton_Click` .  
  
     [!code-vb[VbPowerPacksDataRepeaterSearch#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-search-data-in-a-datarepeater-control-visual-studio_1.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterSearch#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-search-data-in-a-datarepeater-control-visual-studio_1.cs)]  
  
     Remplacez *ProductsBindingSource* par le nom de la <xref:System.Windows.Forms.BindingSource> pour votre <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>et remplacez *ProductID* avec le nom du champ que vous souhaitez rechercher.  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- [Introduction au contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [Dépannage des problèmes liés au contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [Guide pratique pour Modifier l’apparence d’un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
