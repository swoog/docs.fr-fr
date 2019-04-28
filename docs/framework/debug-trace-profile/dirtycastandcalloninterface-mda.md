---
title: Assistant Débogage managé dirtyCastAndCallOnInterface
ms.date: 03/30/2017
helpviewer_keywords:
- managed debugging assistants (MDAs), early bound calls AutoDispatch
- dispatch-only mode
- dirtyCastAndCallOnInterface
- early-bound managed classes
- early bound calls on AutoDispatch
- MDAs (managed debugging assistants), early bound calls AutoDispatch
- EarlyBoundCallOnAutorDispatchClassInteface MDA
ms.assetid: aa388ed3-7e3d-48ea-a0b5-c47ae19cec38
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5a28820479ca15ad72475ae9a7754bbbf99ce5c5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61754711"
---
# <a name="dirtycastandcalloninterface-mda"></a><span data-ttu-id="66def-102">Assistant Débogage managé dirtyCastAndCallOnInterface</span><span class="sxs-lookup"><span data-stu-id="66def-102">dirtyCastAndCallOnInterface MDA</span></span>
<span data-ttu-id="66def-103">L'Assistant Débogage managé (MDA) `dirtyCastAndCallOnInterface` est activé quand une tentative d'appel à liaison anticipée par un vtable est effectuée sur une interface de classes qui a été marquée comme étant à liaison tardive uniquement.</span><span class="sxs-lookup"><span data-stu-id="66def-103">The `dirtyCastAndCallOnInterface` managed debugging assistant (MDA) is activated when an early-bound call through a vtable is attempted on a class interface that has been marked late-bound only.</span></span>  
  
## <a name="symptoms"></a><span data-ttu-id="66def-104">Symptômes</span><span class="sxs-lookup"><span data-stu-id="66def-104">Symptoms</span></span>  
 <span data-ttu-id="66def-105">Une application lève une violation d'accès ou a un comportement inattendu quand un appel à liaison anticipée est placé via COM dans le CLR.</span><span class="sxs-lookup"><span data-stu-id="66def-105">An application throws an access violation or has unexpected behavior when placing an early-bound call via COM into the CLR.</span></span>  
  
## <a name="cause"></a><span data-ttu-id="66def-106">Cause</span><span class="sxs-lookup"><span data-stu-id="66def-106">Cause</span></span>  
 <span data-ttu-id="66def-107">Le code tente un appel à liaison anticipée par un vtable via une interface de classes qui est à liaison tardive uniquement.</span><span class="sxs-lookup"><span data-stu-id="66def-107">Code is attempting an early-bound call through a vtable via a class interface that is late-bound only.</span></span> <span data-ttu-id="66def-108">Notez que, par défaut, les interfaces de classes sont identifiées comme étant à liaison tardive uniquement.</span><span class="sxs-lookup"><span data-stu-id="66def-108">Note that by default class interfaces are identified as being late-bound only.</span></span> <span data-ttu-id="66def-109">Elles peuvent également être identifiées comme étant à liaison tardive à l'aide de l'attribut <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> défini à la valeur <xref:System.Runtime.InteropServices.ClassInterfaceType.AutoDispatch> (`[ClassInterface(ClassInterfaceType.AutoDispatch)]`).</span><span class="sxs-lookup"><span data-stu-id="66def-109">They can also be identified as late-bound with the <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> attribute with an <xref:System.Runtime.InteropServices.ClassInterfaceType.AutoDispatch> value (`[ClassInterface(ClassInterfaceType.AutoDispatch)]`).</span></span>  
  
## <a name="resolution"></a><span data-ttu-id="66def-110">Résolution</span><span class="sxs-lookup"><span data-stu-id="66def-110">Resolution</span></span>  
 <span data-ttu-id="66def-111">La résolution recommandée consiste à définir une interface explicite destinée à être utilisée par COM et à faire appeler les clients COM via cette interface plutôt que via l’interface de classes générée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="66def-111">The recommended resolution is to define an explicit interface for use by COM and have the COM clients call through this interface instead of through the automatically generated class interface.</span></span> <span data-ttu-id="66def-112">L'appel de COM peut aussi être changé en appel à liaison tardive via `IDispatch`.</span><span class="sxs-lookup"><span data-stu-id="66def-112">Alternatively, the call from COM can be transformed into a late-bound call via `IDispatch`.</span></span>  
  
 <span data-ttu-id="66def-113">Enfin, il est possible d'identifier la classe comme <xref:System.Runtime.InteropServices.ClassInterfaceType.AutoDual> (`[ClassInterface(ClassInterfaceType.AutoDual)]`) pour permettre aux appels à liaison anticipée d'être placés par COM. L'utilisation de <xref:System.Runtime.InteropServices.ClassInterfaceType.AutoDual> est toutefois fortement déconseillée en raison des limitations du contrôle de version décrites dans <xref:System.Runtime.InteropServices.ClassInterfaceAttribute>.</span><span class="sxs-lookup"><span data-stu-id="66def-113">Finally, it is possible to identify the class as <xref:System.Runtime.InteropServices.ClassInterfaceType.AutoDual> (`[ClassInterface(ClassInterfaceType.AutoDual)]`) to allow early bound calls to be placed from COM; however, using <xref:System.Runtime.InteropServices.ClassInterfaceType.AutoDual> is strongly discouraged because of the versioning limitations described in <xref:System.Runtime.InteropServices.ClassInterfaceAttribute>.</span></span>  
  
## <a name="effect-on-the-runtime"></a><span data-ttu-id="66def-114">Effet sur le runtime</span><span class="sxs-lookup"><span data-stu-id="66def-114">Effect on the Runtime</span></span>  
 <span data-ttu-id="66def-115">Cet Assistant Débogage managé n'a aucun effet sur le CLR.</span><span class="sxs-lookup"><span data-stu-id="66def-115">This MDA has no effect on the CLR.</span></span> <span data-ttu-id="66def-116">Il fournit uniquement des données relatives aux appels à liaison anticipée qui sont effectués sur les interfaces à liaison tardive.</span><span class="sxs-lookup"><span data-stu-id="66def-116">It only reports data about early-bound calls on late-bound interfaces.</span></span>  
  
## <a name="output"></a><span data-ttu-id="66def-117">Sortie</span><span class="sxs-lookup"><span data-stu-id="66def-117">Output</span></span>  
 <span data-ttu-id="66def-118">Nom de la méthode ou nom du champ qui fait l'objet d'un accès à liaison anticipée.</span><span class="sxs-lookup"><span data-stu-id="66def-118">The name of the method or name of the field being accessed early-bound.</span></span>  
  
## <a name="configuration"></a><span data-ttu-id="66def-119">Configuration</span><span class="sxs-lookup"><span data-stu-id="66def-119">Configuration</span></span>  
  
```xml  
<mdaConfig>  
  <assistants>  
    <dirtyCastAndCallOnInterface />  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a><span data-ttu-id="66def-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66def-120">See also</span></span>

- <xref:System.Runtime.InteropServices.ClassInterfaceAttribute>
- [<span data-ttu-id="66def-121">Diagnostic d’erreurs avec les Assistants Débogage managé</span><span class="sxs-lookup"><span data-stu-id="66def-121">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
