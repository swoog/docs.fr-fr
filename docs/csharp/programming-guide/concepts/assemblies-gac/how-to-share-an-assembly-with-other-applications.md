---
title: Guide pratique pour partager un assembly avec d’autres applications (C#)
ms.date: 07/20/2015
ms.assetid: c30e972b-1693-4e05-b115-c31831fdf9f2
ms.openlocfilehash: a5b20061c759fd914193f24aa123317f13d31dce
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44266467"
---
# <a name="how-to-share-an-assembly-with-other-applications-c"></a><span data-ttu-id="077b3-102">Guide pratique pour partager un assembly avec d’autres applications (C#)</span><span class="sxs-lookup"><span data-stu-id="077b3-102">How to: Share an Assembly with Other Applications (C#)</span></span>
<span data-ttu-id="077b3-103">Les assemblys peuvent être privés ou partagés. Par défaut, la plupart des programmes simples se composent d’un assembly privé, car ils ne sont pas destinés à être utilisés par d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="077b3-103">Assemblies can be private or shared: by default, most simple programs consist of a private assembly because they are not intended to be used by other applications.</span></span>  
  
 <span data-ttu-id="077b3-104">Pour partager un assembly avec d’autres applications, celui-ci doit être placé dans le [Global Assembly Cache](../../../../framework/app-domains/gac.md) (GAC).</span><span class="sxs-lookup"><span data-stu-id="077b3-104">In order to share an assembly with other applications, it must be placed in the [Global Assembly Cache](../../../../framework/app-domains/gac.md) (GAC).</span></span>  
  
### <a name="sharing-an-assembly"></a><span data-ttu-id="077b3-105">Partage d’un assembly</span><span class="sxs-lookup"><span data-stu-id="077b3-105">Sharing an assembly</span></span>  
  
1.  <span data-ttu-id="077b3-106">Créez votre assembly.</span><span class="sxs-lookup"><span data-stu-id="077b3-106">Create your assembly.</span></span> <span data-ttu-id="077b3-107">Pour plus d’informations, consultez [Création d’assemblys](../../../../framework/app-domains/create-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="077b3-107">For more information, see [Creating Assemblies](../../../../framework/app-domains/create-assemblies.md).</span></span>  
  
2.  <span data-ttu-id="077b3-108">Attribuez un nom fort à votre assembly.</span><span class="sxs-lookup"><span data-stu-id="077b3-108">Assign a strong name to your assembly.</span></span> <span data-ttu-id="077b3-109">Pour plus d’informations, consultez [Guide pratique pour signer un assembly avec un nom fort](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span><span class="sxs-lookup"><span data-stu-id="077b3-109">For more information, see [How to: Sign an Assembly with a Strong Name](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span></span>  
  
3.  <span data-ttu-id="077b3-110">Assignez des informations de version à votre assembly.</span><span class="sxs-lookup"><span data-stu-id="077b3-110">Assign version information to your assembly.</span></span> <span data-ttu-id="077b3-111">Pour plus d’informations, consultez [Versioning des assemblys](../../../../../docs/framework/app-domains/assembly-versioning.md).</span><span class="sxs-lookup"><span data-stu-id="077b3-111">For more information, see [Assembly Versioning](../../../../../docs/framework/app-domains/assembly-versioning.md).</span></span>  
  
4.  <span data-ttu-id="077b3-112">Ajoutez votre assembly au Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="077b3-112">Add your assembly to the Global Assembly Cache.</span></span> <span data-ttu-id="077b3-113">Pour plus d’informations, consultez [Guide pratique pour installer un assembly dans le Global Assembly Cache](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md).</span><span class="sxs-lookup"><span data-stu-id="077b3-113">For more information, see [How to: Install an Assembly into the Global Assembly Cache](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md).</span></span>  
  
5.  <span data-ttu-id="077b3-114">Accédez aux types contenus dans l’assembly à partir d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="077b3-114">Access the types contained in the assembly from the other applications.</span></span> <span data-ttu-id="077b3-115">Pour plus d’informations, consultez [Guide pratique pour référencer un assembly avec un nom fort](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md).</span><span class="sxs-lookup"><span data-stu-id="077b3-115">For more information, see [How to: Reference a Strong-Named Assembly](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="077b3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="077b3-116">See Also</span></span>

- [<span data-ttu-id="077b3-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="077b3-117">C# Programming Guide</span></span>](../../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="077b3-118">Programmation à l’aide d’assemblys</span><span class="sxs-lookup"><span data-stu-id="077b3-118">Programming with Assemblies</span></span>](../../../../framework/app-domains/programming-with-assemblies.md)
