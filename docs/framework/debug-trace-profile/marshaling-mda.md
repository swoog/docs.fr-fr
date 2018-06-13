---
title: Assistant Débogage managé marshaling
ms.date: 03/30/2017
helpviewer_keywords:
- marshaling, run-time errors
- marshaling MDA
- managed debugging assistants (MDAs), marshaling
- MDAs (managed debugging assistants), marshaling
ms.assetid: 5433b1f8-b0e5-40c9-a49a-0e5bd213363d
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 164c7a6e4411d7ff3e66643c6f012fdba790ef49
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33386676"
---
# <a name="marshaling-mda"></a><span data-ttu-id="7101c-102">Assistant Débogage managé marshaling</span><span class="sxs-lookup"><span data-stu-id="7101c-102">marshaling MDA</span></span>
<span data-ttu-id="7101c-103">L'Assistant Débogage managé (MDA) `marshaling` est activé quand le CLR définit des informations de marshaling pour un paramètre de méthode ou un champ de structure.</span><span class="sxs-lookup"><span data-stu-id="7101c-103">The `marshaling` managed debugging assistant (MDA) is activated when the CLR sets up marshaling information for a method parameter or a field of a structure.</span></span> <span data-ttu-id="7101c-104">Ce MDA ne fonctionne pas pour les assemblys compilés juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="7101c-104">This MDA does not work for JIT-compiled assemblies.</span></span>  
  
## <a name="effect-on-the-runtime"></a><span data-ttu-id="7101c-105">Effet sur le runtime</span><span class="sxs-lookup"><span data-stu-id="7101c-105">Effect on the Runtime</span></span>  
 <span data-ttu-id="7101c-106">Cet Assistant Débogage managé n'a aucun effet sur le CLR.</span><span class="sxs-lookup"><span data-stu-id="7101c-106">This MDA has no effect on the CLR.</span></span>  
  
## <a name="output"></a><span data-ttu-id="7101c-107">Sortie</span><span class="sxs-lookup"><span data-stu-id="7101c-107">Output</span></span>  
 <span data-ttu-id="7101c-108">Le MDA affiche le type du paramètre ou du champ dans les contextes managés et non managés ainsi que la structure ou la méthode qui contient ce type.</span><span class="sxs-lookup"><span data-stu-id="7101c-108">The MDA displays the type of the parameter or field in the managed and unmanaged contexts, and the structure or method containing the type.</span></span>  <span data-ttu-id="7101c-109">Voici un exemple de sortie pour un champ :</span><span class="sxs-lookup"><span data-stu-id="7101c-109">The following is an example of the output for a field:</span></span>  
  
```  
Marshaling from 'Char' to 'ANSI char'  
name="assembly!Namespace.Class::myChar  
```  
  
## <a name="configuration"></a><span data-ttu-id="7101c-110">Configuration</span><span class="sxs-lookup"><span data-stu-id="7101c-110">Configuration</span></span>  
 <span data-ttu-id="7101c-111">La configuration du MDA vous permet de filtrer les informations de marshaling signalées en fonction des noms de champs ou de méthodes impliqués.</span><span class="sxs-lookup"><span data-stu-id="7101c-111">The MDA configuration allows you to filter the reported marshaling information based on the involved field or method names.</span></span>  <span data-ttu-id="7101c-112">L'exemple suivant illustre l'utilisation des éléments `methodFilter`, `fieldFilter` et `match` pour spécifier des filtres.</span><span class="sxs-lookup"><span data-stu-id="7101c-112">The following example shows the use of the `methodFilter`, `fieldFilter`, and `match` elements to specify filters.</span></span>  <span data-ttu-id="7101c-113">L'utilisation d'un astérisque (\*) avec l'attribut `name` permet de spécifier tous les noms.</span><span class="sxs-lookup"><span data-stu-id="7101c-113">Setting the `name` attribute to an asterisk (\*) will match everything.</span></span>  
  
```xml  
<mdaConfig>  
  <assistants>  
    <marshaling>  
      <methodFilter>  
        <match name="Method1"/>  
        <match name="Method2"/>  
      </methodFilter>  
      <fieldFilter>  
        <match name="Field1"/>  
        <match name="Field2"/>  
       </fieldFilter>  
    </marshaling>  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a><span data-ttu-id="7101c-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7101c-114">See Also</span></span>  
 <xref:System.Runtime.InteropServices.MarshalAsAttribute>  
 [<span data-ttu-id="7101c-115">Diagnostic d’erreurs avec les Assistants Débogage managé</span><span class="sxs-lookup"><span data-stu-id="7101c-115">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)  
 [<span data-ttu-id="7101c-116">Marshaling d'interopérabilité</span><span class="sxs-lookup"><span data-stu-id="7101c-116">Interop Marshaling</span></span>](../../../docs/framework/interop/interop-marshaling.md)
