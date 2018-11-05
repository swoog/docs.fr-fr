---
title: 'Bien démarrer avec F # dans Visual Studio'
description: 'Découvrez comment utiliser F # avec Visual Studio.'
ms.date: 07/03/2018
ms.openlocfilehash: 3dac8466501338873aeb308ceac9274a7934a8a9
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43872849"
---
# <a name="get-started-with-f-in-visual-studio"></a>Bien démarrer avec F # dans Visual Studio

F # et les outils Visual F # sont pris en charge dans l’IDE Visual Studio.

Pour commencer, assurez-vous d’avoir [installé Visual Studio avec F #](install-fsharp.md#install-f-with-visual-studio).

## <a name="creating-a-console-application"></a>Création d’une application de console

Un des projets plus simples dans Visual Studio est l’Application de Console.  Voici comment faire.  Une fois que Visual Studio est ouvert :

1. Sur le **fichier** menu, pointez sur **New**, puis choisissez **projet**.

2.  Dans la nouvelle boîte de dialogue projet, sous **modèles**, vous devez voir **Visual F #**.  Choisissez cette option pour afficher les modèles F #.

3. Sélectionnez **.NET Core application Console** ou **application Console**.

3. Choisissez le **OK** bouton pour créer le projet F # !  Vous devez maintenant voir un projet F # dans l’Explorateur de solutions.

## <a name="writing-your-code"></a>Écrivez votre code

Commençons par écrire du code tout d’abord.  Assurez-vous que le `Program.fs` fichier est ouvert, puis remplacez son contenu par le code suivant :

[!code-fsharp[HelloSquare](../../../samples/snippets/fsharp/getting-started/hello-square.fs)]

Dans l’exemple de code précédent, une fonction `square` a été trouvé qui accepte une entrée nommée `x` et le multiplie par lui-même.  Étant donné que F # utilise [l’inférence de Type](../language-reference/type-inference.md), le type de `x` n’a pas besoin d’être spécifié.  Le compilateur F # comprend les types où la multiplication est valide et affectera un type à `x` selon la façon dont `square` est appelée.  Si vous pointez sur `square`, vous devez voir les éléments suivants :

```
val square: x:int -> int
```

C’est ce qui est appelé signature de type de la fonction.  Il peut être lu comme suit : « carré est une fonction qui prend un entier nommé x et produit un entier ».  Notez que le compilateur retournait `square` le `int` type pour le moment - il s’agit, car la multiplication n’est pas générique sur *tous les* types, mais plutôt générique entre un ensemble fermé de types.  Le compilateur F # prélevé `int` sur ce point, mais il ajuste la signature de type si vous appelez `square` avec un autre type d’entrée, comme un `float`.

Une autre fonction, `main`, est défini, ce qui est décoré avec le `EntryPoint` attribut pour indiquer au compilateur F # que l’exécution du programme doit commencer.  Il suit la même convention que les autres [les langages de programmation de style C](https://en.wikipedia.org/wiki/Entry_point#C_and_C.2B.2B), où les arguments de ligne de commande peuvent être passés à cette fonction, et un code entier est retourné (généralement `0`).

Il se trouve dans cette fonction que nous appelons le `square` fonction avec un argument de `12`.  Le compilateur F # puis assigne le type de `square` être `int -> int` (autrement dit, une fonction qui prend un `int` et produit un `int`).  L’appel à `printfn` est une fonction d’impression mis en forme qui utilise une chaîne de format, similaire aux langages de programmation de style C, les paramètres qui correspondent à celles spécifiées dans la chaîne de format et imprime ensuite le résultat et une nouvelle ligne.

## <a name="running-your-code"></a>Exécution de votre code

Vous pouvez exécuter le code et afficher les résultats en appuyant sur **Ctrl**+**F5**.  Cela exécute le programme sans débogage et vous permet de voir les résultats.  Vous pouvez également choisir le **déboguer** menu de niveau supérieur d’élément dans Visual Studio et choisissez **démarrer sans débogage**.

Vous devez maintenant voir ce qui suit imprimé dans la fenêtre de console Visual Studio de s’afficher :

```
12 squared is 144!
```

Félicitations !  Vous avez créé votre premier projet F # dans Visual Studio, écrit qu'une fonction F # imprimer les résultats de l’appel de cette fonction et exécutez le projet pour afficher certains résultats.

## <a name="next-steps"></a>Étapes suivantes

Si vous n’avez pas déjà, consultez le [visite guidée de F #](../tour.md), qui aborde certaines des principales fonctionnalités du langage F #.  Il vous donner une vue d’ensemble de certaines des fonctionnalités de F # et fournissent des exemples de code suffisamment que vous pouvez copier dans Visual Studio et exécuter.  Il existe également des ressources exceptionnelles externes, vous pouvez utiliser, présentée dans le [Guide F #](../index.md).

## <a name="see-also"></a>Voir aussi

- [Présentation de F#](../tour.md)
- [Référence du langage F #](../language-reference/index.md)
- [Inférence de type](../language-reference/type-inference.md)
- [Référence des symboles et d’opérateur](../language-reference/symbol-and-operator-reference/index.md)
