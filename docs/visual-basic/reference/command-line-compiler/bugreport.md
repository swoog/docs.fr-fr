---
title: -bugreport
ms.date: 03/08/2018
helpviewer_keywords:
- -bugreport compiler option [Visual Basic]
- bugreport compiler option [Visual Basic]
- /bugreport compiler option [Visual Basic]
ms.assetid: e4325406-8dbd-4b48-b311-9ee0799e48bb
ms.openlocfilehash: 0383a5e369ee4a8146764c13b2f12f48ebe52190
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33653492"
---
# <a name="-bugreport"></a><span data-ttu-id="bd0a6-102">-bugreport</span><span class="sxs-lookup"><span data-stu-id="bd0a6-102">-bugreport</span></span>
<span data-ttu-id="bd0a6-103">Crée un fichier que vous pouvez utiliser lorsque vous archivez un rapport de bogue.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-103">Creates a file that you can use when you file a bug report.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd0a6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd0a6-104">Syntax</span></span>  
  
```  
-bugreport:file  
```  
  
## <a name="arguments"></a><span data-ttu-id="bd0a6-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="bd0a6-105">Arguments</span></span>  
  
|<span data-ttu-id="bd0a6-106">Terme</span><span class="sxs-lookup"><span data-stu-id="bd0a6-106">Term</span></span>|<span data-ttu-id="bd0a6-107">Définition</span><span class="sxs-lookup"><span data-stu-id="bd0a6-107">Definition</span></span>|  
|---|---|  
|`file`|<span data-ttu-id="bd0a6-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-108">Required.</span></span> <span data-ttu-id="bd0a6-109">Le nom du fichier qui contient votre rapport de bogue.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-109">The name of the file that will contain your bug report.</span></span> <span data-ttu-id="bd0a6-110">Placez le nom de fichier entre guillemets ( » «) si le nom contient un espace.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-110">Enclose the file name in quotation marks (" ") if the name contains a space.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bd0a6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bd0a6-111">Remarks</span></span>  
 <span data-ttu-id="bd0a6-112">Les informations suivantes sont ajoutées à `file`:</span><span class="sxs-lookup"><span data-stu-id="bd0a6-112">The following information is added to `file`:</span></span>  
  
-   <span data-ttu-id="bd0a6-113">Une copie de tous les fichiers de code source dans la compilation.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-113">A copy of all source-code files in the compilation.</span></span>  
  
-   <span data-ttu-id="bd0a6-114">Une liste des options du compilateur utilisé dans la compilation.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-114">A list of the compiler options used in the compilation.</span></span>  
  
-   <span data-ttu-id="bd0a6-115">Informations de version sur votre compilateur, le common language runtime et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-115">Version information about your compiler, common language runtime, and operating system.</span></span>  
  
-   <span data-ttu-id="bd0a6-116">Les résultats de la compilation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-116">Compiler output, if any.</span></span>  
  
-   <span data-ttu-id="bd0a6-117">Description du problème pour lequel vous êtes invité.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-117">A description of the problem, for which you are prompted.</span></span>  
  
