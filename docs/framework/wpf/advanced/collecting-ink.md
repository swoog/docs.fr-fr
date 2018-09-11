---
title: Collecter l’encre dans les applications WPF
ms.date: 08/15/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ink [WPF], collecting
- InkCanvas element [WPF]
- properties [WPF], DrawingAttributes
- collecting digital ink [WPF]
- digital ink [WPF], collecting
- properties [WPF], DefaultDrawingAttributes
- DefaultDrawingAttributes property [WPF]
ms.assetid: 66a3129d-9577-43eb-acbd-56c147282016
ms.openlocfilehash: 25f9c0141a97d8e52e0883b14fd3e1f4574a05ea
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2018
ms.locfileid: "44360685"
---
# <a name="collect-ink"></a>Collecter l’encre

La collecte d’encre numérique fait partie des principales fonctionnalités de la plateforme [Windows Presentation Foundation](../../../../docs/framework/wpf/index.md). Cette rubrique décrit les méthodes de collecte d’encre dans Windows Presentation Foundation (WPF).

## <a name="prerequisites"></a>Prérequis

Pour utiliser les exemples suivants, vous devez d’abord installer Visual Studio et le [!INCLUDE[TLA2#tla_winfxsdk](../../../../includes/tla2sharptla-winfxsdk-md.md)]. Vous devez également comprendre comment écrire des applications pour le WPF. Pour plus d’informations sur la mise en route avec WPF, consultez [procédure pas à pas : Ma première application de bureau WPF](../../../../docs/framework/wpf/getting-started/walkthrough-my-first-wpf-desktop-application.md).

## <a name="use-the-inkcanvas-element"></a>Utilisez l’élément InkCanvas

Le <xref:System.Windows.Controls.InkCanvas?displayProperty=fullName> élément fournit le moyen le plus simple pour collecter l’encre dans WPF. Utilisez un <xref:System.Windows.Controls.InkCanvas> élément pour recevoir et afficher l’entrée d’encre. Généralement, vous entrez de l’encre à l’aide d’un stylet qui interagit avec un digitaliseur pour produire des traits d’encre. En outre, vous pouvez utiliser une souris à la place du stylet. Les traits créés sont représentés en tant que <xref:System.Windows.Ink.Stroke> objets et ils peuvent être manipulés par programme et par l’utilisateur d’entrée. Le <xref:System.Windows.Controls.InkCanvas> permet aux utilisateurs de sélectionner, modifier ou supprimer une existante <xref:System.Windows.Ink.Stroke>.

À l’aide de XAML, vous pouvez définir la collecte d’encre aussi facilement que l’ajout d’un **InkCanvas** élément à votre arborescence. L’exemple suivant ajoute un <xref:System.Windows.Controls.InkCanvas> à un projet WPF par défaut créé dans Visual Studio :

[!code-xaml[DigitalInkTopics#6](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml#6)]

Le **InkCanvas** élément peut également contenir des éléments enfants, ce qui permet d’ajouter des fonctions d’annotation manuscrite à quasiment tout type d’élément XAML. Par exemple, pour ajouter des fonctions d’encrage à un élément de texte, définissez-le simplement qu’un enfant d’un <xref:System.Windows.Controls.InkCanvas>:

[!code-xaml[DigitalInkTopics#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml#5)]

Ajout de prise en charge pour baliser une image avec l’encre est tout aussi simple :

[!code-xaml[DigitalInkTopics#7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml#7)]

### <a name="inkcollection-modes"></a>Modes InkCollection

Le <xref:System.Windows.Controls.InkCanvas> prend en charge de différents modes d’entrée via son <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> propriété.

### <a name="manipulate-ink"></a>Manipuler l’encre

Le <xref:System.Windows.Controls.InkCanvas> prend en charge de nombreuses opérations de modification de l’encre. Par exemple, <xref:System.Windows.Controls.InkCanvas> prend en charge back-la gomme du stylet, et aucun code supplémentaire n’est nécessaire pour ajouter les fonctionnalités à l’élément.

#### <a name="selection"></a>Sélection

Définition du mode de sélection est aussi simple que le paramètre le <xref:System.Windows.Controls.InkCanvasEditingMode> propriété **sélectionnez**.

Le code suivant définit le mode d’édition basé sur la valeur d’un <xref:System.Windows.Forms.CheckBox>:

[!code-csharp[DigitalInkTopics#8](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window1.xaml.cs#8)]
[!code-vb[DigitalInkTopics#8](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window1.xaml.vb#8)]

#### <a name="drawingattributes"></a>DrawingAttributes

Utilisez le <xref:System.Windows.Ink.Stroke.DrawingAttributes%2A> propriété à modifier l’apparence des traits d’encre. Par exemple, le <xref:System.Windows.Ink.DrawingAttributes.Color%2A> membre <xref:System.Windows.Ink.DrawingAttributes> définit la couleur rendue <xref:System.Windows.Ink.Stroke>.

L’exemple suivant modifie la couleur des traits sélectionnés en rouge :

[!code-csharp[DigitalInkTopics#9](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window1.xaml.cs#9)]
[!code-vb[DigitalInkTopics#9](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window1.xaml.vb#9)]

### <a name="defaultdrawingattributes"></a>DefaultDrawingAttributes

Le <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> propriété fournit l’accès aux propriétés telles que la hauteur, la largeur et la couleur des traits à créer dans un <xref:System.Windows.Controls.InkCanvas>. Une fois que vous modifiez le <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A>, tous les futurs traits entrés dans le <xref:System.Windows.Controls.InkCanvas> sont restitués avec les nouvelles valeurs de propriété.

En plus de modifier le <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> dans le fichier code-behind, vous pouvez utiliser la syntaxe XAML pour la spécification <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> propriétés.

L’exemple suivant montre comment définir le <xref:System.Windows.Ink.DrawingAttributes.Color%2A> propriété. Pour utiliser ce code, créez un projet WPF intitulé « HelloInkCanvas » dans Visual Studio. Remplacez le code dans le *MainWindow.xaml* fichier par le code suivant :

[!code-xaml[HelloInkCanvas#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HelloInkCanvas/CSharp/Window1.xaml#1)]

Ensuite, ajoutez les gestionnaires d’événements de bouton suivant pour le fichier code-behind, à l’intérieur de la classe MainWindow :

[!code-csharp[HelloInkCanvas#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HelloInkCanvas/CSharp/Window1.xaml.cs#2)]

Après avoir copié ce code, appuyez sur **F5** dans Visual Studio pour exécuter le programme dans le débogueur.

Notez comment la <xref:System.Windows.Controls.StackPanel> place les boutons en haut de la <xref:System.Windows.Controls.InkCanvas>. Si vous tentez de l’encre en haut des boutons, le <xref:System.Windows.Controls.InkCanvas> collecte et restitue l’encre derrière les boutons. Il s’agit, car les boutons sont des frères du <xref:System.Windows.Controls.InkCanvas> par opposition aux enfants. De même, les boutons sont plus haut dans l’ordre de plan ; l’encre est donc restituée derrière eux.

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Ink.DrawingAttributes>
- <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A>
- <xref:System.Windows.Ink>