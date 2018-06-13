---
title: 'Comment : gérer manuellement des graphiques mis en mémoire tampon'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing by manually managing graphics
- graphics [Windows Forms], managing buffered
ms.assetid: 4c2a90ee-bbbe-4ff6-9170-1b06c195c918
ms.openlocfilehash: f8675582fe6bafefd94d6a740c3263e407dfd4e7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33523953"
---
# <a name="how-to-manually-manage-buffered-graphics"></a><span data-ttu-id="ecc9c-102">Comment : gérer manuellement des graphiques mis en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="ecc9c-102">How to: Manually Manage Buffered Graphics</span></span>
<span data-ttu-id="ecc9c-103">Pour des scénarios de doubles mise en mémoire tampon plus avancés, vous pouvez utiliser la [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] classes à implémenter votre propre logique de mécanisme de double tampon.</span><span class="sxs-lookup"><span data-stu-id="ecc9c-103">For more advanced double buffering scenarios, you can use the [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] classes to implement your own double-buffering logic.</span></span> <span data-ttu-id="ecc9c-104">La classe chargée de l’allocation et la gestion des mémoires tampon de graphiques individuelles est la <xref:System.Drawing.BufferedGraphicsContext> classe.</span><span class="sxs-lookup"><span data-stu-id="ecc9c-104">The class responsible for allocating and managing individual graphics buffers is the <xref:System.Drawing.BufferedGraphicsContext> class.</span></span> <span data-ttu-id="ecc9c-105">Chaque application possède sa propre valeur par défaut <xref:System.Drawing.BufferedGraphicsContext> qui gère toutes la valeur par défaut est de double tampon pour cette application.</span><span class="sxs-lookup"><span data-stu-id="ecc9c-105">Every application has its own default <xref:System.Drawing.BufferedGraphicsContext> that manages all of the default double buffering for that application.</span></span> <span data-ttu-id="ecc9c-106">Vous pouvez récupérer une référence à cette instance en appelant le <xref:System.Drawing.BufferedGraphicsManager.Current%2A>.</span><span class="sxs-lookup"><span data-stu-id="ecc9c-106">You can retrieve a reference to this instance by calling the <xref:System.Drawing.BufferedGraphicsManager.Current%2A>.</span></span>  
  
### <a name="to-obtain-a-reference-to-the-default-bufferedgraphicscontext"></a><span data-ttu-id="ecc9c-107">Pour obtenir une référence à la valeur par défaut BufferedGraphicsContext</span><span class="sxs-lookup"><span data-stu-id="ecc9c-107">To obtain a reference to the default BufferedGraphicsContext</span></span>  
  
-   <span data-ttu-id="ecc9c-108">Définir le <xref:System.Drawing.BufferedGraphicsManager.Current%2A> propriété, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ecc9c-108">Set the <xref:System.Drawing.BufferedGraphicsManager.Current%2A> property, as shown in the following code example.</span></span>  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#11)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#11)]  
  
    > [!NOTE]
    >  <span data-ttu-id="ecc9c-109">Vous n’avez pas besoin d’appeler le `Dispose` méthode sur le <xref:System.Drawing.BufferedGraphicsContext> référence que vous recevez à partir de la <xref:System.Drawing.BufferedGraphicsManager> classe.</span><span class="sxs-lookup"><span data-stu-id="ecc9c-109">You do not need to call the `Dispose` method on the <xref:System.Drawing.BufferedGraphicsContext> reference that you receive from the <xref:System.Drawing.BufferedGraphicsManager> class.</span></span> <span data-ttu-id="ecc9c-110">Le <xref:System.Drawing.BufferedGraphicsManager> gère l’ensemble de l’allocation de mémoire et de distribution par défaut <xref:System.Drawing.BufferedGraphicsContext> instances.</span><span class="sxs-lookup"><span data-stu-id="ecc9c-110">The <xref:System.Drawing.BufferedGraphicsManager> handles all of the memory allocation and distribution for default <xref:System.Drawing.BufferedGraphicsContext> instances.</span></span>  
  
     <span data-ttu-id="ecc9c-111">Pour les applications gourmandes en ressources graphiques telles que l’animation, vous pouvez parfois améliorer les performances en utilisant une dédiée <xref:System.Drawing.BufferedGraphicsContext> au lieu du <xref:System.Drawing.BufferedGraphicsContext> fournie par le <xref:System.Drawing.BufferedGraphicsManager>.</span><span class="sxs-lookup"><span data-stu-id="ecc9c-111">For graphically intensive applications such as animation, you can sometimes improve performance by using a dedicated <xref:System.Drawing.BufferedGraphicsContext> instead of the <xref:System.Drawing.BufferedGraphicsContext> provided by the <xref:System.Drawing.BufferedGraphicsManager>.</span></span> <span data-ttu-id="ecc9c-112">Cela vous permet de créer et gérer les mémoires tampon de graphiques individuellement, sans subir la surcharge des performances de la gestion de tous les autres mises en mémoire tampon graphiques associés à votre application, bien que la mémoire consommée par l’application sera supérieure.</span><span class="sxs-lookup"><span data-stu-id="ecc9c-112">This enables you to create and manage graphics buffers individually, without incurring the performance overhead of managing all the other buffered graphics associated with your application, though the memory consumed by the application will be greater.</span></span>  
  
### <a name="to-create-a-dedicated-bufferedgraphicscontext"></a><span data-ttu-id="ecc9c-113">Pour créer un BufferedGraphicsContext dédié</span><span class="sxs-lookup"><span data-stu-id="ecc9c-113">To create a dedicated BufferedGraphicsContext</span></span>  
  
-   <span data-ttu-id="ecc9c-114">Déclarez et créez une nouvelle instance de la <xref:System.Drawing.BufferedGraphicsContext> classe, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ecc9c-114">Declare and create a new instance of the <xref:System.Drawing.BufferedGraphicsContext> class, as shown in the following code example.</span></span>  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#12)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#12)]  
  
## <a name="see-also"></a><span data-ttu-id="ecc9c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecc9c-115">See Also</span></span>  
 <xref:System.Drawing.BufferedGraphicsContext>  
 [<span data-ttu-id="ecc9c-116">Graphiques mis deux fois en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="ecc9c-116">Double Buffered Graphics</span></span>](../../../../docs/framework/winforms/advanced/double-buffered-graphics.md)  
 [<span data-ttu-id="ecc9c-117">Guide pratique pour restituer manuellement des graphiques mis en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="ecc9c-117">How to: Manually Render Buffered Graphics</span></span>](../../../../docs/framework/winforms/advanced/how-to-manually-render-buffered-graphics.md)