-   <span data-ttu-id="bd0a6-118">Obtenir une description de la façon dont vous pensez que le problème doit être corrigée pour lequel vous êtes invité.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-118">A description of how you think the problem should be fixed, for which you are prompted.</span></span>  
  
 <span data-ttu-id="bd0a6-119">Une copie de tous les fichiers de code source est inclus dans `file`, vous pouvez souhaiter reproduire l’erreur de code (supposée) dans le programme le plus court possible.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-119">Because a copy of all source-code files is included in `file`, you may want to reproduce the (suspected) code defect in the shortest possible program.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="bd0a6-120">Le `-bugreport` option génère un fichier qui contient des informations potentiellement sensibles.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-120">The `-bugreport` option produces a file that contains potentially sensitive information.</span></span> <span data-ttu-id="bd0a6-121">Cela inclut l’heure actuelle, la version du compilateur, [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] version, version du système d’exploitation, nom d’utilisateur, les arguments de ligne de commande avec laquelle le compilateur a été exécuté, tout le code source, et la forme binaire de tout assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-121">This includes current time, compiler version, [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] version, OS version, user name, the command-line arguments with which the compiler was run, all source code, and the binary form of any referenced assembly.</span></span> <span data-ttu-id="bd0a6-122">Cette option est accessible en spécifiant des options de ligne de commande dans le fichier Web.config pour une compilation côté serveur d’un [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] application.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-122">This option can be accessed by specifying command-line options in the Web.config file for a server-side compilation of an [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] application.</span></span> <span data-ttu-id="bd0a6-123">Pour éviter ce problème, modifiez le fichier Machine.config pour empêcher les utilisateurs de se compiler sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-123">To prevent this, modify the Machine.config file to disallow users from compiling on the server.</span></span>  
  
 <span data-ttu-id="bd0a6-124">Si cette option est utilisée avec `-errorreport:prompt`, `-errorreport:queue`, ou `-errorreport:send`, et votre application rencontre une erreur interne du compilateur, les informations contenues dans `file` sont envoyées à Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-124">If this option is used with `-errorreport:prompt`, `-errorreport:queue`, or `-errorreport:send`, and your application encounters an internal compiler error, the information in `file` is sent to Microsoft Corporation.</span></span> <span data-ttu-id="bd0a6-125">Ces informations aideront les ingénieurs de Microsoft à identifier la cause de l’erreur et peuvent aider à améliorer la prochaine version de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-125">That information will help Microsoft engineers identify the cause of the error and may help improve the next release of Visual Basic.</span></span> <span data-ttu-id="bd0a6-126">Par défaut, aucune information n’est envoyée à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-126">By default, no information is sent to Microsoft.</span></span> <span data-ttu-id="bd0a6-127">Toutefois, lorsque vous compilez une application à l’aide de `-errorreport:queue`, qui est activé par défaut, l’application rassemble ses rapports d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-127">However, when you compile an application by using `-errorreport:queue`, which is enabled by default, the application collects its error reports.</span></span> <span data-ttu-id="bd0a6-128">Ensuite, lorsque l’administrateur de l’ordinateur se connecte, le système de création de rapports d’erreurs affiche une fenêtre contextuelle qui permet à l’administrateur à envoyer à Microsoft les rapports de toute erreur qui se sont produites depuis l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-128">Then, when the computer's administrator logs in, the error reporting system displays a pop-up window that enables the administrator to forward to Microsoft any error reports that occurred since the logon.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bd0a6-129">Le `/bugreport` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lorsque vous compilez à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-129">The `/bugreport` option is not available from within the Visual Studio development environment; it is available only when you compile from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bd0a6-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="bd0a6-130">Example</span></span>  
 <span data-ttu-id="bd0a6-131">L’exemple suivant compile `T2.vb` et y place toutes les informations de rapport de bogue dans le fichier `Problem.txt`.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-131">The following example compiles `T2.vb` and puts all bug-reporting information in the file `Problem.txt`.</span></span>  
  
```  
vbc -bugreport:problem.txt t2.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="bd0a6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd0a6-132">See Also</span></span>  
 [<span data-ttu-id="bd0a6-133">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bd0a6-133">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="bd0a6-134">-debug (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bd0a6-134">-debug (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/debug.md)  
 [<span data-ttu-id="bd0a6-135">-errorreport</span><span class="sxs-lookup"><span data-stu-id="bd0a6-135">-errorreport</span></span>](../../../visual-basic/reference/command-line-compiler/errorreport.md)  
 [<span data-ttu-id="bd0a6-136">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="bd0a6-136">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="bd0a6-137">trustLevel, élément de securityPolicy (schéma des paramètres ASP.NET)</span><span class="sxs-lookup"><span data-stu-id="bd0a6-137">trustLevel Element for securityPolicy (ASP.NET Settings Schema)</span></span>](http://msdn.microsoft.com/library/729ab04c-03da-4ee5-86b1-be9d08a09369)
