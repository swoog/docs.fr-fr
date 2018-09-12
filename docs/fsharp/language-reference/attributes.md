---
title: Attributs (F#)
description: 'Découvrez comment F # attributs activer les métadonnées à appliquer à une construction de programmation.'
ms.date: 05/16/2016
ms.openlocfilehash: 3e7f1d0ff383e1070b3db72e633f80ea37150548
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44494302"
---
# <a name="attributes"></a>Attributs

Attributs activent les métadonnées à appliquer à une construction de programmation.

## <a name="syntax"></a>Syntaxe

```fsharp
[<target:attribute-name(arguments)>]
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, le *cible* est facultatif et, s’il est présent, spécifie le type d’entité de programme qui l’attribut s’applique à. Les valeurs valides pour *cible* figurent dans le tableau situé plus loin dans ce document.

Le *nom de l’attribut* fait référence au nom (éventuellement qualifié avec des espaces de noms) d’un type d’attribut valide, avec ou sans le suffixe `Attribute` qui est généralement utilisé dans les noms de type d’attribut. Par exemple, le type `ObsoleteAttribute` peut être abrégé en `Obsolete` dans ce contexte.

Le *arguments* sont les arguments au constructeur pour le type d’attribut. Si un attribut possède un constructeur par défaut, la liste d’arguments et les parenthèses peuvent être omis. Attributs prennent en charge les arguments positionnels et des arguments nommés. *Arguments de position* sont des arguments qui sont utilisés dans l’ordre dans lequel ils apparaissent. Arguments nommés peuvent être utilisés si l’attribut a des propriétés publiques. Vous pouvez les définir à l’aide de la syntaxe suivante dans la liste d’arguments.

```
*property-name* = *property-value*
```

Ces initialisations de propriété peuvent être dans n’importe quel ordre, mais ils doivent suivre les arguments positionnels. Voici un exemple d’un attribut qui utilise des arguments positionnels et des initialisations de propriété.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6202.fs)]

Dans cet exemple, l’attribut est `DllImportAttribute`, utilisé ici sous forme abrégée. Le premier argument est un paramètre positionnel et le second est une propriété.

Les attributs sont une construction de programmation .NET qui permet à un objet appelé un *attribut* à associer à un type ou un autre élément de programme. L’élément de programme auquel un attribut est appliqué est appelé le *cible de l’attribut*. L’attribut contient généralement des métadonnées sur sa cible. Dans ce contexte, les métadonnées peuvent être des données sur le type autre que les champs et leurs membres.

Attributs en F # peuvent être appliqués pour les constructions de programmation suivantes : fonctions, méthodes, assemblys, modules, types (classes, enregistrements, structures, interfaces, délégués, énumérations, unions et ainsi de suite), constructeurs, propriétés, champs, paramètres, paramètres de type et les valeurs de retour. Les attributs ne sont pas autorisées sur `let` liaisons à l’intérieur des classes, des expressions ou des expressions de flux de travail.

En règle générale, la déclaration d’attribut apparaît directement avant la déclaration de l’attribut cible. Plusieurs déclarations d’attribut peuvent être utilisées ensemble, comme suit.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6603.fs)]

Vous pouvez interroger les attributs au moment de l’exécution en utilisant la réflexion .NET.

Vous pouvez déclarer plusieurs attributs individuellement, comme dans l’exemple de code précédent, ou vous pouvez les déclarer dans un jeu de crochets si vous utilisez un point-virgule pour séparer les différents attributs et les constructeurs, comme illustré ici.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6604.fs)]

Attributs généralement rencontrés incluent le `Obsolete` attribut, les attributs en matière de sécurité, les attributs de prise en charge COM, les attributs qui se rapportent à la propriété de code et les attributs indiquant si un type peut être sérialisé. L’exemple suivant illustre l’utilisation de la `Obsolete` attribut.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6605.fs)]

Pour les cibles d’attribut `assembly` et `module`, vous appliquez les attributs à un niveau supérieur `do` liaison dans votre assembly. Vous pouvez inclure le mot `assembly` ou `module` dans la déclaration d’attribut, comme suit.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6606.fs)]

Si vous omettez la cible d’attribut pour un attribut appliqué à un `do` de liaison, le compilateur F # tente de déterminer la cible d’attribut qui a du sens pour cet attribut. Plusieurs classes d’attributs ont un attribut de type `System.AttributeUsageAttribute` qui inclut des informations sur les cibles possibles prises en charge pour cet attribut. Si le `System.AttributeUsageAttribute` indique que l’attribut prend en charge les fonctions en tant que cibles, l’attribut est pris à appliquer au point d’entrée principal du programme. Si le `System.AttributeUsageAttribute` indique que l’attribut prend en charge les assemblys en tant que cibles, le compilateur prend l’attribut à appliquer à l’assembly. La plupart des attributs ne s’appliquent pas aux fonctions et assemblys, mais dans les cas où ils le font, l’attribut est effectuée à appliquer à la fonction principale du programme. Si la cible d’attribut est spécifiée explicitement, l’attribut est appliqué à la cible spécifiée.

Bien que vous n’avez généralement pas besoin de spécifier l’attribut cible explicitement, les valeurs valides pour *cible* dans un attribut sont affichés dans le tableau ci-dessous, ainsi que des exemples d’utilisation.

<table>
  <tr>
    <th>Cible d’attribut</td>
    <th>Exemple</td> 
  </tr>
  <tr>
    <td>assembly</td>
    <td>`[<assembly: AssemblyVersionAttribute("1.0.0.0")>]`</td> 
  </tr>
  <tr>
    <td>return</td>
    <td>' fonction1 permettent de x : [<return: Obsolete>] int = x + 1'</td> 
  </tr>
  <tr>
    <td>champ</td>
    <td>« [<field: DefaultValue>] x: int mutable val »</td> 
  </tr>
  <tr>
    <td>propriété</td>
    <td>' [<property: Obsolete>] cela. MyProperty = x'</td> 
  </tr>
  <tr>
    <td>param</td>
    <td>' membre cela. MyMethod ([<param: Out>] x : ref<int>) = x : = 10'</td> 
  </tr>
  <tr>
    <td>type</td>
    <td>
        ```
        [<type: StructLayout(Sequential)>] tapez MyStruct = struct x : y de l’octet : int fin ```
    </td> 
  </tr>
</table>

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
