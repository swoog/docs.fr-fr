---
title: Assistant Débogage managé pInvokeStackImbalance
ms.date: 03/30/2017
helpviewer_keywords:
- signatures, platform invoke
- stack depth
- platform invoke stack imbalance
- MDAs (managed debugging assistants), platform invoke
- platform invoke, run-time errors
- PInvokeStackImbalance MDA
- managed debugging assistants (MDAs), platform invoke
ms.assetid: 34ddc6bd-1675-4f35-86aa-de1645d5c631
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5594166081c36fbda1e5d1a62e017aaceb7a553d
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2018
ms.locfileid: "42912112"
---
# <a name="pinvokestackimbalance-mda"></a><span data-ttu-id="edd58-102">PInvokeStackImbalance (MDA)</span><span class="sxs-lookup"><span data-stu-id="edd58-102">PInvokeStackImbalance MDA</span></span>

<span data-ttu-id="edd58-103">Le `PInvokeStackImbalance` assistant débogage managé (MDA) est activé lorsque le CLR détecte que la profondeur de la pile après un appel de code non managé ne correspond pas à la profondeur de pile attendue, étant donnée la convention d’appel spécifiée dans le <xref:System.Runtime.InteropServices.DllImportAttribute> attribut et le déclaration des paramètres dans la signature managée.</span><span class="sxs-lookup"><span data-stu-id="edd58-103">The `PInvokeStackImbalance` managed debugging assistant (MDA) is activated when the CLR detects that the stack depth after a platform invoke call does not match the expected stack depth, given the calling convention specified in the <xref:System.Runtime.InteropServices.DllImportAttribute> attribute and the declaration of the parameters in the managed signature.</span></span>

<span data-ttu-id="edd58-104">L'Assistant Débogage managé (MDA) `PInvokeStackImbalance` est implémenté uniquement pour les plateformes 32 bits x86.</span><span class="sxs-lookup"><span data-stu-id="edd58-104">The `PInvokeStackImbalance` MDA is implemented only for 32-bit x86 platforms.</span></span>

> [!NOTE]
> <span data-ttu-id="edd58-105">Le `PInvokeStackImbalance` Assistant Débogage MANAGÉ est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="edd58-105">The `PInvokeStackImbalance` MDA is disabled by default.</span></span> <span data-ttu-id="edd58-106">Dans Visual Studio 2017, le `PInvokeStackImbalance` MDA s’affiche dans le **Assistants Débogage managé** liste dans le **paramètres d’Exception** boîte de dialogue (qui s’affiche lorsque vous sélectionnez **déboguer**  >  **Windows** > **paramètres d’Exception**).</span><span class="sxs-lookup"><span data-stu-id="edd58-106">In Visual Studio 2017, The `PInvokeStackImbalance` MDA appears in the **Managed Debugging Assistants** list in the **Exception Settings** dialog box (which is displayed when you select **Debug** > **Windows** > **Exception Settings**).</span></span> <span data-ttu-id="edd58-107">Toutefois, en sélectionnant ou en désactivant le **arrêter lorsque levée** case à cocher ne pas activer ou désactiver l’Assistant Débogage MANAGÉ ; cela détermine seulement si Visual Studio lève une exception lorsque l’Assistant Débogage MANAGÉ est activé.</span><span class="sxs-lookup"><span data-stu-id="edd58-107">However, selecting or clearing the **Break When Thrown** check box does not enable or disable the MDA; it only controls whether Visual Studio throws an exception when the MDA is activated.</span></span>

## <a name="symptoms"></a><span data-ttu-id="edd58-108">Symptômes</span><span class="sxs-lookup"><span data-stu-id="edd58-108">Symptoms</span></span>

<span data-ttu-id="edd58-109">Une application rencontre une violation d'accès ou une altération de la mémoire pendant ou après un appel de code non managé.</span><span class="sxs-lookup"><span data-stu-id="edd58-109">An application encounters an access violation or memory corruption when making or following a platform invoke call.</span></span>

## <a name="cause"></a><span data-ttu-id="edd58-110">Cause</span><span class="sxs-lookup"><span data-stu-id="edd58-110">Cause</span></span>

