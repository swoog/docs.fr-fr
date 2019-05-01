---
title: 'Procédure : Contrôler quand le texte TextBox met à jour la source'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- source updates [WPF], timing of
- data binding [WPF], timing of source updates
- timing of source updates [WPF]
ms.assetid: ffb7b96a-351d-4c68-81e7-054033781c64
ms.openlocfilehash: 5272a19f69b3caf80fd7d5187c9a6a386cd44621
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62051999"
---
# <a name="how-to-control-when-the-textbox-text-updates-the-source"></a>Procédure : Contrôler quand le texte TextBox met à jour la source
Cette rubrique explique comment utiliser le <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> propriété pour contrôler le minutage des mises à jour de la source de liaison. La rubrique utilise le <xref:System.Windows.Controls.TextBox> contrôle comme exemple.  
  
## <a name="example"></a>Exemple  
 L’élément de langage <xref:System.Windows.Controls.TextBox>.<xref:System.Windows.Controls.TextBox.Text%2A> propriété a une valeur par défaut <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> valeur <xref:System.Windows.Data.UpdateSourceTrigger.LostFocus>. Cela signifie que si une application a un <xref:System.Windows.Controls.TextBox> avec une limite de données <xref:System.Windows.Controls.TextBox>.<xref:System.Windows.Controls.TextBox.Text%2A> propriété, le texte que vous tapez dans la <xref:System.Windows.Controls.TextBox> ne met pas à jour la source jusqu'à ce que le <xref:System.Windows.Controls.TextBox> perd le focus (par exemple, lorsque vous cliquez en dehors de la <xref:System.Windows.Controls.TextBox>).  
  
 Si vous souhaitez que la source de mise à jour que vous tapez, définissez le <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> de la liaison à <xref:System.Windows.Data.UpdateSourceTrigger.PropertyChanged>. Dans l’exemple suivant, les lignes de code en surbrillance montrent que la `Text` propriétés des deux le <xref:System.Windows.Controls.TextBox> et <xref:System.Windows.Controls.TextBlock> sont liés à la même propriété source. Le <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> propriété de la <xref:System.Windows.Controls.TextBox> liaison est définie sur <xref:System.Windows.Data.UpdateSourceTrigger.PropertyChanged>.  
  
 [!code-xaml[SimpleBinding#USTHowTo](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleBinding/VisualBasic/Page1.xaml?highlight=33-39,41-42)]  
  
 Par conséquent, le <xref:System.Windows.Controls.TextBlock> affiche le même texte (car la source change) que l’utilisateur entre du texte dans le <xref:System.Windows.Controls.TextBox>, comme illustré par la capture d’écran suivante de l’exemple :  
  
 ![Capture d’écran de données simple liaison exemple](./media/databindingsimplebindingsample2.png "DataBindingSimpleBindingSample2")  
  
 Si vous avez une boîte de dialogue ou un formulaire modifiable par l’utilisateur et que vous souhaitez différer les mises à jour de la source jusqu'à ce que l’utilisateur a fini de modifier les champs et clique sur « OK », vous pouvez définir le <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> valeur de vos liaisons sur <xref:System.Windows.Data.UpdateSourceTrigger.Explicit>, comme dans l’exemple suivant :  
  
 [!code-xaml[UpdateSource#2](~/samples/snippets/csharp/VS_Snippets_Wpf/UpdateSource/CSharp/Window1.xaml#2)]  
  
 Lorsque vous définissez la <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> valeur <xref:System.Windows.Data.UpdateSourceTrigger.Explicit>, la valeur source change uniquement lorsque l’application appelle le <xref:System.Windows.Data.BindingExpression.UpdateSource%2A> (méthode). L’exemple suivant montre comment appeler <xref:System.Windows.Data.BindingExpression.UpdateSource%2A> pour `itemNameTextBox`:  
  
 [!code-csharp[UpdateSource#1](~/samples/snippets/csharp/VS_Snippets_Wpf/UpdateSource/CSharp/Window1.xaml.cs#1)]
 [!code-vb[UpdateSource#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/UpdateSource/VisualBasic/Window1.xaml.vb#1)]  
  
> [!NOTE]
>  Vous pouvez utiliser la même technique pour les propriétés d’autres contrôles, mais n’oubliez pas que la plupart des autres propriétés ont une valeur par défaut <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> valeur <xref:System.Windows.Data.UpdateSourceTrigger.PropertyChanged>. Pour plus d’informations, consultez le <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> page de propriétés.  
  
> [!NOTE]
>  Le <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> propriété porte sur la source des mises à jour et par conséquent concerne uniquement les <xref:System.Windows.Data.BindingMode.TwoWay> ou <xref:System.Windows.Data.BindingMode.OneWayToSource> liaisons. Pour <xref:System.Windows.Data.BindingMode.TwoWay> et <xref:System.Windows.Data.BindingMode.OneWayToSource> liaisons fonctionne, l’objet source doit fournir des notifications de modification de propriété. Vous pouvez consulter les exemples figurant dans cette rubrique pour plus d’informations. Vous pouvez également consulter la page [Implémenter la notification des modifications de propriétés](how-to-implement-property-change-notification.md).  
  
## <a name="see-also"></a>Voir aussi

- [Rubriques de guide pratique](data-binding-how-to-topics.md)
