---
title: Un appel à une propriété ou une méthode ne peut pas utiliser une référence vers un objet privé, que ce soit comme argument ou comme valeur de retour
ms.date: 07/20/2015
f1_keywords:
- vbrID98
ms.assetid: 059b43e1-202d-4fa2-806b-7bad63c1e7ca
ms.openlocfilehash: 04124ca044ad8dbff58f85230d7e10ea336d41e7
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59341473"
---
# <a name="a-property-or-method-call-cannot-include-a-reference-to-a-private-object-either-as-an-argument-or-as-a-return-value"></a>Un appel à une propriété ou une méthode ne peut pas utiliser une référence vers un objet privé, que ce soit comme argument ou comme valeur de retour
Cette erreur peut avoir plusieurs causes, dont les suivantes :  
  
-   Un client a appelé une propriété ou méthode d’un composant hors processus et a tenté de passer une référence à un objet privé comme l’un des arguments.  
  
-   Un composant hors processus a appelé une méthode de rappel sur son client et a tenté de passer une référence à un objet privé.  
  
-   Un composant hors processus a tenté de passer une référence à un objet privé comme argument d’un événement qu’il a déclenché.  
  
-   Un client a tenté d’assigner une référence d’objet privé à un argument `ByRef` d’un événement qu’il gérait.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Supprimez la référence.  
  
## <a name="see-also"></a>Voir aussi

- [Private](../../../visual-basic/language-reference/modifiers/private.md)
