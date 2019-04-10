---
title: La procédure Property Let n'est pas définie et la procédure Property Get n'a pas retourné d'objet
ms.date: 07/20/2015
f1_keywords:
- vbrID451
ms.assetid: 8542382a-689f-4e1b-abc0-c1e2dadb92f4
ms.openlocfilehash: 7da1de98132f47740e805ed34ff3890f0ba0f889
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59334703"
---
# <a name="property-let-procedure-not-defined-and-property-get-procedure-did-not-return-an-object"></a>La procédure Property Let n'est pas définie et la procédure Property Get n'a pas retourné d'objet
Certaines propriétés, méthodes et les opérations peuvent s’appliquent uniquement aux `Collection` objets. Vous avez spécifié une opération ou une propriété qui est réservée aux collections, mais l’objet n’est pas une collection.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Vérifiez l’orthographe du nom d’objet ou de propriété, ou vérifiez que l’objet est un `Collection` objet.  
  
2. Examinez le `Add` méthode utilisée pour ajouter l’objet à la collection pour être sûr que la syntaxe est correcte et que tous les identificateurs ont été correctement orthographiés.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Collection>
