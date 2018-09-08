---
title: Classes (F#)
description: 'Découvrez comment F # Classes sont des types qui représentent des objets qui peuvent avoir des propriétés, méthodes et événements.'
ms.date: 05/16/2016
ms.openlocfilehash: 71cd713d192d28565e879b79b2fc9e0530e5f841
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44199828"
---
# <a name="classes"></a>Classes

*Classes* sont des types qui représentent des objets qui peuvent avoir des propriétés, méthodes et événements.

## <a name="syntax"></a>Syntaxe

```fsharp
// Class definition:
type [access-modifier] type-name [type-params] [access-modifier] ( parameter-list ) [ as identifier ] =
[ class ]
[ inherit base-type-name(base-constructor-args) ]
[ let-bindings ]
[ do-bindings ]
member-list
...
[ end ]
// Mutually recursive class definitions:
type [access-modifier] type-name1 ...
and [access-modifier] type-name2 ...
...
```

## <a name="remarks"></a>Notes

Les classes représentent la description fondamentale des types d’objet .NET ; la classe est le concept de type principal qui prend en charge la programmation orientée objet en F #.

Dans la syntaxe précédente, le `type-name` est n’importe quel identificateur valid. Le `type-params` décrit les paramètres de type générique facultatifs. Il se compose des noms de paramètre de type et des contraintes placé entourés crochets pointus (`<` et `>`). Pour plus d’informations, consultez [génériques](generics/index.md) et [contraintes](generics/constraints.md). Le `parameter-list` décrit les paramètres du constructeur. Le modificateur d’accès associé au type ; le second se rapporte au constructeur principal. Dans les deux cas, la valeur par défaut est `public`.

Vous spécifiez la classe de base pour une classe à l’aide de la `inherit` mot clé. Vous devez fournir des arguments entre parenthèses, pour le constructeur de classe de base.

Vous déclarez des champs ou des valeurs qui sont locales à la classe à l’aide de fonction `let` liaisons et vous devez suivre les règles générales pour `let` liaisons. Le `do-bindings` section comprend le code à exécuter après la construction de l’objet.

Le `member-list` se compose de constructeurs supplémentaires, instance déclarations de méthode statique, les déclarations d’interface, liaisons abstraites et des déclarations de propriété et d’événement. Ceux-ci sont décrits dans [membres](members/index.md).

Le `identifier` qui est utilisé avec le paramètre facultatif `as` mot clé donne un nom à la variable d’instance, ou auto-identificateur, qui peut être utilisé dans la définition de type pour faire référence à l’instance du type. Pour plus d’informations, consultez la section auto-identificateurs plus loin dans cette rubrique.

Les mots clés `class` et `end` qui marquent le début et fin de la définition sont facultatifs.

Types mutuellement récursifs, qui sont des types qui se référencent mutuellement, sont joints avec le `and` mot clé simplement comme mutuellement fonctions récursives. Pour obtenir un exemple, consultez la section Types mutuellement récursifs.

## <a name="constructors"></a>Constructeurs

Le constructeur est un code qui crée une instance du type classe. Constructeurs des classes fonctionnent un peu différemment dans F # que dans d’autres langages .NET. Dans une classe F #, il y a toujours un constructeur principal dont les arguments sont décrits dans le `parameter-list` qui suit le nom de type, et dont le corps se compose de la `let` (et `let rec`) liaisons au début de la déclaration de classe et le `do`liaisons qui suivent. Les arguments du constructeur principal sont dans la portée dans l’ensemble de la déclaration de classe.

Vous pouvez ajouter des constructeurs supplémentaires en utilisant le `new` mot clé pour ajouter un membre, comme suit :

`new`(`argument-list`) = `constructor-body`

Le corps du nouveau constructeur doit appeler le constructeur principal qui est spécifié en haut de la déclaration de classe.

L’exemple suivant illustre ce concept. Dans le code suivant, `MyClass` a deux constructeurs : un constructeur principal qui prend deux arguments et un autre constructeur qui n’accepte aucun argument.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2401.fs)]

