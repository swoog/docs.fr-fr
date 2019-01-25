---
title: Dépannage des problèmes liés au contrôle DataRepeater (Visual Studio)
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, troubleshooting
ms.assetid: c0ab9469-eced-4f52-aa18-4bd8dd4f1a9a
ms.openlocfilehash: 7b045e1c45221cbde82c88286da8e698a763d844
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54580601"
---
# <a name="troubleshooting-the-datarepeater-control-visual-studio"></a>Dépannage des problèmes liés au contrôle DataRepeater (Visual Studio)
Cette rubrique répertorie les problèmes courants qui peuvent se produire lorsque vous travaillez avec le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle.  
  
## <a name="datarepeater-keyboard-and-mouse-events-are-not-raised"></a>DataRepeater clavier et les événements de souris ne sont pas déclenchés.  
 Certains <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> des événements de contrôle, tels que des événements de clavier et de la souris, ne sont pas déclenchés. Ceci est normal. Le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle lui-même est un conteneur pour <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem> objets et n’est pas accessible au moment de l’exécution. Le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem> n’expose pas les événements au moment du design. Par conséquent, en cliquant sur un élément ou en appuyant sur une touche lorsque l’élément a le focus ne déclenche pas d’événement.  
  
 L’exception à cette règle est lorsque le <xref:System.Windows.Forms.Control.Padding%2A> propriété est définie sur une grande valeur suffisante pour exposer les bords de la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle. Dans ce cas, en cliquant dans la marge exposée déclenche des événements de souris.  
  
 Pour résoudre ce problème, ajoutez un <xref:System.Windows.Forms.Panel> le contrôle à la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> section de la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôler, puis ajoutez le reste des contrôles à la <xref:System.Windows.Forms.Panel>. Vous pouvez ensuite ajouter le code pour le <xref:System.Windows.Forms.Panel> gestionnaires d’événements pour les événements de clavier et souris.  
  
## <a name="the-datarepeater-is-partially-hidden-behind-the-binding-navigator"></a>Le contrôle DataRepeater est partiellement masqué derrière le navigateur de liaisons  
 Lorsque vous ajoutez un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> le contrôle à un formulaire, puis ajoutez les contrôles liés aux données à partir de la **des Sources de données** fenêtre, le <xref:System.Windows.Forms.BindingNavigator> contrôle peut apparaître en haut de la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle. Il s’agit d’une limitation connue de la **des Sources de données** fenêtre et est cohérent avec le comportement d’autres contrôles, tels que le <xref:System.Windows.Forms.DataGridView> contrôle.  
  
 Vous pouvez déplacer le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> inférieure à la <xref:System.Windows.Forms.BindingNavigator> contrôle au moment du design, ou ajouter du code qui ressemble à ce qui suit dans le `Load` Gestionnaire d’événements.  
  
```vb  
DataRepeater1.Top = ProductsBindingNavigator.Height  
```  
  
```csharp  
dataRepeater1.Top = productsBindingNavigator.Height;  
```  
  
## <a name="controls-are-not-displayed-correctly-at-run-time"></a>Les contrôles ne sont pas affichés correctement au moment de l’exécution  
 Certains contrôles dans un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle ne s’affichent pas comme prévu au moment de l’exécution. Le processus utilisé pour cloner des contrôles à partir de la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> à la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem> ne peut pas toujours déterminer toutes les propriétés de tous les contrôles. Par exemple, si vous ajoutez un indépendant <xref:System.Windows.Forms.ListBox> le contrôle à un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle au moment du design et de remplir son <xref:System.Windows.Forms.ListBox.Items%2A> collection avec une liste de chaînes, la <xref:System.Windows.Forms.ListBox> sera vide au moment de l’exécution. Il s’agit, car le processus de clonage ne peut pas prendre en compte la <xref:System.Windows.Forms.ListBox.Items%2A> propriété.  
  
 Vous pouvez corriger les problèmes tels que cela en restaurant les propriétés manquantes dans le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemCloned> événement qui se produit après que le clonage par défaut est terminé. L’exemple suivant montre comment réparer le <xref:System.Windows.Forms.ListBox.Items%2A> collection d’un <xref:System.Windows.Forms.ListBox> dans contrôler le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemCloned> Gestionnaire d’événements.  
  
 [!code-csharp[VbPowerPacksDataRepeaterItemCloned#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/troubleshooting-the-datarepeater-control-visual-studio_1.cs)]
 [!code-vb[VbPowerPacksDataRepeaterItemCloned#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/troubleshooting-the-datarepeater-control-visual-studio_1.vb)]  
  
## <a name="the-selection-symbol-on-the-item-header-is-missing"></a>Le symbole de sélection sur l’en-tête d’élément est manquant  
 Lorsque vous modifiez le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor%2A> propriété de l’en-tête d’élément dans un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle, certains choix de couleurs peut provoquer la disparition du symbole de sélection. Modification de la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize%2A> propriété peut également provoquer la disparition du symbole de sélection.  
  
 Impossible de modifier la couleur et la taille du symbole de sélection.  
  
-   Si vous définissez la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor%2A> à <xref:System.Drawing.Color.White%2A>, le symbole de sélection ne seront pas visible quand un élément est sélectionné en premier.  
  
-   Si vous définissez la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor%2A> à <xref:System.Drawing.Color.Black%2A>, le symbole de sélection ne seront pas visible quand un contrôle est sélectionné, et le symbole crayon ne seront pas visible lorsqu’un contrôle est en mode édition.  
  
-   Si le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize%2A> propriété est définie sur une valeur inférieure à 11, les symboles d’indicateur dans l’en-tête d’élément s’affichera pas.  
  
 Vous pouvez fournir votre propre symbole en-tête et la sélection d’élément à l’aide un <xref:System.Windows.Forms.PictureBox> contrôle et surveillance le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem.IsCurrent%2A> propriété de la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem> dans le <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem> événements de la <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> contrôle. Pour plus d'informations, consultez <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem.IsCurrent%2A>.  
  
## <a name="see-also"></a>Voir aussi
- [Introduction au contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [Guide pratique pour Afficher des données liées dans un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-display-bound-data-in-a-datarepeater-control-visual-studio.md)
- [Guide pratique pour Afficher les contrôles indépendants dans un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)
- [Guide pratique pour Modifier la disposition d’un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-layout-of-a-datarepeater-control-visual-studio.md)
- [Guide pratique pour Modifier l’apparence d’un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
- [Guide pratique pour Afficher les en-têtes d’élément dans un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-display-item-headers-in-a-datarepeater-control-visual-studio.md)
- [Guide pratique pour Désactiver l’ajout et suppression d’éléments du contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio.md)
- [Guide pratique pour Rechercher des données dans un contrôle DataRepeater](../../../visual-basic/developing-apps/windows-forms/how-to-search-data-in-a-datarepeater-control-visual-studio.md)
- [Guide pratique pour Créer un formulaire maître/détail en utilisant deux contrôles DataRepeater (Visual Studio)](../../../visual-basic/developing-apps/windows-forms/how-to-create-a-master-detail-form-by-using-two-datarepeater-controls.md)
