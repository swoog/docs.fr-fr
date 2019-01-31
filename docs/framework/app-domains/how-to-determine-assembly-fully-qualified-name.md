---
title: 'Procédure : déterminer le nom qualifié complet d’un assembly'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- names [.NET Framework], fully qualified type names
- names [.NET Framework], assemblies
- assemblies [.NET Framework], names
ms.assetid: 009dae23-e1f6-4a64-9a9a-32e4c34802b0
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b7124271c0118800883d4beb68591f8591ac43dc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520709"
---
# <a name="how-to-determine-an-assembly39s-fully-qualified-name"></a><span data-ttu-id="1857e-102">Procédure : déterminer le nom qualifié complet d’un assembly</span><span class="sxs-lookup"><span data-stu-id="1857e-102">How to: Determine an Assembly&#39;s Fully Qualified Name</span></span>
<span data-ttu-id="1857e-103">Pour découvrir le nom qualifié complet d’un assembly dans le Global Assembly Cache, utilisez l’outil Global Assembly Cache ([Gacutil.exe](../../../docs/framework/tools/gacutil-exe-gac-tool.md)).</span><span class="sxs-lookup"><span data-stu-id="1857e-103">To discover the fully qualified name of an assembly in the global assembly cache, use the Global Assembly Cache Tool ([Gacutil.exe](../../../docs/framework/tools/gacutil-exe-gac-tool.md)).</span></span> <span data-ttu-id="1857e-104">Voir [Guide pratique pour visualiser le contenu du Global Assembly Cache](../../../docs/framework/app-domains/how-to-view-the-contents-of-the-gac.md).</span><span class="sxs-lookup"><span data-stu-id="1857e-104">See [How to: View the Contents of the Global Assembly Cache](../../../docs/framework/app-domains/how-to-view-the-contents-of-the-gac.md).</span></span>  
  
 <span data-ttu-id="1857e-105">Pour les assemblys qui ne sont pas dans le Global Assembly Cache, vous pouvez obtenir le nom qualifié complet de l’assembly de différentes façons : vous pouvez utiliser du code pour afficher les informations sur la console ou dans une variable, ou bien vous pouvez utiliser le [Désassembleur MSIL (Ildasm.exe)](../../../docs/framework/tools/ildasm-exe-il-disassembler.md) pour examiner les métadonnées de l’assembly, qui contiennent le nom qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="1857e-105">For assemblies that are not in the global assembly cache, you can get the fully qualified assembly name in a number of ways: can use code to output the information to the console or to a variable, or you can use the [Ildasm.exe (IL Disassembler)](../../../docs/framework/tools/ildasm-exe-il-disassembler.md) to examine the assembly's metadata, which contains the fully qualified name.</span></span>  
  
-   <span data-ttu-id="1857e-106">Si l'assembly est déjà chargé par l'application, vous pouvez récupérer la valeur de la propriété <xref:System.Reflection.Assembly.FullName%2A?displayProperty=nameWithType> pour obtenir le nom complet.</span><span class="sxs-lookup"><span data-stu-id="1857e-106">If the assembly is already loaded by the application, you can retrieve the value of the <xref:System.Reflection.Assembly.FullName%2A?displayProperty=nameWithType> property to get the fully qualified name.</span></span> <span data-ttu-id="1857e-107">Vous pouvez utiliser cette approche que l'assembly se trouve ou non dans le GAC.</span><span class="sxs-lookup"><span data-stu-id="1857e-107">You can use this approach whether or not the assembly is in the GAC.</span></span> <span data-ttu-id="1857e-108">Cet exemple en fournit une illustration.</span><span class="sxs-lookup"><span data-stu-id="1857e-108">The example provides an illustration.</span></span>  
  
