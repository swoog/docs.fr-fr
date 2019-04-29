---
title: Try... Catch... Instruction finally - Visual Basic
description: Apprenez à utiliser des exceptions avec Visual Basic instructions Try/Catch/Finally.
ms.date: 12/07/2018
f1_keywords:
- vb.Try...Catch...Finally
- vb.when
- vb.Finally
- vb.Catch
- vb.Try
helpviewer_keywords:
- Try...Catch...Finally statements
- Try statement [Visual Basic]
- try-catch exception handling, Try...Catch...Finally statements
- error handling, while running code
- Try statement [Visual Basic], Try...Catch...Finally
- Finally keyword [Visual Basic], Try...Catch...Finally
- Catch statement [Visual Basic]
- When keyword [Visual Basic]
- Visual Basic code, handling errors while running
- structured exception handling, Try...Catch...Finally statements
ms.assetid: d6488026-ccb3-42b8-a810-0d97b9d6472b
ms.custom: seodec18
ms.openlocfilehash: 2e4fef836b08f536565105dbab76292b2fc4388e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61934262"
---
# <a name="trycatchfinally-statement-visual-basic"></a>Try...Catch...Finally, instruction (Visual Basic)

Fournit un moyen de gérer certaines ou toutes les erreurs possibles qui peuvent se produire dans un bloc donné du code, tout code en cours d’exécution.

## <a name="syntax"></a>Syntaxe

```vb
Try
    [ tryStatements ]
    [ Exit Try ]
[ Catch [ exception [ As type ] ] [ When expression ]
    [ catchStatements ]
    [ Exit Try ] ]
[ Catch ... ]
[ Finally
    [ finallyStatements ] ]
End Try
```

## <a name="parts"></a>Composants

|Terme|Définition|
|---|---|
|`tryStatements`|Optionnel. Instructions où une erreur peut se produire. Il peut s'agir d'une instruction composée.|
|`Catch`|Optionnel. Plusieurs `Catch` blocs autorisés. Si une exception se produit lors du traitement de la `Try` bloquer, chacun `Catch` instruction est examinée dans l’ordre textuel afin de déterminer si elle gère l’exception, avec `exception` représentant l’exception qui a été levée.|
|`exception`|Optionnel. Tout nom de variable. La valeur initiale de l'argument `exception` est la valeur de l'erreur levée. Utilisé avec `Catch` pour spécifier l’erreur interceptée. Si omis, la `Catch` instruction intercepte toute exception.|
|`type`|Optionnel. Spécifie le type de filtre de la classe. Si la valeur de `exception` est du type spécifié par `type` ou d’un type dérivé, l’identificateur est lié à l’objet exception.|
|`When`|Facultatif. Un `Catch` instruction avec un `When` clause intercepte les exceptions uniquement lorsque `expression` prend la valeur `True`. Un `When` clause est appliquée uniquement après la vérification du type de l’exception, et `expression` peut faire référence à l’identificateur qui représente l’exception.|
|`expression`|Optionnel. Doit être implicitement convertible en `Boolean`. Toute expression qui décrit un filtre générique. Généralement utilisé pour filtrer par numéro d’erreur. Utilisé avec `When` mot clé pour spécifier les circonstances dans lesquelles l’erreur est interceptée.|
|`catchStatements`|Optionnel. Instructions permettant de gérer les erreurs qui se produisent dans associé `Try` bloc. Il peut s'agir d'une instruction composée.|
|`Exit Try`|Optionnel. Mot clé qui décompose le `Try...Catch...Finally` structure. L’exécution reprend avec le code qui suit immédiatement la `End Try` instruction. La `Finally` instruction sera exécutée. Interdit dans `Finally` blocs.|
|`Finally`|Optionnel. Un `Finally` bloc est toujours exécuté quand l’exécution quitte une partie de la `Try...Catch` instruction.|
|`finallyStatements`|Optionnel. Instructions qui sont exécutées une fois que tout autre traitement d’erreur s’est produite.|
|`End Try`|Met fin à la `Try...Catch...Finally` structure.|

## <a name="remarks"></a>Notes

Si vous pensez qu’une exception particulière se produise pendant une section particulière de code, placez le code dans un `Try` bloquer et utiliser un `Catch` bloc pour garder le contrôle et de gérer l’exception si elle se produit.

Un `Try…Catch` instruction se compose d’un `Try` bloc suivie d’une ou plusieurs `Catch` clauses qui spécifient des gestionnaires pour différentes exceptions. Lorsqu’une exception est levée dans un `Try` bloquer, Visual Basic recherche le `Catch` instruction qui gère l’exception. Si une correspondance `Catch` instruction n’est pas trouvée, Visual Basic examine la méthode qui a appelé la méthode actuelle, et ainsi de suite la pile des appels. Si aucun `Catch` bloc est trouvé, Visual Basic affiche un message d’exception non prise en charge pour l’utilisateur et arrête l’exécution du programme.

