---
title: 'Procédure : afficher un élément de style visuel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- visual themes [Windows Forms], applying to elements of Windows Forms applications
- professional appearance [Windows Forms], applying to elements of Windows Forms applications
- visual styles [Windows Forms], rendering Windows Forms controls
ms.assetid: a207781b-1baa-4ce9-b788-1e951bd4b5df
ms.openlocfilehash: 57c2bc5722f77338225d70b514345344211656dc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59312395"
---
# <a name="how-to-render-a-visual-style-element"></a><span data-ttu-id="3df57-102">Procédure : afficher un élément de style visuel</span><span class="sxs-lookup"><span data-stu-id="3df57-102">How to: Render a Visual Style Element</span></span>
<span data-ttu-id="3df57-103">Le <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> expose de l’espace de noms <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> objets qui représentent l’utilisateur Windows de l’interface éléments pris en charge par les styles visuels.</span><span class="sxs-lookup"><span data-stu-id="3df57-103">The <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> namespace exposes <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> objects that represent the Windows user interface (UI) elements supported by visual styles.</span></span> <span data-ttu-id="3df57-104">Cette rubrique montre comment utiliser le <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> classe pour restituer le <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> qui représente le **fermer la session** et **arrêter** boutons du menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="3df57-104">This topic demonstrates how to use the <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> class to render the <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> that represents the **Log Off** and **Shut Down** buttons of the Start menu.</span></span>  
  
### <a name="to-render-a-visual-style-element"></a><span data-ttu-id="3df57-105">Pour restituer un élément de style visuel</span><span class="sxs-lookup"><span data-stu-id="3df57-105">To render a visual style element</span></span>  
  
1. <span data-ttu-id="3df57-106">Créer un <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> et définissez-le sur l’élément que vous souhaitez dessiner.</span><span class="sxs-lookup"><span data-stu-id="3df57-106">Create a <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> and set it to the element you want to draw.</span></span> <span data-ttu-id="3df57-107">Notez l’utilisation de la <xref:System.Windows.Forms.Application.RenderWithVisualStyles%2A?displayProperty=nameWithType> propriété et la <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.IsElementDefined%2A?displayProperty=nameWithType> méthode ; le <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.%23ctor%2A> constructeur lève une exception si les styles visuels sont désactivés ou un élément n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="3df57-107">Note the use of the <xref:System.Windows.Forms.Application.RenderWithVisualStyles%2A?displayProperty=nameWithType> property and the <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.IsElementDefined%2A?displayProperty=nameWithType> method; the <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.%23ctor%2A> constructor will throw an exception if visual styles are disabled or an element is undefined.</span></span>  
  
     [!code-cpp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/cpp/form1.cpp#4)]
     [!code-csharp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/CS/form1.cs#4)]
     [!code-vb[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/VB/form1.vb#4)]  
  
2. <span data-ttu-id="3df57-108">Appelez le <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.DrawBackground%2A> méthode pour restituer l’élément qui le <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> actuellement représente.</span><span class="sxs-lookup"><span data-stu-id="3df57-108">Call the <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.DrawBackground%2A> method to render the element that the <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> currently represents.</span></span>  
  
     [!code-cpp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/cpp/form1.cpp#6)]
     [!code-csharp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/CS/form1.cs#6)]
     [!code-vb[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/VB/form1.vb#6)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="3df57-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="3df57-109">Compiling the Code</span></span>  
 <span data-ttu-id="3df57-110">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="3df57-110">This example requires:</span></span>  
  
-   <span data-ttu-id="3df57-111">Un contrôle personnalisé dérivé de la <xref:System.Windows.Forms.Control> classe.</span><span class="sxs-lookup"><span data-stu-id="3df57-111">A custom control derived from the <xref:System.Windows.Forms.Control> class.</span></span>  
  
-   <span data-ttu-id="3df57-112">Un <xref:System.Windows.Forms.Form> qui héberge le contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3df57-112">A <xref:System.Windows.Forms.Form> that hosts the custom control.</span></span>  
  
-   <span data-ttu-id="3df57-113">Fait référence à la <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, et <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="3df57-113">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, and <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> namespaces.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3df57-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3df57-114">See also</span></span>

- [<span data-ttu-id="3df57-115">Rendu des contrôles avec les styles visuels</span><span class="sxs-lookup"><span data-stu-id="3df57-115">Rendering Controls with Visual Styles</span></span>](rendering-controls-with-visual-styles.md)
