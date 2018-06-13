---
title: 'Procédure pas à pas : incorporation de types provenant d’assemblys managés dans Visual Studio (C#)'
ms.date: 07/20/2015
ms.assetid: 55ed13c9-c5bb-4bc2-bcd8-0587eb568864
ms.openlocfilehash: 90bb523e3eb42cea2cd0a9d1e753e4d9b9873c0c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33339240"
---
# <a name="walkthrough-embedding-types-from-managed-assemblies-in-visual-studio-c"></a><span data-ttu-id="0e48d-102">Procédure pas à pas : incorporation de types provenant d’assemblys managés dans Visual Studio (C#)</span><span class="sxs-lookup"><span data-stu-id="0e48d-102">Walkthrough: Embedding Types from Managed Assemblies in Visual Studio (C#)</span></span>
<span data-ttu-id="0e48d-103">Si vous incorporez des informations de type d’un assembly managé avec nom fort, vous pouvez coupler faiblement des types dans une application pour obtenir une indépendance de version.</span><span class="sxs-lookup"><span data-stu-id="0e48d-103">If you embed type information from a strong-named managed assembly, you can loosely couple types in an application to achieve version independence.</span></span> <span data-ttu-id="0e48d-104">Autrement dit, votre programme peut être écrit de façon à ce qu’il utilise des types de plusieurs versions d’une bibliothèque managée sans que vous n’ayez à effectuer de recompilation pour chaque version.</span><span class="sxs-lookup"><span data-stu-id="0e48d-104">That is, your program can be written to use types from multiple versions of a managed library without having to be recompiled for each version.</span></span>  
  
 <span data-ttu-id="0e48d-105">L’incorporation de type est fréquemment utilisée avec COM Interop, par exemple pour une application qui utilise des objets Automation de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="0e48d-105">Type embedding is frequently used with COM interop, such as an application that uses automation objects from Microsoft Office.</span></span> <span data-ttu-id="0e48d-106">L’incorporation des informations de type permet à la même build d’un programme de fonctionner avec différentes versions de Microsoft Office sur plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="0e48d-106">Embedding type information enables the same build of a program to work with different versions of Microsoft Office on different computers.</span></span> <span data-ttu-id="0e48d-107">Toutefois, vous pouvez également utiliser l’incorporation de type avec une solution totalement managée.</span><span class="sxs-lookup"><span data-stu-id="0e48d-107">However, you can also use type embedding with a fully managed solution.</span></span>  
  
 <span data-ttu-id="0e48d-108">Les informations de type peuvent être incorporées à partir d’un assembly doté des caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e48d-108">Type information can be embedded from an assembly that has the following characteristics:</span></span>  
  
-   <span data-ttu-id="0e48d-109">L’assembly expose au moins une interface publique.</span><span class="sxs-lookup"><span data-stu-id="0e48d-109">The assembly exposes at least one public interface.</span></span>  
  
-   <span data-ttu-id="0e48d-110">Les interfaces incorporées sont annotées avec un attribut `ComImport` et un attribut `Guid` (et un GUID unique).</span><span class="sxs-lookup"><span data-stu-id="0e48d-110">The embedded interfaces are annotated with a `ComImport` attribute and a `Guid` attribute (and a unique GUID).</span></span>  
  
