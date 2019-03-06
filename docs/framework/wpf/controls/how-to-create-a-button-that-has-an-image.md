---
title: 'Procédure : Créer un bouton comportant une image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Button controls [WPF], creating
ms.assetid: 607a193c-4098-4dd8-8dc0-51256cec2020
ms.openlocfilehash: fe9f35a6f83c5a839823d94c4d3c55e01b192fb1
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57352033"
---
# <a name="how-to-create-a-button-that-has-an-image"></a><span data-ttu-id="e69dc-102">Procédure : Créer un bouton comportant une image</span><span class="sxs-lookup"><span data-stu-id="e69dc-102">How to: Create a Button That Has an Image</span></span>
<span data-ttu-id="e69dc-103">Cet exemple montre comment inclure une image sur un <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="e69dc-103">This example shows how to include an image on a <xref:System.Windows.Controls.Button>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e69dc-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e69dc-104">Example</span></span>  
 <span data-ttu-id="e69dc-105">L’exemple suivant crée deux <xref:System.Windows.Controls.Button> contrôles.</span><span class="sxs-lookup"><span data-stu-id="e69dc-105">The following example creates two <xref:System.Windows.Controls.Button> controls.</span></span> <span data-ttu-id="e69dc-106">Un <xref:System.Windows.Controls.Button> contient du texte et l’autre contient une image.</span><span class="sxs-lookup"><span data-stu-id="e69dc-106">One <xref:System.Windows.Controls.Button> contains text and the other contains an image.</span></span> <span data-ttu-id="e69dc-107">L’image est dans un dossier appelé données, qui sont un sous-dossier du dossier du projet de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e69dc-107">The image is in a folder called data, which is a subfolder of the example’s project folder.</span></span> <span data-ttu-id="e69dc-108">Lorsqu’un utilisateur clique sur le <xref:System.Windows.Controls.Button> qui a l’image, l’arrière-plan et le texte de l’autre <xref:System.Windows.Controls.Button> modifier.</span><span class="sxs-lookup"><span data-stu-id="e69dc-108">When a user clicks the <xref:System.Windows.Controls.Button> that has the image, the background and the text of the other <xref:System.Windows.Controls.Button> change.</span></span>  
  
 <span data-ttu-id="e69dc-109">Cet exemple crée <xref:System.Windows.Controls.Button> contrôle à l’aide du balisage, mais utilise le code pour écrire la <xref:System.Windows.Controls.Primitives.ButtonBase.Click> gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="e69dc-109">This example creates <xref:System.Windows.Controls.Button> controls by using markup but uses code to write the <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event handlers.</span></span>  
  
 [!code-xaml[BtnColor#4](~/samples/snippets/csharp/VS_Snippets_Wpf/BtnColor/CSharp/Pane1.xaml#4)]  
  
 [!code-csharp[BtnColor#6](~/samples/snippets/csharp/VS_Snippets_Wpf/BtnColor/CSharp/Pane1.xaml.cs#6)]
 [!code-vb[BtnColor#6](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BtnColor/VisualBasic/Pane1.xaml.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="e69dc-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e69dc-110">See also</span></span>
- [<span data-ttu-id="e69dc-111">Contrôles</span><span class="sxs-lookup"><span data-stu-id="e69dc-111">Controls</span></span>](index.md)
- [<span data-ttu-id="e69dc-112">Bibliothèque de contrôles</span><span class="sxs-lookup"><span data-stu-id="e69dc-112">Control Library</span></span>](control-library.md)
