---
title: Assistant Débogage managé invalidVariant
ms.date: 03/30/2017
helpviewer_keywords:
- MDAs (managed debugging assistants), invalid variant
- VARIANT type errors
- InvalidVariant MDA
- invalid VARIANT types
- managed debugging assistants (MDAs), invalid variant
ms.assetid: d273e070-d1b1-4a53-a9c7-7af837b04a3d
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 426b9df449b12d2f34fa70fc721cc050fa3e4ddd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33386715"
---
# <a name="invalidvariant-mda"></a><span data-ttu-id="009fa-102">Assistant Débogage managé invalidVariant</span><span class="sxs-lookup"><span data-stu-id="009fa-102">invalidVariant MDA</span></span>
<span data-ttu-id="009fa-103">L'Assistant Débogage managé (MDA) `invalidVariant` est activé quand une structure `VARIANT` non valide est rencontrée lors d'un appel du code natif ou non managé au code managé.</span><span class="sxs-lookup"><span data-stu-id="009fa-103">The `invalidVariant` managed debugging assistant (MDA) is activated when an invalid `VARIANT` structure is encountered during a call from native or unmanaged code to managed code.</span></span>  
  
## <a name="symptoms"></a><span data-ttu-id="009fa-104">Symptômes</span><span class="sxs-lookup"><span data-stu-id="009fa-104">Symptoms</span></span>  
 <span data-ttu-id="009fa-105">Comportement inattendu pendant une transition entre du code natif et managé impliquant le marshaling d'une structure `VARIANT` en objet.</span><span class="sxs-lookup"><span data-stu-id="009fa-105">Unexpected behavior during a transition between native and managed code involving the marshaling of a `VARIANT` to an object.</span></span>  
  
## <a name="cause"></a><span data-ttu-id="009fa-106">Cause</span><span class="sxs-lookup"><span data-stu-id="009fa-106">Cause</span></span>  
 <span data-ttu-id="009fa-107">Le code natif passe une structure `VARIANT` incorrecte au code managé.</span><span class="sxs-lookup"><span data-stu-id="009fa-107">Native code is passing a malformed `VARIANT` structure to managed code.</span></span>  <span data-ttu-id="009fa-108">Le runtime tente de marshaler cette `VARIANT` en objet et active l'Assistant Débogage managé si la `VARIANT` n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="009fa-108">The runtime attempts to marshal this `VARIANT` to an object and activates the MDA if the `VARIANT` is not valid.</span></span> <span data-ttu-id="009fa-109">Exemples de structures `VARIANT` non valides : une structure `VARIANT` avec un `VARTYPE` VT_EMPTY &#124; VT_BYREF ou une structure `VARIANT` avec le `VARTYPE` VT_VARIANT.</span><span class="sxs-lookup"><span data-stu-id="009fa-109">Examples of invalid `VARIANT`S include a `VARIANT` with `VARTYPE` VT_EMPTY &#124; VT_BYREF or a `VARIANT` with `VARTYPE` VT_VARIANT.</span></span>  
  
## <a name="resolution"></a><span data-ttu-id="009fa-110">Résolution</span><span class="sxs-lookup"><span data-stu-id="009fa-110">Resolution</span></span>  
 <span data-ttu-id="009fa-111">Le code natif ou non managé qui passe la structure `VARIANT` doit s'assurer que la `VARIANT` est correcte et bien initialisée.</span><span class="sxs-lookup"><span data-stu-id="009fa-111">The native or unmanaged code passing the `VARIANT` must ensure that the `VARIANT` is correctly formed and initialized.</span></span>  
  
## <a name="effect-on-the-runtime"></a><span data-ttu-id="009fa-112">Effet sur le runtime</span><span class="sxs-lookup"><span data-stu-id="009fa-112">Effect on the Runtime</span></span>  
 <span data-ttu-id="009fa-113">Cet Assistant Débogage managé n'a aucun effet sur le comportement du runtime.</span><span class="sxs-lookup"><span data-stu-id="009fa-113">The MDA has no effect on the runtime's behavior.</span></span>  
  
## <a name="output"></a><span data-ttu-id="009fa-114">Sortie</span><span class="sxs-lookup"><span data-stu-id="009fa-114">Output</span></span>  
 <span data-ttu-id="009fa-115">Message de l'Assistant Débogage managé indiquant que le runtime a détecté qu'une structure `VARIANT` incorrecte a été passée au code managé par un module non managé.</span><span class="sxs-lookup"><span data-stu-id="009fa-115">An MDA message indicating that the runtime detected an invalid `VARIANT` passed to managed code by an unmanaged module.</span></span>  
  
## <a name="configuration"></a><span data-ttu-id="009fa-116">Configuration</span><span class="sxs-lookup"><span data-stu-id="009fa-116">Configuration</span></span>  
  
```xml  
<mdaConfig>  
  <assistants>  
    <invalidVariant />  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a><span data-ttu-id="009fa-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="009fa-117">See Also</span></span>  
 <xref:System.Runtime.InteropServices.MarshalAsAttribute>  
 [<span data-ttu-id="009fa-118">Diagnostic d’erreurs avec les Assistants Débogage managé</span><span class="sxs-lookup"><span data-stu-id="009fa-118">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)  
 [<span data-ttu-id="009fa-119">Marshaling d'interopérabilité</span><span class="sxs-lookup"><span data-stu-id="009fa-119">Interop Marshaling</span></span>](../../../docs/framework/interop/interop-marshaling.md)