## <a name="let-and-do-bindings"></a>Let et liaisons do

Le `let` et `do` liaisons dans une définition de classe forment le corps du constructeur de classe principal, et par conséquent, elles s’exécutent chaque fois qu’une instance de classe est créée. Si un `let` liaison est une fonction, il est compilé dans un membre. Si le `let` liaison est une valeur qui n’est pas utilisée dans une fonction ou un membre, il est compilé dans une variable qui est locale au constructeur. Sinon, il est compilé dans un champ de la classe. Le `do` expressions qui suivent sont compilées dans le constructeur principal et d’exécuter du code d’initialisation pour chaque instance. Étant donné que les constructeurs supplémentaires toujours appellent le constructeur principal, le `let` liaisons et `do` s’exécutent toujours quel que soit le constructeur est appelé.

Les champs qui sont créés par `let` liaisons sont accessibles dans les méthodes et propriétés de la classe ; Toutefois, ils ne sont pas accessibles à partir de méthodes statiques, même si les méthodes statiques prennent une variable d’instance en tant que paramètre. Ils ne sont pas accessibles à l’aide de l’auto-identificateur, s’il en existe.

## <a name="self-identifiers"></a>Auto-identificateurs

Un *auto-identificateur* est un nom qui représente l’instance actuelle. Auto-identificateurs ressembler à la `this` mot clé en c# ou C++ ou `Me` dans Visual Basic. Vous pouvez définir un auto-identificateur de deux manières différentes, selon que vous souhaitez l’auto-identificateur pour être dans la portée pour la définition de classe entière ou simplement pour une méthode individuelle.

Pour définir un auto-identificateur pour la classe entière, utilisez le `as` mot clé après la parenthèse fermante du paramètre de constructeur de liste et spécifiez le nom d’identificateur.

Pour définir un auto-identificateur pour qu’une seule méthode, indiquez l’auto-identificateur dans la déclaration de membre, juste avant le nom de méthode et un point (.) comme séparateur.

L’exemple de code suivant illustre les deux façons de créer un identificateur personnel. Dans la première ligne, le `as` mot clé est utilisé pour définir l’auto-identificateur. Dans la cinquième ligne, l’identificateur `this` est utilisé pour définir un auto-identificateur dont la portée est limitée à la méthode `PrintMessage`.

```fsharp
type MyClass2(dataIn) as self =
    let data = dataIn
    do
        self.PrintMessage()
    member this.PrintMessage() =
        printf "Creating MyClass2 with Data %d" data
```

Contrairement à d’autres langages .NET, vous pouvez nommer l’auto-identificateur comme vous le souhaitez ; vous n’êtes pas limité aux noms tels que `self`, `Me`, ou `this`.

L’auto-identificateur qui est déclaré avec le `as` mot clé n’est pas initialisée tant qu’après le `let` liaisons sont exécutées. Par conséquent, il ne peut pas être utilisé dans le `let` liaisons. Vous pouvez utiliser l’auto-identificateur dans la `do` section des liaisons.

## <a name="generic-type-parameters"></a>Paramètres de type générique

Paramètres de type générique sont spécifiés dans les crochets pointus (`<` et `>`), sous la forme d’un guillemet simple suivi d’un identificateur. Plusieurs paramètres de type générique sont séparés par des virgules. Le paramètre de type générique est dans l’étendue tout au long de la déclaration. L’exemple de code suivant montre comment spécifier des paramètres de type générique.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2403.fs)]

Arguments de type sont déduits lorsque le type est utilisé. Dans le code suivant, le type déduit est une séquence de tuples.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet24031.fs)]

## <a name="specifying-inheritance"></a>Spécification de l’héritage

Le `inherit` clause identifie la classe de base directe, le cas échéant. En F #, qu’une seule classe de base directe est autorisée. Les interfaces qu’une classe implémente ne sont pas considérés comme des classes de base. Interfaces sont traitées dans le [Interfaces](Interfaces.md) rubrique.

