---
title: Assistant Débogage managé illegalPrepareConstrainedRegion
ms.date: 03/30/2017
helpviewer_keywords:
- PrepareConstrainedRegions method
- managed debugging assistants (MDAs), illegal PrepareConstrainedRegions
- try/catch exception handling, managed debugging assistants
- IllegalPrepareConstrainedRegions MDA
- MDAs (managed debugging assistants), illegal PrepareConstrainedRegions
ms.assetid: 2f9b5031-f910-4e01-a196-f89eab313eaf
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 59a2b7f7ed855cd6b7d363ea5d4723c7d7b8d629
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="illegalprepareconstrainedregion-mda"></a>Assistant Débogage managé illegalPrepareConstrainedRegion
L’Assistant Débogage managé `illegalPrepareConstrainedRegion` est activé quand un appel de méthode <xref:System.Runtime.CompilerServices.RuntimeHelpers.PrepareConstrainedRegions%2A?displayProperty=nameWithType> ne précède pas immédiatement l’instruction `try` du gestionnaire d’exceptions. Cette restriction étant au niveau MSIL, il est permis d’avoir une source générant du non-code entre l’appel et `try`, telle que les commentaires.  
  
## <a name="symptoms"></a>Symptômes  
 Une région d’exécution limitée n’est jamais traitée comme telle, mais comme un bloc de gestion des exceptions simple (`finally` ou `catch`). Par conséquent, la région ne s’exécute pas en cas de mémoire insuffisante ou d’interruption de thread.  
  
## <a name="cause"></a>Cause  
 Le modèle de préparation pour une région d’exécution limitée n’est pas suivi correctement.  Il s’agit d’un événement d’erreur. Le <xref:System.Runtime.CompilerServices.RuntimeHelpers.PrepareConstrainedRegions%2A> appel de méthode utilisé pour marquer des gestionnaires d’exceptions comme introduisant une CER dans leurs `catch` / `finally` / `fault` / `filter` blocs doivent être utilisés qu’immédiatement avant le `try` instruction.  
  
## <a name="resolution"></a>Résolution  
 Vérifiez que l’appel à <xref:System.Runtime.CompilerServices.RuntimeHelpers.PrepareConstrainedRegions%2A> se produit immédiatement avant l’instruction `try`.  
  
## <a name="effect-on-the-runtime"></a>Effet sur le runtime  
 Cet Assistant Débogage managé n'a aucun effet sur le CLR.  
  
## <a name="output"></a>Sortie  
 L’Assistant Débogage managé affiche le nom de la méthode qui appelle la méthode <xref:System.Runtime.CompilerServices.RuntimeHelpers.PrepareConstrainedRegions%2A>, l’offset MSIL et un message indiquant que l’appel ne précède pas immédiatement le début du bloc try.  
  
## <a name="configuration"></a>Configuration  
  
```xml  
<mdaConfig>  
  <assistants>  
    <illegalPrepareConstrainedRegion/>  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant illustre le modèle qui provoque l’activation de cet Assistant Débogage managé.  
  
```  
void MethodWithInvalidPCR()  
{  
    RuntimeHelpers.PrepareConstrainedRegions();  
    Object o = new Object();  
    try  
    {  
        …  
    }  
    finally  
    {  
        …  
    }  
}  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Runtime.InteropServices.MarshalAsAttribute>  
 <xref:System.Runtime.CompilerServices.RuntimeHelpers.PrepareConstrainedRegions%2A>  
 [Diagnostic d’erreurs avec les Assistants Débogage managé](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)  
 [Marshaling d'interopérabilité](../../../docs/framework/interop/interop-marshaling.md)
