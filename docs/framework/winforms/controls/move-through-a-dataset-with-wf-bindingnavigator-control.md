---
title: 'Procédure : Parcourir un DataSet avec le contrôle BindingNavigator Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- datasets [Windows Forms], moving through
- BindingNavigator control [Windows Forms], moving through datasets
- examples [Windows Forms], BindingNavigator control
ms.assetid: 146d97be-3d97-400e-accb-860bbf47729d
ms.openlocfilehash: 62cc5598aae646c11c0e46276e2e3dca97edc335
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54717816"
---
# <a name="how-to-move-through-a-dataset-with-the-windows-forms-bindingnavigator-control"></a>Procédure : Parcourir un DataSet avec le contrôle BindingNavigator Windows Forms
Quand vous générez des applications pilotées par les données, vous devez souvent présenter des collections de données aux utilisateurs. Le contrôle <xref:System.Windows.Forms.BindingNavigator>, associé au composant <xref:System.Windows.Forms.BindingSource>, fournit une solution pratique et extensible pour parcourir une collection et afficher des éléments de façon séquentielle.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment utiliser un contrôle <xref:System.Windows.Forms.BindingNavigator> pour parcourir des données. Le jeu est contenu dans un <xref:System.Data.DataView>, qui est lié à un contrôle <xref:System.Windows.Forms.TextBox> avec un composant <xref:System.Windows.Forms.BindingSource>.  
  
> [!NOTE]
>  Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application. L'utilisation de l'authentification Windows (également appelée sécurité intégrée) offre un moyen plus sûr de contrôler l'accès à une base de données. Pour plus d’informations, consultez [Protection des informations de connexion](../../../../docs/framework/data/adonet/protecting-connection-information.md).  
  
 [!code-csharp[System.Windows.Forms.DataNavigator#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataNavigator/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataNavigator#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataNavigator/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Data, System.Drawing, System.Windows.Forms et System.Xml.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Voir également [Guide pratique pour Compiler et exécuter un exemple de Code complet de Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.BindingSource>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [BindingNavigator, contrôle](../../../../docs/framework/winforms/controls/bindingnavigator-control-windows-forms.md)
- [BindingSource, composant](../../../../docs/framework/winforms/controls/bindingsource-component.md)
- [Guide pratique pour Lier un contrôle de formulaires Windows à un Type](../../../../docs/framework/winforms/controls/how-to-bind-a-windows-forms-control-to-a-type.md)
