---
title: Procédures Sub (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Sub procedures [Visual Basic], about Sub procedures
- statement blocks
- Sub procedures [Visual Basic], calling
- procedures [Visual Basic], calling
- Sub procedures [Visual Basic], syntax
- Sub procedures
- procedures [Visual Basic], Sub
- syntax [Visual Basic], Sub procedures
ms.assetid: 6a0a4958-ed0a-4d3d-8d31-0772c82bda58
ms.openlocfilehash: b70594e002bbf08f0890586e78df901ccb26c7ce
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58843101"
---
# <a name="sub-procedures-visual-basic"></a>Procédures Sub (Visual Basic)
Un `Sub` procédure est une série d’instructions Visual Basic délimitée par le `Sub` et `End Sub` instructions. Le `Sub` procédure effectue une tâche, puis retourne le contrôle au code appelant, mais il ne retourne pas une valeur au code appelant.  
  
 Chaque fois que la procédure est appelée, ses instructions sont exécutées, en commençant par la première instruction exécutable après le `Sub` instruction et se terminant par la première `End Sub`, `Exit Sub`, ou `Return` instruction rencontrée.  
  
 Vous pouvez définir un `Sub` procédure dans les modules, les classes et structures. Par défaut, il est `Public`, ce qui signifie que vous pouvez l’appeler depuis n’importe où dans votre application qui a accès au module, classe ou structure dans laquelle vous l’avez définie. Le terme, *méthode*, décrit une `Sub` ou `Function` procédure qui est accessible depuis l’extérieur de sa définition de module, classe ou structure. Pour plus d’informations, consultez [Procédures](./index.md).  
  
 Un `Sub` procédure peut prendre des arguments, tels que les constantes, variables ou expressions qui sont passées par le code appelant.  
  
## <a name="declaration-syntax"></a>Syntaxe de déclaration  
 La syntaxe pour déclarer un `Sub` procédure est la suivante :  
  
 `[` *modificateurs* `] Sub` *subname* `[(` *parameterlist* `)]`  
  
 `' Statements of the Sub procedure.`  
  
 `End Sub`  
  
 Le `modifiers` peut spécifier de niveau d’accès et des informations sur la surcharge, substitution, le partage et l’occultation. Pour plus d’informations, consultez [Sub, instruction](../../../../visual-basic/language-reference/statements/sub-statement.md).  
  
## <a name="parameter-declaration"></a>Déclaration de paramètre  
 Vous déclarez chaque paramètre de procédure de la même façon pour comment vous déclarez une variable, en spécifiant le type de données et le nom de paramètre. Vous pouvez également spécifier le mécanisme de passage et indique si le paramètre est facultatif ou un tableau de paramètres.  
  
 La syntaxe pour chaque paramètre dans la liste de paramètres est la suivante :  
  
 `[Optional] [ByVal | ByRef] [ParamArray]`  *parametername*  `As`  *datatype*  
  
 Si le paramètre est facultatif, vous devez également fournir une valeur par défaut dans le cadre de sa déclaration. La syntaxe de spécification d’une valeur par défaut est la suivante :  
  
 `Optional [ByVal | ByRef]`  *parametername*  `As`  *datatype*  `=`  *defaultvalue*  
  
### <a name="parameters-as-local-variables"></a>Paramètres en tant que Variables locales  
 Lorsque le contrôle passe à la procédure, chaque paramètre est traité comme une variable locale. Cela signifie que sa durée de vie est identique à celui de la procédure et son étendue est l’ensemble de la procédure.  
  
## <a name="calling-syntax"></a>Syntaxe d’appel  
 Vous appelez un `Sub` procédure explicitement avec une instruction d’appel autonome. Vous ne pouvez pas l’appeler à l’aide de son nom dans une expression. Vous devez fournir des valeurs pour tous les arguments qui ne sont pas facultatives, et vous devez placer la liste d’arguments entre parenthèses. Si aucun argument n’est fourni, vous pouvez éventuellement omettre les parenthèses. L’utilisation de la `Call` mot clé est facultative mais pas recommandée.  
  
 La syntaxe pour un appel à une `Sub` procédure est la suivante :  
  
 `[Call]`  *subname* `[(` *argumentlist* `)]`  
  
 Vous pouvez appeler un `Sub` méthode à partir en dehors de la classe qui le définit. Tout d’abord, vous devez utiliser le `New` mot clé pour créer une instance de la classe, ou appelez une méthode qui retourne une instance de la classe. Pour plus d’informations, consultez [nouvel opérateur](../../../../visual-basic/language-reference/operators/new-operator.md). Ensuite, vous pouvez utiliser la syntaxe suivante pour appeler le `Sub` méthode sur l’objet d’instance :  
  
 *Objet*. *MethodName*`[(`*argumentlist*`)]`  
  
### <a name="illustration-of-declaration-and-call"></a>Illustration de déclaration et d’appel  
 Ce qui suit `Sub` procédure indique à l’opérateur la tâche que l’application est sur le point d’effectuer et affiche également un horodatage. Au lieu de répéter ce code au début de chaque tâche, l’application appelle simplement `tellOperator` à partir de différents emplacements. Chaque appel passe une chaîne dans le `task` argument qui identifie la tâche en cours de démarrage.  
  
 [!code-vb[VbVbcnProcedures#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#2)]  
  
 L’exemple suivant montre un appel typique à `tellOperator`.  
  
 [!code-vb[VbVbcnProcedures#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#3)]  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Procédures Function](./function-procedures.md)
- [Procédures de propriété](./property-procedures.md)
- [Procédures d’opérateur](./operator-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Sub (instruction)](../../../../visual-basic/language-reference/statements/sub-statement.md)
- [Guide pratique pour Appeler une procédure qui ne retourne pas de valeur](./how-to-call-a-procedure-that-does-not-return-a-value.md)
- [Guide pratique pour Appeler un gestionnaire d’événements en Visual Basic](./how-to-call-an-event-handler.md)
