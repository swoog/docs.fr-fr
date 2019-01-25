---
title: -doc
ms.date: 03/10/2018
helpviewer_keywords:
- doc compiler option [Visual Basic]
- -doc compiler option [Visual Basic]
- /doc compiler option [Visual Basic]
ms.assetid: 5fc32ec9-a149-4648-994c-a8d0cccd0a65
ms.openlocfilehash: eccd68d77eb9afabdc3bd4301f6258b80b7d7e7f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54736651"
---
# <a name="-doc"></a><span data-ttu-id="6dd48-102">-doc</span><span class="sxs-lookup"><span data-stu-id="6dd48-102">-doc</span></span>
<span data-ttu-id="6dd48-103">Traite les commentaires de documentation pour les diriger vers un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="6dd48-103">Processes documentation comments to an XML file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6dd48-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6dd48-104">Syntax</span></span>  
  
```  
-doc[+ | -]  
' -or-  
-doc:file  
```  
  
## <a name="arguments"></a><span data-ttu-id="6dd48-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="6dd48-105">Arguments</span></span>  
  
|<span data-ttu-id="6dd48-106">Terme</span><span class="sxs-lookup"><span data-stu-id="6dd48-106">Term</span></span>|<span data-ttu-id="6dd48-107">Définition</span><span class="sxs-lookup"><span data-stu-id="6dd48-107">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="6dd48-108">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="6dd48-108">`+` &#124; `-`</span></span>|<span data-ttu-id="6dd48-109">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6dd48-109">Optional.</span></span> <span data-ttu-id="6dd48-110">Si vous spécifiez +, ou simplement `-doc`, le compilateur génère des informations de documentation et les place dans un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="6dd48-110">Specifying +, or just `-doc`, causes the compiler to generate documentation information and place it in an XML file.</span></span> <span data-ttu-id="6dd48-111">Si vous spécifiez `-`, ce qui équivaut à ne pas spécifier `-doc`, aucune information de documentation n’est créée.</span><span class="sxs-lookup"><span data-stu-id="6dd48-111">Specifying `-` is the equivalent of not specifying `-doc`, causing no documentation information to be created.</span></span>|  
|`file`|<span data-ttu-id="6dd48-112">Obligatoire si l'option `-doc:` est utilisée.</span><span class="sxs-lookup"><span data-stu-id="6dd48-112">Required if `-doc:` is used.</span></span> <span data-ttu-id="6dd48-113">Spécifie le fichier XML de sortie, qui est renseigné avec les commentaires des fichiers de code source de la compilation.</span><span class="sxs-lookup"><span data-stu-id="6dd48-113">Specifies the output XML file, which is populated with the comments from the source-code files of the compilation.</span></span> <span data-ttu-id="6dd48-114">Si le nom de fichier contient un espace, placez-le entre des guillemets (" ").</span><span class="sxs-lookup"><span data-stu-id="6dd48-114">If the file name contains a space, surround the name with quotation marks (" ").</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6dd48-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6dd48-115">Remarks</span></span>  
 <span data-ttu-id="6dd48-116">L’option `-doc` contrôle si le compilateur génère un fichier XML contenant les commentaires de documentation.</span><span class="sxs-lookup"><span data-stu-id="6dd48-116">The `-doc` option controls whether the compiler generates an XML file containing the documentation comments.</span></span> <span data-ttu-id="6dd48-117">Si vous utilisez la syntaxe `-doc:file`, le paramètre `file` spécifie le nom du fichier XML.</span><span class="sxs-lookup"><span data-stu-id="6dd48-117">If you use the `-doc:file` syntax, the `file` parameter specifies the name of the XML file.</span></span> <span data-ttu-id="6dd48-118">Si vous utilisez `-doc` ou `-doc+`, le compilateur prend le nom de fichier XML du fichier exécutable ou de la bibliothèque en cours de création.</span><span class="sxs-lookup"><span data-stu-id="6dd48-118">If you use `-doc` or `-doc+`, the compiler takes the XML file name from the executable file or library that the compiler is creating.</span></span> <span data-ttu-id="6dd48-119">Si vous utilisez `-doc-` ou que vous ne spécifiez pas l’option `-doc`, le compilateur ne crée pas de fichier XML.</span><span class="sxs-lookup"><span data-stu-id="6dd48-119">If you use `-doc-` or do not specify the `-doc` option, the compiler does not create an XML file.</span></span>  
  
 <span data-ttu-id="6dd48-120">Dans les fichiers de code source, des commentaires de documentation peuvent précéder les définitions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6dd48-120">In source-code files, documentation comments can precede the following definitions:</span></span>  
  
