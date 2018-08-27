---
title: 'Comment : appeler le compilateur de ligne de commande (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- command-line arguments
- vbc.exe
- Visual Basic compiler, starting
- command line [Visual Basic], arguments
ms.assetid: 0fd9a8f6-f34e-4c35-a49d-9b9bbd8da4a9
ms.openlocfilehash: 0b835bb5654574a5aa6f32eede1e942b11e7dcb0
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932152"
---
# <a name="how-to-invoke-the-command-line-compiler-visual-basic"></a><span data-ttu-id="c6329-102">Comment : appeler le compilateur de ligne de commande (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c6329-102">How to: Invoke the Command-Line Compiler (Visual Basic)</span></span>
<span data-ttu-id="c6329-103">Vous pouvez appeler le compilateur de ligne de commande en tapant le nom de son fichier exécutable dans la ligne de commande, également appelée invite de commande MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="c6329-103">You can invoke the command-line compiler by typing the name of its executable file into the command line, also known as the MS-DOS prompt.</span></span> <span data-ttu-id="c6329-104">Si vous compilez à partir de l’invite de commandes de Windows par défaut, vous devez taper le chemin d’accès complet au fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="c6329-104">If you compile from the default Windows Command Prompt, you must type the fully qualified path to the executable file.</span></span> <span data-ttu-id="c6329-105">Pour remplacer ce comportement par défaut, vous pouvez utiliser l’invite de commandes Visual Studio, ou modifier la variable d’environnement PATH.</span><span class="sxs-lookup"><span data-stu-id="c6329-105">To override this default behavior, you can either use the Visual Studio Command Prompt, or modify the PATH environment variable.</span></span> <span data-ttu-id="c6329-106">Les deux permettent de compiler à partir de n’importe quel répertoire il suffit de taper le nom du compilateur.</span><span class="sxs-lookup"><span data-stu-id="c6329-106">Both allow you to compile from any directory by simply typing the compiler name.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-invoke-the-compiler-using-the-visual-studio-command-prompt"></a><span data-ttu-id="c6329-107">Pour appeler le compilateur à l’aide de l’invite de commandes Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c6329-107">To invoke the compiler using the Visual Studio Command Prompt</span></span>  
  
1.  <span data-ttu-id="c6329-108">Ouvrez le dossier de programme Visual Studio Tools dans le groupe de programmes de Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c6329-108">Open the Visual Studio Tools program folder within the Microsoft Visual Studio program group.</span></span>  
  
2.  <span data-ttu-id="c6329-109">Vous pouvez utiliser l’invite de commandes Visual Studio pour accéder au compilateur à partir de n’importe quel répertoire sur votre ordinateur, si Visual Studio est installé.</span><span class="sxs-lookup"><span data-stu-id="c6329-109">You can use the Visual Studio Command Prompt to access the compiler from any directory on your machine, if Visual Studio is installed.</span></span>  
  
3.  <span data-ttu-id="c6329-110">Appeler l’invite de commandes de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c6329-110">Invoke the Visual Studio Command Prompt.</span></span>  
  
4.  <span data-ttu-id="c6329-111">À la ligne de commande, tapez `vbc.exe` *sourceFileName* puis appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="c6329-111">At the command line, type `vbc.exe` *sourceFileName* and then press ENTER.</span></span>  
  
     <span data-ttu-id="c6329-112">Par exemple, si vous avez stocké votre code source dans un répertoire appelé `SourceFiles`, vous ouvririez l’invite de commandes et le type `cd SourceFiles` pour accéder à ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="c6329-112">For example, if you stored your source code in a directory called `SourceFiles`, you would open the Command Prompt and type `cd SourceFiles` to change to that directory.</span></span> <span data-ttu-id="c6329-113">Si le répertoire contenait un fichier source nommé `Source.vb`, vous pouvez le compiler en tapant `vbc.exe Source.vb`.</span><span class="sxs-lookup"><span data-stu-id="c6329-113">If the directory contained a source file named `Source.vb`, you could compile it by typing `vbc.exe Source.vb`.</span></span>  
  
### <a name="to-set-the-path-environment-variable-to-the-compiler-for-the-windows-command-prompt"></a><span data-ttu-id="c6329-114">Pour définir la variable d’environnement de chemin d’accès au compilateur pour l’invite de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="c6329-114">To set the PATH environment variable to the compiler for the Windows Command Prompt</span></span>  
  
