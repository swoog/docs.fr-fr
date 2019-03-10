---
title: 'Procédure : Construire des familles de polices et des polices'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- font families [Windows Forms], constructing
- fonts [Windows Forms], constructing
ms.assetid: d3a4a223-9492-4b54-9afd-db1c31c3cefd
ms.openlocfilehash: b651671e525ae5cfc365a392b96d258ac835a21c
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57708552"
---
# <a name="how-to-construct-font-families-and-fonts"></a><span data-ttu-id="eb623-102">Procédure : Construire des familles de polices et des polices</span><span class="sxs-lookup"><span data-stu-id="eb623-102">How to: Construct Font Families and Fonts</span></span>
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] <span data-ttu-id="eb623-103">regroupe les polices avec le même type de caractère, mais des styles différents dans des familles de polices.</span><span class="sxs-lookup"><span data-stu-id="eb623-103">groups fonts with the same typeface but different styles into font families.</span></span> <span data-ttu-id="eb623-104">Par exemple, la famille de polices Arial contient les polices suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb623-104">For example, the Arial font family contains the following fonts:</span></span>  
  
-   <span data-ttu-id="eb623-105">Arial normal</span><span class="sxs-lookup"><span data-stu-id="eb623-105">Arial Regular</span></span>  
  
-   <span data-ttu-id="eb623-106">Arial gras</span><span class="sxs-lookup"><span data-stu-id="eb623-106">Arial Bold</span></span>  
  
-   <span data-ttu-id="eb623-107">Arial italique</span><span class="sxs-lookup"><span data-stu-id="eb623-107">Arial Italic</span></span>  
  
-   <span data-ttu-id="eb623-108">Arial gras italique</span><span class="sxs-lookup"><span data-stu-id="eb623-108">Arial Bold Italic</span></span>  
  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] <span data-ttu-id="eb623-109">utilise quatre styles pour former des familles : normal, gras, italique et gras italique.</span><span class="sxs-lookup"><span data-stu-id="eb623-109">uses four styles to form families: regular, bold, italic, and bold italic.</span></span> <span data-ttu-id="eb623-110">Adjectifs comme *affiner* et *arrondi* ne sont pas considérés comme des styles ; au lieu de cela ils font partie du nom de famille.</span><span class="sxs-lookup"><span data-stu-id="eb623-110">Adjectives such as *narrow* and *rounded* are not considered styles; rather they are part of the family name.</span></span> <span data-ttu-id="eb623-111">Par exemple, Arial Narrow est une famille de polices avec les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eb623-111">For example, Arial Narrow is a font family with the following members:</span></span>  
  
-   <span data-ttu-id="eb623-112">Arial Regular étroit</span><span class="sxs-lookup"><span data-stu-id="eb623-112">Arial Narrow Regular</span></span>  
  
-   <span data-ttu-id="eb623-113">Arial Condensé en gras</span><span class="sxs-lookup"><span data-stu-id="eb623-113">Arial Narrow Bold</span></span>  
  
-   <span data-ttu-id="eb623-114">Arial italique étroit</span><span class="sxs-lookup"><span data-stu-id="eb623-114">Arial Narrow Italic</span></span>  
  
-   <span data-ttu-id="eb623-115">Arial gras italique étroit</span><span class="sxs-lookup"><span data-stu-id="eb623-115">Arial Narrow Bold Italic</span></span>  
  
 <span data-ttu-id="eb623-116">Vous pouvez dessiner du texte avec [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], vous devez construire un <xref:System.Drawing.FontFamily> objet et un <xref:System.Drawing.Font> objet.</span><span class="sxs-lookup"><span data-stu-id="eb623-116">Before you can draw text with [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], you need to construct a <xref:System.Drawing.FontFamily> object and a <xref:System.Drawing.Font> object.</span></span> <span data-ttu-id="eb623-117">Le <xref:System.Drawing.FontFamily> objet spécifie le type de caractères (par exemple, Arial) et le <xref:System.Drawing.Font> objet spécifie la taille, style et les unités.</span><span class="sxs-lookup"><span data-stu-id="eb623-117">The <xref:System.Drawing.FontFamily> object specifies the typeface (for example, Arial), and the <xref:System.Drawing.Font> object specifies the size, style, and units.</span></span>  
  
## <a name="example"></a><span data-ttu-id="eb623-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb623-118">Example</span></span>  
 <span data-ttu-id="eb623-119">L’exemple suivant construit un style régulière police Arial, avec une taille de 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="eb623-119">The following example constructs a regular style Arial font with a size of 16 pixels.</span></span> <span data-ttu-id="eb623-120">Dans le code suivant, le premier argument passé à la <xref:System.Drawing.Font.%23ctor%2A> constructeur est le <xref:System.Drawing.FontFamily> objet.</span><span class="sxs-lookup"><span data-stu-id="eb623-120">In the following code, the first argument passed to the <xref:System.Drawing.Font.%23ctor%2A> constructor is the <xref:System.Drawing.FontFamily> object.</span></span> <span data-ttu-id="eb623-121">Le deuxième argument spécifie la taille de la police mesurée en unités identifiées par le quatrième argument.</span><span class="sxs-lookup"><span data-stu-id="eb623-121">The second argument specifies the size of the font measured in units identified by the fourth argument.</span></span> <span data-ttu-id="eb623-122">Le troisième argument identifie le style.</span><span class="sxs-lookup"><span data-stu-id="eb623-122">The third argument identifies the style.</span></span>  
  
 <span data-ttu-id="eb623-123"><xref:System.Drawing.GraphicsUnit.Pixel> est un membre de la <xref:System.Drawing.GraphicsUnit> énumération, et <xref:System.Drawing.FontStyle.Regular> est un membre de la <xref:System.Drawing.FontStyle> énumération.</span><span class="sxs-lookup"><span data-stu-id="eb623-123"><xref:System.Drawing.GraphicsUnit.Pixel> is a member of the <xref:System.Drawing.GraphicsUnit> enumeration, and <xref:System.Drawing.FontStyle.Regular> is a member of the <xref:System.Drawing.FontStyle> enumeration.</span></span>  
  
 [!code-csharp[System.Drawing.FontsAndText#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.FontsAndText#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="eb623-124">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="eb623-124">Compiling the Code</span></span>  
 <span data-ttu-id="eb623-125">L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="eb623-125">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb623-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb623-126">See also</span></span>
- [<span data-ttu-id="eb623-127">Utilisation de polices et de texte</span><span class="sxs-lookup"><span data-stu-id="eb623-127">Using Fonts and Text</span></span>](using-fonts-and-text.md)
- [<span data-ttu-id="eb623-128">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb623-128">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
