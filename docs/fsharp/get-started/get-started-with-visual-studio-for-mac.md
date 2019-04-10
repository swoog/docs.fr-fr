---
title: Prise en main F# dans Visual Studio pour Mac
description: Découvrez comment utiliser F# avec Visual Studio pour Mac.
ms.date: 07/03/2018
ms.openlocfilehash: a6997f139d7e6c5fdf77878442db0b0b75b3d727
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59331861"
---
# <a name="get-started-with-f-in-visual-studio-for-mac"></a>Prise en main F# dans Visual Studio pour Mac

F#et le visuel F# outils sont pris en charge dans Visual Studio pour Mac IDE. Assurez-vous d’avoir [Visual Studio pour Mac installé](install-fsharp.md#install-f-with-visual-studio-for-mac).

## <a name="creating-a-console-application"></a>Création d’une application de console

Un des projets plus simples dans Visual Studio pour Mac est l’Application de Console.  Voici comment faire.  Une fois que Visual Studio pour Mac est ouvert :

1. Sur le **fichier** menu, pointez sur **nouvelle Solution**.

2. Dans la boîte de dialogue Nouveau projet, il existe 2 différents modèles d’Application de Console.  Il y a un sous autre -> .NET qui cible le .NET Framework.  L’autre modèle est sous .NET Core -> application qui cible .NET Core.  Un modèle doit fonctionner pour les besoins de cet article.

3. Sous l’application de console, modifiez C# à F# si nécessaire.  Choisissez le **suivant** bouton Déplacer vers l’avant !  

4. Donnez un nom à votre projet, puis choisissez les options souhaitées pour l’application.  Notez, le volet de visualisation vers le côté de l’écran qui affiche la structure de répertoires qui est créée en fonction des options sélectionnées.  

5. Cliquez sur **Créer**.  Vous devriez maintenant voir un F# projet dans l’Explorateur de solutions.

## <a name="writing-your-code"></a>Écrivez votre code

Commençons par écrire du code tout d’abord.  Assurez-vous que le `Program.fs` fichier est ouvert, puis remplacez son contenu par le code suivant :

[!code-fsharp[HelloSquare](../../../samples/snippets/fsharp/getting-started/hello-square.fs)]

Dans l’exemple de code précédent, une fonction `square` a été trouvé qui accepte une entrée nommée `x` et le multiplie par lui-même.  Étant donné que F# utilise [l’inférence de Type](../language-reference/type-inference.md), le type de `x` n’a pas besoin d’être spécifié.  Le F# compilateur comprend les types où la multiplication est valide et affectera un type à `x` selon la façon dont `square` est appelée.  Si vous pointez sur `square`, vous devez voir les éléments suivants :

```
val square: x:int -> int
```

C’est ce qui est appelé signature de type de la fonction.  Il peut être lu comme suit : « Carré est une fonction qui prend un entier nommé x et produit un entier ».  Notez que le compilateur retournait `square` le `int` type pour le moment - il s’agit, car la multiplication n’est pas générique sur *tous les* types, mais plutôt générique entre un ensemble fermé de types.  Le F# compilateur prélevé `int` sur ce point, mais il ajuste la signature de type si vous appelez `square` avec un autre type d’entrée, comme un `float`.

Une autre fonction, `main`, est défini, ce qui est décoré avec le `EntryPoint` attribut pour indiquer la F# compilateur que l’exécution du programme doit commencer.  Il suit la même convention que les autres [les langages de programmation de style C](https://en.wikipedia.org/wiki/Entry_point#C_and_C.2B.2B), où les arguments de ligne de commande peuvent être passés à cette fonction, et un code entier est retourné (généralement `0`).

Il se trouve dans cette fonction que nous appelons le `square` fonction avec un argument de `12`.  Le F# compilateur puis assigne le type de `square` être `int -> int` (autrement dit, une fonction qui prend un `int` et produit un `int`).  L’appel à `printfn` est une fonction d’impression mis en forme qui utilise une chaîne de format, similaire aux langages de programmation de style C, les paramètres qui correspondent à celles spécifiées dans la chaîne de format et imprime ensuite le résultat et une nouvelle ligne.

