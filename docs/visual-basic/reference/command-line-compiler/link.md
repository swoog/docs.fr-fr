---
title: -link (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- l compiler option [Visual Basic]
- EmbedInteropTypes
- embed interop types [COM Interop]
- -link compiler option [Visual Basic]
- /link compiler option [Visual Basic]
- link compiler option [Visual Basic]
- -l compiler option [Visual Basic]
- /l compiler option [Visual Basic]
ms.assetid: 1885f24a-86f5-486c-a064-9fb7e455ccec
ms.openlocfilehash: 91eba53eb8094e55af09d406515dad16fc71937d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43405300"
---
# <a name="-link-visual-basic"></a><span data-ttu-id="35e6f-102">-link (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="35e6f-102">-link (Visual Basic)</span></span>
<span data-ttu-id="35e6f-103">Fait que le compilateur rend disponible pour le projet en cours de compilation les informations de type COM des assemblys spécifiés.</span><span class="sxs-lookup"><span data-stu-id="35e6f-103">Causes the compiler to make COM type information in the specified assemblies available to the project that you are currently compiling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35e6f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35e6f-104">Syntax</span></span>  
  
```  
-link:fileList  
' -or-  
-l:fileList  
```  
  
## <a name="arguments"></a><span data-ttu-id="35e6f-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="35e6f-105">Arguments</span></span>  
  
|<span data-ttu-id="35e6f-106">Terme</span><span class="sxs-lookup"><span data-stu-id="35e6f-106">Term</span></span>|<span data-ttu-id="35e6f-107">Définition</span><span class="sxs-lookup"><span data-stu-id="35e6f-107">Definition</span></span>|  
|---|---|  
|`fileList`|<span data-ttu-id="35e6f-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="35e6f-108">Required.</span></span> <span data-ttu-id="35e6f-109">Liste délimitée par des virgules des noms de fichiers d’assembly.</span><span class="sxs-lookup"><span data-stu-id="35e6f-109">Comma-delimited list of assembly file names.</span></span> <span data-ttu-id="35e6f-110">Si le nom de fichier contient un espace, placez-le entre des guillemets.</span><span class="sxs-lookup"><span data-stu-id="35e6f-110">If the file name contains a space, enclose the name in quotation marks.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="35e6f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="35e6f-111">Remarks</span></span>  
 <span data-ttu-id="35e6f-112">L’option `-link` vous permet de déployer une application qui a des informations de type incorporées.</span><span class="sxs-lookup"><span data-stu-id="35e6f-112">The `-link` option enables you to deploy an application that has embedded type information.</span></span> <span data-ttu-id="35e6f-113">L’application peut ensuite utiliser des types dans un assembly de runtime qui implémentent les informations de type incorporées sans nécessiter une référence à l’assembly de runtime.</span><span class="sxs-lookup"><span data-stu-id="35e6f-113">The application can then use types in a runtime assembly that implement the embedded type information without requiring a reference to the runtime assembly.</span></span> <span data-ttu-id="35e6f-114">Si différentes versions de l’assembly de runtime sont publiées, l’application qui contient les informations de type incorporées peut fonctionner avec les différentes versions sans devoir être recompilée.</span><span class="sxs-lookup"><span data-stu-id="35e6f-114">If various versions of the runtime assembly are published, the application that contains the embedded type information can work with the various versions without having to be recompiled.</span></span> <span data-ttu-id="35e6f-115">Pour un exemple, consultez [Procédure pas à pas : incorporation de types provenant d’assemblys managés](https://msdn.microsoft.com/library/b28ec92c-1867-4847-95c0-61adfe095e21).</span><span class="sxs-lookup"><span data-stu-id="35e6f-115">For an example, see [Walkthrough: Embedding Types from Managed Assemblies](https://msdn.microsoft.com/library/b28ec92c-1867-4847-95c0-61adfe095e21).</span></span>  
  
 <span data-ttu-id="35e6f-116">L’utilisation de l’option `-link` est particulièrement utile quand vous travaillez avec COM Interop.</span><span class="sxs-lookup"><span data-stu-id="35e6f-116">Using the `-link` option is especially useful when you are working with COM interop.</span></span> <span data-ttu-id="35e6f-117">Vous pouvez incorporer des types COM afin que votre application ne nécessite plus un assembly PIA (Primary Interop Assembly) sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="35e6f-117">You can embed COM types so that your application no longer requires a primary interop assembly (PIA) on the target computer.</span></span> <span data-ttu-id="35e6f-118">L’option `-link` indique au compilateur d’incorporer les informations de type COM provenant de l’assembly Interop référencé dans le code compilé résultant.</span><span class="sxs-lookup"><span data-stu-id="35e6f-118">The `-link` option instructs the compiler to embed the COM type information from the referenced interop assembly into the resulting compiled code.</span></span> <span data-ttu-id="35e6f-119">Le type COM est identifié par la valeur du CLSID (GUID).</span><span class="sxs-lookup"><span data-stu-id="35e6f-119">The COM type is identified by the CLSID (GUID) value.</span></span> <span data-ttu-id="35e6f-120">Par conséquent, votre application peut s’exécuter sur un ordinateur cible où les mêmes types COM ont été installés avec les mêmes valeurs de CLSID.</span><span class="sxs-lookup"><span data-stu-id="35e6f-120">As a result, your application can run on a target computer that has installed the same COM types with the same CLSID values.</span></span> <span data-ttu-id="35e6f-121">Les applications qui automatisent Microsoft Office sont un bon exemple.</span><span class="sxs-lookup"><span data-stu-id="35e6f-121">Applications that automate Microsoft Office are a good example.</span></span> <span data-ttu-id="35e6f-122">Étant donné que les applications comme Office gardent habituellement la même valeur de CLSID à travers différentes versions, votre application peut utiliser les types COM référencés dès lors que le .NET Framework 4 ou ultérieur est installé sur l’ordinateur cible, et que votre application utilise les méthodes, propriétés ou événements qui sont inclus dans les types COM référencés.</span><span class="sxs-lookup"><span data-stu-id="35e6f-122">Because applications like Office usually keep the same CLSID value across different versions, your application can use the referenced COM types as long as .NET Framework 4 or later is installed on the target computer and your application uses methods, properties, or events that are included in the referenced COM types.</span></span>  
  
 <span data-ttu-id="35e6f-123">L’option `-link` incorpore seulement les interfaces, les structures et les délégués.</span><span class="sxs-lookup"><span data-stu-id="35e6f-123">The `-link` option embeds only interfaces, structures, and delegates.</span></span> <span data-ttu-id="35e6f-124">L’incorporation de classes COM n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="35e6f-124">Embedding COM classes is not supported.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="35e6f-125">Quand vous créez une instance d’un type COM incorporé dans votre code, vous devez créer l’instance à l’aide de l’interface appropriée.</span><span class="sxs-lookup"><span data-stu-id="35e6f-125">When you create an instance of an embedded COM type in your code, you must create the instance by using the appropriate interface.</span></span> <span data-ttu-id="35e6f-126">Une tentative de création d’une instance d’un type COM incorporé à l’aide de la coclasse provoque une erreur.</span><span class="sxs-lookup"><span data-stu-id="35e6f-126">Attempting to create an instance of an embedded COM type by using the CoClass causes an error.</span></span>  
  
 <span data-ttu-id="35e6f-127">Pour définir l’option `-link` dans Visual Studio, ajoutez une référence d’assembly et définissez la propriété `Embed Interop Types` sur **true**.</span><span class="sxs-lookup"><span data-stu-id="35e6f-127">To set the `-link` option in Visual Studio, add an assembly reference and set the `Embed Interop Types` property to **true**.</span></span> <span data-ttu-id="35e6f-128">La valeur par défaut pour la propriété `Embed Interop Types` est **false**.</span><span class="sxs-lookup"><span data-stu-id="35e6f-128">The default for the `Embed Interop Types` property is **false**.</span></span>  
  
 <span data-ttu-id="35e6f-129">Si vous liez à un assembly COM (Assembly A) qui référence lui-même un autre assembly COM (Assembly B), vous devez également lier à l’Assembly B si une des conditions suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="35e6f-129">If you link to a COM assembly (Assembly A) which itself references another COM assembly (Assembly B), you also have to link to Assembly B if either of the following is true:</span></span>  
  
-   <span data-ttu-id="35e6f-130">Un type de l’Assembly A hérite d’un type ou implémente une interface de l’Assembly B.</span><span class="sxs-lookup"><span data-stu-id="35e6f-130">A type from Assembly A inherits from a type or implements an interface from Assembly B.</span></span>  
  
-   <span data-ttu-id="35e6f-131">Un champ, une propriété, un événement ou une méthode qui a un type de retour ou un type de paramètre de l’Assembly B est appelé.</span><span class="sxs-lookup"><span data-stu-id="35e6f-131">A field, property, event, or method that has a return type or parameter type from Assembly B is invoked.</span></span>  
  
 <span data-ttu-id="35e6f-132">Utilisez [- libpath](../../../visual-basic/reference/command-line-compiler/libpath.md) pour spécifier le répertoire dans lequel sont trouvent une ou plusieurs de vos références d’assembly.</span><span class="sxs-lookup"><span data-stu-id="35e6f-132">Use [-libpath](../../../visual-basic/reference/command-line-compiler/libpath.md) to specify the directory in which one or more of your assembly references is located.</span></span>  
  
 <span data-ttu-id="35e6f-133">Comme le [/reference](../../../visual-basic/reference/command-line-compiler/reference.md) option du compilateur, le `-link` option du compilateur utilise le fichier réponse Vbc.rsp, qui référence fréquemment utilisés [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] assemblys.</span><span class="sxs-lookup"><span data-stu-id="35e6f-133">Like the [/reference](../../../visual-basic/reference/command-line-compiler/reference.md) compiler option, the `-link` compiler option uses the Vbc.rsp response file, which references frequently used [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] assemblies.</span></span> <span data-ttu-id="35e6f-134">Utiliser le [- noconfig](../../../visual-basic/reference/command-line-compiler/noconfig.md) option du compilateur si vous ne souhaitez pas que le compilateur utilise le fichier Vbc.rsp.</span><span class="sxs-lookup"><span data-stu-id="35e6f-134">Use the [-noconfig](../../../visual-basic/reference/command-line-compiler/noconfig.md) compiler option if you do not want the compiler to use the Vbc.rsp file.</span></span>  
  
 <span data-ttu-id="35e6f-135">La forme abrégée de `-link` est `-l`.</span><span class="sxs-lookup"><span data-stu-id="35e6f-135">The short form of `-link` is `-l`.</span></span>  
  
## <a name="generics-and-embedded-types"></a><span data-ttu-id="35e6f-136">Types génériques et imbriqués</span><span class="sxs-lookup"><span data-stu-id="35e6f-136">Generics and Embedded Types</span></span>  
 <span data-ttu-id="35e6f-137">Les sections suivantes décrivent les limitations de l’utilisation de types génériques dans les applications qui incorporent des types interop.</span><span class="sxs-lookup"><span data-stu-id="35e6f-137">The following sections describe the limitations on using generic types in applications that embed interop types.</span></span>  
  
### <a name="generic-interfaces"></a><span data-ttu-id="35e6f-138">Interfaces génériques</span><span class="sxs-lookup"><span data-stu-id="35e6f-138">Generic Interfaces</span></span>  
 <span data-ttu-id="35e6f-139">Vous ne pouvez pas utiliser des interfaces génériques incorporées depuis un assembly d’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="35e6f-139">Generic interfaces that are embedded from an interop assembly cannot be used.</span></span> <span data-ttu-id="35e6f-140">L'exemple suivant le démontre.</span><span class="sxs-lookup"><span data-stu-id="35e6f-140">This is shown in the following example.</span></span>  
  
 [!code-vb[VbLinkCompiler#1](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/link_1.vb)]  
  
### <a name="types-that-have-generic-parameters"></a><span data-ttu-id="35e6f-141">Types ayant des paramètres génériques</span><span class="sxs-lookup"><span data-stu-id="35e6f-141">Types That Have Generic Parameters</span></span>  
 <span data-ttu-id="35e6f-142">Vous ne pouvez pas utiliser des types qui ont un paramètre générique dont le type est incorporé depuis un assembly d’interopérabilité si ce type provient d’un assembly externe.</span><span class="sxs-lookup"><span data-stu-id="35e6f-142">Types that have a generic parameter whose type is embedded from an interop assembly cannot be used if that type is from an external assembly.</span></span> <span data-ttu-id="35e6f-143">Cette restriction ne s’applique pas aux interfaces.</span><span class="sxs-lookup"><span data-stu-id="35e6f-143">This restriction does not apply to interfaces.</span></span> <span data-ttu-id="35e6f-144">Prenons l’exemple de l’interface <xref:Microsoft.Office.Interop.Excel.Range> qui est définie dans l’assembly <xref:Microsoft.Office.Interop.Excel>.</span><span class="sxs-lookup"><span data-stu-id="35e6f-144">For example, consider the <xref:Microsoft.Office.Interop.Excel.Range> interface that is defined in the <xref:Microsoft.Office.Interop.Excel> assembly.</span></span> <span data-ttu-id="35e6f-145">Si une bibliothèque incorpore les types interop de l’assembly <xref:Microsoft.Office.Interop.Excel> et expose une méthode qui retourne un type générique qui a un paramètre dont le type est l’interface <xref:Microsoft.Office.Interop.Excel.Range>, cette méthode doit retourner une interface générique, comme dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="35e6f-145">If a library embeds interop types from the <xref:Microsoft.Office.Interop.Excel> assembly and exposes a method that returns a generic type that has a parameter whose type is the <xref:Microsoft.Office.Interop.Excel.Range> interface, that method must return a generic interface, as shown in the following code example.</span></span>  
  
 [!code-vb[VbLinkCompiler#2](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/link_2.vb)]  
[!code-vb[VbLinkCompiler#3](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/link_3.vb)]  
[!code-vb[VbLinkCompiler#4](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/link_4.vb)]  
  
 <span data-ttu-id="35e6f-146">Dans l’exemple suivant, le code client peut appeler la méthode qui retourne l’interface générique <xref:System.Collections.IList> sans erreur.</span><span class="sxs-lookup"><span data-stu-id="35e6f-146">In the following example, client code can call the method that returns the <xref:System.Collections.IList> generic interface without error.</span></span>  
  
 [!code-vb[VbLinkCompiler#5](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/link_5.vb)]  
  
## <a name="example"></a><span data-ttu-id="35e6f-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="35e6f-147">Example</span></span>  
 <span data-ttu-id="35e6f-148">La ligne de commande suivante compile le fichier source `OfficeApp.vb` et référence des assemblys à partir de `COMData1.dll` et `COMData2.dll` pour produire `OfficeApp.exe`.</span><span class="sxs-lookup"><span data-stu-id="35e6f-148">The following command line compiles source file `OfficeApp.vb` and reference assemblies from `COMData1.dll` and `COMData2.dll` to produce `OfficeApp.exe`.</span></span>  
  
```console  
vbc -link:COMData1.dll,COMData2.dll /out:OfficeApp.exe OfficeApp.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="35e6f-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35e6f-149">See Also</span></span>  
 [<span data-ttu-id="35e6f-150">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="35e6f-150">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="35e6f-151">Procédure pas à pas : incorporation de types provenant d’assemblys managés</span><span class="sxs-lookup"><span data-stu-id="35e6f-151">Walkthrough: Embedding Types from Managed Assemblies</span></span>](https://msdn.microsoft.com/library/b28ec92c-1867-4847-95c0-61adfe095e21)  
 [<span data-ttu-id="35e6f-152">-référence (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="35e6f-152">-reference (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/reference.md)  
 [<span data-ttu-id="35e6f-153">-noconfig</span><span class="sxs-lookup"><span data-stu-id="35e6f-153">-noconfig</span></span>](../../../visual-basic/reference/command-line-compiler/noconfig.md)  
 [<span data-ttu-id="35e6f-154">-libpath</span><span class="sxs-lookup"><span data-stu-id="35e6f-154">-libpath</span></span>](../../../visual-basic/reference/command-line-compiler/libpath.md)  
 [<span data-ttu-id="35e6f-155">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="35e6f-155">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="35e6f-156">Introduction à COM Interop</span><span class="sxs-lookup"><span data-stu-id="35e6f-156">Introduction to COM Interop</span></span>](../../../visual-basic/programming-guide/com-interop/introduction-to-com-interop.md)
