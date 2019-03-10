---
title: Graphiques et dessins dans les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms]
- graphics [Windows Forms], using in Windows Forms
- GDI+, using in managed code
- drawing [Windows Forms]
ms.assetid: 362532c5-1a06-4257-bdc8-723461009ede
ms.openlocfilehash: 08f87436ade62bb54295b012a1c24dc177ea9667
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57705420"
---
# <a name="graphics-and-drawing-in-windows-forms"></a><span data-ttu-id="fd4cb-102">Graphiques et dessins dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fd4cb-102">Graphics and Drawing in Windows Forms</span></span>
<span data-ttu-id="fd4cb-103">Le Common Language Runtime utilise une implémentation avancée de l'interface GDI Windows ([!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)]) appelée [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4cb-103">The common language runtime uses an advanced implementation of the Windows Graphics Device Interface ([!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)]) called [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)].</span></span> <span data-ttu-id="fd4cb-104">Avec [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], vous pouvez créer des graphismes, dessiner du texte et manipuler des images graphiques comme des objets.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-104">With [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] you can create graphics, draw text, and manipulate graphical images as objects.</span></span> [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] <span data-ttu-id="fd4cb-105">est conçu pour offrir à la fois de hautes performances et une facilité d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-105">is designed to offer performance and ease of use.</span></span> <span data-ttu-id="fd4cb-106">Vous pouvez utiliser [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] pour restituer des images graphiques sur des Windows Forms et des contrôles.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-106">You can use [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] to render graphical images on Windows Forms and controls.</span></span> <span data-ttu-id="fd4cb-107">Bien que vous ne puissiez pas utiliser [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] directement sur des Web Forms, vous pouvez afficher des images graphiques via le contrôle serveur web Image.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-107">Although you cannot use [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] directly on Web Forms, you can display graphical images through the Image Web Server control.</span></span>  
  
 <span data-ttu-id="fd4cb-108">Dans cette section, vous trouverez des rubriques qui présentent les notions de base de la programmation [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4cb-108">In this section, you will find topics that introduce the fundamentals of [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] programming.</span></span> <span data-ttu-id="fd4cb-109">Bien qu’il ne s’agisse pas d’une référence exhaustive, cette section comprend des informations sur les objets <xref:System.Drawing.Graphics>, <xref:System.Drawing.Pen>, <xref:System.Drawing.Brush>, et <xref:System.Drawing.Color> et explique comment effectuer des tâches telles que dessiner des formes et du texte ou afficher des images.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-109">Although not intended to be a comprehensive reference, this section includes information about the <xref:System.Drawing.Graphics>, <xref:System.Drawing.Pen>, <xref:System.Drawing.Brush>, and <xref:System.Drawing.Color> objects, and explains how to perform such tasks as drawing shapes, drawing text, or displaying images.</span></span> <span data-ttu-id="fd4cb-110">Pour plus d’informations, consultez [référence GDI +](/windows/desktop/gdiplus/-gdiplus-class-gdi-reference).</span><span class="sxs-lookup"><span data-stu-id="fd4cb-110">For more information, see [GDI+ Reference](/windows/desktop/gdiplus/-gdiplus-class-gdi-reference).</span></span>  
  
 <span data-ttu-id="fd4cb-111">Si vous voulez vous lancer et commencer immédiatement, consultez [Bien démarrer avec la programmation graphique](getting-started-with-graphics-programming.md).</span><span class="sxs-lookup"><span data-stu-id="fd4cb-111">If you'd like to jump in and get started right away, see [Getting Started with Graphics Programming](getting-started-with-graphics-programming.md).</span></span> <span data-ttu-id="fd4cb-112">Elle comporte des rubriques sur l’utilisation de code pour dessiner des lignes, des formes, du texte et d’autres éléments sur les Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-112">It has topics on how to use code to draw lines, shapes, text, and more on Windows forms.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="fd4cb-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="fd4cb-113">In This Section</span></span>  
 [<span data-ttu-id="fd4cb-114">Vue d’ensemble des graphiques</span><span class="sxs-lookup"><span data-stu-id="fd4cb-114">Graphics Overview</span></span>](graphics-overview-windows-forms.md)  
 <span data-ttu-id="fd4cb-115">Fournit une introduction aux classes managées graphiques.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-115">Provides an introduction to the graphics-related managed classes.</span></span>  
  
 [<span data-ttu-id="fd4cb-116">À propos du code managé GDI+</span><span class="sxs-lookup"><span data-stu-id="fd4cb-116">About GDI+ Managed Code</span></span>](about-gdi-managed-code.md)  
 <span data-ttu-id="fd4cb-117">Fournit des informations sur les classes managées [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4cb-117">Provides information about the managed [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] classes.</span></span>  
  
 [<span data-ttu-id="fd4cb-118">Utilisation de classes graphiques managées</span><span class="sxs-lookup"><span data-stu-id="fd4cb-118">Using Managed Graphics Classes</span></span>](using-managed-graphics-classes.md)  
 <span data-ttu-id="fd4cb-119">Montre comment effectuer diverses tâches à l'aide des classes managées [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4cb-119">Demonstrates how to complete a variety of tasks using the [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] managed classes.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="fd4cb-120">Référence</span><span class="sxs-lookup"><span data-stu-id="fd4cb-120">Reference</span></span>  
 <xref:System.Drawing>  
 <span data-ttu-id="fd4cb-121">Fournit l'accès aux fonctionnalités graphiques de base [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4cb-121">Provides access to [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] basic graphics functionality.</span></span>  
  
 <xref:System.Drawing.Drawing2D>  
 <span data-ttu-id="fd4cb-122">Fournit des fonctionnalités graphiques vectorielles et à deux dimensions avancées.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-122">Provides advanced two-dimensional and vector graphics functionality.</span></span>  
  
 <xref:System.Drawing.Imaging>  
 <span data-ttu-id="fd4cb-123">Fournit des fonctionnalités d'imagerie [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] avancées.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-123">Provides advanced [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] imaging functionality.</span></span>  
  
 <xref:System.Drawing.Text>  
 <span data-ttu-id="fd4cb-124">Fournit des fonctionnalités typographiques [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] avancées.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-124">Provides advanced [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] typography functionality.</span></span> <span data-ttu-id="fd4cb-125">Les classes dans cet espace de noms peuvent être utilisées pour créer et utiliser des collections de polices.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-125">The classes in this namespace can be used to create and use collections of fonts.</span></span>  
  
 <xref:System.Drawing.Printing>  
 <span data-ttu-id="fd4cb-126">Fournit des fonctionnalités d'impression.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-126">Provides printing functionality.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="fd4cb-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd4cb-127">Related Sections</span></span>  
 [<span data-ttu-id="fd4cb-128">Dessin et rendu personnalisés des contrôles</span><span class="sxs-lookup"><span data-stu-id="fd4cb-128">Custom Control Painting and Rendering</span></span>](../controls/custom-control-painting-and-rendering.md)  
 <span data-ttu-id="fd4cb-129">Explique comment fournir du code pour des contrôles de dessin.</span><span class="sxs-lookup"><span data-stu-id="fd4cb-129">Details how to provide code for painting controls.</span></span>