-   <span data-ttu-id="0e48d-111">L’assembly est annoté avec l’attribut `ImportedFromTypeLib` ou l’attribut `PrimaryInteropAssembly` et un attribut `Guid` au niveau de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="0e48d-111">The assembly is annotated with the `ImportedFromTypeLib` attribute or the `PrimaryInteropAssembly` attribute, and an assembly-level `Guid` attribute.</span></span> <span data-ttu-id="0e48d-112">(Par défaut, les modèles de projet Visual C# incluent un attribut `Guid` au niveau de l’assembly.)</span><span class="sxs-lookup"><span data-stu-id="0e48d-112">(By default, Visual C# project templates include an assembly-level `Guid` attribute.)</span></span>  
  
 <span data-ttu-id="0e48d-113">Après avoir spécifié les interfaces publiques qui peuvent être incorporées, vous pouvez créer des classes runtime qui implémentent ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="0e48d-113">After you have specified the public interfaces that can be embedded, you can create runtime classes that implement those interfaces.</span></span> <span data-ttu-id="0e48d-114">Un programme client peut ensuite incorporer les informations de type pour ces interfaces au moment de la conception en référençant l’assembly qui contient les interfaces publiques et en affectant à la propriété `Embed Interop Types` de la référence la valeur `True`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-114">A client program can then embed the type information for those interfaces at design time by referencing the assembly that contains the public interfaces and setting the `Embed Interop Types` property of the reference to `True`.</span></span> <span data-ttu-id="0e48d-115">Cela revient à utiliser le compilateur de ligne de commande et à référencer l’assembly à l’aide de l’option de compilateur `/link`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-115">This is equivalent to using the command line compiler and referencing the assembly by using the `/link` compiler option.</span></span> <span data-ttu-id="0e48d-116">Le programme client peut ensuite charger des instances de vos objets d’exécution possédant le même type que ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="0e48d-116">The client program can then load instances of your runtime objects typed as those interfaces.</span></span> <span data-ttu-id="0e48d-117">Si vous créez une version de votre assembly runtime avec nom fort, le programme client n’a pas besoin d’être recompilé avec l’assembly runtime mis à jour.</span><span class="sxs-lookup"><span data-stu-id="0e48d-117">If you create a new version of your strong-named runtime assembly, the client program does not have to be recompiled with the updated runtime assembly.</span></span> <span data-ttu-id="0e48d-118">En revanche, le programme client continue d’utiliser la version de l’assembly runtime disponible avec les informations de type incorporées pour les interfaces publiques.</span><span class="sxs-lookup"><span data-stu-id="0e48d-118">Instead, the client program continues to use whichever version of the runtime assembly is available to it, using the embedded type information for the public interfaces.</span></span>  
  
 <span data-ttu-id="0e48d-119">Étant donné que la fonction principale de l’incorporation de type est de prendre en charge l’incorporation d’informations de type à partir d’assemblys COM Interop, les limitations suivantes s’appliquent quand vous incorporez des informations de type dans une solution totalement managée :</span><span class="sxs-lookup"><span data-stu-id="0e48d-119">Because the primary function of type embedding is to support embedding of type information from COM interop assemblies, the following limitations apply when you embed type information in a fully managed solution:</span></span>  
  
-   <span data-ttu-id="0e48d-120">Seuls les attributs spécifiques à COM Interop sont incorporés ; les autres attributs sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="0e48d-120">Only attributes specific to COM interop are embedded; other attributes are ignored.</span></span>  
  
-   <span data-ttu-id="0e48d-121">Si un type utilise des paramètres génériques et que le type du paramètre générique est un type incorporé, ce type ne peut pas être utilisé au-delà de la limite de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="0e48d-121">If a type uses generic parameters and the type of the generic parameter is an embedded type, that type cannot be used across an assembly boundary.</span></span> <span data-ttu-id="0e48d-122">Les exemples de passage de la limite de l’assembly incluent l’appel d’une méthode à partir d’un autre assembly ou la dérivation d’un type à partir d’un type défini dans un autre assembly.</span><span class="sxs-lookup"><span data-stu-id="0e48d-122">Examples of crossing an assembly boundary include calling a method from another assembly or a deriving a type from a type defined in another assembly.</span></span>  
  
-   <span data-ttu-id="0e48d-123">Les constantes ne sont pas incorporées.</span><span class="sxs-lookup"><span data-stu-id="0e48d-123">Constants are not embedded.</span></span>  
  
-   <span data-ttu-id="0e48d-124">La classe <xref:System.Collections.Generic.Dictionary%602?displayProperty=nameWithType> ne prend pas en charge un type incorporé comme clé.</span><span class="sxs-lookup"><span data-stu-id="0e48d-124">The <xref:System.Collections.Generic.Dictionary%602?displayProperty=nameWithType> class does not support an embedded type as a key.</span></span> <span data-ttu-id="0e48d-125">Vous pouvez implémenter votre propre type de dictionnaire pour prendre en charge un type incorporé comme clé.</span><span class="sxs-lookup"><span data-stu-id="0e48d-125">You can implement your own dictionary type to support an embedded type as a key.</span></span>  
  
 <span data-ttu-id="0e48d-126">Dans cette procédure pas à pas, vous exécuterez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e48d-126">In this walkthrough, you will do the following:</span></span>  
  
-   <span data-ttu-id="0e48d-127">Créer un assembly avec nom fort doté d’une interface publique contenant des informations de type qui peuvent être incorporées.</span><span class="sxs-lookup"><span data-stu-id="0e48d-127">Create a strong-named assembly that has a public interface that contains type information that can be embedded.</span></span>  
  
-   <span data-ttu-id="0e48d-128">Créer un assembly runtime avec nom fort qui implémente cette interface publique.</span><span class="sxs-lookup"><span data-stu-id="0e48d-128">Create a strong-named runtime assembly that implements that public interface.</span></span>  
  
-   <span data-ttu-id="0e48d-129">Créer un programme client qui incorpore les informations de type de l’interface publique et crée une instance de la classe à partir de l’assembly runtime.</span><span class="sxs-lookup"><span data-stu-id="0e48d-129">Create a client program that embeds the type information from the public interface and creates an instance of the class from the runtime assembly.</span></span>  
  
-   <span data-ttu-id="0e48d-130">Modifier et régénérer l’assembly runtime.</span><span class="sxs-lookup"><span data-stu-id="0e48d-130">Modify and rebuild the runtime assembly.</span></span>  
  
-   <span data-ttu-id="0e48d-131">Exécuter le programme client pour constater que la nouvelle version de l’assembly runtime est utilisée sans devoir recompiler le programme client.</span><span class="sxs-lookup"><span data-stu-id="0e48d-131">Run the client program to see that the new version of the runtime assembly is being used without having to recompile the client program.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
## <a name="creating-an-interface"></a><span data-ttu-id="0e48d-132">Création d’une interface</span><span class="sxs-lookup"><span data-stu-id="0e48d-132">Creating an Interface</span></span>  
  
#### <a name="to-create-the-type-equivalence-interface-project"></a><span data-ttu-id="0e48d-133">Pour créer le projet d’interface d’équivalence des types</span><span class="sxs-lookup"><span data-stu-id="0e48d-133">To create the type equivalence interface project</span></span>  
  
1.  <span data-ttu-id="0e48d-134">Dans Visual Studio, dans le menu **Fichier**, choisissez **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-134">In Visual Studio, on the **File** menu, choose **New** and then click **Project**.</span></span>  
  
2.  <span data-ttu-id="0e48d-135">Dans la boîte de dialogue **Nouveau projet**, dans le volet **Types de projets**, vérifiez que **Windows** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0e48d-135">In the **New Project** dialog box, in the **Project Types** pane, make sure that **Windows** is selected.</span></span> <span data-ttu-id="0e48d-136">Sélectionnez **Bibliothèque de classes** dans le volet **Modèles**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-136">Select **Class Library** in the **Templates** pane.</span></span> <span data-ttu-id="0e48d-137">Dans la zone **Nom**, tapez `TypeEquivalenceInterface`, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-137">In the **Name** box, type `TypeEquivalenceInterface`, and then click **OK**.</span></span> <span data-ttu-id="0e48d-138">Le nouveau projet est créé.</span><span class="sxs-lookup"><span data-stu-id="0e48d-138">The new project is created.</span></span>  
  
3.  <span data-ttu-id="0e48d-139">Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur le fichier Class1.cs, puis cliquez sur **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-139">In **Solution Explorer**, right-click the Class1.cs file and click **Rename**.</span></span> <span data-ttu-id="0e48d-140">Renommez le fichier `ISampleInterface.cs` et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="0e48d-140">Rename the file to `ISampleInterface.cs` and press ENTER.</span></span> <span data-ttu-id="0e48d-141">Quand vous renommez le fichier, la classe est également renommée `ISampleInterface`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-141">Renaming the file will also rename the class to `ISampleInterface`.</span></span> <span data-ttu-id="0e48d-142">Cette classe représente l’interface publique pour la classe.</span><span class="sxs-lookup"><span data-stu-id="0e48d-142">This class will represent the public interface for the class.</span></span>  
  
4.  <span data-ttu-id="0e48d-143">Cliquez avec le bouton droit sur le projet TypeEquivalenceInterface, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-143">Right-click the TypeEquivalenceInterface project and click **Properties**.</span></span> <span data-ttu-id="0e48d-144">Cliquez sur l’onglet **Générer**. Affectez au chemin de sortie un emplacement valide sur votre ordinateur de développement, tel que `C:\TypeEquivalenceSample`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-144">Click the **Build** tab. Set the output path to a valid location on your development computer, such as `C:\TypeEquivalenceSample`.</span></span> <span data-ttu-id="0e48d-145">Cet emplacement sera également utilisé dans une étape ultérieure de cette procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="0e48d-145">This location will also be used in a later step in this walkthrough.</span></span>  
  
5.  <span data-ttu-id="0e48d-146">Tout en modifiant les propriétés de projet, cliquez sur l’onglet **Signature**. Sélectionnez l’option **Signer l’assembly**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-146">While still editing the project properties, click the **Signing** tab. Select the **Sign the assembly** option.</span></span> <span data-ttu-id="0e48d-147">Dans la liste **Choisir un fichier de clé de nom fort**, cliquez sur **<Nouveau...>**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-147">In the **Choose a strong name key file** list, click **<New...>**.</span></span> <span data-ttu-id="0e48d-148">Dans la zone **Nom du fichier de clé**, tapez `key.snk`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-148">In the **Key file name** box, type `key.snk`.</span></span> <span data-ttu-id="0e48d-149">Décochez la case **Protéger mon fichier de clé par un mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-149">Clear the **Protect my key file with a password** check box.</span></span> <span data-ttu-id="0e48d-150">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-150">Click **OK**.</span></span>  
  
6.  <span data-ttu-id="0e48d-151">Ouvrez le fichier ISampleInterface.cs.</span><span class="sxs-lookup"><span data-stu-id="0e48d-151">Open the ISampleInterface.cs file.</span></span> <span data-ttu-id="0e48d-152">Ajoutez le code suivant au fichier de classe ISampleInterface pour créer l’interface ISampleInterface.</span><span class="sxs-lookup"><span data-stu-id="0e48d-152">Add the following code to the ISampleInterface class file to create the ISampleInterface interface.</span></span>  
  
    ```csharp  
    using System;  
    using System.Runtime.InteropServices;  
  
    namespace TypeEquivalenceInterface  
    {  
        [ComImport]  
        [Guid("8DA56996-A151-4136-B474-32784559F6DF")]  
        public interface ISampleInterface  
        {  
            void GetUserInput();  
            string UserInput { get; }  
        }  
    }  
    ```  
  
7.  <span data-ttu-id="0e48d-153">Dans le menu **Outils**, cliquez sur **Créer un Guid**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-153">On the **Tools** menu, click **Create Guid**.</span></span> <span data-ttu-id="0e48d-154">Dans la boîte de dialogue **Créer un Guid**, cliquez sur **Format du Registre**, puis sur **Copier**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-154">In the **Create GUID** dialog box, click **Registry Format** and then click **Copy**.</span></span> <span data-ttu-id="0e48d-155">Cliquez sur **Quitter**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-155">Click **Exit**.</span></span>  
  
8.  <span data-ttu-id="0e48d-156">Dans l’attribut `Guid`, supprimez l’exemple de GUID et collez le GUID que vous avez copié à partir de la boîte de dialogue **Créer un Guid**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-156">In the `Guid` attribute, delete the sample GUID and paste in the GUID that you copied from the **Create GUID** dialog box.</span></span> <span data-ttu-id="0e48d-157">Supprimez les accolades ({}) du GUID copié.</span><span class="sxs-lookup"><span data-stu-id="0e48d-157">Remove the braces ({}) from the copied GUID.</span></span>  
  
9. <span data-ttu-id="0e48d-158">Dans l’**Explorateur de solutions**, développez le dossier **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-158">In **Solution Explorer**, expand the **Properties** folder.</span></span> <span data-ttu-id="0e48d-159">Double-cliquez sur le fichier AssemblyInfo.cs.</span><span class="sxs-lookup"><span data-stu-id="0e48d-159">Double-click the AssemblyInfo.cs file.</span></span> <span data-ttu-id="0e48d-160">Ajoutez l’attribut suivant au fichier.</span><span class="sxs-lookup"><span data-stu-id="0e48d-160">Add the following attribute to the file.</span></span>  
  
    ```csharp  
    [assembly: ImportedFromTypeLib("")]  
    ```  
  
     <span data-ttu-id="0e48d-161">Enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="0e48d-161">Save the file.</span></span>  
  
10. <span data-ttu-id="0e48d-162">Enregistrez le projet.</span><span class="sxs-lookup"><span data-stu-id="0e48d-162">Save the project.</span></span>  
  
11. <span data-ttu-id="0e48d-163">Cliquez avec le bouton droit sur le projet TypeEquivalenceInterface, puis cliquez sur **Générer**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-163">Right-click the TypeEquivalenceInterface project and click **Build**.</span></span> <span data-ttu-id="0e48d-164">Le fichier .dll de bibliothèque de classes est compilé et enregistré dans le chemin de sortie de la génération spécifié (par exemple, C:\TypeEquivalenceSample).</span><span class="sxs-lookup"><span data-stu-id="0e48d-164">The class library .dll file is compiled and saved to the specified build output path (for example, C:\TypeEquivalenceSample).</span></span>  
  
## <a name="creating-a-runtime-class"></a><span data-ttu-id="0e48d-165">Création d’une classe runtime</span><span class="sxs-lookup"><span data-stu-id="0e48d-165">Creating a Runtime Class</span></span>  
  
#### <a name="to-create-the-type-equivalence-runtime-project"></a><span data-ttu-id="0e48d-166">Pour créer le projet d’exécution d’équivalence des types</span><span class="sxs-lookup"><span data-stu-id="0e48d-166">To create the type equivalence runtime project</span></span>  
  
1.  <span data-ttu-id="0e48d-167">Dans Visual Studio, dans le menu **Fichier**,pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-167">In Visual Studio, on the **File** menu, point to **New** and then click **Project**.</span></span>  
  
2.  <span data-ttu-id="0e48d-168">Dans la boîte de dialogue **Nouveau projet**, dans le volet **Types de projets**, vérifiez que **Windows** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0e48d-168">In the **New Project** dialog box, in the **Project Types** pane, make sure that **Windows** is selected.</span></span> <span data-ttu-id="0e48d-169">Sélectionnez **Bibliothèque de classes** dans le volet **Modèles**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-169">Select **Class Library** in the **Templates** pane.</span></span> <span data-ttu-id="0e48d-170">Dans la zone **Nom**, tapez `TypeEquivalenceRuntime`, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-170">In the **Name** box, type `TypeEquivalenceRuntime`, and then click **OK**.</span></span> <span data-ttu-id="0e48d-171">Le nouveau projet est créé.</span><span class="sxs-lookup"><span data-stu-id="0e48d-171">The new project is created.</span></span>  
  
3.  <span data-ttu-id="0e48d-172">Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur le fichier Class1.cs, puis cliquez sur **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-172">In **Solution Explorer**, right-click the Class1.cs file and click **Rename**.</span></span> <span data-ttu-id="0e48d-173">Renommez le fichier `SampleClass.cs` et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="0e48d-173">Rename the file to `SampleClass.cs` and press ENTER.</span></span> <span data-ttu-id="0e48d-174">Quand vous renommez le fichier, la classe est également renommée `SampleClass`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-174">Renaming the file also renames the class to `SampleClass`.</span></span> <span data-ttu-id="0e48d-175">Cette classe va implémenter l’interface `ISampleInterface`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-175">This class will implement the `ISampleInterface` interface.</span></span>  
  
4.  <span data-ttu-id="0e48d-176">Cliquez avec le bouton droit sur le projet TypeEquivalenceRuntime, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-176">Right-click the TypeEquivalenceRuntime project and click **Properties**.</span></span> <span data-ttu-id="0e48d-177">Cliquez sur l’onglet **Générer**. Affectez au chemin de sortie le même emplacement que celui que vous avez utilisé dans le projet TypeEquivalenceInterface, par exemple `C:\TypeEquivalenceSample`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-177">Click the **Build** tab. Set the output path to the same location you used in the TypeEquivalenceInterface project, for example, `C:\TypeEquivalenceSample`.</span></span>  
  
5.  <span data-ttu-id="0e48d-178">Tout en modifiant les propriétés de projet, cliquez sur l’onglet **Signature**. Sélectionnez l’option **Signer l’assembly**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-178">While still editing the project properties, click the **Signing** tab. Select the **Sign the assembly** option.</span></span> <span data-ttu-id="0e48d-179">Dans la liste **Choisir un fichier de clé de nom fort**, cliquez sur **<Nouveau...>**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-179">In the **Choose a strong name key file** list, click **<New...>**.</span></span> <span data-ttu-id="0e48d-180">Dans la zone **Nom du fichier de clé**, tapez `key.snk`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-180">In the **Key file name** box, type `key.snk`.</span></span> <span data-ttu-id="0e48d-181">Décochez la case **Protéger mon fichier de clé par un mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-181">Clear the **Protect my key file with a password** check box.</span></span> <span data-ttu-id="0e48d-182">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-182">Click **OK**.</span></span>  
  
6.  <span data-ttu-id="0e48d-183">Cliquez avec le bouton droit sur le projet TypeEquivalenceRuntime, puis cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-183">Right-click the TypeEquivalenceRuntime project and click **Add Reference**.</span></span> <span data-ttu-id="0e48d-184">Cliquez sur l’onglet **Parcourir** et recherchez le dossier du chemin de sortie.</span><span class="sxs-lookup"><span data-stu-id="0e48d-184">Click the **Browse** tab and browse to the output path folder.</span></span> <span data-ttu-id="0e48d-185">Sélectionnez le fichier TypeEquivalenceInterface.dll et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-185">Select the TypeEquivalenceInterface.dll file and click **OK**.</span></span>  
  
7.  <span data-ttu-id="0e48d-186">Dans l’**Explorateur de solutions**, développez le dossier **Références**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-186">In **Solution Explorer**, expand the **References** folder.</span></span> <span data-ttu-id="0e48d-187">Sélectionnez la référence TypeEquivalenceInterface.</span><span class="sxs-lookup"><span data-stu-id="0e48d-187">Select the TypeEquivalenceInterface reference.</span></span> <span data-ttu-id="0e48d-188">Dans la fenêtre Propriétés de la référence TypeEquivalenceInterface, affectez à la propriété **Version spécifique** la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-188">In the Properties window for the TypeEquivalenceInterface reference, set the **Specific Version** property to **False**.</span></span>  
  
8.  <span data-ttu-id="0e48d-189">Ajoutez le code suivant au fichier de classe SampleClass pour créer la classe SampleClass.</span><span class="sxs-lookup"><span data-stu-id="0e48d-189">Add the following code to the SampleClass class file to create the SampleClass class.</span></span>  
  
    ```csharp  
    using System;  
    using System.Collections.Generic;  
    using System.Linq;  
    using System.Text;  
    using TypeEquivalenceInterface;  
  
    namespace TypeEquivalenceRuntime  
    {  
        public class SampleClass : ISampleInterface  
        {  
            private string p_UserInput;  
            public string UserInput { get { return p_UserInput; } }  
  
            public void GetUserInput()  
            {  
                Console.WriteLine("Please enter a value:");  
                p_UserInput = Console.ReadLine();  
            }  
        }  
    )  
    ```  
  
9. <span data-ttu-id="0e48d-190">Enregistrez le projet.</span><span class="sxs-lookup"><span data-stu-id="0e48d-190">Save the project.</span></span>  
  
10. <span data-ttu-id="0e48d-191">Cliquez avec le bouton droit sur le projet TypeEquivalenceRuntime, puis cliquez sur **Générer**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-191">Right-click the TypeEquivalenceRuntime project and click **Build**.</span></span> <span data-ttu-id="0e48d-192">Le fichier .dll de bibliothèque de classes est compilé et enregistré dans le chemin de sortie de la génération spécifié (par exemple, C:\TypeEquivalenceSample).</span><span class="sxs-lookup"><span data-stu-id="0e48d-192">The class library .dll file is compiled and saved to the specified build output path (for example, C:\TypeEquivalenceSample).</span></span>  
  
## <a name="creating-a-client-project"></a><span data-ttu-id="0e48d-193">Création d’un projet client</span><span class="sxs-lookup"><span data-stu-id="0e48d-193">Creating a Client Project</span></span>  
  
#### <a name="to-create-the-type-equivalence-client-project"></a><span data-ttu-id="0e48d-194">Pour créer le projet client d’équivalence des types</span><span class="sxs-lookup"><span data-stu-id="0e48d-194">To create the type equivalence client project</span></span>  
  
1.  <span data-ttu-id="0e48d-195">Dans Visual Studio, dans le menu **Fichier**,pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-195">In Visual Studio, on the **File** menu, point to **New** and then click **Project**.</span></span>  
  
2.  <span data-ttu-id="0e48d-196">Dans la boîte de dialogue **Nouveau projet**, dans le volet **Types de projets**, vérifiez que **Windows** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0e48d-196">In the **New Project** dialog box, in the **Project Types** pane, make sure that **Windows** is selected.</span></span> <span data-ttu-id="0e48d-197">Sélectionnez **Application console** dans le volet **Modèles**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-197">Select **Console Application** in the **Templates** pane.</span></span> <span data-ttu-id="0e48d-198">Dans la zone **Nom**, tapez `TypeEquivalenceClient`, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-198">In the **Name** box, type `TypeEquivalenceClient`, and then click **OK**.</span></span> <span data-ttu-id="0e48d-199">Le nouveau projet est créé.</span><span class="sxs-lookup"><span data-stu-id="0e48d-199">The new project is created.</span></span>  
  
3.  <span data-ttu-id="0e48d-200">Cliquez avec le bouton droit sur le projet TypeEquivalenceClient, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-200">Right-click the TypeEquivalenceClient project and click **Properties**.</span></span> <span data-ttu-id="0e48d-201">Cliquez sur l’onglet **Générer**. Affectez au chemin de sortie le même emplacement que celui que vous avez utilisé dans le projet TypeEquivalenceInterface, par exemple `C:\TypeEquivalenceSample`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-201">Click the **Build** tab. Set the output path to the same location you used in the TypeEquivalenceInterface project, for example, `C:\TypeEquivalenceSample`.</span></span>  
  
4.  <span data-ttu-id="0e48d-202">Cliquez avec le bouton droit sur le projet TypeEquivalenceClient, puis cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-202">Right-click the TypeEquivalenceClient project and click **Add Reference**.</span></span> <span data-ttu-id="0e48d-203">Cliquez sur l’onglet **Parcourir** et recherchez le dossier du chemin de sortie.</span><span class="sxs-lookup"><span data-stu-id="0e48d-203">Click the **Browse** tab and browse to the output path folder.</span></span> <span data-ttu-id="0e48d-204">Sélectionnez le fichier TypeEquivalenceInterface.dll (pas le fichier TypeEquivalenceRuntime.dll) et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-204">Select the TypeEquivalenceInterface.dll file (not the TypeEquivalenceRuntime.dll) and click **OK**.</span></span>  
  
5.  <span data-ttu-id="0e48d-205">Dans l’**Explorateur de solutions**, développez le dossier **Références**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-205">In **Solution Explorer**, expand the **References** folder.</span></span> <span data-ttu-id="0e48d-206">Sélectionnez la référence TypeEquivalenceInterface.</span><span class="sxs-lookup"><span data-stu-id="0e48d-206">Select the TypeEquivalenceInterface reference.</span></span> <span data-ttu-id="0e48d-207">Dans la fenêtre Propriétés de la référence TypeEquivalenceInterface, affectez à la propriété **Incorporer les types d’interopérabilité** la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-207">In the Properties window for the TypeEquivalenceInterface reference, set the **Embed Interop Types** property to **True**.</span></span>  
  
6.  <span data-ttu-id="0e48d-208">Ajoutez le code suivant au fichier Program.cs pour créer le programme client.</span><span class="sxs-lookup"><span data-stu-id="0e48d-208">Add the following code to the Program.cs file to create the client program.</span></span>  
  
    ```csharp  
    using System;  
    using System.Collections.Generic;  
    using System.Linq;  
    using System.Text;  
    using TypeEquivalenceInterface;  
    using System.Reflection;  
  
    namespace TypeEquivalenceClient  
    {  
        class Program  
        {  
            static void Main(string[] args)  
            {  
                Assembly sampleAssembly = Assembly.Load("TypeEquivalenceRuntime");  
                ISampleInterface sampleClass =   
                    (ISampleInterface)sampleAssembly.CreateInstance("TypeEquivalenceRuntime.SampleClass");  
                sampleClass.GetUserInput();  
                Console.WriteLine(sampleClass.UserInput);  
                Console.WriteLine(sampleAssembly.GetName().Version.ToString());  
                Console.ReadLine();  
            }  
        }  
    }  
    ```  
  
7.  <span data-ttu-id="0e48d-209">Appuyez sur CTRL+F5 pour générer et exécuter le programme.</span><span class="sxs-lookup"><span data-stu-id="0e48d-209">Press CTRL+F5 to build and run the program.</span></span>  
  
## <a name="modifying-the-interface"></a><span data-ttu-id="0e48d-210">Modification de l’interface</span><span class="sxs-lookup"><span data-stu-id="0e48d-210">Modifying the Interface</span></span>  
  
#### <a name="to-modify-the-interface"></a><span data-ttu-id="0e48d-211">Pour modifier l’interface</span><span class="sxs-lookup"><span data-stu-id="0e48d-211">To modify the interface</span></span>  
  
1.  <span data-ttu-id="0e48d-212">Dans Visual Studio, dans le menu **Fichier**, pointez sur **Ouvrir**, puis cliquez sur **Projet/Solution**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-212">In Visual Studio, on the **File** menu, point to **Open**, and then click **Project/Solution**.</span></span>  
  
2.  <span data-ttu-id="0e48d-213">Dans la boîte de dialogue **Ouvrir un projet**, cliquez avec le bouton droit sur le projet TypeEquivalenceInterface, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-213">In the **Open Project** dialog box, right-click the TypeEquivalenceInterface project, and then click **Properties**.</span></span> <span data-ttu-id="0e48d-214">Cliquez sur l’onglet **Application** . Cliquez sur le bouton **Informations de l’assembly**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-214">Click the **Application** tab. Click the **Assembly Information** button.</span></span> <span data-ttu-id="0e48d-215">Remplacez les valeurs de **Version de l’assembly** et **Version de fichier** par `2.0.0.0`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-215">Change the **Assembly Version** and **File Version** values to `2.0.0.0`.</span></span>  
  
3.  <span data-ttu-id="0e48d-216">Ouvrez le fichier SampleInterface.cs.</span><span class="sxs-lookup"><span data-stu-id="0e48d-216">Open the SampleInterface.cs file.</span></span> <span data-ttu-id="0e48d-217">Ajoutez la ligne de code suivante à l’interface ISampleInterface.</span><span class="sxs-lookup"><span data-stu-id="0e48d-217">Add the following line of code to the ISampleInterface interface.</span></span>  
  
    ```csharp  
    DateTime GetDate();  
    ```  
  
     <span data-ttu-id="0e48d-218">Enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="0e48d-218">Save the file.</span></span>  
  
4.  <span data-ttu-id="0e48d-219">Enregistrez le projet.</span><span class="sxs-lookup"><span data-stu-id="0e48d-219">Save the project.</span></span>  
  
5.  <span data-ttu-id="0e48d-220">Cliquez avec le bouton droit sur le projet TypeEquivalenceInterface, puis cliquez sur **Générer**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-220">Right-click the TypeEquivalenceInterface project and click **Build**.</span></span> <span data-ttu-id="0e48d-221">Une nouvelle version du fichier .dll de bibliothèque de classes est compilée et enregistrée dans le chemin de sortie de la génération spécifié (par exemple, C:\TypeEquivalenceSample).</span><span class="sxs-lookup"><span data-stu-id="0e48d-221">A new version of the class library .dll file is compiled and saved in the specified build output path (for example, C:\TypeEquivalenceSample).</span></span>  
  
## <a name="modifying-the-runtime-class"></a><span data-ttu-id="0e48d-222">Modification de la classe runtime</span><span class="sxs-lookup"><span data-stu-id="0e48d-222">Modifying the Runtime Class</span></span>  
  
#### <a name="to-modify-the-runtime-class"></a><span data-ttu-id="0e48d-223">Pour modifier la classe runtime</span><span class="sxs-lookup"><span data-stu-id="0e48d-223">To modify the runtime class</span></span>  
  
1.  <span data-ttu-id="0e48d-224">Dans Visual Studio, dans le menu **Fichier**, pointez sur **Ouvrir**, puis cliquez sur **Projet/Solution**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-224">In Visual Studio, on the **File** menu, point to **Open**, and then click **Project/Solution**.</span></span>  
  
2.  <span data-ttu-id="0e48d-225">Dans la boîte de dialogue **Ouvrir un projet**, cliquez avec le bouton droit sur le projet TypeEquivalenceRuntime, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-225">In the **Open Project** dialog box, right-click the TypeEquivalenceRuntime project and click **Properties**.</span></span> <span data-ttu-id="0e48d-226">Cliquez sur l’onglet **Application** . Cliquez sur le bouton **Informations de l’assembly**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-226">Click the **Application** tab. Click the **Assembly Information** button.</span></span> <span data-ttu-id="0e48d-227">Remplacez les valeurs de **Version de l’assembly** et **Version de fichier** par `2.0.0.0`.</span><span class="sxs-lookup"><span data-stu-id="0e48d-227">Change the **Assembly Version** and **File Version** values to `2.0.0.0`.</span></span>  
  
3.  <span data-ttu-id="0e48d-228">Ouvrez le fichier SampleClass.cs.</span><span class="sxs-lookup"><span data-stu-id="0e48d-228">Open the SampleClass.cs file.</span></span> <span data-ttu-id="0e48d-229">Ajoutez les lignes de code suivantes à la classe SampleClass.</span><span class="sxs-lookup"><span data-stu-id="0e48d-229">Add the following lines of code to the SampleClass class.</span></span>  
  
    ```csharp  
    public DateTime GetDate()  
    {  
        return DateTime.Now;  
    }  
    ```  
  
     <span data-ttu-id="0e48d-230">Enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="0e48d-230">Save the file.</span></span>  
  
4.  <span data-ttu-id="0e48d-231">Enregistrez le projet.</span><span class="sxs-lookup"><span data-stu-id="0e48d-231">Save the project.</span></span>  
  
5.  <span data-ttu-id="0e48d-232">Cliquez avec le bouton droit sur le projet TypeEquivalenceRuntime, puis cliquez sur **Générer**.</span><span class="sxs-lookup"><span data-stu-id="0e48d-232">Right-click the TypeEquivalenceRuntime project and click **Build**.</span></span> <span data-ttu-id="0e48d-233">Une version mise à jour du fichier .dll de bibliothèque de classes est compilée et enregistrée dans le chemin de sortie de la génération précédemment spécifié (par exemple, C:\TypeEquivalenceSample).</span><span class="sxs-lookup"><span data-stu-id="0e48d-233">An updated version of the class library .dll file is compiled and saved in the previously specified build output path (for example, C:\TypeEquivalenceSample).</span></span>  
  
6.  <span data-ttu-id="0e48d-234">Dans l’Explorateur de fichiers, ouvrez le dossier du chemin de sortie (par exemple, C:\TypeEquivalenceSample).</span><span class="sxs-lookup"><span data-stu-id="0e48d-234">In File Explorer, open the output path folder (for example, C:\TypeEquivalenceSample).</span></span> <span data-ttu-id="0e48d-235">Double-cliquez sur le fichier TypeEquivalenceClient.exe pour exécuter le programme.</span><span class="sxs-lookup"><span data-stu-id="0e48d-235">Double-click the TypeEquivalenceClient.exe to run the program.</span></span> <span data-ttu-id="0e48d-236">Le programme reflète la nouvelle version de l’assembly TypeEquivalenceRuntime sans aucune recompilation.</span><span class="sxs-lookup"><span data-stu-id="0e48d-236">The program will reflect the new version of the TypeEquivalenceRuntime assembly without having been recompiled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e48d-237">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e48d-237">See Also</span></span>  
 [<span data-ttu-id="0e48d-238">/link (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="0e48d-238">/link (C# Compiler Options)</span></span>](../../../../csharp/language-reference/compiler-options/link-compiler-option.md)  
 [<span data-ttu-id="0e48d-239">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0e48d-239">C# Programming Guide</span></span>](../../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="0e48d-240">Programmation à l’aide d’assemblys</span><span class="sxs-lookup"><span data-stu-id="0e48d-240">Programming with Assemblies</span></span>](../../../../framework/app-domains/programming-with-assemblies.md)  
 [<span data-ttu-id="0e48d-241">Assemblys et le Global Assembly Cache (C#)</span><span class="sxs-lookup"><span data-stu-id="0e48d-241">Assemblies and the Global Assembly Cache (C#)</span></span>](../../../../csharp/programming-guide/concepts/assemblies-gac/index.md)
