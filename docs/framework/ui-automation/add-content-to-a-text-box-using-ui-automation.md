---
title: Ajouter du contenu à une zone de texte à l'aide d'UI Automation
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adding content to text boxes
- text boxes, adding content
- UI Automation, adding content to text boxes
ms.assetid: 8bdd1a73-1ecb-4a05-a891-a7827ebb767f
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: 7c4772d36a88dfede04f7592c1cab776ddcd7d7d
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47084356"
---
# <a name="add-content-to-a-text-box-using-ui-automation"></a><span data-ttu-id="423b5-102">Ajouter du contenu à une zone de texte à l'aide d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="423b5-102">Add Content to a Text Box Using UI Automation</span></span>
> [!NOTE]
>  <span data-ttu-id="423b5-103">Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>.</span><span class="sxs-lookup"><span data-stu-id="423b5-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="423b5-104">Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span><span class="sxs-lookup"><span data-stu-id="423b5-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="423b5-105">Cette rubrique contient des exemples de code qui montre comment utiliser [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] pour insérer du texte dans une zone de texte à ligne unique.</span><span class="sxs-lookup"><span data-stu-id="423b5-105">This topic contains example code that demonstrates how to use [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] to insert text into a single-line text box.</span></span> <span data-ttu-id="423b5-106">Une autre méthode est fournie pour les contrôles de texte enrichi et multilignes où [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] n’est pas applicable.</span><span class="sxs-lookup"><span data-stu-id="423b5-106">An alternate method is provided for multi-line and rich text controls where [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] is not applicable.</span></span> <span data-ttu-id="423b5-107">À des fins de comparaison, l’exemple montre également comment utiliser les méthodes Win32 pour obtenir les mêmes résultats.</span><span class="sxs-lookup"><span data-stu-id="423b5-107">For comparison purposes, the example also demonstrates how to use Win32 methods to accomplish the same results.</span></span>  
  
## <a name="example"></a><span data-ttu-id="423b5-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="423b5-108">Example</span></span>  
 <span data-ttu-id="423b5-109">L’exemple suivant parcourt une séquence de contrôles de texte dans une application cible.</span><span class="sxs-lookup"><span data-stu-id="423b5-109">The following example steps through a sequence of text controls in a target application.</span></span> <span data-ttu-id="423b5-110">Chaque contrôle de texte est testé pour voir si un <xref:System.Windows.Automation.ValuePattern> objet peut être obtenu à partir de celui-ci à l’aide de la <xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="423b5-110">Each text control is tested to see if a <xref:System.Windows.Automation.ValuePattern> object can be obtained from it using the <xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A> method.</span></span> <span data-ttu-id="423b5-111">Si le contrôle de texte ne prend pas en charge <xref:System.Windows.Automation.ValuePattern>, le <xref:System.Windows.Automation.ValuePattern.SetValue%2A> méthode est utilisée pour insérer une chaîne définie par l’utilisateur dans le contrôle de texte.</span><span class="sxs-lookup"><span data-stu-id="423b5-111">If the text control does support <xref:System.Windows.Automation.ValuePattern>, the <xref:System.Windows.Automation.ValuePattern.SetValue%2A> method is used to insert a user-defined string into the text control.</span></span> <span data-ttu-id="423b5-112">Sinon, le <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType> méthode est utilisée.</span><span class="sxs-lookup"><span data-stu-id="423b5-112">Otherwise, the <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType> method is used.</span></span>  
  
 [!code-csharp[InsertText#InsertText](../../../samples/snippets/csharp/VS_Snippets_Wpf/InsertText/CSharp/Window1.xaml.cs#inserttext)]
 [!code-vb[InsertText#InsertText](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/InsertText/VisualBasic/Window1.xaml.vb#inserttext)]  
  
## <a name="see-also"></a><span data-ttu-id="423b5-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="423b5-113">See Also</span></span>  
 [<span data-ttu-id="423b5-114">Exemple de texte TextPattern Insert</span><span class="sxs-lookup"><span data-stu-id="423b5-114">TextPattern Insert Text Sample</span></span>](https://msdn.microsoft.com/library/67353f93-7ee2-42f2-ab76-5c078cf6ca16)
