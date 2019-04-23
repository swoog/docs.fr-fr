---
title: 'Procédure : Ajouter un écran de démarrage dans une application WPF'
ms.date: 08/18/2018
helpviewer_keywords:
- WPF [WPF], splash screen
- startup window [WPF]
- SplashScreen class [WPF]
- splash screen [WPF]
ms.assetid: d70a25c4-5fb9-4c27-b01d-b1b8ef39b3fd
ms.openlocfilehash: 3120ee64d65822d323800a89466c6b707169aaaa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59307479"
---
# <a name="how-to-add-a-splash-screen-to-a-wpf-application"></a><span data-ttu-id="3a361-102">Procédure : Ajouter un écran de démarrage dans une application WPF</span><span class="sxs-lookup"><span data-stu-id="3a361-102">How to: Add a Splash Screen to a WPF Application</span></span>

<span data-ttu-id="3a361-103">Cette rubrique montre comment ajouter une fenêtre de démarrage, ou *écran de démarrage*, à une application Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="3a361-103">This topic shows how to add a startup window, or *splash screen*, to a Windows Presentation Foundation (WPF) application.</span></span>

## <a name="to-add-an-existing-image-as-a-splash-screen"></a><span data-ttu-id="3a361-104">Pour ajouter une image existante en tant qu’un écran de démarrage</span><span class="sxs-lookup"><span data-stu-id="3a361-104">To add an existing image as a splash screen</span></span>

1. <span data-ttu-id="3a361-105">Créer ou rechercher une image que vous souhaitez utiliser pour l’écran de démarrage.</span><span class="sxs-lookup"><span data-stu-id="3a361-105">Create or find an image that you want to use for the splash screen.</span></span> <span data-ttu-id="3a361-106">Vous pouvez utiliser n’importe quel format d’image pris en charge par le composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="3a361-106">You can use any image format that is supported by the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="3a361-107">Par exemple, vous pouvez utiliser le format BMP, GIF, JPEG, PNG ou TIFF.</span><span class="sxs-lookup"><span data-stu-id="3a361-107">For example, you can use the BMP, GIF, JPEG, PNG, or TIFF format.</span></span>

2. <span data-ttu-id="3a361-108">Ajoutez le fichier image au projet d’Application WPF.</span><span class="sxs-lookup"><span data-stu-id="3a361-108">Add the image file to the WPF Application project.</span></span>

3. <span data-ttu-id="3a361-109">Dans **l’Explorateur de solutions**, sélectionnez l’image.</span><span class="sxs-lookup"><span data-stu-id="3a361-109">In **Solution Explorer**, select the image.</span></span>

4. <span data-ttu-id="3a361-110">Dans la fenêtre Propriétés, cliquez sur la flèche déroulante pour le **Action de génération** propriété.</span><span class="sxs-lookup"><span data-stu-id="3a361-110">In the Properties window, click the drop-down arrow for the **Build Action** property.</span></span>

5. <span data-ttu-id="3a361-111">Sélectionnez **SplashScreen** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="3a361-111">Select **SplashScreen** from the drop-down list.</span></span>

6. <span data-ttu-id="3a361-112">Appuyez sur **F5** pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="3a361-112">Press **F5** to build and run the application.</span></span>

     <span data-ttu-id="3a361-113">L’image d’écran de démarrage s’affiche dans le centre de l’écran, puis disparaît lorsque la fenêtre principale de l’application s’affiche.</span><span class="sxs-lookup"><span data-stu-id="3a361-113">The splash screen image appears in the center of the screen, and then fades when the main application window appears.</span></span>

## <a name="to-exclude-the-splash-screen-from-build"></a><span data-ttu-id="3a361-114">Pour exclure de l’écran de démarrage à partir de la build</span><span class="sxs-lookup"><span data-stu-id="3a361-114">To exclude the splash screen from build</span></span>

1. <span data-ttu-id="3a361-115">Dans **l’Explorateur de solutions**, sélectionnez l’image d’écran de démarrage.</span><span class="sxs-lookup"><span data-stu-id="3a361-115">In **Solution Explorer**, select the splash screen image.</span></span>

2. <span data-ttu-id="3a361-116">Dans le **propriétés** fenêtre, définissez la **Action de génération** à **aucun**.</span><span class="sxs-lookup"><span data-stu-id="3a361-116">In the **Properties** window, set the **Build Action** to **None**.</span></span>

## <a name="to-remove-the-splash-screen-from-an-application"></a><span data-ttu-id="3a361-117">Pour supprimer l’écran de démarrage à partir d’une application</span><span class="sxs-lookup"><span data-stu-id="3a361-117">To remove the splash screen from an application</span></span>

<span data-ttu-id="3a361-118">Dans **l’Explorateur de solutions**, supprimez l’image d’écran de démarrage.</span><span class="sxs-lookup"><span data-stu-id="3a361-118">In **Solution Explorer**, delete the splash screen image.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a361-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a361-119">See also</span></span>

- <xref:System.Windows.SplashScreen>
- <span data-ttu-id="3a361-120">[Guide pratique pour Ajouter des éléments existants à un projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="3a361-120">[How to: Add Existing Items to a Project](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))</span></span>
