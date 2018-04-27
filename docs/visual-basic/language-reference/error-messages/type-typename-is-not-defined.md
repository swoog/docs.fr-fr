---
title: Type &#39; &lt;typename&gt; &#39; n’est pas défini
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc30002
- bc30002
helpviewer_keywords:
- BC30002
ms.assetid: b0faf204-57fd-44de-8c05-9db027eea663
caps.latest.revision: 18
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 7c3efbcabf1e40c7f550b5f54d16e697561cf82c
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="type-39lttypenamegt39-is-not-defined"></a><span data-ttu-id="f746b-102">Type &#39; &lt;typename&gt; &#39; n’est pas défini</span><span class="sxs-lookup"><span data-stu-id="f746b-102">Type &#39;&lt;typename&gt;&#39; is not defined</span></span>
<span data-ttu-id="f746b-103">L’instruction a fait référence à un type qui n’a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="f746b-103">The statement has made reference to a type that has not been defined.</span></span> <span data-ttu-id="f746b-104">Vous pouvez définir un type dans une instruction de déclaration, tel que `Enum`, `Structure`, `Class`, ou `Interface`.</span><span class="sxs-lookup"><span data-stu-id="f746b-104">You can define a type in a declaration statement such as `Enum`, `Structure`, `Class`, or `Interface`.</span></span>  
  
 <span data-ttu-id="f746b-105">**ID d’erreur :** BC30002</span><span class="sxs-lookup"><span data-stu-id="f746b-105">**Error ID:** BC30002</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f746b-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f746b-106">To correct this error</span></span>  
  
-   <span data-ttu-id="f746b-107">Assurez-vous que la définition de type et sa référence utilisent tous deux la même orthographe.</span><span class="sxs-lookup"><span data-stu-id="f746b-107">Ensure that the type definition and its reference both use the same spelling.</span></span>  
  
-   <span data-ttu-id="f746b-108">Assurez-vous que la définition de type est accessible à la référence.</span><span class="sxs-lookup"><span data-stu-id="f746b-108">Ensure that the type definition is accessible to the reference.</span></span> <span data-ttu-id="f746b-109">Par exemple, si le type est dans un autre module et a été déclaré `Private`, déplacez la définition de type vers le module de référence ou déclarez-le `Public`.</span><span class="sxs-lookup"><span data-stu-id="f746b-109">For example, if the type is in another module and has been declared `Private`, move the type definition to the referencing module or declare it `Public`.</span></span>  
  
-   <span data-ttu-id="f746b-110">Assurez-vous que l’espace de noms du type n’est pas redéfinie dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="f746b-110">Ensure that the namespace of the type is not redefined within your project.</span></span> <span data-ttu-id="f746b-111">Si tel est le cas, utilisez le `Global` (mot clé) pour qualifier complètement le nom de type.</span><span class="sxs-lookup"><span data-stu-id="f746b-111">If it is, use the `Global` keyword to fully qualify the type name.</span></span> <span data-ttu-id="f746b-112">Par exemple, si un projet définit un espace de noms `System`, le <xref:System.Object?displayProperty=nameWithType> type ne sont pas accessibles, sauf si elle est qualifié avec le `Global` (mot clé) : `Global.System.Object`.</span><span class="sxs-lookup"><span data-stu-id="f746b-112">For example, if a project defines a namespace named `System`, the <xref:System.Object?displayProperty=nameWithType> type cannot be accessed unless it is fully qualified with the `Global` keyword: `Global.System.Object`.</span></span>  
  
-   <span data-ttu-id="f746b-113">Si le type est défini, mais que la bibliothèque d’objets ou la bibliothèque de types dans laquelle il est défini n’est pas inscrit dans Visual Basic, cliquez sur **ajouter une référence** sur la **projet** menu et sélectionnez l’objet approprié bibliothèque ou bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="f746b-113">If the type is defined, but the object library or type library in which it is defined is not registered in Visual Basic, click **Add Reference** on the **Project** menu, and then select the appropriate object library or type library.</span></span>  
  
-   <span data-ttu-id="f746b-114">Assurez-vous que le type est dans un assembly qui fait partie du profil .NET Framework ciblé.</span><span class="sxs-lookup"><span data-stu-id="f746b-114">Ensure that the type is in an assembly that is part of the targeted .NET Framework profile.</span></span> <span data-ttu-id="f746b-115">Pour plus d’informations, consultez [Dépannage des erreurs de ciblage du .NET Framework](/visualstudio/msbuild/troubleshooting-dotnet-framework-targeting-errors).</span><span class="sxs-lookup"><span data-stu-id="f746b-115">For more information, see [Troubleshooting .NET Framework Targeting Errors](/visualstudio/msbuild/troubleshooting-dotnet-framework-targeting-errors).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f746b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f746b-116">See Also</span></span>  
 [<span data-ttu-id="f746b-117">Espaces de noms dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f746b-117">Namespaces in Visual Basic</span></span>](../../../visual-basic/programming-guide/program-structure/namespaces.md)  
 [<span data-ttu-id="f746b-118">Enum (instruction)</span><span class="sxs-lookup"><span data-stu-id="f746b-118">Enum Statement</span></span>](../../../visual-basic/language-reference/statements/enum-statement.md)  
 [<span data-ttu-id="f746b-119">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="f746b-119">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)  
 [<span data-ttu-id="f746b-120">Class (instruction)</span><span class="sxs-lookup"><span data-stu-id="f746b-120">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)  
 [<span data-ttu-id="f746b-121">Interface (instruction)</span><span class="sxs-lookup"><span data-stu-id="f746b-121">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)  
 [<span data-ttu-id="f746b-122">Gestion des références dans un projet</span><span class="sxs-lookup"><span data-stu-id="f746b-122">Managing references in a project</span></span>](/visualstudio/ide/managing-references-in-a-project)