## <a name="running-your-code"></a>Exécution de votre code

Vous pouvez exécuter le code et afficher les résultats en cliquant sur **exécuter** dans le menu de niveau supérieur, puis **démarrer sans débogage**.  Cela exécutera le programme sans débogage et vous permet de voir les résultats.

Vous devez maintenant voir ce qui suit imprimé dans la fenêtre de console Visual Studio pour Mac est apparue :

```
12 squared is 144!
```

Félicitations !  Vous avez créé votre premier F# projet dans Visual Studio pour Mac, écrit un F# fonction Imprimer les résultats de l’appel de fonction, puis exécutez le projet pour voir des résultats.

## <a name="using-f-interactive"></a>À l’aide de F# Interactive

Une des meilleures fonctionnalités de l’élément visuel F# outils dans Visual Studio pour Mac est la F# fenêtre Interactive.  Il vous permet d’envoyer le code sur à un processus dans lequel vous pouvez appeler ce code et afficher le résultat de manière interactive.

Pour commencer à l’utiliser, mettez en surbrillance le `square` fonction définie dans votre code.  Ensuite, cliquez sur **modifier** dans le menu de niveau supérieur.  Sélectionnez ensuite **envoyer la sélection à F# Interactive**.  Cela exécute le code dans le F# fenêtre Interactive.  Ou bien, vous pouvez cliquez avec le bouton droit sur la sélection et choisissez **envoyer la sélection à F# Interactive**.  Vous devez voir le F# fenêtre Interactive s’affichent par le code suivant dans celui-ci :

```
>

val square : x:int -> int

>
```

Cela montre la même signature de fonction pour le `square` (fonction), vous l’avez vu précédemment lorsque vous pointez sur la fonction.  Étant donné que `square` est maintenant définie dans le F# processus interactif, vous pouvez l’appeler avec des valeurs différentes :

```
> square 12;;
val it : int = 144
>square 13;;
val it : int = 169
```

Cela exécute la fonction, lie le résultat vers un nouveau nom `it`et affiche le type et la valeur de `it`.  Notez que vous devez terminer chaque ligne avec `;;`.  Voici comment F# Interactive sait quand votre appel de fonction est terminée.  Vous pouvez également définir des nouvelles fonctions dans F# Interactive :

```
> let isOdd x = x % 2 <> 0;;

val isOdd : x:int -> bool

> isOdd 12;;
val it : bool = false
```

La méthode ci-dessus définit une nouvelle fonction, `isOdd`, qui accepte un `int` et vérifie s’il est impair !  Vous pouvez appeler cette fonction pour afficher sa valeur de retour avec des entrées différentes.  Vous pouvez appeler des fonctions dans les appels de fonction :

```
> isOdd (square 15);;
val it : bool = true
```

Vous pouvez également utiliser le [opérateur de canal-forward](../language-reference/symbol-and-operator-reference/index.md) au pipeline de la valeur dans les deux fonctions :

```
> 15 |> square |> isOdd;;
val it : bool = true
```

L’opérateur de redirection de canal et bien plus encore, sont traités dans les didacticiels suivants.

Il s’agit uniquement d’un aperçu dans ce que vous pouvez faire avec F# Interactive.  Pour plus d’informations, consultez [programmation Interactive avec F# ](../tutorials/fsharp-interactive/index.md).

## <a name="next-steps"></a>Étapes suivantes

Si vous n’avez pas déjà, consultez le [visite guidée de F# ](../tour.md), qui aborde certaines des principales fonctionnalités de la F# langage.  Il vous donnera une vue d’ensemble de certaines des fonctionnalités de F#et fournissent des exemples de code suffisamment que vous pouvez copier dans Visual Studio pour Mac et d’exécution.  Il existe également des ressources exceptionnelles externes, vous pouvez utiliser, présentée dans le [ F# Guide](../index.md).

## <a name="see-also"></a>Voir aussi

- [Visual F#](../index.md)
- [Visite guidée de F#](../tour.md)
- [F#référence du langage](../language-reference/index.md)
- [Inférence de type](../language-reference/type-inference.md)
- [Référence des symboles et d’opérateur](../language-reference/symbol-and-operator-reference/index.md)
