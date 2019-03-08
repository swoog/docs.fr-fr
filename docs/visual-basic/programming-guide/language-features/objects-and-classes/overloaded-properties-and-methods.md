---
title: Propriétés surchargées et méthodes (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- properties [Visual Basic], overloading
- methods [Visual Basic], overloading
- shadowing
- names [Visual Basic], multiple procedures with same
- procedures [Visual Basic], multiples with same name
- classes [Visual Basic], properties
- classes [Visual Basic], methods
- method overloading
- Overloads keyword [Visual Basic], overloaded members
ms.assetid: b686fb97-e7d7-4001-afaa-6650cba08f0d
ms.openlocfilehash: 8d7341370d9770d2e57f786ac7c68277e66a9bbd
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57677394"
---
# <a name="overloaded-properties-and-methods-visual-basic"></a>Propriétés surchargées et méthodes (Visual Basic)

La surcharge est la création de plusieurs procédures, de constructeur d’instance ou de propriété dans une classe avec le même nom mais différents types d’arguments.

## <a name="overloading-usage"></a>Utilisation de la surcharge

La surcharge est particulièrement utile lorsque votre modèle objet impose l’utilisation de noms identiques pour les procédures qui opèrent sur les différents types de données. Par exemple, une classe qui peut afficher plusieurs types de données différents peut avoir `Display` procédures ressemblent à ceci :

[!code-vb[VbVbalrOOP#64](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#64)]

Sans surcharge, vous devez créer des noms distincts pour chaque procédure, même s’ils font la même chose, comme indiqué ci-après :

[!code-vb[VbVbalrOOP#65](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#65)]

La surcharge rend plus facile à utiliser des propriétés ou méthodes, car elle fournit un choix de types de données qui peut être utilisé. Par exemple, surchargées `Display` méthode décrite ci-dessus peut être appelée avec une des lignes de code suivantes :

[!code-vb[VbVbalrOOP#66](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#66)]

Au moment de l’exécution, Visual Basic appelle la procédure correcte en fonction des types de données des paramètres que vous spécifiez.

## <a name="overloading-rules"></a>Règles de surcharge

 Vous créez un membre surchargé d’une classe en ajoutant deux ou plusieurs propriétés ou méthodes portant le même nom. À l’exception des membres dérivés surchargés, chaque membre surchargé doit avoir des listes de paramètres différentes, et les éléments suivants ne peuvent pas être utilisés comme une fonctionnalité de différenciation lors de la surcharge d’une propriété ou procédure :

- Modificateurs, tels que `ByVal` ou `ByRef`, qui s’appliquent à un membre ou les paramètres du membre.

- Noms des paramètres

- Types de retour de procédures

Le `Overloads` mot clé est facultatif lors de la surcharge, mais les éventuelles surchargé membre utilise le `Overloads` mot clé, puis tous les autres membres surchargés portant le même nom doivent également spécifier ce mot clé.

Les classes dérivées peuvent surcharger les membres hérités avec des membres qui ont des paramètres identiques et des types de paramètres, un processus appelé *occultation par nom et signature*. Si le `Overloads` mot clé est utilisé lors de l’occultation par le nom et la signature, implémentation de la classe dérivée du membre sera utilisée au lieu de l’implémentation dans la classe de base, et toutes les autres surcharges de ce membre seront disponibles pour les instances de la classe dérivée.

Si le `Overloads` mot clé est omis lors de la surcharge d’un membre hérité avec un membre qui possède des paramètres identiques et les types de paramètre, puis la surcharge est appelée *occultation par le nom*. Occultation par le nom remplace l’implémentation héritée d’un membre, et rend toutes les autres surcharges indisponibles pour les instances de la classe dérivée et ses descendants.

Le `Overloads` et `Shadows` modificateurs ne peuvent pas être utilisés avec la même propriété ou méthode.

### <a name="example"></a>Exemple

L’exemple suivant crée des méthodes surchargées qui acceptent soit un `String` ou `Decimal` représentation d’un montant en dollars et un retour d’une chaîne contenant la taxe.

#### <a name="to-use-this-example-to-create-an-overloaded-method"></a>Pour utiliser cet exemple pour créer une méthode surchargée

1. Ouvrez un nouveau projet et ajoutez une classe nommée `TaxClass`.

2. Ajoutez le code suivant à la classe `TaxClass` .

    [!code-vb[VbVbalrOOP#67](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#67)]

3. Ajoutez la procédure suivante à votre formulaire.

    [!code-vb[VbVbalrOOP#68](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#68)]

4. Ajouter un bouton à votre formulaire et appelez le `ShowTax` procédure à partir de la `Button1_Click` événements du bouton.

5. Exécutez le projet et cliquez sur le bouton du formulaire pour tester surchargées `ShowTax` procédure.

Au moment de l’exécution, le compilateur choisit la fonction surchargée appropriée qui correspond aux paramètres utilisés. Lorsque vous cliquez sur le bouton, la méthode surchargée est appelée en premier avec un `Price` paramètre qui est une chaîne et le message « le prix est une chaîne. Taxe est $5,12" s’affiche. `TaxAmount` est appelée avec un `Decimal` valeur de la deuxième fois et le message, « prix est un nombre décimal. Taxe est $5,12" s’affiche.

## <a name="see-also"></a>Voir aussi

- [Objets et classes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
- [Occultation dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
- [Sub (instruction)](../../../../visual-basic/language-reference/statements/sub-statement.md)
- [Éléments fondamentaux de l’héritage](../../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
- [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md)
- [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md)
- [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md)
- [Overloads](../../../../visual-basic/language-reference/modifiers/overloads.md)
- [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md)
