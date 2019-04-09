---
title: Assistant Débogage managé memberInfoCacheCreation
ms.date: 03/30/2017
helpviewer_keywords:
- member info cache creation
- MemberInfoCacheCreation MDA
- reflection, run-time errors
- MDAs (managed debugging assistants), cache
- cache [.NET Framework], reflection
- managed debugging assistants (MDAs), cache
- MemberInfo cache
ms.assetid: 5abdad23-1335-4744-8acb-934002c0b6fe
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 90f59f4d593a8aa077a6710cc0f5c1747ac1a3ad
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59103764"
---
# <a name="memberinfocachecreation-mda"></a><span data-ttu-id="ee40a-102">Assistant Débogage managé memberInfoCacheCreation</span><span class="sxs-lookup"><span data-stu-id="ee40a-102">memberInfoCacheCreation MDA</span></span>
<span data-ttu-id="ee40a-103">L’Assistant Débogage managé `memberInfoCacheCreation` est activé quand le cache <xref:System.Reflection.MemberInfo> est créé.</span><span class="sxs-lookup"><span data-stu-id="ee40a-103">The `memberInfoCacheCreation` managed debugging assistant (MDA) is activated when a <xref:System.Reflection.MemberInfo> cache is created.</span></span> <span data-ttu-id="ee40a-104">Il s’agit d’une indication forte d’un programme qui utilise des fonctionnalités de réflexion coûteuses en ressources.</span><span class="sxs-lookup"><span data-stu-id="ee40a-104">This is a strong indication of a program that is making use of resource-expensive reflection features.</span></span>  
  
## <a name="symptoms"></a><span data-ttu-id="ee40a-105">Symptômes</span><span class="sxs-lookup"><span data-stu-id="ee40a-105">Symptoms</span></span>  
 <span data-ttu-id="ee40a-106">La plage de travail d’un programme augmente, car il utilise une réflexion coûteuse en ressources.</span><span class="sxs-lookup"><span data-stu-id="ee40a-106">A program's working set increases because the program is using resource-expensive reflection.</span></span>  
  
## <a name="cause"></a><span data-ttu-id="ee40a-107">Cause</span><span class="sxs-lookup"><span data-stu-id="ee40a-107">Cause</span></span>  
 <span data-ttu-id="ee40a-108">Les opérations de réflexion qui impliquent des objets <xref:System.Reflection.MemberInfo> sont considérées comme coûteuses en ressources, car elles doivent lire les métadonnées stockées dans des pages peu consultées et elles indiquent généralement que le programme utilise un type de scénario à liaison tardive.</span><span class="sxs-lookup"><span data-stu-id="ee40a-108">Reflection operations that involve <xref:System.Reflection.MemberInfo> objects are considered resource expensive because they must read metadata that is stored in cold pages and in general they indicate the program is using some type of late-bound scenario.</span></span>  
  
## <a name="resolution"></a><span data-ttu-id="ee40a-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="ee40a-109">Resolution</span></span>  
 <span data-ttu-id="ee40a-110">Vous pouvez déterminer où la réflexion est utilisée dans votre programme en activant cet Assistant Débogage managé puis en exécutant votre code dans un débogueur, ou en effectuant un attachement avec un débogueur quand l’Assistant Débogage managé est activé.</span><span class="sxs-lookup"><span data-stu-id="ee40a-110">You can determine where reflection is being used in your program by enabling this MDA and then running your code in a debugger or attaching with a debugger when the MDA is activated.</span></span> <span data-ttu-id="ee40a-111">Avec un débogueur, vous obtenez une arborescence des appels de procédure indiquant où le cache <xref:System.Reflection.MemberInfo> a été créé et, à partir de là, vous pouvez déterminer où votre programme utilise la réflexion.</span><span class="sxs-lookup"><span data-stu-id="ee40a-111">Under a debugger you will get a stack trace showing where the <xref:System.Reflection.MemberInfo> cache was created and from there you can determine where your program is using reflection.</span></span>  
  
 <span data-ttu-id="ee40a-112">La résolution dépend des objectifs du code.</span><span class="sxs-lookup"><span data-stu-id="ee40a-112">The resolution is dependent on the objectives of the code.</span></span> <span data-ttu-id="ee40a-113">Cet Assistant Débogage managé vous avertit que votre programme a un scénario à liaison tardive.</span><span class="sxs-lookup"><span data-stu-id="ee40a-113">This MDA alerts you that your program has a late-bound scenario.</span></span> <span data-ttu-id="ee40a-114">Vous pouvez alors déterminer si vous pouvez substituer un scénario à liaison anticipée ou considérer les performances du scénario à liaison tardive.</span><span class="sxs-lookup"><span data-stu-id="ee40a-114">You might want to determine if you can substitute an early-bound scenario or consider the performance of the late bound scenario.</span></span>  
  
## <a name="effect-on-the-runtime"></a><span data-ttu-id="ee40a-115">Effet sur le runtime</span><span class="sxs-lookup"><span data-stu-id="ee40a-115">Effect on the Runtime</span></span>  
 <span data-ttu-id="ee40a-116">Cet Assistant Débogage managé est activé pour chaque cache <xref:System.Reflection.MemberInfo> créé.</span><span class="sxs-lookup"><span data-stu-id="ee40a-116">This MDA is activated for every <xref:System.Reflection.MemberInfo> cache that is created.</span></span> <span data-ttu-id="ee40a-117">L’impact sur les performances est négligeable.</span><span class="sxs-lookup"><span data-stu-id="ee40a-117">The performance impact is negligible.</span></span>  
  
## <a name="output"></a><span data-ttu-id="ee40a-118">Sortie</span><span class="sxs-lookup"><span data-stu-id="ee40a-118">Output</span></span>  
 <span data-ttu-id="ee40a-119">L’Assistant Débogage managé génère un message indiquant que le cache <xref:System.Reflection.MemberInfo> a été créé.</span><span class="sxs-lookup"><span data-stu-id="ee40a-119">The MDA outputs a message indicating the <xref:System.Reflection.MemberInfo> cache was created.</span></span> <span data-ttu-id="ee40a-120">Pour obtenir une arborescence des appels de procédure montrant l’endroit où votre programme utilise la réflexion, utilisez un débogueur.</span><span class="sxs-lookup"><span data-stu-id="ee40a-120">Use a debugger to get a stack trace showing where your program is using reflection.</span></span>  
  
## <a name="configuration"></a><span data-ttu-id="ee40a-121">Configuration</span><span class="sxs-lookup"><span data-stu-id="ee40a-121">Configuration</span></span>  
  
```xml  
<mdaConfig>  
  <assistants>  
    <memberInfoCacheCreation/>  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="example"></a><span data-ttu-id="ee40a-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="ee40a-122">Example</span></span>  
 <span data-ttu-id="ee40a-123">Cet exemple de code active l’Assistant Débogage managé `memberInfoCacheCreation`.</span><span class="sxs-lookup"><span data-stu-id="ee40a-123">This sample code will activate the `memberInfoCacheCreation` MDA.</span></span>  
  
```csharp
using System;  
  
public class Exe  
{  
    public static void Main()  
    {  
        typeof(object).GetMethods();  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="ee40a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee40a-124">See also</span></span>

- <xref:System.Reflection.MemberInfo>
- [<span data-ttu-id="ee40a-125">Diagnostic d'erreurs avec les Assistants de débogage managés</span><span class="sxs-lookup"><span data-stu-id="ee40a-125">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
