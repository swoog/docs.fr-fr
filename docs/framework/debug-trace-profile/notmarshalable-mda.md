---
title: notMarshalable (MDA)
ms.date: 03/30/2017
helpviewer_keywords:
- managed debugging assistants (MDAs), interface pointer not marshalable
- interface pointer not marshalable MDA
- MDAs (managed debugging assistants), interface pointer not marshalable
- marshaling, run-time errors
- managed debugging assistants (MDAs), marshaling
- marshalable interface pointers
- MDAs (managed debugging assistants), marshaling
- notMarshalable MDA
ms.assetid: 96e7b2c1-843f-4d64-b519-740c3a18b50a
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 30db07ddf935b5ce13b1fe4212f7f6a40270ae93
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59226103"
---
# <a name="notmarshalable-mda"></a><span data-ttu-id="66592-102">notMarshalable (MDA)</span><span class="sxs-lookup"><span data-stu-id="66592-102">notMarshalable MDA</span></span>
<span data-ttu-id="66592-103">L’Assistant Débogage managé (MDA) `notMarshalable` est activé lorsque le Common Language Runtime (CLR) rencontre un pointeur d’interface COM sans proxy/stub inscrit valide ou une implémentation d’interface `IMarshal` incorrecte lors d’une tentative de marshaling de l’interface entre plusieurs contextes.</span><span class="sxs-lookup"><span data-stu-id="66592-103">The `notMarshalable` managed debugging assistant (MDA) is activated when the common language runtime (CLR) encounters a COM interface pointer without a valid registered proxy/stub or an incorrect `IMarshal` interface implementation while attempting to marshal the interface across contexts.</span></span>  
  
## <a name="symptoms"></a><span data-ttu-id="66592-104">Symptômes</span><span class="sxs-lookup"><span data-stu-id="66592-104">Symptoms</span></span>  
 <span data-ttu-id="66592-105">Les appels ne sont pas traités ou ils se produisent dans le contexte incorrect pour les pointeurs d'interface COM.</span><span class="sxs-lookup"><span data-stu-id="66592-105">Calls are not serviced, or calls occur in the wrong context for COM interface pointers.</span></span>  
  
## <a name="cause"></a><span data-ttu-id="66592-106">Cause</span><span class="sxs-lookup"><span data-stu-id="66592-106">Cause</span></span>  
 <span data-ttu-id="66592-107">Absence de proxy/stub inscrit valide ou présence d’une interface `IMarshal` incorrecte lors d’une tentative de marshaling de l’interface entre plusieurs contextes.</span><span class="sxs-lookup"><span data-stu-id="66592-107">No valid registered proxy/stub or an incorrect `IMarshal` while attempting to marshal the interface across contexts.</span></span>  
  
## <a name="resolution"></a><span data-ttu-id="66592-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="66592-108">Resolution</span></span>  
 <span data-ttu-id="66592-109">Assurez-vous que vous avez un stub/proxy inscrit et que l'implémentation de `IMarshal` est correcte.</span><span class="sxs-lookup"><span data-stu-id="66592-109">Make sure you have a proxy stub registered and that the `IMarshal` implementation is valid.</span></span>  
  
## <a name="effect-on-the-runtime"></a><span data-ttu-id="66592-110">Effet sur le runtime</span><span class="sxs-lookup"><span data-stu-id="66592-110">Effect on the Runtime</span></span>  
 <span data-ttu-id="66592-111">Cet Assistant Débogage managé n'a aucun effet sur le runtime.</span><span class="sxs-lookup"><span data-stu-id="66592-111">This MDA has no effect on the runtime.</span></span>  
  
## <a name="output"></a><span data-ttu-id="66592-112">Sortie</span><span class="sxs-lookup"><span data-stu-id="66592-112">Output</span></span>  
 <span data-ttu-id="66592-113">Message décrivant le problème.</span><span class="sxs-lookup"><span data-stu-id="66592-113">A message describing the problem.</span></span>  
  
## <a name="configuration"></a><span data-ttu-id="66592-114">Configuration</span><span class="sxs-lookup"><span data-stu-id="66592-114">Configuration</span></span>  
  
```xml  
<mdaConfig>  
  <assistants>  
    <notMarshalable/>  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a><span data-ttu-id="66592-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66592-115">See also</span></span>

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [<span data-ttu-id="66592-116">Diagnostic d’erreurs avec les Assistants Débogage managé</span><span class="sxs-lookup"><span data-stu-id="66592-116">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [<span data-ttu-id="66592-117">Marshaling d'interopérabilité</span><span class="sxs-lookup"><span data-stu-id="66592-117">Interop Marshaling</span></span>](../../../docs/framework/interop/interop-marshaling.md)
