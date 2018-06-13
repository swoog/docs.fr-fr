---
title: Écriture de projets ciblant le .NET Framework versions 3.0 et 3.5 dans Visual Studio 2010
ms.date: 03/30/2017
ms.assetid: 81858ab7-763c-4eac-83fe-d7205e5c4c98
ms.openlocfilehash: 1469ce2906c1101bae4098cbcabd4a10a64c1c7e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33513817"
---
# <a name="writing-projects-targeting-the-net-framework-30-and-35-in-visual-studio-2010"></a><span data-ttu-id="bd064-102">Écriture de projets ciblant le .NET Framework versions 3.0 et 3.5 dans Visual Studio 2010</span><span class="sxs-lookup"><span data-stu-id="bd064-102">Writing Projects Targeting the .NET Framework 3.0 and 3.5 in Visual Studio 2010</span></span>
<span data-ttu-id="bd064-103">Vous pouvez utiliser [!INCLUDE[vs2010](../../../includes/vs2010-md.md)] pour créer des projets qui ciblent le [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] version 3.0 ou 3.5.</span><span class="sxs-lookup"><span data-stu-id="bd064-103">You can use [!INCLUDE[vs2010](../../../includes/vs2010-md.md)] to create projects that target the [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] version 3.0 or 3.5.</span></span> <span data-ttu-id="bd064-104">Cette rubrique décrit comment procéder.</span><span class="sxs-lookup"><span data-stu-id="bd064-104">This topic describes how to do this.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bd064-105">Lorsque vous ajoutez des activités, assurez-vous que la version souhaitée du [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] est définie.</span><span class="sxs-lookup"><span data-stu-id="bd064-105">When adding activities, make sure that the desired version of the [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] is set.</span></span> <span data-ttu-id="bd064-106">La modification de la version cible du workflow après que les activités ont été ajoutées entraînera l'échec de la validation du workflow.</span><span class="sxs-lookup"><span data-stu-id="bd064-106">Changing the target version of the workflow after activities are added will cause the workflow to fail validation.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="bd064-107">L'ouverture de workflows existants dans [!INCLUDE[vs2010](../../../includes/vs2010-md.md)] qui ont des activités .Net Framework 3.5 provoquera une erreur au niveau de `this.SetValue()`.</span><span class="sxs-lookup"><span data-stu-id="bd064-107">Opening existing workflows in [!INCLUDE[vs2010](../../../includes/vs2010-md.md)] that have .Net Framework 3.5 activities will cause an error at `this.SetValue()`.</span></span> <span data-ttu-id="bd064-108">Pour ouvrir les projets créés dans les versions antérieures du .NET Framework, ouvrez d'abord un workflow vide dans le concepteur, puis ajoutez une activité .NET Framework 3.5.</span><span class="sxs-lookup"><span data-stu-id="bd064-108">In order to open projects created with previous versions of the .Net Framework, first open a blank workflow in the designer and add a .Net Framework 3.5 activity.</span></span>  
  
## <a name="to-create-a-net-framework--30-or-35-project-with-visual-studio-2010"></a><span data-ttu-id="bd064-109">Pour créer un projet .NET Framework 3.0 ou 3.5 avec Visual Studio 2010</span><span class="sxs-lookup"><span data-stu-id="bd064-109">To create a .NET Framework  3.0 or 3.5 project with Visual Studio 2010</span></span>  
  
1.  <span data-ttu-id="bd064-110">Ouvrez [!INCLUDE[vs2010](../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="bd064-110">Open [!INCLUDE[vs2010](../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="bd064-111">Sélectionnez **fichier**, **nouveau**, **projet**.</span><span class="sxs-lookup"><span data-stu-id="bd064-111">Select **File**, **New**, **Project**.</span></span>  
  
3.  <span data-ttu-id="bd064-112">Dans la liste déroulante en haut de la boîte de dialogue, sélectionnez la version souhaitée du [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)].</span><span class="sxs-lookup"><span data-stu-id="bd064-112">In the drop-down list at the top of the dialog box, select the desired version of the [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)].</span></span>  
  
## <a name="to-upgrade-the-targeted-version-of-the-net-framework"></a><span data-ttu-id="bd064-113">Pour mettre à niveau la version ciblée du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="bd064-113">To upgrade the targeted version of the .NET Framework</span></span>  
  
1.  <span data-ttu-id="bd064-114">Cliquez sur le projet dans l’Explorateur de solutions, puis sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="bd064-114">Right-click the project in Solution Explorer, and select **Properties**.</span></span>  
  
2.  <span data-ttu-id="bd064-115">Dans le **Framework cible** liste déroulante, sélectionnez la version souhaitée.</span><span class="sxs-lookup"><span data-stu-id="bd064-115">In the **Target Framework** drop-down list, select the desired version.</span></span>
