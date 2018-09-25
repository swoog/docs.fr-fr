---
title: 'Comment : partager un Assembly avec d’autres Applications (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 5388aedc-cb42-4622-8b70-8e701eee057a
ms.openlocfilehash: 3d29a3558a64c02fc8c59035f2fee5c64c4a776f
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47089410"
---
# <a name="how-to-share-an-assembly-with-other-applications-visual-basic"></a><span data-ttu-id="b8d28-102">Comment : partager un Assembly avec d’autres Applications (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b8d28-102">How to: Share an Assembly with Other Applications (Visual Basic)</span></span>
<span data-ttu-id="b8d28-103">Les assemblys peuvent être privés ou partagés. Par défaut, la plupart des programmes simples se composent d’un assembly privé, car ils ne sont pas destinés à être utilisés par d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="b8d28-103">Assemblies can be private or shared: by default, most simple programs consist of a private assembly because they are not intended to be used by other applications.</span></span>  
  
 <span data-ttu-id="b8d28-104">Pour partager un assembly avec d’autres applications, celui-ci doit être placé dans le [Global Assembly Cache](../../../../framework/app-domains/gac.md) (GAC).</span><span class="sxs-lookup"><span data-stu-id="b8d28-104">In order to share an assembly with other applications, it must be placed in the [Global Assembly Cache](../../../../framework/app-domains/gac.md) (GAC).</span></span>  
  
### <a name="sharing-an-assembly"></a><span data-ttu-id="b8d28-105">Partage d’un assembly</span><span class="sxs-lookup"><span data-stu-id="b8d28-105">Sharing an assembly</span></span>  
  
1.  <span data-ttu-id="b8d28-106">Créez votre assembly.</span><span class="sxs-lookup"><span data-stu-id="b8d28-106">Create your assembly.</span></span> <span data-ttu-id="b8d28-107">Pour plus d’informations, consultez [Création d’assemblys](../../../../framework/app-domains/create-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="b8d28-107">For more information, see [Creating Assemblies](../../../../framework/app-domains/create-assemblies.md).</span></span>  
  
2.  <span data-ttu-id="b8d28-108">Attribuez un nom fort à votre assembly.</span><span class="sxs-lookup"><span data-stu-id="b8d28-108">Assign a strong name to your assembly.</span></span> <span data-ttu-id="b8d28-109">Pour plus d’informations, consultez [Guide pratique pour signer un assembly avec un nom fort](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span><span class="sxs-lookup"><span data-stu-id="b8d28-109">For more information, see [How to: Sign an Assembly with a Strong Name](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span></span>  
  
3.  <span data-ttu-id="b8d28-110">Assignez des informations de version à votre assembly.</span><span class="sxs-lookup"><span data-stu-id="b8d28-110">Assign version information to your assembly.</span></span> <span data-ttu-id="b8d28-111">Pour plus d’informations, consultez [Versioning des assemblys](../../../../framework/app-domains/assembly-versioning.md).</span><span class="sxs-lookup"><span data-stu-id="b8d28-111">For more information, see [Assembly Versioning](../../../../framework/app-domains/assembly-versioning.md).</span></span>  
  
4.  <span data-ttu-id="b8d28-112">Ajoutez votre assembly au Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="b8d28-112">Add your assembly to the Global Assembly Cache.</span></span> <span data-ttu-id="b8d28-113">Pour plus d’informations, consultez [Guide pratique pour installer un assembly dans le Global Assembly Cache](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md).</span><span class="sxs-lookup"><span data-stu-id="b8d28-113">For more information, see [How to: Install an Assembly into the Global Assembly Cache](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md).</span></span>  
  
5.  <span data-ttu-id="b8d28-114">Accédez aux types contenus dans l’assembly à partir d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="b8d28-114">Access the types contained in the assembly from the other applications.</span></span> <span data-ttu-id="b8d28-115">Pour plus d’informations, consultez [Guide pratique pour référencer un assembly avec un nom fort](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md).</span><span class="sxs-lookup"><span data-stu-id="b8d28-115">For more information, see [How to: Reference a Strong-Named Assembly](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8d28-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8d28-116">See also</span></span>

- [<span data-ttu-id="b8d28-117">Concepts de programmation</span><span class="sxs-lookup"><span data-stu-id="b8d28-117">Programming Concepts</span></span>](../../../../visual-basic/programming-guide/concepts/index.md)
- [<span data-ttu-id="b8d28-118">Assemblys et le Global Assembly Cache (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b8d28-118">Assemblies and the Global Assembly Cache (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)  
- [<span data-ttu-id="b8d28-119">Programmation à l’aide d’assemblys</span><span class="sxs-lookup"><span data-stu-id="b8d28-119">Programming with Assemblies</span></span>](../../../../framework/app-domains/programming-with-assemblies.md)
