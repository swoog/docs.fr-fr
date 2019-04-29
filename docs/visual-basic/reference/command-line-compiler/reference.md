---
title: -référence (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- /reference compiler option [Visual Basic]
- r compiler option [Visual Basic]
- -reference compiler option [Visual Basic]
- /r compiler option [Visual Basic]
- reference compiler option [Visual Basic]
- -r compiler option [Visual Basic]
ms.assetid: 66bdfced-bbf6-43d1-a554-bc0990315737
ms.openlocfilehash: 21efca701eb16898dd291d73bf0431641ba75d12
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61788880"
---
# <a name="-reference-visual-basic"></a><span data-ttu-id="9db73-102">-référence (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9db73-102">-reference (Visual Basic)</span></span>
<span data-ttu-id="9db73-103">Indique au compilateur de rendre les informations de type dans les assemblys spécifiés disponibles pour le projet en cours de compilation.</span><span class="sxs-lookup"><span data-stu-id="9db73-103">Causes the compiler to make type information in the specified assemblies available to the project you are currently compiling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9db73-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9db73-104">Syntax</span></span>  
  
```  
-reference:fileList  
' -or-  
-r:fileList  
```  
  
## <a name="arguments"></a><span data-ttu-id="9db73-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="9db73-105">Arguments</span></span>  
  
|<span data-ttu-id="9db73-106">Terme</span><span class="sxs-lookup"><span data-stu-id="9db73-106">Term</span></span>|<span data-ttu-id="9db73-107">Définition</span><span class="sxs-lookup"><span data-stu-id="9db73-107">Definition</span></span>|  
|---|---|  
|`fileList`|<span data-ttu-id="9db73-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9db73-108">Required.</span></span> <span data-ttu-id="9db73-109">Liste délimitée par des virgules des noms de fichiers d’assembly.</span><span class="sxs-lookup"><span data-stu-id="9db73-109">Comma-delimited list of assembly file names.</span></span> <span data-ttu-id="9db73-110">Si le nom de fichier contient un espace, placez-le entre des guillemets.</span><span class="sxs-lookup"><span data-stu-id="9db73-110">If the file name contains a space, enclose the name in quotation marks.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9db73-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9db73-111">Remarks</span></span>  
 <span data-ttu-id="9db73-112">Les fichiers que vous importez doivent contenir des métadonnées de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="9db73-112">The file(s) you import must contain assembly metadata.</span></span> <span data-ttu-id="9db73-113">Seuls les types publics sont visibles en dehors de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="9db73-113">Only public types are visible outside the assembly.</span></span> <span data-ttu-id="9db73-114">Le [/addmodule](../../../visual-basic/reference/command-line-compiler/addmodule.md) option importe des métadonnées à partir d’un module.</span><span class="sxs-lookup"><span data-stu-id="9db73-114">The [/addmodule](../../../visual-basic/reference/command-line-compiler/addmodule.md) option imports metadata from a module.</span></span>  
  
 <span data-ttu-id="9db73-115">Si vous référencez un assembly (Assembly A) qui lui-même référence un autre assembly (Assembly B), vous devez référencer l’Assembly B si :</span><span class="sxs-lookup"><span data-stu-id="9db73-115">If you reference an assembly (Assembly A) which itself references another assembly (Assembly B), you need to reference Assembly B if:</span></span>  
  
- <span data-ttu-id="9db73-116">Un type de l’Assembly A hérite d’un type ou implémente une interface de l’Assembly B.</span><span class="sxs-lookup"><span data-stu-id="9db73-116">A type from Assembly A inherits from a type or implements an interface from Assembly B.</span></span>  
  
- <span data-ttu-id="9db73-117">Un champ, une propriété, un événement ou une méthode qui a un type de retour ou un type de paramètre de l’Assembly B est appelé.</span><span class="sxs-lookup"><span data-stu-id="9db73-117">A field, property, event, or method that has a return type or parameter type from Assembly B is invoked.</span></span>  
  
 <span data-ttu-id="9db73-118">Utilisez [- libpath](../../../visual-basic/reference/command-line-compiler/libpath.md) pour spécifier le répertoire dans lequel sont trouvent une ou plusieurs de vos références d’assembly.</span><span class="sxs-lookup"><span data-stu-id="9db73-118">Use [-libpath](../../../visual-basic/reference/command-line-compiler/libpath.md) to specify the directory in which one or more of your assembly references is located.</span></span>  
  
 <span data-ttu-id="9db73-119">Pour le compilateur reconnaisse un type dans un assembly (pas un module), il doit être forcé à résoudre le type.</span><span class="sxs-lookup"><span data-stu-id="9db73-119">For the compiler to recognize a type in an assembly (not a module), it must be forced to resolve the type.</span></span> <span data-ttu-id="9db73-120">Un exemple de comment vous pouvez faire cela consiste à définir une instance du type.</span><span class="sxs-lookup"><span data-stu-id="9db73-120">One example of how you can do this is to define an instance of the type.</span></span> <span data-ttu-id="9db73-121">Autres méthodes sont disponibles pour résoudre les noms de type dans un assembly pour le compilateur.</span><span class="sxs-lookup"><span data-stu-id="9db73-121">Other ways are available to resolve type names in an assembly for the compiler.</span></span> <span data-ttu-id="9db73-122">Par exemple, si vous héritez d’un type dans un assembly, le nom de type puis devienne connu du compilateur.</span><span class="sxs-lookup"><span data-stu-id="9db73-122">For example, if you inherit from a type in an assembly, the type name then becomes known to the compiler.</span></span>  
  
 <span data-ttu-id="9db73-123">Le fichier réponse Vbc.rsp, qui référence couramment utilisés [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] assemblys, est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="9db73-123">The Vbc.rsp response file, which references commonly used [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] assemblies, is used by default.</span></span> <span data-ttu-id="9db73-124">Utilisez `-noconfig` si vous ne souhaitez pas que le compilateur utilise Vbc.rsp.</span><span class="sxs-lookup"><span data-stu-id="9db73-124">Use `-noconfig` if you do not want the compiler to use Vbc.rsp.</span></span>  
  
 <span data-ttu-id="9db73-125">La forme abrégée de `-reference` est `/r`.</span><span class="sxs-lookup"><span data-stu-id="9db73-125">The short form of `-reference` is `/r`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9db73-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="9db73-126">Example</span></span>  
 <span data-ttu-id="9db73-127">La commande suivante compile le fichier source `Input.vb` et référence des assemblys à partir de `Metad1.dll` et `Metad2.dll` pour produire `Out.exe`.</span><span class="sxs-lookup"><span data-stu-id="9db73-127">The following command compiles source file `Input.vb` and reference assemblies from `Metad1.dll` and `Metad2.dll` to produce `Out.exe`.</span></span>  
  
```console
vbc -reference:metad1.dll,metad2.dll -out:out.exe input.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="9db73-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9db73-128">See also</span></span>

- [<span data-ttu-id="9db73-129">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9db73-129">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="9db73-130">-noconfig</span><span class="sxs-lookup"><span data-stu-id="9db73-130">-noconfig</span></span>](../../../visual-basic/reference/command-line-compiler/noconfig.md)
- [<span data-ttu-id="9db73-131">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9db73-131">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)
- [<span data-ttu-id="9db73-132">Public</span><span class="sxs-lookup"><span data-stu-id="9db73-132">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)
- [<span data-ttu-id="9db73-133">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="9db73-133">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
