---
title: -win32manifest (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /win32manifest
helpviewer_keywords:
- /win32manifest compiler option [C#]
- win32manifest compiler option [C#]
- -win32manifest compiler option [C#]
ms.assetid: 9460ea1b-6c9f-44b8-8f73-301b30a01de1
ms.openlocfilehash: 3ac2b60b5e638290ea7e17e539519e3a0d355c12
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33214956"
---
# <a name="-win32manifest-c-compiler-options"></a><span data-ttu-id="fca13-102">-win32manifest (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="fca13-102">-win32manifest (C# Compiler Options)</span></span>
<span data-ttu-id="fca13-103">Utilisez l’option **-win32manifest** pour spécifier un fichier manifeste d’application Win32 défini par l’utilisateur à incorporer dans le fichier exécutable portable (PE) d’un projet.</span><span class="sxs-lookup"><span data-stu-id="fca13-103">Use the **-win32manifest** option to specify a user-defined Win32 application manifest file to be embedded into a project's portable executable (PE) file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fca13-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fca13-104">Syntax</span></span>  
  
```console  
-win32manifest: filename  
```  
  
## <a name="arguments"></a><span data-ttu-id="fca13-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="fca13-105">Arguments</span></span>  
 `filename`  
 <span data-ttu-id="fca13-106">Nom et emplacement du fichier manifeste personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fca13-106">The name and location of the custom manifest file.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fca13-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fca13-107">Remarks</span></span>  
 <span data-ttu-id="fca13-108">Par défaut, le compilateur Visual C# incorpore un manifeste d’application qui spécifie le niveau d’exécution requis « asInvoker ».</span><span class="sxs-lookup"><span data-stu-id="fca13-108">By default, the Visual C# compiler embeds an application manifest that specifies a requested execution level of "asInvoker."</span></span> <span data-ttu-id="fca13-109">Il crée le manifeste dans le même dossier que celui dans lequel l’exécutable est généré, normalement le dossier bin\Debug ou bin\Release quand vous utilisez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fca13-109">It creates the manifest in the same folder in which the executable is built, typically the bin\Debug or bin\Release folder when you use Visual Studio.</span></span> <span data-ttu-id="fca13-110">Pour fournir un manifeste personnalisé, par exemple pour spécifier le niveau d’exécution requis « highestAvailable » ou « requireAdministrator », utilisez cette option pour indiquer le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="fca13-110">If you want to supply a custom manifest, for example to specify a requested execution level of "highestAvailable" or "requireAdministrator," use this option to specify the name of the file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fca13-111">Cette option et l’option [-win32res (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/win32res-compiler-option.md) s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="fca13-111">This option and the [-win32res (C# Compiler Options)](../../../csharp/language-reference/compiler-options/win32res-compiler-option.md) option are mutually exclusive.</span></span> <span data-ttu-id="fca13-112">Si vous tentez d’utiliser ces deux options dans la même ligne de commande, une erreur de build se produira.</span><span class="sxs-lookup"><span data-stu-id="fca13-112">If you try to use both options in the same command line you will get a build error.</span></span>  
  
 <span data-ttu-id="fca13-113">Une application sans manifeste d’application pour spécifier le niveau d’exécution requis est soumise à une virtualisation des fichiers/registres sous la fonctionnalité de contrôle de compte d’utilisateur de Windows.</span><span class="sxs-lookup"><span data-stu-id="fca13-113">An application that has no application manifest that specifies a requested execution level will be subject to file/registry virtualization under the User Account Control feature in Windows.</span></span> <span data-ttu-id="fca13-114">Pour plus d’informations, consultez [Contrôle de compte d’utilisateur](/windows/access-protection/user-account-control/user-account-control-overview).</span><span class="sxs-lookup"><span data-stu-id="fca13-114">For more information, see [User Account Control](/windows/access-protection/user-account-control/user-account-control-overview).</span></span>  
  
 <span data-ttu-id="fca13-115">Votre application sera soumise à la virtualisation si l’une de ces conditions est vérifiée :</span><span class="sxs-lookup"><span data-stu-id="fca13-115">Your application will be subject to virtualization if either of these conditions is true:</span></span>  
  
-   <span data-ttu-id="fca13-116">Vous utilisez l’option **-nowin32manifest** sans fournir de manifeste au cours d’une étape de génération ultérieure ou en tant que partie du fichier de ressources Windows (.res) à l’aide de l’option **-win32res**.</span><span class="sxs-lookup"><span data-stu-id="fca13-116">You use the **-nowin32manifest** option and you do not provide a manifest in a later build step or as part of a Windows Resource (.res) file by using the **-win32res** option.</span></span>  
  
-   <span data-ttu-id="fca13-117">Vous fournissez un manifeste personnalisé qui ne spécifie pas le niveau d’exécution requis.</span><span class="sxs-lookup"><span data-stu-id="fca13-117">You provide a custom manifest that does not specify a requested execution level.</span></span>  
  
 <span data-ttu-id="fca13-118">Visual Studio crée un fichier .manifest par défaut et le stocke dans les répertoires de débogage et de mise en production avec le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="fca13-118">Visual Studio creates a default .manifest file and stores it in the debug and release directories alongside the executable file.</span></span> <span data-ttu-id="fca13-119">Vous pouvez ajouter un manifeste personnalisé en en créant un dans un éditeur de texte et en ajoutant le fichier au projet.</span><span class="sxs-lookup"><span data-stu-id="fca13-119">You can add a custom manifest by creating one in any text editor and then adding the file to the project.</span></span> <span data-ttu-id="fca13-120">Vous pouvez également cliquer avec le bouton droit sur l’icône **Projet** de l’**Explorateur de solutions**, cliquer sur **Ajouter un nouvel élément**, puis sur **Fichier manifeste d’application**.</span><span class="sxs-lookup"><span data-stu-id="fca13-120">Alternatively, you can right-click the **Project** icon in **Solution Explorer**, click **Add New Item**, and then click **Application Manifest File**.</span></span> <span data-ttu-id="fca13-121">Une fois que vous avez ajouté votre fichier manifeste nouveau ou existant, il apparaît dans la liste déroulante **Manifeste**.</span><span class="sxs-lookup"><span data-stu-id="fca13-121">After you have added your new or existing manifest file, it will appear in the **Manifest** drop down list.</span></span> <span data-ttu-id="fca13-122">Pour plus d’informations, consultez [Page Application, Concepteur de projets (C#)](/visualstudio/ide/reference/application-page-project-designer-csharp).</span><span class="sxs-lookup"><span data-stu-id="fca13-122">For more information, see [Application Page, Project Designer (C#)](/visualstudio/ide/reference/application-page-project-designer-csharp).</span></span>  
  
 <span data-ttu-id="fca13-123">Vous pouvez fournir le manifeste d’application en tant qu’étape après génération personnalisée ou en tant que partie d’un fichier de ressources Win32 à l’aide de l’option [-nowin32manifest (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/nowin32manifest-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="fca13-123">You can provide the application manifest as a custom post-build step or as part of a Win32 resource file by using the [-nowin32manifest (C# Compiler Options)](../../../csharp/language-reference/compiler-options/nowin32manifest-compiler-option.md) option.</span></span> <span data-ttu-id="fca13-124">Utilisez cette même option pour que votre application soit soumise à la virtualisation des fichiers ou des registres dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fca13-124">Use that same option if you want your application to be subject to file or registry virtualization on Windows Vista.</span></span> <span data-ttu-id="fca13-125">Cela empêche le compilateur de créer et d’incorporer un manifeste par défaut dans le fichier exécutable portable (PE).</span><span class="sxs-lookup"><span data-stu-id="fca13-125">This will prevent the compiler from creating and embedding a default manifest in the portable executable (PE) file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fca13-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="fca13-126">Example</span></span>  
 <span data-ttu-id="fca13-127">L’exemple suivant présente le manifeste par défaut que le compilateur Visual C# insère dans un fichier PE.</span><span class="sxs-lookup"><span data-stu-id="fca13-127">The following example shows the default manifest that the Visual C# compiler inserts into a PE.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fca13-128">Le compilateur ajoute un nom d’application standard « MyApplication.app » au fichier xml.</span><span class="sxs-lookup"><span data-stu-id="fca13-128">The compiler inserts a standard application name " MyApplication.app " into the xml.</span></span> <span data-ttu-id="fca13-129">Cela permet aux applications de s’exécuter dans Windows Server 2003 Service Pack 3.</span><span class="sxs-lookup"><span data-stu-id="fca13-129">This is a workaround to enable applications to run on Windows Server 2003 Service Pack 3.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8" standalone="yes"?>  
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">  
  <assemblyIdentity version="1.0.0.0" name="MyApplication.app"/>  
  <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">  
    <security>  
      <requestedPrivileges xmlns="urn:schemas-microsoft-com:asm.v3">  
        <requestedExecutionLevel level="asInvoker"/>  
      </requestedPrivileges>  
    </security>  
  </trustInfo>  
</assembly>  
```  
  
## <a name="see-also"></a><span data-ttu-id="fca13-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fca13-130">See Also</span></span>  
 [<span data-ttu-id="fca13-131">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="fca13-131">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)  
 [<span data-ttu-id="fca13-132">-nowin32manifest (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="fca13-132">-nowin32manifest (C# Compiler Options)</span></span>](../../../csharp/language-reference/compiler-options/nowin32manifest-compiler-option.md)  
 [<span data-ttu-id="fca13-133">Gestion des propriétés des projets et des solutions</span><span class="sxs-lookup"><span data-stu-id="fca13-133">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