-   <span data-ttu-id="1857e-109">Si vous connaissez le chemin d'accès de l'assembly dans le système de fichiers, vous pouvez appeler la méthode statique (`Shared` en Visual Basic) <xref:System.Reflection.AssemblyName.GetAssemblyName%2A?displayProperty=nameWithType> pour obtenir le nom complet de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="1857e-109">If you know the assembly's file system path, you can call the static (`Shared` in Visual Basic) <xref:System.Reflection.AssemblyName.GetAssemblyName%2A?displayProperty=nameWithType> method to get the fully qualified assembly name.</span></span> <span data-ttu-id="1857e-110">Voici un exemple simple.</span><span class="sxs-lookup"><span data-stu-id="1857e-110">The following is a simple example.</span></span>  
  
     [!code-csharp[System.Reflection.AssemblyName.GetAssemblyName#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.reflection.assemblyname.getassemblyname/cs/getassemblyname1.cs#1)]
     [!code-vb[System.Reflection.AssemblyName.GetAssemblyName#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.reflection.assemblyname.getassemblyname/vb/getassemblyname1.vb#1)]  
  
-   <span data-ttu-id="1857e-111">Vous pouvez utiliser le [Désassembleur IL (Ildasm.exe)](../../../docs/framework/tools/ildasm-exe-il-disassembler.md) pour examiner les métadonnées de l’assembly, qui contiennent le nom complet.</span><span class="sxs-lookup"><span data-stu-id="1857e-111">You can use the [Ildasm.exe (IL Disassembler)](../../../docs/framework/tools/ildasm-exe-il-disassembler.md) to examine the assembly's metadata, which contains the fully qualified name.</span></span>  
  
 <span data-ttu-id="1857e-112">Pour plus d’informations sur la définition des attributs d’un assembly, comme la version, la culture et le nom d’assembly, consultez [Définition des attributs d’assembly](../../../docs/framework/app-domains/set-assembly-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1857e-112">For more information about setting assembly attributes such as version, culture, and assembly name, see [Setting Assembly Attributes](../../../docs/framework/app-domains/set-assembly-attributes.md).</span></span> <span data-ttu-id="1857e-113">Pour plus d’informations sur l’attribution d’un nom fort à un assembly, consultez [Création et utilisation d’assemblys avec nom fort](../../../docs/framework/app-domains/create-and-use-strong-named-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="1857e-113">For more information about giving an assembly a strong name, see [Creating and Using Strong-Named Assemblies](../../../docs/framework/app-domains/create-and-use-strong-named-assemblies.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1857e-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="1857e-114">Example</span></span>  
 <span data-ttu-id="1857e-115">L'exemple de code suivant montre comment afficher sur la console le nom complet d'un assembly contenant une classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1857e-115">The following code example shows how to display the fully qualified name of an assembly containing a specified class to the console.</span></span> <span data-ttu-id="1857e-116">Comme il récupère le nom d'un assembly que l'application a déjà chargé, peu importe si l'assembly se trouve dans le GAC.</span><span class="sxs-lookup"><span data-stu-id="1857e-116">Because it retrieves the name of an assembly that the app has already loaded, it does not matter whether the assembly is in the GAC.</span></span>  
  
 [!code-cpp[Assembly.Fullname#2](../../../samples/snippets/cpp/VS_Snippets_CLR/Assembly.FullName/CPP/example2.cpp#2)]
 [!code-csharp[Assembly.Fullname#2](../../../samples/snippets/csharp/VS_Snippets_CLR/Assembly.FullName/CS/example2.cs#2)]
 [!code-vb[Assembly.Fullname#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/Assembly.FullName/VB/example2.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="1857e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1857e-117">See also</span></span>
- [<span data-ttu-id="1857e-118">Noms d’assemblys</span><span class="sxs-lookup"><span data-stu-id="1857e-118">Assembly Names</span></span>](../../../docs/framework/app-domains/assembly-names.md)
- [<span data-ttu-id="1857e-119">Création d’assemblys</span><span class="sxs-lookup"><span data-stu-id="1857e-119">Creating Assemblies</span></span>](../../../docs/framework/app-domains/create-assemblies.md)
- [<span data-ttu-id="1857e-120">Création et utilisation d’assemblys avec nom fort</span><span class="sxs-lookup"><span data-stu-id="1857e-120">Creating and Using Strong-Named Assemblies</span></span>](../../../docs/framework/app-domains/create-and-use-strong-named-assemblies.md)
- [<span data-ttu-id="1857e-121">Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="1857e-121">Global Assembly Cache</span></span>](../../../docs/framework/app-domains/gac.md)
- [<span data-ttu-id="1857e-122">Méthode de localisation des assemblys par le runtime</span><span class="sxs-lookup"><span data-stu-id="1857e-122">How the Runtime Locates Assemblies</span></span>](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
- [<span data-ttu-id="1857e-123">Programmation à l’aide d’assemblys</span><span class="sxs-lookup"><span data-stu-id="1857e-123">Programming with Assemblies</span></span>](../../../docs/framework/app-domains/programming-with-assemblies.md)
