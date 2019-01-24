---
title: 'Procédure : Ajouter ou supprimer des Images ImageList avec le Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- ImageList component [Windows Forms], adding images
- ImageList component [Windows Forms], removing images
- images [Windows Forms], adding to ImageList component
ms.assetid: 5699b244-e37c-4d20-bc35-7441e55c1e3a
ms.openlocfilehash: f03ad1735d7da450d6ebc10c227e3f2bbb41a3d8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54688140"
---
# <a name="how-to-add-or-remove-imagelist-images-with-the-designer"></a><span data-ttu-id="e5002-102">Procédure : Ajouter ou supprimer des Images ImageList avec le Concepteur</span><span class="sxs-lookup"><span data-stu-id="e5002-102">How to: Add or Remove ImageList Images with the Designer</span></span>
<span data-ttu-id="e5002-103">Vous pouvez ajouter des images à un <xref:System.Windows.Forms.ImageList> composant plusieurs façons différentes.</span><span class="sxs-lookup"><span data-stu-id="e5002-103">You can add images to an <xref:System.Windows.Forms.ImageList> component several different ways.</span></span> <span data-ttu-id="e5002-104">Vous pouvez ajouter très rapidement des images à l’aide de la balise active associée le <xref:System.Windows.Forms.ImageList>, ou si vous définissez plusieurs autres propriétés sur le <xref:System.Windows.Forms.ImageList>, vous pouvez s’avérer plus facile d’ajouter des images avec la fenêtre Propriétés.</span><span class="sxs-lookup"><span data-stu-id="e5002-104">You can add images very quickly by using the smart tag associated with the <xref:System.Windows.Forms.ImageList>, or if you are setting several other properties on the <xref:System.Windows.Forms.ImageList>, you may find it more convenient to add images with the Properties window.</span></span> <span data-ttu-id="e5002-105">Vous pouvez également ajouter des images à l’aide de code.</span><span class="sxs-lookup"><span data-stu-id="e5002-105">You can also add images by using code.</span></span> <span data-ttu-id="e5002-106">Pour plus d’informations sur la façon d’ajouter des images avec le code, consultez [Comment : Ajouter ou supprimer des Images avec les Windows Forms composant ImageList](../../../../docs/framework/winforms/controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span><span class="sxs-lookup"><span data-stu-id="e5002-106">For more information about how to add images with code, see [How to: Add or Remove Images with the Windows Forms ImageList Component](../../../../docs/framework/winforms/controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span></span> <span data-ttu-id="e5002-107">En général vous remplissez le <xref:System.Windows.Forms.ImageList> composant avec des images avant il est associé à un contrôle, mais cela n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e5002-107">Typically you populate the <xref:System.Windows.Forms.ImageList> component with images before it is associated with a control, but this is not required.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e5002-108">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="e5002-108">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="e5002-109">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="e5002-109">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="e5002-110">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="e5002-110">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-add-or-remove-images-by-using-the-properties-window"></a><span data-ttu-id="e5002-111">Pour ajouter ou supprimer des images à l’aide de la fenêtre Propriétés</span><span class="sxs-lookup"><span data-stu-id="e5002-111">To add or remove images by using the Properties window</span></span>  
  
1.  <span data-ttu-id="e5002-112">Sélectionnez le <xref:System.Windows.Forms.ImageList> composant, ou en ajouter un au formulaire.</span><span class="sxs-lookup"><span data-stu-id="e5002-112">Select the <xref:System.Windows.Forms.ImageList> component, or add one to the form.</span></span>  
  
2.  <span data-ttu-id="e5002-113">Dans la fenêtre Propriétés, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) à côté du <xref:System.Windows.Forms.ImageList.Images%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="e5002-113">In the Properties window, click the ellipsis button (![VisualStudioEllipsesButton screenshot](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) next to the <xref:System.Windows.Forms.ImageList.Images%2A> property.</span></span>  
  
3.  <span data-ttu-id="e5002-114">Dans le **éditeur de Collection d’images**, cliquez sur **ajouter** ou **supprimer** pour ajouter ou supprimer des images à partir de la liste.</span><span class="sxs-lookup"><span data-stu-id="e5002-114">In the **Image Collection Editor**, click **Add** or **Remove** to add or remove images from the list.</span></span>  
  
### <a name="to-add-or-remove-images-using-the-smart-tag"></a><span data-ttu-id="e5002-115">Pour ajouter ou supprimer des images à l’aide de la balise active</span><span class="sxs-lookup"><span data-stu-id="e5002-115">To add or remove images using the smart tag</span></span>  
  
1.  <span data-ttu-id="e5002-116">Sélectionnez le <xref:System.Windows.Forms.ImageList> composant, ou en ajouter un au formulaire.</span><span class="sxs-lookup"><span data-stu-id="e5002-116">Select the <xref:System.Windows.Forms.ImageList> component, or add one to the form.</span></span>  
  
2.  <span data-ttu-id="e5002-117">Cliquez sur le glyphe de balise active (![glyphe de balise active](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph"))</span><span class="sxs-lookup"><span data-stu-id="e5002-117">Click the smart tag glyph (![Smart Tag Glyph](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph"))</span></span>  
  
3.  <span data-ttu-id="e5002-118">Dans le **tâches ImageList** boîte de dialogue, sélectionnez **choisir des Images**.</span><span class="sxs-lookup"><span data-stu-id="e5002-118">In the **ImageList Tasks** dialog box, select **Choose Images**.</span></span>  
  
4.  <span data-ttu-id="e5002-119">Dans le **éditeur de collections d’Images** cliquez sur **ajouter** ou **supprimer** pour ajouter ou supprimer des images à partir de la liste.</span><span class="sxs-lookup"><span data-stu-id="e5002-119">In the **Images Collection Editor** click **Add** or **Remove** to add or remove images from the list.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5002-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5002-120">See also</span></span>
- [<span data-ttu-id="e5002-121">Images, bitmaps et métafichiers</span><span class="sxs-lookup"><span data-stu-id="e5002-121">Images, Bitmaps, and Metafiles</span></span>](../../../../docs/framework/winforms/advanced/images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="e5002-122">Procédure pas à pas : Effectuer des tâches courantes à l’aide d’intelligent des balises sur Windows Forms contrôles</span><span class="sxs-lookup"><span data-stu-id="e5002-122">Walkthrough: Performing Common Tasks Using Smart Tags on Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/performing-common-tasks-using-smart-tags-on-wf-controls.md)
- [<span data-ttu-id="e5002-123">ImageList, composant</span><span class="sxs-lookup"><span data-stu-id="e5002-123">ImageList Component</span></span>](../../../../docs/framework/winforms/controls/imagelist-component-windows-forms.md)
