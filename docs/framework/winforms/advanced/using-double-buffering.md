---
title: Utilisation de doubles tampons d'enregistrements
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], double buffering
- double buffering
- flicker [Windows Forms], reducing in Windows Forms
- buffering [Windows Forms], double buffering
ms.assetid: dc484e33-7101-4e4b-ada5-d3c96155fbcd
ms.openlocfilehash: 9b09210eba0ac3a141219a7cdbff15f22c6ed003
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33523908"
---
# <a name="using-double-buffering"></a><span data-ttu-id="3bb53-102">Utilisation de doubles tampons d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="3bb53-102">Using Double Buffering</span></span>
<span data-ttu-id="3bb53-103">Vous pouvez utiliser des graphiques de double tampon pour réduire le scintillement dans vos applications qui contiennent des opérations de peinture complexes.</span><span class="sxs-lookup"><span data-stu-id="3bb53-103">You can use double-buffered graphics to reduce flicker in your applications that contain complex painting operations.</span></span> <span data-ttu-id="3bb53-104">Le .NET Framework contient une prise en charge intégrée de double tampon, ou vous pouvez gérer et restituer manuellement des graphiques.</span><span class="sxs-lookup"><span data-stu-id="3bb53-104">The .NET Framework contains built-in support for double-buffering or you can manage and render graphics manually.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="3bb53-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3bb53-105">In This Section</span></span>  
 [<span data-ttu-id="3bb53-106">Graphiques mis deux fois en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="3bb53-106">Double Buffered Graphics</span></span>](../../../../docs/framework/winforms/advanced/double-buffered-graphics.md)  
 <span data-ttu-id="3bb53-107">Introduit la double mise en mémoire tampon concept et les plans .NET Framework prise en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb53-107">Introduces double buffering concept and outlines .NET Framework support.</span></span>  
  
 [<span data-ttu-id="3bb53-108">Guide pratique pour réduire le scintillement des graphiques à l’aide de la double mise en mémoire tampon pour les formulaires et les contrôles</span><span class="sxs-lookup"><span data-stu-id="3bb53-108">How to: Reduce Graphics Flicker with Double Buffering for Forms and Controls</span></span>](../../../../docs/framework/winforms/advanced/how-to-reduce-graphics-flicker-with-double-buffering-for-forms-and-controls.md)  
 <span data-ttu-id="3bb53-109">Montre comment utiliser la valeur par défaut de double tampon prise en charge dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="3bb53-109">Demonstrates how to use the default double buffering support in the .NET Framework.</span></span>  
  
 [<span data-ttu-id="3bb53-110">Guide pratique pour gérer manuellement des graphiques mis en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="3bb53-110">How to: Manually Manage Buffered Graphics</span></span>](../../../../docs/framework/winforms/advanced/how-to-manually-manage-buffered-graphics.md)  
 <span data-ttu-id="3bb53-111">Montre comment gérer le mécanisme de double tampon dans les applications.</span><span class="sxs-lookup"><span data-stu-id="3bb53-111">Shows how to manage double buffering in applications.</span></span>  
  
 [<span data-ttu-id="3bb53-112">Guide pratique pour restituer manuellement des graphiques mis en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="3bb53-112">How to: Manually Render Buffered Graphics</span></span>](../../../../docs/framework/winforms/advanced/how-to-manually-render-buffered-graphics.md)  
 <span data-ttu-id="3bb53-113">Montre comment restituer des graphiques de double tampon.</span><span class="sxs-lookup"><span data-stu-id="3bb53-113">Demonstrates how to render double-buffered graphics.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="3bb53-114">Référence</span><span class="sxs-lookup"><span data-stu-id="3bb53-114">Reference</span></span>  
 <span data-ttu-id="3bb53-115"><xref:System.Windows.Forms.Control.SetStyle%2A> ,</span><span class="sxs-lookup"><span data-stu-id="3bb53-115"><xref:System.Windows.Forms.Control.SetStyle%2A> ,</span></span>  
 <span data-ttu-id="3bb53-116">Méthode de contrôle qui active le mécanisme de double tampon.</span><span class="sxs-lookup"><span data-stu-id="3bb53-116">Control method that enables double buffering.</span></span>  
  
 <span data-ttu-id="3bb53-117"><xref:System.Drawing.BufferedGraphicsContext> ,</span><span class="sxs-lookup"><span data-stu-id="3bb53-117"><xref:System.Drawing.BufferedGraphicsContext> ,</span></span>  
 <span data-ttu-id="3bb53-118">Fournit des méthodes pour créer des mémoires tampon de graphiques.</span><span class="sxs-lookup"><span data-stu-id="3bb53-118">Provides methods for creating graphics buffers.</span></span>  
  
 <xref:System.Drawing.BufferedGraphicsManager>  
 <span data-ttu-id="3bb53-119">Fournit l’accès au contexte graphique mis en mémoire tampon pour un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="3bb53-119">Provides access to the buffered graphics context for a application domain.</span></span>