<span data-ttu-id="edd58-111">Il se peut que la signature managée de l'appel de code non managé ne corresponde pas à la signature non managée de la méthode qui est appelée.</span><span class="sxs-lookup"><span data-stu-id="edd58-111">The managed signature of the platform invoke call might not match the unmanaged signature of the method being called.</span></span>  <span data-ttu-id="edd58-112">Cette incompatibilité peut être due au fait que la signature managée ne déclare pas le nombre correct de paramètres ou ne spécifie pas la taille appropriée pour les paramètres.</span><span class="sxs-lookup"><span data-stu-id="edd58-112">This mismatch can be caused by the managed signature not declaring the correct number of parameters or not specifying the appropriate size for the parameters.</span></span>  <span data-ttu-id="edd58-113">L'Assistant Débogage managé (MDA) peut également être activé parce que la convention d'appel, éventuellement spécifiée par l'attribut <xref:System.Runtime.InteropServices.DllImportAttribute>, ne correspond pas à la convention d'appel non managée.</span><span class="sxs-lookup"><span data-stu-id="edd58-113">The MDA can also activate because the calling convention, possibly specified by the <xref:System.Runtime.InteropServices.DllImportAttribute> attribute, does not match the unmanaged calling convention.</span></span>

## <a name="resolution"></a><span data-ttu-id="edd58-114">Résolution</span><span class="sxs-lookup"><span data-stu-id="edd58-114">Resolution</span></span>

<span data-ttu-id="edd58-115">Vérifiez que la signature managée de l'appel de code non managé et la convention d'appel correspondent à la signature et à la convention d'appel de la cible native.</span><span class="sxs-lookup"><span data-stu-id="edd58-115">Review the managed platform invoke signature and calling convention to confirm it matches the signature and calling convention of the native target.</span></span>  <span data-ttu-id="edd58-116">Essayez de spécifier explicitement la convention d'appel à la fois du côté managé et du côté non managé.</span><span class="sxs-lookup"><span data-stu-id="edd58-116">Try explicitly specifying the calling convention on both the managed and unmanaged sides.</span></span> <span data-ttu-id="edd58-117">Il est également possible, mais moins probable, que la fonction non managée ait déséquilibré la pile pour une raison quelconque, telle qu'un bogue dans le compilateur non managé.</span><span class="sxs-lookup"><span data-stu-id="edd58-117">It is also possible, although not as likely, that the unmanaged function unbalanced the stack for some other reason, such as a bug in the unmanaged compiler.</span></span>

## <a name="effect-on-the-runtime"></a><span data-ttu-id="edd58-118">Effet sur le runtime</span><span class="sxs-lookup"><span data-stu-id="edd58-118">Effect on the Runtime</span></span>

<span data-ttu-id="edd58-119">Oblige tous les appels de code non managé à prendre le chemin d'accès non optimisé dans le CLR.</span><span class="sxs-lookup"><span data-stu-id="edd58-119">Forces all platform invoke calls to take the nonoptimized path in the CLR.</span></span>

## <a name="output"></a><span data-ttu-id="edd58-120">Sortie</span><span class="sxs-lookup"><span data-stu-id="edd58-120">Output</span></span>

<span data-ttu-id="edd58-121">Le message de l'Assistant Débogage managé (MDA) donne le nom de l'appel de méthode d'appel de code non managé qui provoque le déséquilibre de la pile.</span><span class="sxs-lookup"><span data-stu-id="edd58-121">The MDA message gives the name of the platform invoke method call that is causing the stack imbalance.</span></span> <span data-ttu-id="edd58-122">Voici un exemple de message d'un appel de code non managé sur la méthode `SampleMethod` :</span><span class="sxs-lookup"><span data-stu-id="edd58-122">A sample message of a platform invoke call on method `SampleMethod` is:</span></span>

<span data-ttu-id="edd58-123">**Un appel à la fonction PInvoke 'SampleMethod' a ait déséquilibré la pile. Cela est probablement parce que la signature PInvoke managée ne correspond pas à la signature cible non managée. Vérifiez que la convention d’appel et les paramètres de la signature PInvoke correspondent à la signature non managée cible.**</span><span class="sxs-lookup"><span data-stu-id="edd58-123">**A call to PInvoke function 'SampleMethod' has unbalanced the stack. This is likely because the managed PInvoke signature does not match the unmanaged target signature. Check that the calling convention and parameters of the PInvoke signature match the target unmanaged signature.**</span></span>

## <a name="configuration"></a><span data-ttu-id="edd58-124">Configuration</span><span class="sxs-lookup"><span data-stu-id="edd58-124">Configuration</span></span>

```xml
<mdaConfig>
  <assistants>
    <pInvokeStackImbalance />
  </assistants>
</mdaConfig>
```

## <a name="see-also"></a><span data-ttu-id="edd58-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edd58-125">See Also</span></span>

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [<span data-ttu-id="edd58-126">Diagnostic d’erreurs avec les Assistants Débogage managé</span><span class="sxs-lookup"><span data-stu-id="edd58-126">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [<span data-ttu-id="edd58-127">Marshaling d'interopérabilité</span><span class="sxs-lookup"><span data-stu-id="edd58-127">Interop Marshaling</span></span>](../../../docs/framework/interop/interop-marshaling.md)
