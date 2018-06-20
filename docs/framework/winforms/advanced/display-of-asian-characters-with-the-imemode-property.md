---
title: Affichage des caractères asiatiques avec la propriété ImeMode
ms.date: 03/30/2017
helpviewer_keywords:
- Asian languages [Windows Forms], displaying with ImeMode
- Chinese characters [Windows Forms], displaying with ImeMode
- IME mode
- Japanese characters [Windows Forms], displaying with ImeMode
- international applications [Windows Forms], character display
- international characters
- Korean characters
- Asian languages
- Input Method Editor (IME), mode
- localization [Windows Forms], character sets
- globalization [Windows Forms], character sets
ms.assetid: c60ae399-0dab-4f07-9dea-6dbfb15ec0ae
ms.openlocfilehash: d3733f642d4218c851040582ee5637b5486a7804
ms.sourcegitcommit: 6bc4efca63e526ce6f2d257fa870f01f8c459ae4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36208583"
---
# <a name="display-of-asian-characters-with-the-imemode-property"></a><span data-ttu-id="e489c-102">Affichage des caractères asiatiques avec la propriété ImeMode</span><span class="sxs-lookup"><span data-stu-id="e489c-102">Display of Asian Characters with the ImeMode Property</span></span>
<span data-ttu-id="e489c-103">Le <xref:System.Windows.Forms.Control.ImeMode%2A> propriété est utilisée par les formulaires et les contrôles pour forcer un mode spécifique pour un éditeur de méthode d’entrée (IME).</span><span class="sxs-lookup"><span data-stu-id="e489c-103">The <xref:System.Windows.Forms.Control.ImeMode%2A> property is used by forms and controls to force a specific mode for an input method editor (IME).</span></span> <span data-ttu-id="e489c-104">L’IME est un composant essentiel pour écrire en chinois, japonais et coréen, étant donné que ces systèmes d’écriture ont plus de caractères que ce que vous pouvez coder pour un clavier standard.</span><span class="sxs-lookup"><span data-stu-id="e489c-104">The IME is an essential component for writing Chinese, Japanese, and Korean scripts, since these writing systems have more characters than can be encoded for a regular keyboard.</span></span> <span data-ttu-id="e489c-105">Par exemple, vous voulez autoriser uniquement des caractères ASCII dans une zone de texte particulière.</span><span class="sxs-lookup"><span data-stu-id="e489c-105">For example, you may want to allow only ASCII characters in a particular text box.</span></span> <span data-ttu-id="e489c-106">Dans ce cas, vous pouvez définir le <xref:System.Windows.Forms.Control.ImeMode%2A> propriété <xref:System.Windows.Forms.ImeMode> et les utilisateurs seulement sera en mesure d’entrer des caractères ASCII pour cette zone de texte particulière.</span><span class="sxs-lookup"><span data-stu-id="e489c-106">In such a case you can set the <xref:System.Windows.Forms.Control.ImeMode%2A> property to <xref:System.Windows.Forms.ImeMode> and users will only be able to enter ASCII characters for that particular text box.</span></span> <span data-ttu-id="e489c-107">La valeur par défaut de la <xref:System.Windows.Forms.Control.ImeMode%2A> propriété <xref:System.Windows.Forms.ImeMode>, de sorte que si vous définissez la propriété d’un formulaire, tous les contrôles sur le formulaire héritent ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="e489c-107">The default value of the <xref:System.Windows.Forms.Control.ImeMode%2A> property is <xref:System.Windows.Forms.ImeMode>, so if you set the property for a form, all controls on the form will inherit that setting.</span></span> <span data-ttu-id="e489c-108">Pour plus d’informations, consultez <xref:System.Windows.Forms.Control.ImeMode%2A> ) et <xref:System.Windows.Forms.ImeMode>.</span><span class="sxs-lookup"><span data-stu-id="e489c-108">For more information, see <xref:System.Windows.Forms.Control.ImeMode%2A> ) and <xref:System.Windows.Forms.ImeMode>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e489c-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e489c-109">See also</span></span>

[<span data-ttu-id="e489c-110">Globalisation des applications Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e489c-110">Globalizing Windows Forms applications</span></span>](globalizing-windows-forms.md)