-   <span data-ttu-id="6dd48-121">Types définis par l’utilisateur ([classe](../../../visual-basic/language-reference/statements/class-statement.md), [interface](../../../visual-basic/language-reference/statements/interface-statement.md), etc.)</span><span class="sxs-lookup"><span data-stu-id="6dd48-121">User-defined types, such as a [class](../../../visual-basic/language-reference/statements/class-statement.md) or [interface](../../../visual-basic/language-reference/statements/interface-statement.md)</span></span>  
  
-   <span data-ttu-id="6dd48-122">Membres (champ, [événement](../../../visual-basic/language-reference/statements/event-statement.md), [propriété](../../../visual-basic/language-reference/statements/property-statement.md), [fonction](../../../visual-basic/language-reference/statements/function-statement.md), [sous-routine](../../../visual-basic/language-reference/statements/sub-statement.md), etc.)</span><span class="sxs-lookup"><span data-stu-id="6dd48-122">Members, such as a field, [event](../../../visual-basic/language-reference/statements/event-statement.md), [property](../../../visual-basic/language-reference/statements/property-statement.md), [function](../../../visual-basic/language-reference/statements/function-statement.md), or [subroutine](../../../visual-basic/language-reference/statements/sub-statement.md).</span></span>  
  
 <span data-ttu-id="6dd48-123">Pour utiliser le fichier XML généré avec la fonctionnalité [IntelliSense](/visualstudio/ide/using-intellisense) de Visual Studio, faites en sorte que le nom du fichier XML soit identique à l’assembly que vous souhaitez prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="6dd48-123">To use the generated XML file with the Visual Studio [IntelliSense](/visualstudio/ide/using-intellisense) feature, let the file name of the XML file be the same as the assembly you want to support.</span></span> <span data-ttu-id="6dd48-124">Vérifiez que le fichier XML se trouve dans le même répertoire que l’assembly. De cette façon, quand l’assembly est référencé dans le projet Visual Studio, le fichier .xml est aussi localisé.</span><span class="sxs-lookup"><span data-stu-id="6dd48-124">Make sure the XML file is in the same directory as the assembly so that when the assembly is referenced in the Visual Studio project, the .xml file is found as well.</span></span> <span data-ttu-id="6dd48-125">Les fichiers de documentation XML ne sont pas nécessaires au bon fonctionnement d’IntelliSense avec du code dans un projet ou dans des projets référencés par un projet.</span><span class="sxs-lookup"><span data-stu-id="6dd48-125">XML documentation files are not required for IntelliSense to work for code within a project or within projects referenced by a project.</span></span>  
  
 <span data-ttu-id="6dd48-126">Le fichier XML contient les balises `<assembly></assembly>`, sauf si vous effectuez la compilation avec `/target:module`.</span><span class="sxs-lookup"><span data-stu-id="6dd48-126">Unless you compile with `/target:module`, the XML file contains the tags `<assembly></assembly>`.</span></span> <span data-ttu-id="6dd48-127">Ces balises spécifient le nom du fichier contenant le manifeste d’assembly pour le fichier de sortie de la compilation.</span><span class="sxs-lookup"><span data-stu-id="6dd48-127">These tags specify the name of the file containing the assembly manifest for the output file of the compilation.</span></span>  
  
 <span data-ttu-id="6dd48-128">Pour découvrir comment générer de la documentation à partir de commentaires dans votre code, consultez [Balises de commentaires XML](../../../visual-basic/language-reference/xmldoc/index.md).</span><span class="sxs-lookup"><span data-stu-id="6dd48-128">See [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/index.md) for ways to generate documentation from comments in your code.</span></span>  
  
|<span data-ttu-id="6dd48-129">Pour définir -doc dans l’environnement de développement intégré Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6dd48-129">To set -doc in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="6dd48-130">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="6dd48-130">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="6dd48-131">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="6dd48-131">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="6dd48-132">2.  Cliquez sur l’onglet **Compiler**.</span><span class="sxs-lookup"><span data-stu-id="6dd48-132">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="6dd48-133">3.  Définissez la valeur dans la zone **Générer le fichier de documentation XML**.</span><span class="sxs-lookup"><span data-stu-id="6dd48-133">3.  Set the value in the **Generate XML documentation file** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="6dd48-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="6dd48-134">Example</span></span>  
 <span data-ttu-id="6dd48-135">Pour obtenir un exemple, consultez [Documentation de votre code avec le langage XML](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md).</span><span class="sxs-lookup"><span data-stu-id="6dd48-135">See [Documenting Your Code with XML](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md) for a sample.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6dd48-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dd48-136">See also</span></span>
- [<span data-ttu-id="6dd48-137">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6dd48-137">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="6dd48-138">Documentation de votre code avec le langage XML</span><span class="sxs-lookup"><span data-stu-id="6dd48-138">Documenting Your Code with XML</span></span>](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)