Vous pouvez utiliser plusieurs `Catch` instruction dans un `Try…Catch` instruction. Dans ce cas, l’ordre de la `Catch` clauses est important, car ils sont examinés dans l’ordre. Interceptez les exceptions plus spécifiques avant les moins spécifiques.

Ce qui suit `Catch` conditions de l’instruction sont les moins spécifiques et intercepte toutes les exceptions qui dérivent de la <xref:System.Exception> classe. Vous devez normalement utiliser une de ces variations comme dernier `Catch` bloquer le `Try...Catch...Finally` structure, après l’interception de toutes les exceptions spécifiques que vous attendez. Flux de contrôle ne peut jamais atteindre un `Catch` bloc qui suit une de ces variantes.

- Le `type` est `Exception`, par exemple : `Catch ex As Exception`

- L’instruction n’a aucun `exception` variable, par exemple : `Catch`

Quand un `Try…Catch…Finally` instruction est imbriquée dans une autre `Try` bloc, Visual Basic examine tout d’abord chaque `Catch` instruction dans la plus intérieure `Try` bloc. Si aucune correspondance `Catch` instruction est trouvée, la recherche se poursuit à le `Catch` instructions d’externe `Try…Catch…Finally` bloc.

Les variables locales à partir d’un `Try` bloc ne sont pas disponibles dans un `Catch` bloqué, car ils sont des blocs séparés. Si vous souhaitez utiliser une variable dans plusieurs blocs, déclarez la variable en dehors de la `Try...Catch...Finally` structure.

> [!TIP]
> La `Try…Catch…Finally` instruction est disponible en tant qu’un extrait de code IntelliSense. Dans le Gestionnaire des extraits de Code, développez **modèles de Code - If, For Each, Try Catch, propriété, etc.**, puis **(Exceptions) de gestion des erreurs**. Pour plus d’informations, consultez [Extraits de code](/visualstudio/ide/code-snippets).

## <a name="finally-block"></a>Bloc finally

Si vous avez une ou plusieurs instructions qui doivent s’exécuter avant de quitter le `Try` structure, utilisez un `Finally` bloc. Le contrôle passe à la `Finally` bloquer juste avant de sortir de la `Try…Catch` structure. Cela est vrai même si une exception se produit n’importe où à l’intérieur de la `Try` structure.

Un `Finally` bloc est utile pour l’exécution de tout code qui doit s’exécuter même s’il existe une exception. Le contrôle est passé à la `Finally` bloc quelle que soit la façon dont le `Try...Catch` bloquer se ferme.

Le code dans un `Finally` bloque s’exécute même si votre code rencontre une `Return` instruction dans un `Try` ou `Catch` bloc. Contrôle ne passe pas d’un `Try` ou `Catch` bloquer correspondant `Finally` bloquer dans les cas suivants :

- Un [instruction End](end-statement.md) est rencontré dans le `Try` ou `Catch` bloc.

- Un <xref:System.StackOverflowException> est levée dans le `Try` ou `Catch` bloc.

Il n’est pas valide pour transférer explicitement l’exécution dans un `Finally` bloc. Transfert de l’exécution hors d’un `Finally` bloc n’est pas valide, sauf via une exception.

Si un `Try` instruction ne contient-elle pas au moins un `Catch` bloc, il doit contenir un `Finally` bloc.

> [!TIP]
> Si vous n’avez pas intercepter des exceptions spécifiques, le `Using` instruction se comporte comme un `Try…Finally` bloc et garantit l’élimination des ressources, quel que soit la manière dont vous quittez le bloc. Cela est vrai même avec une exception non gérée. Pour plus d’informations, consultez [using, instruction](using-statement.md).

## <a name="exception-argument"></a>Argument d’exception

Le `Catch` bloc `exception` argument est une instance de la <xref:System.Exception> classe ou une classe qui dérive de la `Exception` classe. Le `Exception` instance de classe correspond à l’erreur qui s’est produite dans le `Try` bloc.

Les propriétés de la `Exception` aide à identifier la cause et l’emplacement d’une exception de l’objet. Par exemple, le <xref:System.Exception.StackTrace%2A> propriété répertorie les méthodes appelées qui a conduit à l’exception, ce qui vous aide à trouver où l’erreur s’est produite dans le code. <xref:System.Exception.Message%2A> Retourne un message qui décrit l’exception. <xref:System.Exception.HelpLink%2A> Renvoie un lien vers un fichier d’aide associé. <xref:System.Exception.InnerException%2A> Retourne le `Exception` objet qui a provoqué l’exception actuelle, ou elle retourne `Nothing` s’il n’existe aucun original `Exception`.

