---
title: Assistant Débogage managé dllMainReturnsFalse
ms.date: 03/30/2017
helpviewer_keywords:
- managed debugging assistants (MDAs), DllMain returns false
- DllMainReturnsFalse MDA
- DllMain function
- MDAs (managed debugging assistants), DllMain returns false
ms.assetid: e2abdd04-f571-4b97-8c16-2221b8588429
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fd987cea78d082eee26032d5f98a54dc0cd3e1d5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59072621"
---
# <a name="dllmainreturnsfalse-mda"></a><span data-ttu-id="faf2f-102">Assistant Débogage managé dllMainReturnsFalse</span><span class="sxs-lookup"><span data-stu-id="faf2f-102">dllMainReturnsFalse MDA</span></span>
<span data-ttu-id="faf2f-103">L’Assistant Débogage managé `dllMainReturnsFalse` est activé si la fonction `DllMain` managée d’un assembly utilisateur, appelée avec la raison DLL_PROCESS_ATTACH, retourne FALSE.</span><span class="sxs-lookup"><span data-stu-id="faf2f-103">The `dllMainReturnsFalse` managed debugging assistant (MDA) is activated if the managed `DllMain` function of a user assembly, called with reason DLL_PROCESS_ATTACH, returns FALSE.</span></span>  
  
## <a name="symptoms"></a><span data-ttu-id="faf2f-104">Symptômes</span><span class="sxs-lookup"><span data-stu-id="faf2f-104">Symptoms</span></span>  
 <span data-ttu-id="faf2f-105">La fonction `DllMain` a retourné FALSE, indiquant qu’elle ne s’est pas exécuté correctement.</span><span class="sxs-lookup"><span data-stu-id="faf2f-105">The `DllMain` function returned FALSE, indicating that it did not execute properly.</span></span> <span data-ttu-id="faf2f-106">Cela peut entraîner des problèmes indéterminés, car les fonctions `DllMain` contiennent généralement du code d’initialisation important.</span><span class="sxs-lookup"><span data-stu-id="faf2f-106">This can cause undetermined issues because `DllMain` functions typically contain important initialization code.</span></span>  
  
## <a name="cause"></a><span data-ttu-id="faf2f-107">Cause</span><span class="sxs-lookup"><span data-stu-id="faf2f-107">Cause</span></span>  
 <span data-ttu-id="faf2f-108">La fonction `DllMain` est appelée avec la raison DLL_PROCESS_ATTACH pour l’initialisation de DLL lors du chargement.</span><span class="sxs-lookup"><span data-stu-id="faf2f-108">The `DllMain` function is called with reason DLL_PROCESS_ATTACH for DLL initialization upon load.</span></span> <span data-ttu-id="faf2f-109">Si elle retourne FALSE, cela signifie que l’initialisation de la DLL a échoué.</span><span class="sxs-lookup"><span data-stu-id="faf2f-109">If it returns FALSE, it means that DLL initialization failed.</span></span>  
  
## <a name="resolution"></a><span data-ttu-id="faf2f-110">Résolution</span><span class="sxs-lookup"><span data-stu-id="faf2f-110">Resolution</span></span>  
 <span data-ttu-id="faf2f-111">Analysez le code de la fonction `DllMain` de la DLL ayant échoué, et identifiez la cause de l’échec d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="faf2f-111">Analyze the code of the `DllMain` function of the failed DLL and identify the cause of the initialization failure.</span></span>  
  
## <a name="effect-on-the-runtime"></a><span data-ttu-id="faf2f-112">Effet sur le runtime</span><span class="sxs-lookup"><span data-stu-id="faf2f-112">Effect on the Runtime</span></span>  
 <span data-ttu-id="faf2f-113">Cet Assistant Débogage managé n'a aucun effet sur le CLR.</span><span class="sxs-lookup"><span data-stu-id="faf2f-113">This MDA has no effect on the CLR.</span></span> <span data-ttu-id="faf2f-114">Il fournit uniquement des données sur la valeur de retour pour `DllMain`.</span><span class="sxs-lookup"><span data-stu-id="faf2f-114">It only reports data about the return value for `DllMain`.</span></span>  
  
## <a name="output"></a><span data-ttu-id="faf2f-115">Sortie</span><span class="sxs-lookup"><span data-stu-id="faf2f-115">Output</span></span>  
 <span data-ttu-id="faf2f-116">Un message indiquant qu’une fonction `DllMain`, appelée pour la raison DLL_PROCESS_ATTACH, a retourné FALSE.</span><span class="sxs-lookup"><span data-stu-id="faf2f-116">A message indicating that a `DllMain` function, called for reason DLL_PROCESS_ATTACH, returned FALSE.</span></span> <span data-ttu-id="faf2f-117">Notez que cet Assistant Débogage managé est activé uniquement si `DllMain` est implémenté dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="faf2f-117">Note that this MDA is activated only if `DllMain` is implemented in managed code.</span></span>  
  
## <a name="configuration"></a><span data-ttu-id="faf2f-118">Configuration</span><span class="sxs-lookup"><span data-stu-id="faf2f-118">Configuration</span></span>  
  
```xml  
<mdaConfig>  
  <assistants>  
    <dllMainReturnsFalse />  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a><span data-ttu-id="faf2f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="faf2f-119">See also</span></span>

- [<span data-ttu-id="faf2f-120">Diagnostic d'erreurs avec les Assistants de débogage managés</span><span class="sxs-lookup"><span data-stu-id="faf2f-120">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
