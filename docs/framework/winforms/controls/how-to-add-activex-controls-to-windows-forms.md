---
title: 'Procédure : ajouter des contrôles ActiveX à des Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, ActiveX controls
- forms [Windows Forms], adding ActiveX controls
- ActiveX controls [Windows Forms], adding
ms.assetid: 54a61e5b-555e-4887-b41e-6244fed271eb
ms.openlocfilehash: 780411949c543a2178de5e7c531bd2202703f27a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59166047"
---
# <a name="how-to-add-activex-controls-to-windows-forms"></a><span data-ttu-id="e50fd-102">Procédure : ajouter des contrôles ActiveX à des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e50fd-102">How to: Add ActiveX Controls to Windows Forms</span></span>
<span data-ttu-id="e50fd-103">Alors que le Concepteur de formulaires Windows est optimisé pour héberger des contrôles Windows Forms, vous pouvez également placer des contrôles ActiveX sur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e50fd-103">While the Windows Forms Designer is optimized to host Windows Forms controls, you can also put ActiveX controls on Windows Forms.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="e50fd-104">Il existe des limitations de performances pour les Windows Forms lorsque des contrôles ActiveX leur sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="e50fd-104">There are performance limitations for Windows Forms when ActiveX controls are added to them.</span></span>  
  
 <span data-ttu-id="e50fd-105">Avant d’ajouter des contrôles ActiveX à votre formulaire, vous devez les ajouter à la boîte à outils.</span><span class="sxs-lookup"><span data-stu-id="e50fd-105">Before you add ActiveX controls to your form, you must add them to the Toolbox.</span></span> <span data-ttu-id="e50fd-106">Pour plus d’informations, consultez [des composants COM, boîte de dialogue Personnaliser la boîte à outils](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/cby6tzh5(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="e50fd-106">For more information, see [COM Components, Customize Toolbox Dialog Box](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/cby6tzh5(v=vs.100)).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e50fd-107">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="e50fd-107">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="e50fd-108">Pour modifier ces paramètres, cliquez sur **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="e50fd-108">To change your settings, click **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="e50fd-109">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="e50fd-109">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-add-an-activex-control-to-your-windows-form"></a><span data-ttu-id="e50fd-110">Pour ajouter un contrôle ActiveX à votre formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="e50fd-110">To add an ActiveX control to your Windows Form</span></span>  
  
-   <span data-ttu-id="e50fd-111">Double-cliquez sur le contrôle sur la boîte à outils.</span><span class="sxs-lookup"><span data-stu-id="e50fd-111">Double-click the control on the Toolbox.</span></span>  
  
     <span data-ttu-id="e50fd-112">Visual Studio ajoute toutes les références au contrôle dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="e50fd-112">Visual Studio adds all references to the control in your project.</span></span> <span data-ttu-id="e50fd-113">Pour plus d’informations sur les éléments à prendre en compte lors de l’utilisation de contrôles ActiveX sur Windows Forms, consultez [considérations sur l’hébergement d’un contrôle ActiveX sur un formulaire Windows](considerations-when-hosting-an-activex-control-on-a-windows-form.md).</span><span class="sxs-lookup"><span data-stu-id="e50fd-113">For more information about things to keep in mind when using ActiveX controls on Windows Forms, see [Considerations When Hosting an ActiveX Control on a Windows Form](considerations-when-hosting-an-activex-control-on-a-windows-form.md).</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="e50fd-114">Windows Forms ActiveX Control Importer (AxImp.exe) crée des arguments d’événement d’un type différent que prévu lors de l’importation de bibliothèques de liens dynamiques ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e50fd-114">The Windows Forms ActiveX Control Importer (AxImp.exe) creates event arguments of a different type than expected upon importation of ActiveX dynamic link libraries.</span></span> <span data-ttu-id="e50fd-115">Les arguments créés par AxImp.exe sont semblables à ce qui suit : `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEvent e)`, lorsque `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEventArgs e)` est attendu.</span><span class="sxs-lookup"><span data-stu-id="e50fd-115">The arguments created by AxImp.exe are similar to the following: `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEvent e)`, when `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEventArgs e)` is expected.</span></span> <span data-ttu-id="e50fd-116">N’oubliez pas que cette anomalie n’empêche pas le code de fonctionner normalement.</span><span class="sxs-lookup"><span data-stu-id="e50fd-116">Be aware that this irregularity does not prevent code from functioning normally.</span></span> <span data-ttu-id="e50fd-117">Pour plus d’informations, consultez [Windows Forms ActiveX Control Importer (Aximp.exe)](../../tools/aximp-exe-windows-forms-activex-control-importer.md).</span><span class="sxs-lookup"><span data-stu-id="e50fd-117">For details, see [Windows Forms ActiveX Control Importer (Aximp.exe)](../../tools/aximp-exe-windows-forms-activex-control-importer.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e50fd-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e50fd-118">See also</span></span>

- [<span data-ttu-id="e50fd-119">contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e50fd-119">Windows Forms Controls</span></span>](index.md)
- [<span data-ttu-id="e50fd-120">Comparaison des contrôles et des objets programmables dans divers langages et bibliothèques</span><span class="sxs-lookup"><span data-stu-id="e50fd-120">Controls and Programmable Objects Compared in Various Languages and Libraries</span></span>](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0061wezk(v=vs.100))
- [<span data-ttu-id="e50fd-121">Procédure : ajouter des contrôles à des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e50fd-121">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
- [<span data-ttu-id="e50fd-122">Disposition des contrôles dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e50fd-122">Arranging Controls on Windows Forms</span></span>](arranging-controls-on-windows-forms.md)
- [<span data-ttu-id="e50fd-123">Création d'étiquettes et de raccourcis pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e50fd-123">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [<span data-ttu-id="e50fd-124">Contrôles à utiliser dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e50fd-124">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
- [<span data-ttu-id="e50fd-125">Classement par fonction des contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e50fd-125">Windows Forms Controls by Function</span></span>](windows-forms-controls-by-function.md)
