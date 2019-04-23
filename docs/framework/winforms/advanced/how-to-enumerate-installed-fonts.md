---
title: 'Procédure : énumérer les polices installées'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [Windows Forms], enumerating installed
- examples [Windows Forms], fonts
ms.assetid: 26d74ef5-0f39-4eeb-8d20-00e66e014abe
ms.openlocfilehash: 92f27399cce9e03a4679c8a34fbdafcf28c32252
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59155010"
---
# <a name="how-to-enumerate-installed-fonts"></a><span data-ttu-id="c2447-102">Procédure : énumérer les polices installées</span><span class="sxs-lookup"><span data-stu-id="c2447-102">How to: Enumerate Installed Fonts</span></span>
<span data-ttu-id="c2447-103">Le <xref:System.Drawing.Text.InstalledFontCollection> classe hérite de la <xref:System.Drawing.Text.FontCollection> classe de base abstraite.</span><span class="sxs-lookup"><span data-stu-id="c2447-103">The <xref:System.Drawing.Text.InstalledFontCollection> class inherits from the <xref:System.Drawing.Text.FontCollection> abstract base class.</span></span> <span data-ttu-id="c2447-104">Vous pouvez utiliser un <xref:System.Drawing.Text.InstalledFontCollection> objet à énumérer les polices installées sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2447-104">You can use an <xref:System.Drawing.Text.InstalledFontCollection> object to enumerate the fonts installed on the computer.</span></span> <span data-ttu-id="c2447-105">Le <xref:System.Drawing.Text.FontCollection.Families%2A> propriété d’un <xref:System.Drawing.Text.InstalledFontCollection> objet est un tableau de <xref:System.Drawing.FontFamily> objets.</span><span class="sxs-lookup"><span data-stu-id="c2447-105">The <xref:System.Drawing.Text.FontCollection.Families%2A> property of an <xref:System.Drawing.Text.InstalledFontCollection> object is an array of <xref:System.Drawing.FontFamily> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c2447-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="c2447-106">Example</span></span>  
 <span data-ttu-id="c2447-107">L’exemple suivant répertorie les noms de toutes les familles de polices installées sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2447-107">The following example lists the names of all the font families installed on the computer.</span></span> <span data-ttu-id="c2447-108">Le code récupère le <xref:System.Drawing.FontFamily.Name%2A> propriété de chaque <xref:System.Drawing.FontFamily> objet dans le tableau retourné par la <xref:System.Drawing.Text.FontCollection.Families%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c2447-108">The code retrieves the <xref:System.Drawing.FontFamily.Name%2A> property of each <xref:System.Drawing.FontFamily> object in the array returned by the <xref:System.Drawing.Text.FontCollection.Families%2A> property.</span></span> <span data-ttu-id="c2447-109">Comme les noms de famille sont récupérés, ils sont concaténés pour former une virgule liste.</span><span class="sxs-lookup"><span data-stu-id="c2447-109">As the family names are retrieved, they are concatenated to form a comma-separated list.</span></span> <span data-ttu-id="c2447-110">Le <xref:System.Drawing.Graphics.DrawString%2A> méthode de la <xref:System.Drawing.Graphics> classe dessine la liste séparée par des virgules dans un rectangle.</span><span class="sxs-lookup"><span data-stu-id="c2447-110">Then the <xref:System.Drawing.Graphics.DrawString%2A> method of the <xref:System.Drawing.Graphics> class draws the comma-separated list in a rectangle.</span></span>  
  
 <span data-ttu-id="c2447-111">Si vous exécutez l’exemple de code, la sortie sera similaire à celle illustrée dans l’illustration suivante :</span><span class="sxs-lookup"><span data-stu-id="c2447-111">If you run the example code, the output will be similar to that shown in the following illustration:</span></span>  
  
 ![Capture d’écran montrant les familles de polices installées.](./media/how-to-enumerate-installed-fonts/list-installed-font-families.png)  
  
 [!code-csharp[System.Drawing.FontsAndText#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.FontsAndText#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c2447-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="c2447-113">Compiling the Code</span></span>  
 <span data-ttu-id="c2447-114">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="c2447-114">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span> <span data-ttu-id="c2447-115">En outre, vous devez importer le <xref:System.Drawing.Text> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="c2447-115">In addition, you should import the <xref:System.Drawing.Text> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2447-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2447-116">See also</span></span>

- [<span data-ttu-id="c2447-117">Utilisation de polices et de texte</span><span class="sxs-lookup"><span data-stu-id="c2447-117">Using Fonts and Text</span></span>](using-fonts-and-text.md)
