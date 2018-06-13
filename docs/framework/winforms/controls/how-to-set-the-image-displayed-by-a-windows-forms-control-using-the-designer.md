---
title: "Comment : définir l'image affichée par un contrôle Windows Forms à l'aide du concepteur"
ms.date: 03/30/2017
helpviewer_keywords:
- Button control [Windows Forms], images
- Windows Forms controls, images
- controls [Windows Forms], images
- images [Windows Forms], Windows Forms controls
- examples [Windows Forms], controls
- setting images [Windows Forms], Windows Forms controls
ms.assetid: ae80d07a-e469-4251-90ca-df71f5852454
ms.openlocfilehash: b3625510028d5941173848849ab915f56260577a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33532783"
---
# <a name="how-to-set-the-image-displayed-by-a-windows-forms-control-using-the-designer"></a><span data-ttu-id="d95be-102">Comment : définir l'image affichée par un contrôle Windows Forms à l'aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="d95be-102">How to: Set the Image Displayed by a Windows Forms Control Using the Designer</span></span>
<span data-ttu-id="d95be-103">Plusieurs contrôles Windows Forms peuvent afficher des images.</span><span class="sxs-lookup"><span data-stu-id="d95be-103">Several Windows Forms controls can display images.</span></span> <span data-ttu-id="d95be-104">L’image peut être une icône qui explicite le but du contrôle, comme une icône de disquette sur un bouton qui dénote le **enregistrer** commande.</span><span class="sxs-lookup"><span data-stu-id="d95be-104">The image can be an icon that clarifies the purpose of the control, such as a disk icon on a button denoting the **Save** command.</span></span> <span data-ttu-id="d95be-105">L’icône peut également être une image d’arrière-plan pour donner au contrôle l’apparence souhaitée.</span><span class="sxs-lookup"><span data-stu-id="d95be-105">Alternatively, the icon can be a background image to give the control the appearance you want.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d95be-106">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="d95be-106">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="d95be-107">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="d95be-107">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="d95be-108">Pour plus d’informations, consultez [Personnalisation des paramètres de développement dans Visual Studio](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3).</span><span class="sxs-lookup"><span data-stu-id="d95be-108">For more information, see [Customizing Development Settings in Visual Studio](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3).</span></span>  
  
### <a name="to-set-the-image-displayed-by-a-control"></a><span data-ttu-id="d95be-109">Pour définir l’image affichée par un contrôle</span><span class="sxs-lookup"><span data-stu-id="d95be-109">To set the image displayed by a control</span></span>  
  
1.  <span data-ttu-id="d95be-110">Dans le **propriétés** fenêtre, sélectionnez le **Image** ou **BackgroundImage** propriété du contrôle, puis cliquez sur le bouton de sélection ()</span><span class="sxs-lookup"><span data-stu-id="d95be-110">In the **Properties** window, select the **Image** or **BackgroundImage** property of the control, then click the ellipsis button (</span></span>  
  
     <span data-ttu-id="d95be-111">![Capture d’écran de VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")</span><span class="sxs-lookup"><span data-stu-id="d95be-111">![VisualStudioEllipsesButton screenshot](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")</span></span>  
  
     <span data-ttu-id="d95be-112">) pour afficher la **sélectionner une ressource** boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d95be-112">) to display the **Select Resource** dialog box.</span></span>  
  
2.  <span data-ttu-id="d95be-113">Sélectionnez l’image que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="d95be-113">Select the image you want to display.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d95be-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d95be-114">See Also</span></span>  
 <xref:System.Drawing.Image.FromFile%2A>  
 <xref:System.Drawing.Image>  
 <xref:System.Windows.Forms.Control.BackgroundImage%2A>  
 [<span data-ttu-id="d95be-115">Création d'étiquettes et de raccourcis pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d95be-115">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
