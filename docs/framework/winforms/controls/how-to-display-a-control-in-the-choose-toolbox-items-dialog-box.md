---
title: 'Procédure : afficher un contrôle dans la boîte de dialogue Choisir des éléments de boîte à outils'
ms.date: 03/30/2017
helpviewer_keywords:
- global assembly cache [Windows Forms], Choose Toolbox Items dialog box
- AssemblyFoldersEx [Windows Forms], Choose Toolbox Items dialog box
- controls [Windows Forms], display in Choose Toolbox Items dialog box
- assembly folder registration [Windows Forms], Choose Toolbox Items dialog box
- Choose Toolbox Items dialog box [Windows Forms], display control
ms.assetid: 01ef6eba-d044-40f0-951d-78eff7ebd9a9
ms.openlocfilehash: d504ace9e5571246ae0e78e165a7ad2bc23fa481
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59085296"
---
# <a name="how-to-display-a-control-in-the-choose-toolbox-items-dialog-box"></a><span data-ttu-id="0e87a-102">Procédure : afficher un contrôle dans la boîte de dialogue Choisir des éléments de boîte à outils</span><span class="sxs-lookup"><span data-stu-id="0e87a-102">How to: Display a Control in the Choose Toolbox Items Dialog Box</span></span>
<span data-ttu-id="0e87a-103">Lorsque vous développez et distribuez des contrôles, vous souhaiterez peut-être ces contrôles s’affichent dans le **Choose Toolbox Items** boîte de dialogue qui s’affiche lorsque vous cliquez sur le **boîte à outils** et sélectionnez  **Choisir des éléments**.</span><span class="sxs-lookup"><span data-stu-id="0e87a-103">As you develop and distribute controls, you may want those controls to appear in the **Choose Toolbox Items** dialog box, which is displayed when you right-click the **Toolbox** and select **Choose Items**.</span></span> <span data-ttu-id="0e87a-104">Vous pouvez activer votre contrôle s’affiche dans cette boîte de dialogue à l’aide de la procédure d’inscription AssemblyFoldersEx.</span><span class="sxs-lookup"><span data-stu-id="0e87a-104">You can enable your control to appear in this dialog box by using the AssemblyFoldersEx registration procedure.</span></span>  
  
### <a name="to-display-your-control-in-the-choose-toolbox-items-dialog-box"></a><span data-ttu-id="0e87a-105">Pour afficher votre contrôle dans la boîte de dialogue Choisir des éléments de boîte à outils</span><span class="sxs-lookup"><span data-stu-id="0e87a-105">To display your control in the Choose Toolbox Items dialog box</span></span>  
  
-   <span data-ttu-id="0e87a-106">Installer votre assembly de contrôle dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="0e87a-106">Install your control assembly to the global assembly cache.</span></span> <span data-ttu-id="0e87a-107">Pour plus d'informations, voir [Procédure : installer un assembly dans le Global Assembly Cache](../../app-domains/how-to-install-an-assembly-into-the-gac.md)</span><span class="sxs-lookup"><span data-stu-id="0e87a-107">For more information, see [How to: Install an Assembly into the Global Assembly Cache](../../app-domains/how-to-install-an-assembly-into-the-gac.md)</span></span>  
  
     <span data-ttu-id="0e87a-108">- ou -</span><span class="sxs-lookup"><span data-stu-id="0e87a-108">-or-</span></span>  
  
-   <span data-ttu-id="0e87a-109">Inscrire votre contrôle et ses assemblys au moment du design associés à l’aide de la procédure d’inscription AssemblyFoldersEx.</span><span class="sxs-lookup"><span data-stu-id="0e87a-109">Register your control and its associated design-time assemblies by using the AssemblyFoldersEx registration procedure.</span></span> <span data-ttu-id="0e87a-110">AssemblyFoldersEx est un emplacement de Registre où les fournisseurs tiers stockent les chemins de chaque version du framework pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0e87a-110">AssemblyFoldersEx is a registry location where third-party vendors store paths for each version of the framework that they support.</span></span> <span data-ttu-id="0e87a-111">La résolution au moment du design peut rechercher à cet emplacement de Registre pour rechercher des assemblys de référence.</span><span class="sxs-lookup"><span data-stu-id="0e87a-111">Design-time resolution can look in this registry location to find reference assemblies.</span></span> <span data-ttu-id="0e87a-112">Le script de Registre peut spécifier les contrôles que vous souhaitez voir apparaître dans la boîte à outils.</span><span class="sxs-lookup"><span data-stu-id="0e87a-112">The registry script can specify the controls you want to appear in the Toolbox.</span></span> <span data-ttu-id="0e87a-113">Pour plus d’informations, consultez [déploiement d’un contrôle personnalisé et les assemblys au moment du Design](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee849818(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="0e87a-113">For more information, see [Deploying a Custom Control and Design-time Assemblies](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee849818(v=vs.100)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e87a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e87a-114">See also</span></span>

- <span data-ttu-id="0e87a-115">[Choisir des éléments de boîte à outils, boîte de dialogue (Visual Studio)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="0e87a-115">[Choose Toolbox Items Dialog Box (Visual Studio)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))</span></span>
- <span data-ttu-id="0e87a-116">[Déploiement d’un contrôle personnalisé et les assemblys au moment du Design](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee849818(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="0e87a-116">[Deploying a Custom Control and Design-time Assemblies](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee849818(v=vs.100))</span></span>
- [<span data-ttu-id="0e87a-117">Développement de contrôles Windows Forms au moment du design</span><span class="sxs-lookup"><span data-stu-id="0e87a-117">Developing Windows Forms Controls at Design Time</span></span>](developing-windows-forms-controls-at-design-time.md)
- [<span data-ttu-id="0e87a-118">Guide pratique pour installer un assembly dans le Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="0e87a-118">How to: Install an Assembly into the Global Assembly Cache</span></span>](../../app-domains/how-to-install-an-assembly-into-the-gac.md)
- [<span data-ttu-id="0e87a-119">Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés</span><span class="sxs-lookup"><span data-stu-id="0e87a-119">Walkthrough: Automatically Populating the Toolbox with Custom Components</span></span>](walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
