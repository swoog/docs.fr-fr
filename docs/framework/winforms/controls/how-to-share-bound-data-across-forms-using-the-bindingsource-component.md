---
title: 'Procédure : Partager des données liées entre des formulaires à l’aide du composant BindingSource'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- examples [Windows Forms], BindingSource component
- data binding [Windows Forms], sharing data across forms
- BindingSource component [Windows Forms], examples
- BindingSource [Windows Forms], using with multiple forms
ms.assetid: a1a49630-db9c-4485-b888-1f62a373a4f7
ms.openlocfilehash: 6bd2c0aca7e24ed903e31f1c27e7e173ade6086b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54619952"
---
# <a name="how-to-share-bound-data-across-forms-using-the-bindingsource-component"></a>Procédure : Partager des données liées entre des formulaires à l’aide du composant BindingSource
Vous pouvez facilement partager des données entre des formulaires à l'aide du composant <xref:System.Windows.Forms.BindingSource>. Par exemple, vous souhaiterez peut-être afficher un formulaire en lecture seule qui résume les données de la source de données et un autre formulaire modifiable qui contient des informations détaillées sur l'élément actuellement sélectionné dans la source de données. Cet exemple illustre ce scénario.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment partager un <xref:System.Windows.Forms.BindingSource> et ses données liées entre des formulaires. Dans cet exemple, le <xref:System.Windows.Forms.BindingSource> partagé est passé au constructeur du formulaire enfant. Le formulaire enfant permet à l'utilisateur de modifier les données de l'élément actuellement sélectionné dans le formulaire principal.  
  
> [!NOTE]
>  L’événement <xref:System.Windows.Forms.BindingSource.BindingComplete> pour le composant <xref:System.Windows.Forms.BindingSource> est géré dans l’exemple pour garantir que les deux formulaires restent synchronisés. Pour plus d’informations à ce sujet, consultez [Comment : S’assurer que plusieurs contrôles liés à la même Source de données restent synchronisés](../../../../docs/framework/winforms/multiple-controls-bound-to-data-source-synchronized.md).  
  
 [!code-csharp[System.Windows.Forms.BindingSourceMultipleForms#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleForms/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.BindingSourceMultipleForms#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleForms/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Windows.Forms, System.Drawing, System.Data et System.Xml.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Voir également [Guide pratique pour Compiler et exécuter un exemple de Code complet de Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi
- [BindingSource, composant](../../../../docs/framework/winforms/controls/bindingsource-component.md)
- [Liaison de données Windows Forms](../../../../docs/framework/winforms/windows-forms-data-binding.md)
- [Guide pratique pour Gérer les erreurs et Exceptions qui se produisent avec Databinding](../../../../docs/framework/winforms/controls/how-to-handle-errors-and-exceptions-that-occur-with-databinding.md)
