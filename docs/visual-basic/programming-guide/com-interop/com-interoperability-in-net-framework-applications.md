---
title: Interopérabilité COM dans les applications .NET Framework (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- interoperability, COM and .NET framework objects
- COM interop [Visual Basic]
- shared components
ms.assetid: f5a72143-c268-4dff-a019-974ad940e17d
ms.openlocfilehash: ceef4255321e208911a16db0227890bc6654b8c5
ms.sourcegitcommit: 70c76a12449439bac0f7a359866be5a0311ce960
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2018
ms.locfileid: "39244662"
---
# <a name="com-interoperability-in-net-framework-applications-visual-basic"></a><span data-ttu-id="6f291-102">Interopérabilité COM dans les applications .NET Framework (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6f291-102">COM Interoperability in .NET Framework Applications (Visual Basic)</span></span>
<span data-ttu-id="6f291-103">Lorsque vous souhaitez utiliser des objets COM et des objets .NET Framework dans la même application, vous devez résoudre les différences dans la façon dont les objets existent dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="6f291-103">When you want to use COM objects and .NET Framework objects in the same application, you need to address the differences in how the objects exist in memory.</span></span> <span data-ttu-id="6f291-104">Un objet .NET Framework se trouve dans la mémoire managée, la mémoire contrôlée par le common language runtime et peut être déplacé par le runtime en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="6f291-104">A .NET Framework object is located in managed memory—the memory controlled by the common language runtime—and may be moved by the runtime as needed.</span></span> <span data-ttu-id="6f291-105">Un objet COM se trouve dans la mémoire non managée et n’est pas prévu de passer à un autre emplacement de mémoire.</span><span class="sxs-lookup"><span data-stu-id="6f291-105">A COM object is located in unmanaged memory and is not expected to move to another memory location.</span></span> <span data-ttu-id="6f291-106">Visual Studio et le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fournissent des outils pour contrôler l’interaction de ces composants managés et.</span><span class="sxs-lookup"><span data-stu-id="6f291-106">Visual Studio and the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] provide tools to control the interaction of these managed and unmanaged components.</span></span> <span data-ttu-id="6f291-107">Pour plus d’informations sur le code managé, consultez [Common Language Runtime](../../../standard/clr.md).</span><span class="sxs-lookup"><span data-stu-id="6f291-107">For more information about managed code, see [Common Language Runtime](../../../standard/clr.md).</span></span>  
  
 <span data-ttu-id="6f291-108">Outre l’utilisation des objets COM dans les applications .NET, vous souhaiterez également utiliser Visual Basic pour développer des objets accessibles à partir de code non managé via COM.</span><span class="sxs-lookup"><span data-stu-id="6f291-108">In addition to using COM objects in .NET applications, you may also want to use Visual Basic to develop objects accessible from unmanaged code through COM.</span></span>  
  
 <span data-ttu-id="6f291-109">Les liens sur cette page fournissent des détails sur les interactions entre les objets COM et .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="6f291-109">The links on this page provide details on the interactions between COM and .NET Framework objects.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="6f291-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f291-110">Related Sections</span></span>  
 [<span data-ttu-id="6f291-111">COM Interop</span><span class="sxs-lookup"><span data-stu-id="6f291-111">COM Interop</span></span>](../../../visual-basic/programming-guide/com-interop/index.md)  
 <span data-ttu-id="6f291-112">Fournit des liens vers des rubriques traitant de l’interopérabilité COM en Visual Basic, y compris les objets COM, les contrôles ActiveX, les DLL Win32, des objets gérés et l’héritage des objets COM.</span><span class="sxs-lookup"><span data-stu-id="6f291-112">Provides links to topics covering COM interoperability in Visual Basic, including COM objects, ActiveX controls, Win32 DLLs, managed objects, and inheritance of COM objects.</span></span>  
  
 [<span data-ttu-id="6f291-113">Erreur de Wrapper COM Interop</span><span class="sxs-lookup"><span data-stu-id="6f291-113">COM Interop Wrapper Error</span></span>](/cpp/misc/com-interop-wrapper-error)  
 <span data-ttu-id="6f291-114">Décrit les conséquences et les options si le système de projet ne peut pas créer un wrapper d’interopérabilité COM pour un composant particulier.</span><span class="sxs-lookup"><span data-stu-id="6f291-114">Describes the consequences and options if the project system cannot create a COM interoperability wrapper for a particular component.</span></span>  
  
 [<span data-ttu-id="6f291-115">Interopération avec du code non managé</span><span class="sxs-lookup"><span data-stu-id="6f291-115">Interoperating with Unmanaged Code</span></span>](../../../framework/interop/index.md)  
 <span data-ttu-id="6f291-116">Certains problèmes d’interaction entre du code managé et décrit brièvement et fournit des liens pour approfondir ce sujet.</span><span class="sxs-lookup"><span data-stu-id="6f291-116">Briefly describes some of the interaction issues between managed and unmanaged code, and provides links for further study.</span></span>  
  
 [<span data-ttu-id="6f291-117">Wrappers COM</span><span class="sxs-lookup"><span data-stu-id="6f291-117">COM Wrappers</span></span>](../../../framework/interop/com-wrappers.md)  
 <span data-ttu-id="6f291-118">Traite des wrappers RCW, qui permettent au code managé d’appeler les méthodes COM, et par COM, qui permettent aux clients COM d’appeler les méthodes d’objet .NET.</span><span class="sxs-lookup"><span data-stu-id="6f291-118">Discusses runtime callable wrappers, which allow managed code to call COM methods, and COM callable wrappers, which allow COM clients to call .NET object methods.</span></span>  
  
 [<span data-ttu-id="6f291-119">Interopérabilité COM avancée</span><span class="sxs-lookup"><span data-stu-id="6f291-119">Advanced COM Interoperability</span></span>](../../../framework/interop/index.md)  
 <span data-ttu-id="6f291-120">Fournit des liens vers des rubriques traitant de l’interopérabilité COM en ce qui concerne les wrappers, exceptions, l’héritage, threading, événements, les conversions et marshaling.</span><span class="sxs-lookup"><span data-stu-id="6f291-120">Provides links to topics covering COM interoperability with respect to wrappers, exceptions, inheritance, threading, events, conversions, and marshaling.</span></span>  
  
 [<span data-ttu-id="6f291-121">Tlbimp.exe (importateur de bibliothèques de types)</span><span class="sxs-lookup"><span data-stu-id="6f291-121">Tlbimp.exe (Type Library Importer)</span></span>](../../../framework/tools/tlbimp-exe-type-library-importer.md)  
 <span data-ttu-id="6f291-122">Traite de l’outil que vous pouvez utiliser pour convertir les définitions de type trouvées dans une bibliothèque de types COM en définitions équivalentes dans un assembly du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="6f291-122">Discusses the tool you can use to convert the type definitions found within a COM type library into equivalent definitions in a common language runtime assembly.</span></span>
