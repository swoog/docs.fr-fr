---
title: 'Comment : définir un paramètre pour une procédure (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedure parameters [Visual Basic], defining data types for
- procedures [Visual Basic], parameters
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- procedure parameters [Visual Basic], defining
ms.assetid: 7962808d-407e-4e84-984e-43e9857c53c9
ms.openlocfilehash: b058f593b8672da449dac250947563c75c8386bf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33651111"
---
# <a name="how-to-define-a-parameter-for-a-procedure-visual-basic"></a>Comment : définir un paramètre pour une procédure (Visual Basic)
A *paramètre* permet au code appelant de passer une valeur à la procédure lorsqu’il l’appelle. Vous déclarez chaque paramètre pour une procédure de la même manière que vous déclarez une variable, en spécifiant son nom et type de données. Vous spécifiez également le mécanisme de passage et si le paramètre est facultatif.  
  
 Pour plus d’informations, consultez [les paramètres de procédure et les Arguments](./procedure-parameters-and-arguments.md).  
  
### <a name="to-define-a-procedure-parameter"></a>Pour définir un paramètre de procédure  
  
1.  Dans la déclaration de procédure, ajoutez le nom du paramètre à la liste de paramètres de la procédure, en le séparant des autres paramètres par des virgules.  
  
2.  Déterminez le type de données du paramètre.  
  
3.  Suivre le nom du paramètre avec un `As` clause pour spécifier le type de données.  
  
4.  Choisissez le mécanisme de passage que vous souhaitez pour le paramètre. Normalement, vous passez un paramètre par valeur, sauf si vous souhaitez que la procédure puisse modifier sa valeur dans le code appelant.  
  
5.  Faites précéder le nom de paramètre avec [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) ou [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md) pour spécifier le mécanisme de passage. Pour plus d’informations, consultez [les différences entre en passant un Argument par valeur et par référence](./differences-between-passing-an-argument-by-value-and-by-reference.md).  
  
6.  Si le paramètre est facultatif, faites précéder le mécanisme de passage de [facultatif](../../../../visual-basic/language-reference/modifiers/optional.md) et suivez le type de données de paramètre avec un signe égal (`=`) et une valeur par défaut.  
  
     L’exemple suivant définit le plan d’un `Sub` procédure avec trois paramètres. Les deux premiers sont requis et le troisième est facultatif. Les déclarations de paramètre sont séparées dans la liste de paramètres par des virgules.  
  
     [!code-vb[VbVbcnProcedures#33](./codesnippet/VisualBasic/how-to-define-a-parameter-for-a-procedure_1.vb)]  
  
     Le premier paramètre accepte une `customer` objet, et `updateCustomer` peut mettre directement à jour la variable passée à `c` , car l’argument est passé [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md). La procédure ne peut pas modifier les valeurs des deux derniers arguments parce qu’ils sont passés [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md).  
  
     Si le code appelant ne fournit pas une valeur pour le `level` paramètre, Visual Basic lui affecte la valeur par défaut 0.  
  
     Si le commutateur de la vérification de type ([Option Strict, instruction](../../../../visual-basic/language-reference/statements/option-strict-statement.md)) est `Off`, le `As` clause est facultative lorsque vous définissez un paramètre. Toutefois, si un paramètre utilise un `As` clause, tous doivent l’utiliser. Si le commutateur de vérification de type est `On`, le `As` clause est requise pour chaque définition de paramètre.  
  
     Spécifier les types de données pour tous les éléments de programmation est appelé *typage fort*. Lorsque vous définissez `Option Strict On`, Visual Basic applique un typage fort. Il est fortement recommandé, pour les raisons suivantes :  
  
    -   Il permet la prise en charge IntelliSense pour les variables et des paramètres. Cela vous permet de vous permet de voir leurs propriétés et autres membres que vous entrez dans votre code.  
  
    -   Il permet au compilateur d’effectuer la vérification du type. Cela permet d’intercepter les instructions peuvent échouer au moment de l’exécution en raison d’erreurs de dépassement de capacité. Il intercepte également les appels aux méthodes sur des objets qui ne les prennent pas en charge.  
  
    -   Il en résulte une exécution plus rapide de votre code. Une des raisons sont que si vous ne spécifiez pas un type de données pour un élément de programmation, le compilateur Visual Basic lui assigne la `Object` type. Votre code compilé peut avoir à convertir entre `Object` et d’autres types de données, ce qui réduit les performances.  
  
## <a name="see-also"></a>Voir aussi

 [Procédures](./index.md)  
 [Procédures Sub](./sub-procedures.md)  
 [Procédures Function](./function-procedures.md)  
 [Guide pratique : passer des arguments à une procédure](./how-to-pass-arguments-to-a-procedure.md)  
 [Passage d’un argument par valeur et par référence](./passing-arguments-by-value-and-by-reference.md)  
 [Procédures récursives](./recursive-procedures.md)  
 [Surcharge de procédure](./procedure-overloading.md)  
 [Objets et classes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)  
 [Programmation orientée objet (Visual Basic)](../../concepts/object-oriented-programming.md)  
