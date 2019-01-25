---
title: 'Procédure : Gérer manuellement des graphiques mis en mémoire tampon'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing by manually managing graphics
- graphics [Windows Forms], managing buffered
ms.assetid: 4c2a90ee-bbbe-4ff6-9170-1b06c195c918
ms.openlocfilehash: b27a013d2cf66fb12365bffc35a07ed32bc25a2e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554489"
---
# <a name="how-to-manually-manage-buffered-graphics"></a><span data-ttu-id="93e18-102">Procédure : Gérer manuellement des graphiques mis en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="93e18-102">How to: Manually Manage Buffered Graphics</span></span>
<span data-ttu-id="93e18-103">Pour des scénarios de double mise en mémoire tampon plus avancés, vous pouvez utiliser le [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] classes pour implémenter votre propre logique de double tampon.</span><span class="sxs-lookup"><span data-stu-id="93e18-103">For more advanced double buffering scenarios, you can use the [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] classes to implement your own double-buffering logic.</span></span> <span data-ttu-id="93e18-104">La classe responsable de l’allocation et la gestion des mémoires tampon de graphiques individuelles est la <xref:System.Drawing.BufferedGraphicsContext> classe.</span><span class="sxs-lookup"><span data-stu-id="93e18-104">The class responsible for allocating and managing individual graphics buffers is the <xref:System.Drawing.BufferedGraphicsContext> class.</span></span> <span data-ttu-id="93e18-105">Chaque application a sa propre valeur par défaut <xref:System.Drawing.BufferedGraphicsContext> qui gère toute la double mise en mémoire tampon pour l’application de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="93e18-105">Every application has its own default <xref:System.Drawing.BufferedGraphicsContext> that manages all of the default double buffering for that application.</span></span> <span data-ttu-id="93e18-106">Vous pouvez récupérer une référence à cette instance en appelant le <xref:System.Drawing.BufferedGraphicsManager.Current%2A>.</span><span class="sxs-lookup"><span data-stu-id="93e18-106">You can retrieve a reference to this instance by calling the <xref:System.Drawing.BufferedGraphicsManager.Current%2A>.</span></span>  
  
### <a name="to-obtain-a-reference-to-the-default-bufferedgraphicscontext"></a><span data-ttu-id="93e18-107">Pour obtenir une référence à la valeur par défaut BufferedGraphicsContext</span><span class="sxs-lookup"><span data-stu-id="93e18-107">To obtain a reference to the default BufferedGraphicsContext</span></span>  
  
-   <span data-ttu-id="93e18-108">Définir le <xref:System.Drawing.BufferedGraphicsManager.Current%2A> propriété, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="93e18-108">Set the <xref:System.Drawing.BufferedGraphicsManager.Current%2A> property, as shown in the following code example.</span></span>  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#11)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#11)]  
  
    > [!NOTE]
    >  <span data-ttu-id="93e18-109">Vous n’avez pas besoin d’appeler le `Dispose` méthode sur le <xref:System.Drawing.BufferedGraphicsContext> référence que vous recevez à partir de la <xref:System.Drawing.BufferedGraphicsManager> classe.</span><span class="sxs-lookup"><span data-stu-id="93e18-109">You do not need to call the `Dispose` method on the <xref:System.Drawing.BufferedGraphicsContext> reference that you receive from the <xref:System.Drawing.BufferedGraphicsManager> class.</span></span> <span data-ttu-id="93e18-110">Le <xref:System.Drawing.BufferedGraphicsManager> traite l’intégralité de l’allocation de mémoire et la distribution par défaut <xref:System.Drawing.BufferedGraphicsContext> instances.</span><span class="sxs-lookup"><span data-stu-id="93e18-110">The <xref:System.Drawing.BufferedGraphicsManager> handles all of the memory allocation and distribution for default <xref:System.Drawing.BufferedGraphicsContext> instances.</span></span>  
  
     <span data-ttu-id="93e18-111">Pour les applications gourmandes en ressources graphiques telles que l’animation, vous pouvez parfois améliorer les performances en utilisant un dédié <xref:System.Drawing.BufferedGraphicsContext> au lieu du <xref:System.Drawing.BufferedGraphicsContext> fournie par le <xref:System.Drawing.BufferedGraphicsManager>.</span><span class="sxs-lookup"><span data-stu-id="93e18-111">For graphically intensive applications such as animation, you can sometimes improve performance by using a dedicated <xref:System.Drawing.BufferedGraphicsContext> instead of the <xref:System.Drawing.BufferedGraphicsContext> provided by the <xref:System.Drawing.BufferedGraphicsManager>.</span></span> <span data-ttu-id="93e18-112">Cela vous permet de créer et gérer les mémoires tampons de graphiques individuellement, sans subir la surcharge de performances de la gestion de tous les autres mises en mémoire tampon graphiques associés à votre application, même si la mémoire consommée par l’application sera supérieure.</span><span class="sxs-lookup"><span data-stu-id="93e18-112">This enables you to create and manage graphics buffers individually, without incurring the performance overhead of managing all the other buffered graphics associated with your application, though the memory consumed by the application will be greater.</span></span>  
  
### <a name="to-create-a-dedicated-bufferedgraphicscontext"></a><span data-ttu-id="93e18-113">Pour créer un BufferedGraphicsContext dédié</span><span class="sxs-lookup"><span data-stu-id="93e18-113">To create a dedicated BufferedGraphicsContext</span></span>  
  
-   <span data-ttu-id="93e18-114">Déclarez et créez une nouvelle instance de la <xref:System.Drawing.BufferedGraphicsContext> classe, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="93e18-114">Declare and create a new instance of the <xref:System.Drawing.BufferedGraphicsContext> class, as shown in the following code example.</span></span>  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#12)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#12)]  
  
## <a name="see-also"></a><span data-ttu-id="93e18-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93e18-115">See also</span></span>
- <xref:System.Drawing.BufferedGraphicsContext>
- [<span data-ttu-id="93e18-116">Graphiques mis deux fois en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="93e18-116">Double Buffered Graphics</span></span>](../../../../docs/framework/winforms/advanced/double-buffered-graphics.md)
- [<span data-ttu-id="93e18-117">Guide pratique pour Restituer manuellement des graphiques mis en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="93e18-117">How to: Manually Render Buffered Graphics</span></span>](../../../../docs/framework/winforms/advanced/how-to-manually-render-buffered-graphics.md)
