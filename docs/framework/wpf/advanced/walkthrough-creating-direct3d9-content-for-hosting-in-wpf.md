---
title: 'Procédure pas à pas : Création de contenu Direct3D9 à héberger dans WPF'
ms.date: 03/30/2017
dev_langs:
- cpp
helpviewer_keywords:
- WPF [WPF], creating Direct3D9 content
- Direct3D9 [WPF interoperability], creating Direct3D9 content
ms.assetid: 286e98bc-1eaa-4b5e-923d-3490a9cca5fc
ms.openlocfilehash: 192036836dfb010274944006feea44e5d81ff4e3
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53168746"
---
# <a name="walkthrough-creating-direct3d9-content-for-hosting-in-wpf"></a><span data-ttu-id="e1c2e-102">Procédure pas à pas : Création de contenu Direct3D9 à héberger dans WPF</span><span class="sxs-lookup"><span data-stu-id="e1c2e-102">Walkthrough: Creating Direct3D9 Content for Hosting in WPF</span></span>
<span data-ttu-id="e1c2e-103">Cette procédure pas à pas montre comment créer un contenu Direct3D9 à héberger dans une application Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="e1c2e-103">This walkthrough shows how to create Direct3D9 content that is suitable for hosting in a Windows Presentation Foundation (WPF) application.</span></span> <span data-ttu-id="e1c2e-104">Pour plus d’informations sur l’hébergement de contenu Direct3D9 dans les applications WPF, consultez [interopérabilité WPF et Direct3D9](../../../../docs/framework/wpf/advanced/wpf-and-direct3d9-interoperation.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2e-104">For more information on hosting Direct3D9 content in WPF applications, see [WPF and Direct3D9 Interoperation](../../../../docs/framework/wpf/advanced/wpf-and-direct3d9-interoperation.md).</span></span>

 <span data-ttu-id="e1c2e-105">Lors de cette procédure pas à pas, vous allez exécuter les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1c2e-105">In this walkthrough, you perform the following tasks:</span></span>

-   <span data-ttu-id="e1c2e-106">Créez un projet Direct3D9.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-106">Create a Direct3D9 project.</span></span>

-   <span data-ttu-id="e1c2e-107">Configurer le projet Direct3D9 à héberger dans une application WPF.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-107">Configure the Direct3D9 project for hosting in a WPF application.</span></span>

 <span data-ttu-id="e1c2e-108">Lorsque vous avez terminé, vous devez une DLL qui contient le contenu Direct3D9 à utiliser dans une application WPF.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-108">When you are finished, you will have a DLL that contains Direct3D9 content for use in a WPF application.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e1c2e-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="e1c2e-109">Prerequisites</span></span>
 <span data-ttu-id="e1c2e-110">Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="e1c2e-110">You need the following components to complete this walkthrough:</span></span>

-   <span data-ttu-id="e1c2e-111">Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-111">Visual Studio 2010.</span></span>

-   <span data-ttu-id="e1c2e-112">DirectX SDK 9 ou version ultérieur.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-112">DirectX SDK 9 or later.</span></span>

## <a name="creating-the-direct3d9-project"></a><span data-ttu-id="e1c2e-113">Création du projet Direct3D9</span><span class="sxs-lookup"><span data-stu-id="e1c2e-113">Creating the Direct3D9 Project</span></span>
 <span data-ttu-id="e1c2e-114">La première étape consiste à créer et configurer le projet Direct3D9.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-114">The first step is to create and configure the Direct3D9 project.</span></span>

#### <a name="to-create-the-direct3d9-project"></a><span data-ttu-id="e1c2e-115">Pour créer le projet Direct3D9</span><span class="sxs-lookup"><span data-stu-id="e1c2e-115">To create the Direct3D9 project</span></span>

1.  <span data-ttu-id="e1c2e-116">Créez un projet Win32 en C++ nommé `D3DContent`.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-116">Create a new Win32 Project in C++ named `D3DContent`.</span></span>

     <span data-ttu-id="e1c2e-117">L’Assistant Application Win32 s’ouvre et affiche l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-117">The Win32 Application Wizard opens and displays the Welcome screen.</span></span>

2.  <span data-ttu-id="e1c2e-118">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-118">Click **Next**.</span></span>

     <span data-ttu-id="e1c2e-119">L’écran de paramètres de l’Application s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-119">The Application Settings screen appears.</span></span>

3.  <span data-ttu-id="e1c2e-120">Dans le **type d’Application :** section, sélectionnez le **DLL** option.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-120">In the **Application type:** section, select the **DLL** option.</span></span>

4.  <span data-ttu-id="e1c2e-121">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-121">Click **Finish**.</span></span>

     <span data-ttu-id="e1c2e-122">Le projet D3DContent est généré.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-122">The D3DContent project is generated.</span></span>

5.  <span data-ttu-id="e1c2e-123">Dans l’Explorateur de solutions, cliquez sur le projet D3DContent, puis sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-123">In Solution Explorer, right-click the D3DContent project and select **Properties**.</span></span>

     <span data-ttu-id="e1c2e-124">Le **Pages de propriétés de D3DContent** boîte de dialogue s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-124">The **D3DContent Property Pages** dialog box opens.</span></span>

6.  <span data-ttu-id="e1c2e-125">Sélectionnez le **C/C++** nœud.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-125">Select the **C/C++** node.</span></span>

7.  <span data-ttu-id="e1c2e-126">Dans le **autres répertoires Include** champ, spécifiez l’emplacement de DirectX incluent le dossier.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-126">In the **Additional Include Directories** field, specify the location of the DirectX include folder.</span></span> <span data-ttu-id="e1c2e-127">L’emplacement par défaut pour ce dossier est %ProgramFiles%\Microsoft DirectX SDK (*version*) \Include.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-127">The default location for this folder is %ProgramFiles%\Microsoft DirectX SDK (*version*)\Include.</span></span>

8.  <span data-ttu-id="e1c2e-128">Double-cliquez sur le **l’éditeur de liens** nœud pour le développer.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-128">Double-click the **Linker** node to expand it.</span></span>

9. <span data-ttu-id="e1c2e-129">Dans le **répertoires de bibliothèques supplémentaires** champ, spécifiez l’emplacement du dossier de bibliothèques DirectX.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-129">In the **Additional Library Directories** field, specify the location of the DirectX libraries folder.</span></span> <span data-ttu-id="e1c2e-130">L’emplacement par défaut pour ce dossier est %ProgramFiles%\Microsoft DirectX SDK (*version*) \Lib\x86.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-130">The default location for this folder is %ProgramFiles%\Microsoft DirectX SDK (*version*)\Lib\x86.</span></span>

10. <span data-ttu-id="e1c2e-131">Sélectionnez le **entrée** nœud.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-131">Select the **Input** node.</span></span>

11. <span data-ttu-id="e1c2e-132">Dans le **dépendances supplémentaires** champ, ajoutez le `d3d9.lib` et `d3dx9.lib` fichiers.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-132">In the **Additional Dependencies** field, add the `d3d9.lib` and `d3dx9.lib` files.</span></span>

12. <span data-ttu-id="e1c2e-133">Dans l’Explorateur de solutions, ajoutez un nouveau fichier de définition de module (.def) nommé `D3DContent.def` au projet.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-133">In Solution Explorer, add a new module definition file (.def) named `D3DContent.def` to the project.</span></span>

## <a name="creating-the-direct3d9-content"></a><span data-ttu-id="e1c2e-134">Création du contenu Direct3D9</span><span class="sxs-lookup"><span data-stu-id="e1c2e-134">Creating the Direct3D9 Content</span></span>
 <span data-ttu-id="e1c2e-135">Pour obtenir des performances optimales, votre contenu Direct3D9 doit utiliser des paramètres particuliers.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-135">To get the best performance, your Direct3D9 content must use particular settings.</span></span> <span data-ttu-id="e1c2e-136">Le code suivant montre comment créer une surface Direct3D9 qui possède les meilleures caractéristiques de performances.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-136">The following code shows how to create a Direct3D9 surface that has the best performance characteristics.</span></span> <span data-ttu-id="e1c2e-137">Pour plus d’informations, consultez [Performance Considerations for Direct3D9 et WPF interopérabilité](../../../../docs/framework/wpf/advanced/performance-considerations-for-direct3d9-and-wpf-interoperability.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2e-137">For more information, see [Performance Considerations for Direct3D9 and WPF Interoperability](../../../../docs/framework/wpf/advanced/performance-considerations-for-direct3d9-and-wpf-interoperability.md).</span></span>

#### <a name="to-create-the-direct3d9-content"></a><span data-ttu-id="e1c2e-138">Pour créer du contenu le Direct3D9</span><span class="sxs-lookup"><span data-stu-id="e1c2e-138">To create the Direct3D9 content</span></span>

1.  <span data-ttu-id="e1c2e-139">À l’aide de l’Explorateur de solutions, ajoutez les trois classes C++ au projet nommé ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-139">Using Solution Explorer, add three C++ classes to the project named the following.</span></span>

     <span data-ttu-id="e1c2e-140">`CRenderer` (avec destructeur virtuel)</span><span class="sxs-lookup"><span data-stu-id="e1c2e-140">`CRenderer` (with virtual destructor)</span></span>

     `CRendererManager`

     `CTriangleRenderer`

2.  <span data-ttu-id="e1c2e-141">Ouvrez Renderer.h dans l’éditeur de Code et remplacez le code généré automatiquement par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-141">Open Renderer.h in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#RendererH](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderer.h#rendererh)]

3.  <span data-ttu-id="e1c2e-142">Ouvrez Renderer.cpp dans l’éditeur de Code et remplacez le code généré automatiquement par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-142">Open Renderer.cpp in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#RendererCPP](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderer.cpp#renderercpp)]

4.  <span data-ttu-id="e1c2e-143">Ouvrez RendererManager.h dans l’éditeur de Code et remplacez le code généré automatiquement par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-143">Open RendererManager.h in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#RendererManagerH](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderermanager.h#renderermanagerh)]

5.  <span data-ttu-id="e1c2e-144">Ouvrez RendererManager.cpp dans l’éditeur de Code et remplacez le code généré automatiquement par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-144">Open RendererManager.cpp in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#RendererManagerCPP](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderermanager.cpp#renderermanagercpp)]

6.  <span data-ttu-id="e1c2e-145">Ouvrez TriangleRenderer.h dans l’éditeur de Code et remplacez le code généré automatiquement par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-145">Open TriangleRenderer.h in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#TriangleRendererH](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/trianglerenderer.h#trianglerendererh)]

7.  <span data-ttu-id="e1c2e-146">Ouvrez TriangleRenderer.cpp dans l’éditeur de Code et remplacez le code généré automatiquement par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-146">Open TriangleRenderer.cpp in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#TriangleRendererCPP](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/trianglerenderer.cpp#trianglerenderercpp)]

8.  <span data-ttu-id="e1c2e-147">Ouvrez stdafx.h dans l’éditeur de Code et remplacez le code généré automatiquement par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-147">Open stdafx.h in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#StdafxH](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/stdafx.h#stdafxh)]

9. <span data-ttu-id="e1c2e-148">Ouvrez dllmain.cpp dans l’éditeur de Code et remplacez le code généré automatiquement par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-148">Open dllmain.cpp in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#DllMain](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/dllmain.cpp#dllmain)]

10. <span data-ttu-id="e1c2e-149">Ouvrez D3DContent.def dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-149">Open D3DContent.def in the code editor.</span></span>

11. <span data-ttu-id="e1c2e-150">Remplacez le code généré automatiquement par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-150">Replace the automatically generated code with the following code.</span></span>

    ```
    LIBRARY "D3DContent"

    EXPORTS

    SetSize
    SetAlpha
    SetNumDesiredSamples
    SetAdapter

    GetBackBufferNoRef
    Render
    Destroy
    ```

12. <span data-ttu-id="e1c2e-151">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-151">Build the project.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e1c2e-152">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e1c2e-152">Next Steps</span></span>

-   <span data-ttu-id="e1c2e-153">Héberger le contenu Direct3D9 dans une application WPF.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-153">Host the Direct3D9 content in a WPF application.</span></span> <span data-ttu-id="e1c2e-154">Pour plus d’informations, consultez [procédure pas à pas : Hébergement de contenu Direct3D9 dans WPF](../../../../docs/framework/wpf/advanced/walkthrough-hosting-direct3d9-content-in-wpf.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2e-154">For more information, see [Walkthrough: Hosting Direct3D9 Content in WPF](../../../../docs/framework/wpf/advanced/walkthrough-hosting-direct3d9-content-in-wpf.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e1c2e-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1c2e-155">See Also</span></span>

- <xref:System.Windows.Interop.D3DImage>
- [<span data-ttu-id="e1c2e-156">Considérations sur les performances de l'interopérabilité entre Direct3D9 et WPF</span><span class="sxs-lookup"><span data-stu-id="e1c2e-156">Performance Considerations for Direct3D9 and WPF Interoperability</span></span>](../../../../docs/framework/wpf/advanced/performance-considerations-for-direct3d9-and-wpf-interoperability.md)
- [<span data-ttu-id="e1c2e-157">Procédure pas à pas : Hébergement de contenu Direct3D9 dans WPF</span><span class="sxs-lookup"><span data-stu-id="e1c2e-157">Walkthrough: Hosting Direct3D9 Content in WPF</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-direct3d9-content-in-wpf.md)