## <a name="considerations-when-using-a-trycatch-statement"></a>Considérations sur l’utilisation d’un bloc Try... Catch, instruction

Utilisez un `Try…Catch` instruction uniquement pour signaler la présence d’événements inhabituels ou imprévus. Pour cela les raisons suivantes :

- Interception des exceptions lors de l’exécution crée une charge supplémentaire et est susceptible d’être plus lent que pré-vérification pour éviter les exceptions.

- Si un `Catch` bloc n’est pas traitée correctement, l’exception peuvent ne pas être déclarée correctement pour les utilisateurs.

- Gestion des exceptions rend plus complexe.

Vous n’avez pas toujours besoin un `Try…Catch` instruction pour vérifier une condition qui est susceptible de se produire. L’exemple suivant vérifie l’existence d’un fichier avant d’essayer de l’ouvrir. Cela réduit la nécessité d’intercepter une exception levée par le <xref:System.IO.File.OpenText%2A> (méthode).

[!code-vb[VbVbalrStatements#94](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#94)]

Assurez-vous que le code de `Catch` blocs peuvent correctement signaler les exceptions aux utilisateurs, via la journalisation thread-safe ou les messages appropriés. Sinon, les exceptions pourraient rester inconnues.

## <a name="async-methods"></a>Méthodes Async

Si vous marquez une méthode avec le [Async](../modifiers/async.md) modificateur, vous pouvez utiliser la [Await](../operators/await-operator.md) opérateur dans la méthode. Une instruction avec le `Await` opérateur suspend l’exécution de la méthode jusqu'à ce que la tâche attendue se termine. La tâche représente un travail en cours. Lorsque la tâche qui est associée la `Await` opérateur terminée, l’exécution reprend dans la même méthode. Pour plus d’informations, consultez [flux de contrôle dans les programmes Async](../../../visual-basic/programming-guide/concepts/async/control-flow-in-async-programs.md).

Une tâche retournée par une méthode Async peut se terminer par un état d’erreur, indiquant qu’il est terminé en raison d’une exception non gérée. Une tâche peut également se terminer dans un état annulé, ce qui entraîne un `OperationCanceledException` levée en dehors de l’expression await. Pour intercepter un type d’exception, placez le `Await` expression qui est associé à la tâche dans un `Try` bloquer et intercepter l’exception dans le `Catch` bloc. Un exemple est fourni plus loin dans cette rubrique.

Une tâche peut être dans un état d’erreur, car plusieurs exceptions ont été responsables de sa défaillance. Par exemple, la tâche peut être le résultat d'un appel à <xref:System.Threading.Tasks.Task.WhenAll%2A?displayProperty=nameWithType>. Lorsque vous attendez une telle tâche, l’exception interceptée est uniquement une des exceptions, et vous ne pouvez pas prédire quelle exception est interceptée. Un exemple est fourni plus loin dans cette rubrique.

Un `Await` expression ne peut pas être à l’intérieur d’un `Catch` bloc ou `Finally` bloc.

## <a name="iterators"></a>Iterators

Une fonction d’itérateur ou `Get` accesseur effectue une itération personnalisée sur une collection. Un itérateur utilise une [Yield](yield-statement.md) instruction pour retourner chaque élément de la collection un à la fois. Vous appelez une fonction d’itérateur en utilisant un [For Each... L’instruction suivante](for-each-next-statement.md).

Un `Yield` instruction peut être à l’intérieur d’un `Try` bloc. Un `Try` bloc qui contient un `Yield` instruction peut avoir `Catch` bloque et peut avoir un `Finally` bloc. Consultez la section « Essayez de blocs dans Visual Basic » de [itérateurs](../../programming-guide/concepts/iterators.md) pour obtenir un exemple.

Un `Yield` instruction ne peut pas être à l’intérieur d’un `Catch` bloc ou une `Finally` bloc.

Si le `For Each` corps (en dehors de la fonction d’itérateur) lève une exception, un `Catch` bloc dans la fonction d’itérateur n’est pas exécuté, mais un `Finally` bloc dans la fonction d’itérateur est exécuté. Un `Catch` bloc à l’intérieur d’une fonction d’itérateur intercepte uniquement les exceptions qui se produisent à l’intérieur de la fonction d’itérateur.

## <a name="partial-trust-situations"></a>Situations de confiance partielle

Dans les situations de confiance partielle, tel qu’une application hébergée sur un partage réseau, `Try...Catch...Finally` n’intercepte pas les exceptions de sécurité qui se produisent avant l’appel de la méthode qui contient l’appel. L’exemple suivant, lorsque vous placez sur un partage de serveur et que vous exécutez à partir de là, génère l’erreur « System.Security.SecurityException : Échoué de la demande. » Pour plus d’informations sur les exceptions de sécurité, consultez la <xref:System.Security.SecurityException> classe.

[!code-vb[VbVbalrStatements#85](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#85)]

Dans une telle situation de confiance partielle, vous devez placer le `Process.Start` instruction dans une fonction `Sub`. L’appel initial à la `Sub` échoue. Cela permet de `Try...Catch` de l’intercepter avant le `Sub` contenant `Process.Start` est démarré et généré l’exception de sécurité.

## <a name="examples"></a>Exemples

### <a name="the-structure-of-trycatchfinally"></a>La structure de Try... Catch... Enfin

L’exemple suivant illustre la structure de la `Try...Catch...Finally` instruction.

[!code-vb[VbVbalrStatements#86](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#86)]  

### <a name="exception-in-a-method-called-from-a-try-block"></a>Exception dans une méthode appelée à partir d’un bloc Try

Dans l’exemple suivant, le `CreateException` méthode lève un `NullReferenceException`. Le code qui génère l’exception n’est pas dans un `Try` bloc. Par conséquent, le `CreateException` méthode ne gère pas l’exception. Le `RunSample` méthode gère l’exception, car l’appel à la `CreateException` méthode se trouve dans un `Try` bloc.

L’exemple inclut `Catch` instructions pour plusieurs types d’exceptions, classées de la plus spécifique au plus général.

[!code-vb[VbVbalrStatements#91](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#91)]

### <a name="the-catch-when-statement"></a>L’instruction Catch lorsque

L’exemple suivant montre comment utiliser un `Catch When` instruction pour filtrer sur une expression conditionnelle. Si l’expression conditionnelle a la valeur `True`, le code dans le `Catch` bloquer s’exécute.

[!code-vb[VbVbalrStatements#92](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#92)]

### <a name="nested-try-statements"></a>Instructions Try imbriquées

L’exemple suivant comprend un `Try…Catch` instruction qui est contenue dans un `Try` bloc. Interne `Catch` bloc lève une exception qui a son `InnerException` propriété définie à l’exception d’origine. Externe `Catch` bloc signale sa propre exception et l’exception interne.

[!code-vb[VbVbalrStatements#93](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#93)]

### <a name="exception-handling-for-async-methods"></a>Gestion des exceptions pour les méthodes async

L'exemple suivant illustre la gestion des exceptions pour les méthodes async. Pour intercepter une exception qui s’applique à une tâche asynchrone, le `Await` expression est dans un `Try` bloc de l’appelant et l’exception est interceptée dans le `Catch` bloc.

Supprimez les marques de commentaire de la ligne `Throw New Exception` dans l'exemple pour illustrer la gestion des exceptions. L’exception est interceptée dans le `Catch` bloquer, de la tâche `IsFaulted` propriété est définie sur `True`et de la tâche `Exception.InnerException` propriété est définie à l’exception.

Supprimez les marques de commentaire de la ligne `Throw New OperationCancelledException` pour montrer ce qui se passe quand vous annulez un processus asynchrone. L’exception est interceptée dans le `Catch` bloc et de la tâche `IsCanceled` propriété est définie sur `True`. Toutefois, dans certaines conditions qui s’appliquent à cet exemple, `IsFaulted` a la valeur `True` et `IsCanceled` est défini sur `False`.

[!code-vb[csAsyncExceptions#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/csasyncexceptions/vb/class1.vb#1)]

### <a name="handling-multiple-exceptions-in-async-methods"></a>Gestion des exceptions multiples dans les méthodes async

L’exemple suivant illustre la gestion des exceptions quand plusieurs tâches peuvent entraîner plusieurs exceptions. Le `Try` bloc a le `Await` expression pour la tâche qui <xref:System.Threading.Tasks.Task.WhenAll%2A?displayProperty=nameWithType> retourné. La tâche est terminée lorsque les trois tâches auquel <xref:System.Threading.Tasks.Task.WhenAll%2A?displayProperty=nameWithType> est appliqué sont terminées.

Chacune de ces trois tâches provoque une exception. Le `Catch` bloc effectue une itération dans les exceptions qui se trouvent dans le `Exception.InnerExceptions` propriété de la tâche qui `Task.WhenAll` retourné.

[!code-vb[csAsyncExceptions#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/csasyncexceptions/vb/class1.vb#3)]

## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Information.Err%2A>
- <xref:System.Exception>
- [Exit (instruction)](exit-statement.md)
- [On Error (instruction)](on-error-statement.md)
- [Bonnes pratiques pour l’utilisation des extraits de code](/visualstudio/ide/best-practices-for-using-code-snippets)
- [Gestion des exceptions](../../../standard/parallel-programming/exception-handling-task-parallel-library.md)
- [Throw (instruction)](throw-statement.md)