---
title: "Comment : lier un contrôle Windows Forms à un type à l'aide du concepteur"
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], binding to a type
- BindingSource component [Windows Forms], binding to a type
- types [Windows Forms], binding controls to
ms.assetid: 5ab984b5-c2d0-4638-a572-1c84013e8746
ms.openlocfilehash: 33df9e050dd8c2b3ace8ff89cbd5939b538fcd95
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44098340"
---
# <a name="how-to-bind-a-windows-forms-control-to-a-type-using-the-designer"></a>Comment : lier un contrôle Windows Forms à un type à l'aide du concepteur
Quand vous créez des contrôles qui interagissent avec des données, vous devez parfois lier un contrôle à un type plutôt qu’à un objet. Cette situation se présente surtout au moment du design, quand les données peuvent ne pas être disponibles mais que vos contrôles liés aux données ont tout de même besoin d’afficher des informations à partir de l’interface publique d’un type. Les procédures suivantes montrent comment créer un nouveau <xref:System.Windows.Forms.BindingSource> qui est lié à un type, puis comment lier une des propriétés du type pour le <xref:System.Windows.Forms.TextBox.Text%2A> propriété d’un <xref:System.Windows.Forms.TextBox>.  
  
### <a name="to-bind-the-bindingsource-to-a-type"></a>Pour lier le BindingSource à un type  
  
1.  Créez un projet Windows Forms (**fichier** > **New** > **projet** > **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).  
  
2.  Dans **conception** afficher, faites glisser un <xref:System.Windows.Forms.BindingSource> composant vers le formulaire.  
  
3.  Dans le **propriétés** fenêtre, cliquez sur la flèche pour la <xref:System.Windows.Forms.BindingSource.DataSource%2A> propriété.  
  
4.  Dans l’**éditeur de types d’interface utilisateur DataSource**, cliquez sur **Ajouter la source de données du projet**.  
  
5.  Sur la page **Choisir un type de source de données**, sélectionnez **Objet**, puis cliquez sur **Suivant**.  
  
6.  Sélectionnez le type à lier :  
  
    -   Si le type avec lequel vous souhaitez établir une liaison se trouve dans le projet actuel, ou si l’assembly qui contient ce type est déjà ajouté en tant que référence, développez les nœuds pour rechercher le type souhaité et sélectionnez-le.  
  
         - ou -  
  
    -   Si le type avec lequel vous souhaitez établir une liaison se trouve actuellement dans un autre assembly, et non dans la liste de références, cliquez sur **Ajouter une référence**, puis cliquez sur l’onglet **Projets**. Sélectionnez le projet contenant l’objet métier de votre choix, puis cliquez sur **OK**. Ce projet apparaît dans la liste des assemblys. Vous pouvez donc développer les nœuds pour rechercher le type que vous souhaitez, puis le sélectionner.  
  
        > [!NOTE]
        >  Pour effectuer une liaison avec un type présent dans une infrastructure ou un assembly Microsoft, décochez la case **Masquer les assemblys qui commencent par Microsoft ou System**.  
  
7.  Cliquez sur **Suivant**, puis sur **Terminer**.  
  
### <a name="to-bind-the-control-to-the-bindingsource"></a>Pour lier le contrôle au BindingSource  
  
1.  Ajoutez un <xref:System.Windows.Forms.TextBox> au formulaire.  
  
2.  Dans la fenêtre **Propriétés**, développez le nœud **(DataBindings)**.  
  
3.  Cliquez sur la flèche en regard du <xref:System.Windows.Forms.TextBox.Text%2A> propriété.  
  
4.  Dans le **éditeur de Type d’interface utilisateur DataSource**, développez le nœud pour le <xref:System.Windows.Forms.BindingSource> ajouté précédemment, puis sélectionnez la propriété du type lié que vous souhaitez lier à la <xref:System.Windows.Forms.TextBox.Text%2A> propriété de la <xref:System.Windows.Forms.TextBox>.  
  
## <a name="see-also"></a>Voir aussi  
 [BindingSource, composant](../../../../docs/framework/winforms/controls/bindingsource-component.md)  
 [Comment : lier un contrôle Windows Forms à un type](../../../../docs/framework/winforms/controls/how-to-bind-a-windows-forms-control-to-a-type.md)  
 [Lier des contrôles à des données dans Visual Studio](/visualstudio/data-tools/bind-controls-to-data-in-visual-studio)
