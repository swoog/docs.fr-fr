---
title: Vue d'ensemble du composant FontDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- FontDialog
helpviewer_keywords:
- Font dialog box [Windows Forms], Windows Forms
- Font dialog box
- FontDialog component [Windows Forms], about FontDialog component
ms.assetid: daf46e57-1b4b-4b7a-bad0-b50ca7ba75dc
ms.openlocfilehash: 854f54454c0c88f965d9ac8240c11f6821f0c64b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54594562"
---
# <a name="fontdialog-component-overview-windows-forms"></a><span data-ttu-id="df66a-102">Vue d'ensemble du composant FontDialog (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="df66a-102">FontDialog Component Overview (Windows Forms)</span></span>
<span data-ttu-id="df66a-103">Les formulaires Windows <xref:System.Windows.Forms.FontDialog> composant est une boîte de dialogue préconfigurée qui est le standard Windows **police** boîte de dialogue permet d’exposer les polices qui sont actuellement installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="df66a-103">The Windows Forms <xref:System.Windows.Forms.FontDialog> component is a pre-configured dialog box, which is the standard Windows **Font** dialog box used to expose the fonts that are currently installed on the system.</span></span> <span data-ttu-id="df66a-104">Utilisez-la dans votre application Windows comme une solution simple pour la sélection de police que de configurer votre propre boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="df66a-104">Use it within your Windows-based application as a simple solution for font selection in lieu of configuring your own dialog box.</span></span>  
  
 <span data-ttu-id="df66a-105">Par défaut, la boîte de dialogue affiche les zones de liste pour la police, style de police et la taille ; cases à cocher pour les effets comme barré et souligné ; une liste déroulante pour le Script ; et un exemple montrant comment la police s’affiche.</span><span class="sxs-lookup"><span data-stu-id="df66a-105">By default, the dialog box shows list boxes for Font, Font style, and Size; check boxes for effects like Strikeout and Underline; a drop-down list for Script; and a sample of how the font will appear.</span></span> <span data-ttu-id="df66a-106">(Script fait référence à différents jeux de caractères qui est disponibles pour une police, par exemple, hébreu ou le japonais.) Pour afficher la boîte de dialogue Police, appelez le <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="df66a-106">(Script refers to different character scripts that are available for a given font, for example, Hebrew or Japanese.) To display the font dialog box, call the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method.</span></span>  
  
## <a name="key-properties"></a><span data-ttu-id="df66a-107">Propriétés de clé</span><span class="sxs-lookup"><span data-stu-id="df66a-107">Key Properties</span></span>  
 <span data-ttu-id="df66a-108">Le composant a un nombre de propriétés qui définissent son apparence.</span><span class="sxs-lookup"><span data-stu-id="df66a-108">The component has a number of properties that configure its appearance.</span></span> <span data-ttu-id="df66a-109">Les propriétés qui définissent les sélections de la boîte de dialogue sont <xref:System.Windows.Forms.FontDialog.Font%2A> et <xref:System.Windows.Forms.FontDialog.Color%2A>.</span><span class="sxs-lookup"><span data-stu-id="df66a-109">The properties that set the dialog-box selections are <xref:System.Windows.Forms.FontDialog.Font%2A> and <xref:System.Windows.Forms.FontDialog.Color%2A>.</span></span> <span data-ttu-id="df66a-110">Le <xref:System.Windows.Forms.FontDialog.Font%2A> propriété définit la police, le style, taille, script et effets ; par exemple, `Arial, 10pt, style=Italic, Strikeout`.</span><span class="sxs-lookup"><span data-stu-id="df66a-110">The <xref:System.Windows.Forms.FontDialog.Font%2A> property sets the font, style, size, script, and effects; for example, `Arial, 10pt, style=Italic, Strikeout`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df66a-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df66a-111">See also</span></span>
- <xref:System.Windows.Forms.FontDialog>
- [<span data-ttu-id="df66a-112">FontDialog, composant</span><span class="sxs-lookup"><span data-stu-id="df66a-112">FontDialog Component</span></span>](../../../../docs/framework/winforms/controls/fontdialog-component-windows-forms.md)
