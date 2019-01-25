---
title: Événement ETW d'exception Thrown_V1
ms.date: 03/30/2017
helpviewer_keywords:
- ExceptionThrown_V1 event [.NET Framework]
- ETW, ExceptionThrown_V1 event (CLR)
ms.assetid: 0d3da389-6b7b-40f6-a877-fac546d6019c
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 07932a12916138dd7cbee2576e4fc747898b8063
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610840"
---
# <a name="exception-thrownv1-etw-event"></a>Événement ETW d'exception Thrown_V1
Cet événement capture des informations sur les exceptions levées.  
  
 Le tableau suivant affiche le mot clé sous lequel l’événement est déclenché, ainsi que le niveau de l’événement. (Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)  
  
|Mot clé pour déclencher l'événement|Niveau|  
|-----------------------------------|-----------|  
|`ExceptionKeyword` (0x8000)|Avertissement (2)|  
  
 Le tableau suivant affiche des informations sur les événements.  
  
|Événement|ID d'événement|Moment du déclenchement|  
|-----------|--------------|-----------------|  
|`ExceptionThrown_V1`|80|Une exception managée est levée.|  
  
 Le tableau suivant affiche des données liées aux événements.  
  
|Nom du champ|Type de données|Description|  
|----------------|---------------|-----------------|  
|Type d'exception|win:UnicodeString|Type de l’exception, par exemple `System.NullReferenceException`.|  
|Message d’exception|win:UnicodeString|Message d’exception réel.|  
|EIPCodeThrow|win:Pointer|Pointeur d’instruction où l’exception s’est produite.|  
|ExceptionHR|win:UInt32|Exception [HRESULT](https://go.microsoft.com/fwlink/?LinkId=179679).|  
|ExceptionFlags|win:UInt16|0 x 01 : HasInnerException (consultez [événements ETW du CLR](../../../docs/framework/performance/clr-etw-events.md) dans la documentation de Visual Basic).<br /><br /> 0 x 02 : IsNestedException.<br /><br /> 0 x 04 : IsRethrownException.<br /><br /> 0 x 08 : IsCorruptedStateException (indique que l’état du processus est endommagé ; consultez [gestion des Exceptions d’état endommagé](https://go.microsoft.com/fwlink/?LinkId=179681) sur MSDN).<br /><br /> 0 x 10 : IsCLSCompliant (une exception qui dérive de <xref:System.Exception> est conforme CLS ; sinon, il n’est pas conforme CLS).|  
|ClrInstanceID|win:UInt16|ID unique de l'instance de CLR ou CoreCLR.|  
  
## <a name="see-also"></a>Voir aussi
- [Événements ETW du CLR](../../../docs/framework/performance/clr-etw-events.md)
