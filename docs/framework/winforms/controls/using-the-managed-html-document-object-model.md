---
title: Utilisation du modèle objet de document HTML managé
ms.date: 03/30/2017
helpviewer_keywords:
- managed HTML DOM
ms.assetid: a017dd5c-cd7b-47e4-952c-f4f54cb48409
ms.openlocfilehash: 1405bb43e971f02bafa892de84a6b8acde2e319b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54691422"
---
# <a name="using-the-managed-html-document-object-model"></a><span data-ttu-id="7a415-102">Utilisation du modèle objet de document HTML managé</span><span class="sxs-lookup"><span data-stu-id="7a415-102">Using the Managed HTML Document Object Model</span></span>
<span data-ttu-id="7a415-103">Le modèle d’objet de document (DOM) HTML managé fournit un wrapper basé sur le [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] pour les classes HTML exposées par Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="7a415-103">The managed HTML document object model (DOM) provides a wrapper based on the [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] for the HTML classes exposed by Internet Explorer.</span></span> <span data-ttu-id="7a415-104">Utilisez ces classes pour manipuler des pages HTML hébergées dans le <xref:System.Windows.Forms.WebBrowser> contrôle, ou pour créer de nouvelles pages à partir du début.</span><span class="sxs-lookup"><span data-stu-id="7a415-104">Use these classes to manipulate HTML pages hosted in the <xref:System.Windows.Forms.WebBrowser> control, or to build new pages from the beginning.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7a415-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7a415-105">In This Section</span></span>  
 [<span data-ttu-id="7a415-106">Guide pratique pour Accéder au modèle d’objet de Document HTML managé</span><span class="sxs-lookup"><span data-stu-id="7a415-106">How to: Access the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/how-to-access-the-managed-html-document-object-model.md)  
 <span data-ttu-id="7a415-107">Décrit comment obtenir une instance valide de <xref:System.Windows.Forms.HtmlDocument> à partir d’une application Windows Forms ou une <xref:System.Windows.Forms.UserControl> hébergée dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="7a415-107">Describes how to obtain a valid instance of <xref:System.Windows.Forms.HtmlDocument> from either a Windows Forms application or a <xref:System.Windows.Forms.UserControl> hosted in Internet Explorer.</span></span>  
  
 [<span data-ttu-id="7a415-108">Guide pratique pour Accéder à la Source HTML dans le modèle d’objet de Document HTML managé</span><span class="sxs-lookup"><span data-stu-id="7a415-108">How to: Access the HTML Source in the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/how-to-access-the-html-source-in-the-managed-html-document-object-model.md)  
 <span data-ttu-id="7a415-109">Décrit comment obtenir la source HTML d’origine, non modifiée et comment obtenir la source « live » qui reflète l’état actuel du DOM.</span><span class="sxs-lookup"><span data-stu-id="7a415-109">Describes how to obtain the original, unmodified HTML source, and how to obtain the "live" source that reflects the current state of the DOM.</span></span>  
  
 [<span data-ttu-id="7a415-110">Guide pratique pour Modifier des Styles d’un élément dans le modèle d’objet de Document HTML managé</span><span class="sxs-lookup"><span data-stu-id="7a415-110">How to: Change Styles on an Element in the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/how-to-change-styles-on-an-element-in-the-managed-html-document-object-model.md)  
 <span data-ttu-id="7a415-111">Décrit comment manipuler les styles, qui sont utilisés pour contrôler l’affichage d’éléments.</span><span class="sxs-lookup"><span data-stu-id="7a415-111">Describes how to manipulate styles, which are used to control the visual display of elements.</span></span>  
  
 [<span data-ttu-id="7a415-112">Accès aux frames dans le modèle objet de document HTML managé</span><span class="sxs-lookup"><span data-stu-id="7a415-112">Accessing Frames in the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/accessing-frames-in-the-managed-html-document-object-model.md)  
 <span data-ttu-id="7a415-113">Décrit les cadres et des jeux de frames et indique comment accéder au DOM d’un frame.</span><span class="sxs-lookup"><span data-stu-id="7a415-113">Describes what frames and framesets are, and how to access the DOM of a frame.</span></span>  
  
 [<span data-ttu-id="7a415-114">Accès aux membres non exposés sur le modèle objet de document HTML managé</span><span class="sxs-lookup"><span data-stu-id="7a415-114">Accessing Unexposed Members on the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/accessing-unexposed-members-on-the-managed-html-document-object-model.md)  
 <span data-ttu-id="7a415-115">Décrit comment accéder aux membres du modèle DOM sous-jacent qui n’ont pas un équivalent managé.</span><span class="sxs-lookup"><span data-stu-id="7a415-115">Describes how to access members of the underlying DOM that do not have a managed equivalent.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="7a415-116">Référence</span><span class="sxs-lookup"><span data-stu-id="7a415-116">Reference</span></span>  
 <xref:System.Windows.Forms.HtmlDocument>  
  
 <xref:System.Windows.Forms.HtmlElement>  
  
 <xref:System.Windows.Forms.HtmlWindow>  
  
## <a name="related-sections"></a><span data-ttu-id="7a415-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a415-117">Related Sections</span></span>  
 [<span data-ttu-id="7a415-118">WebBrowser, contrôle</span><span class="sxs-lookup"><span data-stu-id="7a415-118">WebBrowser Control</span></span>](../../../../docs/framework/winforms/controls/webbrowser-control-windows-forms.md)  
  
## <a name="see-also"></a><span data-ttu-id="7a415-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a415-119">See also</span></span>
- [<span data-ttu-id="7a415-120">À propos du modèle objet DHTML</span><span class="sxs-lookup"><span data-stu-id="7a415-120">About the DHTML Object Model</span></span>](https://msdn.microsoft.com/library/default.asp?url=/workshop/author/om/doc_object.asp)
