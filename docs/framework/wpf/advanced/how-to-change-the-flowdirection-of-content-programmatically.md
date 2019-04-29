---
title: 'Procédure : Modifier la propriété FlowDirection d’un contenu par programmation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- FlowDirection property [WPF], changing programmatically
- documents [WPF], changing FlowDirection property programmatically
ms.assetid: 02f5a8ba-f8c0-4e5a-84b9-4c5bf12922a2
ms.openlocfilehash: ec159ed0efce8b5514788331e8715a55e7a8a638
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776556"
---
# <a name="how-to-change-the-flowdirection-of-content-programmatically"></a><span data-ttu-id="cfd55-102">Procédure : Modifier la propriété FlowDirection d’un contenu par programmation</span><span class="sxs-lookup"><span data-stu-id="cfd55-102">How to: Change the FlowDirection of Content Programmatically</span></span>
<span data-ttu-id="cfd55-103">Cet exemple montre comment changer par programmation le <xref:System.Windows.FrameworkElement.FlowDirection%2A> propriété d’un <xref:System.Windows.Controls.FlowDocumentReader>.</span><span class="sxs-lookup"><span data-stu-id="cfd55-103">This example shows how to programmatically change the <xref:System.Windows.FrameworkElement.FlowDirection%2A> property of a <xref:System.Windows.Controls.FlowDocumentReader>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cfd55-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="cfd55-104">Example</span></span>  
 <span data-ttu-id="cfd55-105">Deux <xref:System.Windows.Controls.Button> éléments sont créés, chacun représentant une des valeurs possibles de <xref:System.Windows.FlowDirection>.</span><span class="sxs-lookup"><span data-stu-id="cfd55-105">Two <xref:System.Windows.Controls.Button> elements are created, each representing one of the possible values of <xref:System.Windows.FlowDirection>.</span></span> <span data-ttu-id="cfd55-106">Lorsqu’un clic est effectué, la valeur de propriété associée est appliquée au contenu d’un <xref:System.Windows.Controls.FlowDocumentReader> nommé `tf1`.</span><span class="sxs-lookup"><span data-stu-id="cfd55-106">When a button is clicked, the associated property value is applied to the contents of a <xref:System.Windows.Controls.FlowDocumentReader> named `tf1`.</span></span>  <span data-ttu-id="cfd55-107">La valeur de propriété est également écrites dans un <xref:System.Windows.Controls.TextBlock> nommé `txt1`.</span><span class="sxs-lookup"><span data-stu-id="cfd55-107">The property value is also written to a <xref:System.Windows.Controls.TextBlock> named `txt1`.</span></span>  
  
 [!code-xaml[FlowDirectionSnippets#_FlowDirectionXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDirectionSnippets/CSharp/Window1.xaml#_flowdirectionxaml)]  
  
## <a name="example"></a><span data-ttu-id="cfd55-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="cfd55-108">Example</span></span>  
 <span data-ttu-id="cfd55-109">Les événements associés aux clics de bouton définis ci-dessus sont gérées dans un C# fichier code-behind.</span><span class="sxs-lookup"><span data-stu-id="cfd55-109">The events associated with the button clicks defined above are handled in a C# code-behind file.</span></span>  
  
 [!code-csharp[FlowDirectionSnippets#_FlowDirection](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDirectionSnippets/CSharp/Window1.xaml.cs#_flowdirection)]
 [!code-vb[FlowDirectionSnippets#_FlowDirection](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDirectionSnippets/VisualBasic/Window1.xaml.vb#_flowdirection)]
