---
title: Assistant Débogage managé failedQI
ms.date: 03/30/2017
helpviewer_keywords:
- failed QueryInterface
- FailedQI MDA
- QueryInterface call failures
- MDAs (managed debugging assistants), failed QueryInterface
- managed debugging assistants (MDAs), failed QueryInterface
ms.assetid: 902dc863-34b3-477c-b433-b8a6bb6133c6
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 60fd5c29f716aa55f35c520794fbc9a0f673b9f8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33387170"
---
# <a name="failedqi-mda"></a>Assistant Débogage managé failedQI
L'Assistant Débogage managé (MDA) `failedQI` est activé quand le runtime appelle `QueryInterface` sur un pointeur d'interface COM au nom d'un wrapper RCW et que l'appel à `QueryInterface` échoue.  
  
## <a name="symptoms"></a>Symptômes  
 Un cast sur un RCW échoue ou un appel à COM à partir d'un RCW échoue de manière inattendue.  
  
## <a name="cause"></a>Cause  
  
-   L'appel est effectué à partir du contexte incorrect.  
  
-   Le proxy inscrit fait échouer l'appel à `QueryInterface`, car la tentative d'appel a été effectuée dans le contexte incorrect.  
  
-   Un proxy détenu par OLE a retourné une erreur HRESULT.  
  
## <a name="resolution"></a>Résolution  
 Consultez la documentation MSDN sur les règles COM.  
  
## <a name="effect-on-the-runtime"></a>Effet sur le runtime  
 Si un appel à `QueryInterface` échoue, le contexte est changé et une nouvelle tentative d'appel à `QueryInterface` est effectuée pour déterminer si un contexte incorrect était en cause.  
  
## <a name="output"></a>Sortie  
 Nom managé de l'interface, GUID de l'interface et valeur HRESULT de l'échec.  
  
## <a name="configuration"></a>Configuration  
  
```xml  
<mdaConfig>  
  <assistants>  
    <failedQI/>  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Runtime.InteropServices.MarshalAsAttribute>  
 [Diagnostic d’erreurs avec les Assistants Débogage managé](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)  
 [Marshaling d'interopérabilité](../../../docs/framework/interop/interop-marshaling.md)
