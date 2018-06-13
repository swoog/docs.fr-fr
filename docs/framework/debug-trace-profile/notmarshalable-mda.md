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
ms.openlocfilehash: c52f104228db0b9e7f664ee7c1de393aa696c71a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33386728"
---
# <a name="notmarshalable-mda"></a>notMarshalable (MDA)
L'Assistant Débogage managé (MDA) `notMarshalable` est activé lorsque le Common Language Runtime (CLR) rencontre un pointeur d'interface COM sans proxy/stub inscrit valide ou une implémentation d'interface `IMarshal` incorrecte lors d'une tentative de marshaling de l'interface entre plusieurs contextes.  
  
## <a name="symptoms"></a>Symptômes  
 Les appels ne sont pas traités ou ils se produisent dans le contexte incorrect pour les pointeurs d'interface COM.  
  
## <a name="cause"></a>Cause  
 Absence de proxy/stub inscrit valide ou présence d'une interface `IMarshal` incorrecte lors d'une tentative de marshaling de l'interface entre plusieurs contextes.  
  
## <a name="resolution"></a>Résolution  
 Assurez-vous que vous avez un stub/proxy inscrit et que l'implémentation de `IMarshal` est correcte.  
  
## <a name="effect-on-the-runtime"></a>Effet sur le runtime  
 Cet Assistant Débogage managé n'a aucun effet sur le runtime.  
  
## <a name="output"></a>Sortie  
 Message décrivant le problème.  
  
## <a name="configuration"></a>Configuration  
  
```xml  
<mdaConfig>  
  <assistants>  
    <notMarshalable/>  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Runtime.InteropServices.MarshalAsAttribute>  
 [Diagnostic d’erreurs avec les Assistants Débogage managé](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)  
 [Marshaling d'interopérabilité](../../../docs/framework/interop/interop-marshaling.md)
