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
ms.openlocfilehash: f54f039fd3477c380a2236a93ad8d80b4f7153b2
ms.sourcegitcommit: acd8ed14fe94e9d4e3a7fb685fe83d05e941073c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56441812"
---
# <a name="windows-forms-and-unmanaged-applications"></a><span data-ttu-id="31859-102">Applications Windows Forms et non managées</span><span class="sxs-lookup"><span data-stu-id="31859-102">Windows Forms and Unmanaged Applications</span></span>
<span data-ttu-id="31859-103">Les contrôles et les applications Windows Forms peuvent interagir avec des applications non managées, avec certaines restrictions.</span><span class="sxs-lookup"><span data-stu-id="31859-103">Windows Forms applications and controls can interoperate with unmanaged applications, with some caveats.</span></span> <span data-ttu-id="31859-104">Les sections suivantes décrivent les scénarios et les configurations pris en charge et non pris en charge par les applications et les contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="31859-104">The following sections describe the scenarios and configurations that Windows Forms applications and controls support and those that they do not support.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="31859-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="31859-105">In This Section</span></span>  
 [<span data-ttu-id="31859-106">Vue d'ensemble des applications Windows Forms et non managées</span><span class="sxs-lookup"><span data-stu-id="31859-106">Windows Forms and Unmanaged Applications Overview</span></span>](../../../../docs/framework/winforms/advanced/windows-forms-and-unmanaged-applications-overview.md)  
 <span data-ttu-id="31859-107">Propose des informations générales sur l'utilisation et l'implémentation des contrôles Windows Forms qui fonctionnent avec les applications non managées.</span><span class="sxs-lookup"><span data-stu-id="31859-107">Offers general information about how to use and implement Windows Forms controls that work with unmanaged applications.</span></span>  
  
 [<span data-ttu-id="31859-108">Guide pratique pour Prennent en charge COM Interop en affichant un formulaire Windows avec la méthode ShowDialog</span><span class="sxs-lookup"><span data-stu-id="31859-108">How to: Support COM Interop by Displaying a Windows Form with the ShowDialog Method</span></span>](../../../../docs/framework/winforms/advanced/com-interop-by-displaying-a-windows-form-shadow.md)  
 <span data-ttu-id="31859-109">Fournit un exemple de code qui montre comment utiliser la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> pour exécuter un Windows Form dans une application non managée.</span><span class="sxs-lookup"><span data-stu-id="31859-109">Provides a code example that shows how to use the <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> method to run a Windows Form in an unmanaged application.</span></span>  
  
 [<span data-ttu-id="31859-110">Guide pratique pour Prennent en charge COM Interop en affichant chaque formulaire Windows sur son propre Thread</span><span class="sxs-lookup"><span data-stu-id="31859-110">How to: Support COM Interop by Displaying Each Windows Form on Its Own Thread</span></span>](../../../../docs/framework/winforms/advanced/how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md)  
 <span data-ttu-id="31859-111">Fournit un exemple de code qui montre comment exécuter un Windows Form sur son propre thread.</span><span class="sxs-lookup"><span data-stu-id="31859-111">Provides a code example that shows how to run a Windows Form on its own thread.</span></span>  
  
 <span data-ttu-id="31859-112">Consultez également [procédure pas à pas : Prise en charge COM Interop en affichant chaque formulaire Windows sur son propre Thread](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233639(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="31859-112">Also see [Walkthrough: Supporting COM Interop by Displaying Each Windows Form on Its Own Thread](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233639(v=vs.100)).</span></span>  
  
## <a name="reference"></a><span data-ttu-id="31859-113">Référence</span><span class="sxs-lookup"><span data-stu-id="31859-113">Reference</span></span>  
 <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType>  
 <span data-ttu-id="31859-114">Permet de créer un thread distinct pour un Windows Form.</span><span class="sxs-lookup"><span data-stu-id="31859-114">Used to create a separate thread for a Windows Form.</span></span>  
  
 <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType>  
 <span data-ttu-id="31859-115">Démarre une boucle de message pour un thread.</span><span class="sxs-lookup"><span data-stu-id="31859-115">Starts a message loop for a thread.</span></span>  
  
 <xref:System.Windows.Forms.Control.Invoke%2A>  
 <span data-ttu-id="31859-116">Marshale les appels à partir d’une application non managée vers un formulaire.</span><span class="sxs-lookup"><span data-stu-id="31859-116">Marshals calls from an unmanaged application to a form.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="31859-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31859-117">Related Sections</span></span>  
 [<span data-ttu-id="31859-118">Exposition de composants .NET Framework à COM</span><span class="sxs-lookup"><span data-stu-id="31859-118">Exposing .NET Framework Components to COM</span></span>](../../../../docs/framework/interop/exposing-dotnet-components-to-com.md)  
 <span data-ttu-id="31859-119">Propose des informations générales sur l'utilisation de types .NET Framework dans les applications non managées.</span><span class="sxs-lookup"><span data-stu-id="31859-119">Offers general information about how to use .NET Framework types in unmanaged applications.</span></span>
