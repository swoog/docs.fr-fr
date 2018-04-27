---
title: Événement &#39; &lt;nom_événement1&gt; &#39; ne peut pas implémenter l’événement &#39; &lt;nom_événement2&gt; &#39; sur l’interface &#39; &lt;interface&gt; &#39; , car leurs types délégués &#39; &lt;delegate1&gt; &#39; et &#39; &lt;delegate2&gt; &#39; ne correspondent pas
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc31423
- bc31423
helpviewer_keywords:
- BC31423
ms.assetid: 2e754b66-5836-48ff-9697-b9c0d7085f18
caps.latest.revision: 6
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 41f5984458eb17db04f20b292a0d80783093dcb4
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="event-39lteventname1gt39-cannot-implement-event-39lteventname2gt39-on-interface-39ltinterfacegt39-because-their-delegate-types-39ltdelegate1gt39-and-39ltdelegate2gt39-do-not-match"></a>Événement &#39; &lt;nom_événement1&gt; &#39; ne peut pas implémenter l’événement &#39; &lt;nom_événement2&gt; &#39; sur l’interface &#39; &lt;interface&gt; &#39; , car leurs types délégués &#39; &lt;delegate1&gt; &#39; et &#39; &lt;delegate2&gt; &#39; ne correspondent pas
Visual Basic ne peut pas implémenter un événement car le type délégué de l’événement ne correspond pas le type délégué de l’événement dans l’interface. Cette erreur peut se produire quand vous définissez plusieurs événements dans une interface et essayez ensuite de les implémenter ensemble avec le même événement. Un événement peut implémenter deux événements ou plus seulement si tous les événements implémentés sont déclarés à l’aide de la syntaxe `As` et s’ils spécifient le même type délégué.  
  
 **ID d’erreur :** BC31423  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Implémentez les événements séparément.  
  
     - ou -  
  
-   Définissez les événements dans l’interface à l’aide de la `As` syntaxe et spécifient le même type délégué.  
  
## <a name="see-also"></a>Voir aussi  
 [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)  
 [Delegate (instruction)](../../../visual-basic/language-reference/statements/delegate-statement.md)  
 [Événements](../../../visual-basic/programming-guide/language-features/events/index.md)
