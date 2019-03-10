---
title: Applications Windows Forms et non managées
ms.date: 03/30/2017
helpviewer_keywords:
- ActiveX controls [Windows Forms]
- COM interop [Windows Forms], Windows Forms
- COM [Windows Forms]
- Windows Forms, unmanaged
- Windows Forms, interop
ms.assetid: 81bc100c-fa49-4614-85a6-0f7ab59eac8a
ms.openlocfilehash: 65465f22b1806d385523c894cce2103afe33c2f0
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57702657"
---
# <a name="windows-forms-and-unmanaged-applications"></a><span data-ttu-id="7368f-102">Applications Windows Forms et non managées</span><span class="sxs-lookup"><span data-stu-id="7368f-102">Windows Forms and Unmanaged Applications</span></span>
<span data-ttu-id="7368f-103">Les contrôles et les applications Windows Forms peuvent interagir avec des applications non managées, avec certaines restrictions.</span><span class="sxs-lookup"><span data-stu-id="7368f-103">Windows Forms applications and controls can interoperate with unmanaged applications, with some caveats.</span></span> <span data-ttu-id="7368f-104">Les sections suivantes décrivent les scénarios et les configurations pris en charge et non pris en charge par les applications et les contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="7368f-104">The following sections describe the scenarios and configurations that Windows Forms applications and controls support and those that they do not support.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7368f-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7368f-105">In This Section</span></span>  
 [<span data-ttu-id="7368f-106">Vue d'ensemble des applications Windows Forms et non managées</span><span class="sxs-lookup"><span data-stu-id="7368f-106">Windows Forms and Unmanaged Applications Overview</span></span>](windows-forms-and-unmanaged-applications-overview.md)  
 <span data-ttu-id="7368f-107">Propose des informations générales sur l'utilisation et l'implémentation des contrôles Windows Forms qui fonctionnent avec les applications non managées.</span><span class="sxs-lookup"><span data-stu-id="7368f-107">Offers general information about how to use and implement Windows Forms controls that work with unmanaged applications.</span></span>  
  
 [<span data-ttu-id="7368f-108">Guide pratique pour Prennent en charge COM Interop en affichant un formulaire Windows avec la méthode ShowDialog</span><span class="sxs-lookup"><span data-stu-id="7368f-108">How to: Support COM Interop by Displaying a Windows Form with the ShowDialog Method</span></span>](com-interop-by-displaying-a-windows-form-shadow.md)  
 <span data-ttu-id="7368f-109">Fournit un exemple de code qui montre comment utiliser la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> pour exécuter un Windows Form dans une application non managée.</span><span class="sxs-lookup"><span data-stu-id="7368f-109">Provides a code example that shows how to use the <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> method to run a Windows Form in an unmanaged application.</span></span>  
  
 [<span data-ttu-id="7368f-110">Guide pratique pour Prennent en charge COM Interop en affichant chaque formulaire Windows sur son propre Thread</span><span class="sxs-lookup"><span data-stu-id="7368f-110">How to: Support COM Interop by Displaying Each Windows Form on Its Own Thread</span></span>](how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md)  
 <span data-ttu-id="7368f-111">Fournit un exemple de code qui montre comment exécuter un Windows Form sur son propre thread.</span><span class="sxs-lookup"><span data-stu-id="7368f-111">Provides a code example that shows how to run a Windows Form on its own thread.</span></span>  
  
 <span data-ttu-id="7368f-112">Consultez également [procédure pas à pas : Prise en charge COM Interop en affichant chaque formulaire Windows sur son propre Thread](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233639(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="7368f-112">Also see [Walkthrough: Supporting COM Interop by Displaying Each Windows Form on Its Own Thread](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233639(v=vs.100)).</span></span>  
  
## <a name="reference"></a><span data-ttu-id="7368f-113">Référence</span><span class="sxs-lookup"><span data-stu-id="7368f-113">Reference</span></span>  
 <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType>  
 <span data-ttu-id="7368f-114">Permet de créer un thread distinct pour un Windows Form.</span><span class="sxs-lookup"><span data-stu-id="7368f-114">Used to create a separate thread for a Windows Form.</span></span>  
  
 <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType>  
 <span data-ttu-id="7368f-115">Démarre une boucle de message pour un thread.</span><span class="sxs-lookup"><span data-stu-id="7368f-115">Starts a message loop for a thread.</span></span>  
  
 <xref:System.Windows.Forms.Control.Invoke%2A>  
 <span data-ttu-id="7368f-116">Marshale les appels à partir d’une application non managée vers un formulaire.</span><span class="sxs-lookup"><span data-stu-id="7368f-116">Marshals calls from an unmanaged application to a form.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="7368f-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7368f-117">Related Sections</span></span>  
 [<span data-ttu-id="7368f-118">Exposition de composants .NET Framework à COM</span><span class="sxs-lookup"><span data-stu-id="7368f-118">Exposing .NET Framework Components to COM</span></span>](../../interop/exposing-dotnet-components-to-com.md)  
 <span data-ttu-id="7368f-119">Propose des informations générales sur l'utilisation de types .NET Framework dans les applications non managées.</span><span class="sxs-lookup"><span data-stu-id="7368f-119">Offers general information about how to use .NET Framework types in unmanaged applications.</span></span>
