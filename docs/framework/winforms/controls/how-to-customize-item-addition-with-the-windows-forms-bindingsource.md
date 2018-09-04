---
title: "Comment : personnaliser l'ajout d'éléments avec le composant BindingSource Windows Forms"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [Windows Forms], creating new items
- BindingSource component [Windows Forms], customizing item addition with
- examples [Windows Forms], BindingSource component
- BindingSource component [Windows Forms], examples
ms.assetid: 1aae11fc-6fb2-4cb9-b3d0-e0638fe77ef0
ms.openlocfilehash: f8956ceb8da2aa14aea8b7e62b9d60ab656a3891
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43529426"
---
# <a name="how-to-customize-item-addition-with-the-windows-forms-bindingsource"></a>Comment : personnaliser l'ajout d'éléments avec le composant BindingSource Windows Forms
Quand vous utilisez un composant <xref:System.Windows.Forms.BindingSource> pour lier un contrôle Windows Forms à une source de données, vous pouvez être contraint de personnaliser la création de nouveaux éléments. Le composant <xref:System.Windows.Forms.BindingSource> simplifie cette personnalisation en fournissant l'événement <xref:System.Windows.Forms.BindingSource.AddingNew> , qui est généralement déclenché quand le contrôle lié doit créer un élément. Votre gestionnaire d'événements peut fournir tout comportement personnalisé nécessaire (par exemple, appeler une méthode sur un service web ou obtenir un nouvel objet à partir d'une fabrique de classe).  
  
> [!NOTE]
>  Quand un élément est ajouté en gérant l'événement <xref:System.Windows.Forms.BindingSource.AddingNew> , cet ajout ne peut pas être annulé.  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre comment lier un contrôle <xref:System.Windows.Forms.DataGridView> à une fabrique de classe à l'aide d'un composant <xref:System.Windows.Forms.BindingSource> . Quand l'utilisateur clique sur la nouvelle ligne du contrôle <xref:System.Windows.Forms.DataGridView> , l'événement <xref:System.Windows.Forms.BindingSource.AddingNew> est déclenché. Le gestionnaire d'événements crée un objet `DemoCustomer`, qui est affecté à la propriété <xref:System.ComponentModel.AddingNewEventArgs.NewObject%2A?displayProperty=nameWithType>. Cela provoque l'ajout du nouvel objet `DemoCustomer` à la liste du composant <xref:System.Windows.Forms.BindingSource> et son affichage sur la nouvelle ligne du contrôle <xref:System.Windows.Forms.DataGridView> .  
  
 [!code-cpp[System.Windows.Forms.DataConnector.AddingNew#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.AddingNew/CPP/form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.DataConnector.AddingNew#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.AddingNew/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnector.AddingNew#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.AddingNew/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Consultez également [Guide pratique pour compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.BindingNavigator>  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.BindingSource>  
 [BindingSource, composant](../../../../docs/framework/winforms/controls/bindingsource-component.md)  
 [Comment : lier un contrôle Windows Forms à un type](../../../../docs/framework/winforms/controls/how-to-bind-a-windows-forms-control-to-a-type.md)