Vous pouvez accéder aux méthodes et propriétés de la classe de base à partir de la classe dérivée à l’aide du mot clé du langage `base` comme identificateur, suivi par un point (.) et le nom du membre.

Pour plus d’informations, consultez [Héritage](inheritance.md).

## <a name="members-section"></a>Section de membres

Dans cette section, vous pouvez définir statique ou méthodes d’instance, propriétés, les implémentations d’interface, membres abstraits, déclarations d’événement et des constructeurs supplémentaires. Let et effectuent des liaisons ne peut pas apparaître dans cette section. Étant donné que les membres peuvent être ajoutés à un large éventail de types F # en plus des classes, ils sont traités dans une rubrique distincte, [membres](members/index.md).

## <a name="mutually-recursive-types"></a>Types mutuellement récursifs

Lorsque vous définissez des types qui se référencent mutuellement de façon circulaire, vous associer les définitions de type à l’aide de la `and` mot clé. Le `and` mot clé remplace le `type` mot clé sur tous sauf la première définition, comme suit.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2404.fs)]

La sortie est une liste de tous les fichiers dans le répertoire actif.

## <a name="when-to-use-classes-unions-records-and-structures"></a>Quand utiliser des Classes, des Unions, des enregistrements et des Structures

Étant donné la diversité des types disponibles, vous devez avoir une bonne compréhension de ce que chaque type est conçu pour sélectionner le type approprié pour une situation particulière. Classes sont conçues pour une utilisation dans des contextes de programmation orientée objet. Programmation orientée objet est le paradigme dominant utilisé dans les applications écrites pour le .NET Framework. Si votre code F # doit travailler en étroite collaboration avec le .NET Framework ou une autre bibliothèque orientée objet, et en particulier si vous avez besoin d’étendre à partir d’un système type orienté objet tel qu’une bibliothèque d’interface utilisateur, les classes sont probablement appropriés.

Si vous n’interagissez pas étroitement avec code orienté objet, ou si vous écrivez du code qui est autonome et par conséquent protégés de l’interaction fréquente avec code orienté objet, vous devez envisager d’utiliser des enregistrements et des unions discriminées. Un seul, bien pensée – hors union discriminée, ainsi que du code, de correspondance au modèle approprié peut souvent être utilisée comme une alternative plus simple à une hiérarchie d’objets. Pour plus d’informations sur les unions discriminées, consultez [Unions discriminées](discriminated-unions.md).

Enregistrements ont l’avantage d’être plus simple que les classes, mais les enregistrements ne sont pas appropriées lorsque les demandes d’un type dépassent ce qui peut être effectué avec leur simplicité. Les enregistrements sont essentiellement des agrégats simples de valeurs, sans constructeurs distincts qui peuvent effectuer des actions personnalisées, sans champs masqués et sans implémentations d’héritage ou d’interface. Bien que les membres tels que les propriétés et méthodes peuvent être ajoutés aux enregistrements pour rendre leur comportement plus complexe, les champs stockés dans un enregistrement existe toujours un agrégat simple de valeurs. Pour plus d’informations à propos des enregistrements, consultez [enregistrements](records.md).

Structures sont également utiles pour les petits volumes de données, mais elles diffèrent à partir des classes et des enregistrements qu’elles sont des types valeur .NET. Classes et les enregistrements sont des types référence. La sémantique des types valeur et types référence est différente dans la mesure où les types valeur sont passés par valeur. Cela signifie qu’ils sont copiés bit par bit lorsqu’ils sont passés en tant que paramètre ou retournés à partir d’une fonction. Ils sont également stockés sur la pile ou, s’ils sont utilisés en tant que champ, incorporé à l’intérieur de l’objet parent au lieu de dans leur propre emplacement distinct sur le tas. Par conséquent, les structures sont appropriées pour les données fréquemment utilisées lors de la surcharge de l’accès à du tas est un problème. Pour plus d’informations sur les structures, consultez [Structures](structures.md).

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Membres](members/index.md)
- [Héritage](inheritance.md)
- [Interfaces](interfaces.md)