1.  <span data-ttu-id="c6329-115">Utilisez la fonctionnalité de Windows Search pour rechercher Vbc.exe sur votre disque local.</span><span class="sxs-lookup"><span data-stu-id="c6329-115">Use the Windows Search feature to find Vbc.exe on your local disk.</span></span>  
  
     <span data-ttu-id="c6329-116">Le nom exact du répertoire où se trouve le compilateur dépend de l’emplacement du répertoire Windows et la version de « Installé le .NET Framework ».</span><span class="sxs-lookup"><span data-stu-id="c6329-116">The exact name of the directory where the compiler is located depends on the location of the Windows directory and the version of the ".NET Framework" installed.</span></span> <span data-ttu-id="c6329-117">Si vous avez plusieurs versions de « .NET Framework » installé, vous devez déterminer quelle version utiliser (généralement la dernière version).</span><span class="sxs-lookup"><span data-stu-id="c6329-117">If you have more than one version of the ".NET Framework" installed, you must determine which version to use (typically the latest version).</span></span>  
  
2.  <span data-ttu-id="c6329-118">À partir de votre **Démarrer** Menu, avec le bouton droit **poste de travail**, puis cliquez sur **propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c6329-118">From your **Start** Menu, right-click **My Computer**, and then click **Properties** from the shortcut menu.</span></span>  
  
3.  <span data-ttu-id="c6329-119">Cliquez sur le **avancé** onglet, puis cliquez sur **Variables d’environnement**.</span><span class="sxs-lookup"><span data-stu-id="c6329-119">Click the **Advanced** tab, and then click **Environment Variables**.</span></span>  
  
4.  <span data-ttu-id="c6329-120">Dans le **système** volet variables, sélectionnez **chemin d’accès** à partir de la liste et cliquez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="c6329-120">In the **System** variables pane, select **Path** from the list and click **Edit**.</span></span>  
  
5.  <span data-ttu-id="c6329-121">Dans le **système modifier** boîte de dialogue Variable déplacer le point d’insertion à la fin de la chaîne dans le **valeur de la Variable** champ et tapez un point-virgule ( ;) suivi du nom complet du répertoire trouvé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="c6329-121">In the **Edit System** Variable dialog box, move the insertion point to the end of the string in the **Variable Value** field and type a semicolon (;) followed by the full directory name found in Step 1.</span></span>  
  
6.  <span data-ttu-id="c6329-122">Cliquez sur **OK** pour confirmer vos modifications et fermer les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c6329-122">Click **OK** to confirm your edits and close the dialog boxes.</span></span>  
  
     <span data-ttu-id="c6329-123">Après avoir modifié la variable d’environnement PATH, vous pouvez exécuter le compilateur Visual Basic à l’invite de commandes Windows à partir de n’importe quel répertoire sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c6329-123">After you change the PATH environment variable, you can run the Visual Basic compiler at the Windows Command Prompt from any directory on the computer.</span></span>  
  
### <a name="to-invoke-the-compiler-using-the-windows-command-prompt"></a><span data-ttu-id="c6329-124">Pour appeler le compilateur à l’aide de l’invite de commandes Windows</span><span class="sxs-lookup"><span data-stu-id="c6329-124">To invoke the compiler using the Windows Command Prompt</span></span>  
  
1.  <span data-ttu-id="c6329-125">À partir de la **Démarrer** menu, cliquez sur le **Accessoires** , puis ouvrez le **invite de commandes Windows**.</span><span class="sxs-lookup"><span data-stu-id="c6329-125">From the **Start** menu, click on the **Accessories** folder, and then open the **Windows Command Prompt**.</span></span>  
  
2.  <span data-ttu-id="c6329-126">À la ligne de commande, tapez `vbc.exe` *sourceFileName* puis appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="c6329-126">At the command line, type `vbc.exe`*sourceFileName* and then press ENTER.</span></span>  
  
     <span data-ttu-id="c6329-127">Par exemple, si vous avez stocké votre code source dans un répertoire appelé `SourceFiles`, vous ouvririez l’invite de commandes et le type `cd SourceFiles` pour accéder à ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="c6329-127">For example, if you stored your source code in a directory called `SourceFiles`, you would open the Command Prompt and type `cd SourceFiles` to change to that directory.</span></span> <span data-ttu-id="c6329-128">Si le répertoire contenait un fichier source nommé `Source.vb`, vous pouvez le compiler en tapant `vbc.exe Source.vb`.</span><span class="sxs-lookup"><span data-stu-id="c6329-128">If the directory contained a source file named `Source.vb`, you could compile it by typing `vbc.exe Source.vb`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6329-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6329-129">See Also</span></span>  
 [<span data-ttu-id="c6329-130">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c6329-130">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="c6329-131">Compilation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="c6329-131">Conditional Compilation</span></span>](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
