---
title: Vue d'ensemble du contrôle StatusStrip
ms.date: 03/30/2017
f1_keywords:
- StatusStrip
helpviewer_keywords:
- StatusStrip control [Windows Forms], about StatusStrip control
- status bars [Windows Forms], about status bars
ms.assetid: c0d9bcbb-f8b8-46ef-bae2-4146b8c8ce99
ms.openlocfilehash: f6f2d4b19b7ec91c964c72e3aca85e0253c7cc22
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59129712"
---
# <a name="statusstrip-control-overview"></a><span data-ttu-id="73d68-102">Vue d'ensemble du contrôle StatusStrip</span><span class="sxs-lookup"><span data-stu-id="73d68-102">StatusStrip Control Overview</span></span>
<span data-ttu-id="73d68-103">Un contrôle <xref:System.Windows.Forms.StatusStrip> affiche des informations sur un objet affiché sur un <xref:System.Windows.Forms.Form>, les composants de l'objet ou des informations contextuelles relatives au fonctionnement de cet objet dans votre application.</span><span class="sxs-lookup"><span data-stu-id="73d68-103">A <xref:System.Windows.Forms.StatusStrip> control displays information about an object being viewed on a <xref:System.Windows.Forms.Form>, the object's components, or contextual information that relates to that object's operation within your application.</span></span> <span data-ttu-id="73d68-104">En règle générale, un contrôle <xref:System.Windows.Forms.StatusStrip> est composé d'objets <xref:System.Windows.Forms.ToolStripStatusLabel>, chacun affichant du texte, une icône ou les deux.</span><span class="sxs-lookup"><span data-stu-id="73d68-104">Typically, a <xref:System.Windows.Forms.StatusStrip> control consists of <xref:System.Windows.Forms.ToolStripStatusLabel> objects, each of which displays text, an icon, or both.</span></span> <span data-ttu-id="73d68-105"><xref:System.Windows.Forms.StatusStrip> peut également contenir des contrôles <xref:System.Windows.Forms.ToolStripDropDownButton>, <xref:System.Windows.Forms.ToolStripSplitButton> et <xref:System.Windows.Forms.ToolStripProgressBar>.</span><span class="sxs-lookup"><span data-stu-id="73d68-105">The <xref:System.Windows.Forms.StatusStrip> can also contain <xref:System.Windows.Forms.ToolStripDropDownButton>, <xref:System.Windows.Forms.ToolStripSplitButton>, and <xref:System.Windows.Forms.ToolStripProgressBar> controls.</span></span>  
  
 <span data-ttu-id="73d68-106">Le <xref:System.Windows.Forms.StatusStrip> par défaut n'a pas de panneau.</span><span class="sxs-lookup"><span data-stu-id="73d68-106">The default <xref:System.Windows.Forms.StatusStrip> has no panels.</span></span> <span data-ttu-id="73d68-107">Pour ajouter des panneaux à un <xref:System.Windows.Forms.StatusStrip>, utilisez la méthode <xref:System.Windows.Forms.ToolStripItemCollection.AddRange%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="73d68-107">To add panels to a <xref:System.Windows.Forms.StatusStrip>, use the <xref:System.Windows.Forms.ToolStripItemCollection.AddRange%2A?displayProperty=nameWithType> method.</span></span>  
  
 <span data-ttu-id="73d68-108">Visual Studio offre une prise en charge complète de la gestion des éléments et des commandes courantes de <xref:System.Windows.Forms.StatusStrip>.</span><span class="sxs-lookup"><span data-stu-id="73d68-108">There is extensive support for handling <xref:System.Windows.Forms.StatusStrip> items and common commands in Visual Studio.</span></span>  
  
 <span data-ttu-id="73d68-109">Consultez également [éditeur de collections d’éléments StatusStrip](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233631(v=vs.100)) et [Tâches StatusStrip, boîte de dialogue](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233642(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="73d68-109">Also see [StatusStrip Items Collection Editor](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233631(v=vs.100)) and [StatusStrip Tasks Dialog Box](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233642(v=vs.100)).</span></span>  
  
 <span data-ttu-id="73d68-110">Bien que <xref:System.Windows.Forms.StatusStrip> remplace et étende le contrôle <xref:System.Windows.Forms.StatusBar> des versions antérieures, <xref:System.Windows.Forms.StatusBar> est conservé à des fins de compatibilité descendante et pour une utilisation ultérieure si tel est votre choix.</span><span class="sxs-lookup"><span data-stu-id="73d68-110">Although <xref:System.Windows.Forms.StatusStrip> replaces and extends the <xref:System.Windows.Forms.StatusBar> control of previous versions, <xref:System.Windows.Forms.StatusBar> is retained for both backward compatibility and future use if you choose.</span></span>  
  
### <a name="important-statusstrip-members"></a><span data-ttu-id="73d68-111">Membres importants de StatusStrip</span><span class="sxs-lookup"><span data-stu-id="73d68-111">Important StatusStrip Members</span></span>  
  
|<span data-ttu-id="73d68-112">Nom</span><span class="sxs-lookup"><span data-stu-id="73d68-112">Name</span></span>|<span data-ttu-id="73d68-113">Description</span><span class="sxs-lookup"><span data-stu-id="73d68-113">Description</span></span>|  
|----------|-----------------|  
|<xref:System.Windows.Forms.StatusStrip.CanOverflow%2A>|<span data-ttu-id="73d68-114">Obtient ou définit une valeur indiquant si le <xref:System.Windows.Forms.StatusStrip> prend en charge les fonctionnalités de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="73d68-114">Gets or sets a value indicating whether the <xref:System.Windows.Forms.StatusStrip> supports overflow functionality.</span></span>|  
|<xref:System.Windows.Forms.StatusStrip.Stretch%2A>|<span data-ttu-id="73d68-115">Obtient ou définit une valeur indiquant si le <xref:System.Windows.Forms.StatusStrip> s'étire d'un bout à l'autre dans son <xref:System.Windows.Forms.ToolStripContainer>.</span><span class="sxs-lookup"><span data-stu-id="73d68-115">Gets or sets a value indicating whether the <xref:System.Windows.Forms.StatusStrip> stretches from end to end in its <xref:System.Windows.Forms.ToolStripContainer>.</span></span>|  
  
### <a name="important-statusstrip-companion-classes"></a><span data-ttu-id="73d68-116">Classes auxiliaires importantes de StatusStrip</span><span class="sxs-lookup"><span data-stu-id="73d68-116">Important StatusStrip Companion Classes</span></span>  
  
|<span data-ttu-id="73d68-117">Nom</span><span class="sxs-lookup"><span data-stu-id="73d68-117">Name</span></span>|<span data-ttu-id="73d68-118">Description</span><span class="sxs-lookup"><span data-stu-id="73d68-118">Description</span></span>|  
|----------|-----------------|  
|<xref:System.Windows.Forms.ToolStripStatusLabel>|<span data-ttu-id="73d68-119">Représente un panneau dans un contrôle <xref:System.Windows.Forms.StatusStrip>.</span><span class="sxs-lookup"><span data-stu-id="73d68-119">Represents a panel in a <xref:System.Windows.Forms.StatusStrip> control.</span></span>|  
|<xref:System.Windows.Forms.ToolStripDropDownButton>|<span data-ttu-id="73d68-120">Affiche un <xref:System.Windows.Forms.ToolStripDropDown> associé à partir duquel l'utilisateur peut sélectionner un élément unique.</span><span class="sxs-lookup"><span data-stu-id="73d68-120">Displays an associated <xref:System.Windows.Forms.ToolStripDropDown> from which the user can select a single item.</span></span>|  
|<xref:System.Windows.Forms.ToolStripSplitButton>|<span data-ttu-id="73d68-121">Représente un contrôle en deux parties constitué d'un bouton standard et d'un menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="73d68-121">Represents a two-part control that is a standard button and a drop-down menu.</span></span>|  
|<xref:System.Windows.Forms.ToolStripProgressBar>|<span data-ttu-id="73d68-122">Affiche l'état d'achèvement d'un processus.</span><span class="sxs-lookup"><span data-stu-id="73d68-122">Displays the completion state of a process.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="73d68-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73d68-123">See also</span></span>

- <xref:System.Windows.Forms.StatusStrip>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- <xref:System.Windows.Forms.ToolStripStatusLabel.Spring%2A>
