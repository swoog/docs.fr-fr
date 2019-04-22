---
title: Types anonymes (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.AnonymousType
helpviewer_keywords:
- anonymous types [Visual Basic], about anonymous types
- anonymous types [Visual Basic]
- types [Visual Basic], anonymous
ms.assetid: 7b87532c-4b3e-4398-8503-6ea9d67574a4
ms.openlocfilehash: 3dc2083e5b4fd06250a1387c32f0eba28e879b30
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58829133"
---
# <a name="anonymous-types-visual-basic"></a>Types anonymes (Visual Basic)
Visual Basic prend en charge les types anonymes, qui vous permettent de créer des objets sans écrire de définition de classe pour le type de données. À la place, le compilateur se charge de générer une classe. La classe n’a aucun nom utilisable, hérite directement de <xref:System.Object>et contient les propriétés que vous spécifiez dans la déclaration de l’objet. Étant donné que le nom du type de données n’est pas spécifié, il est appelé un *type anonyme*.  
  
 L’exemple suivant déclare et crée la variable `product` en tant qu’instance d’un type anonyme qui a deux propriétés, `Name` et `Price`.  
  
 [!code-vb[VbVbalrAnonymousTypes#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class1.vb#1)]  
  
 Un *expression de requête* utilise des types anonymes pour combiner des colonnes de données sélectionnées par une requête. Vous ne pouvez pas définir le type du résultat à l’avance, car vous ne pouvez pas prédire les colonnes de qu'une requête particulière. Les types anonymes permettent d’écrire une requête qui sélectionne n’importe quel nombre de colonnes, dans n’importe quel ordre. Le compilateur crée un type de données qui correspond aux propriétés spécifiées et l’ordre spécifié.  
  
 Dans les exemples suivants, `products` est une liste d’objets de produit, chacun d’eux a de nombreuses propriétés. Variable `namePriceQuery` contient la définition d’une requête qui, lorsqu’elle est exécutée, retourne une collection d’instances d’un type anonyme qui a deux propriétés, `Name` et `Price`.  
  
 [!code-vb[VbVbalrAnonymousTypes#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class1.vb#2)]  
  
 Variable `nameQuantityQuery` contient la définition d’une requête qui, lorsqu’elle est exécutée, retourne une collection d’instances d’un type anonyme qui a deux propriétés, `Name` et `OnHand`.  
  
 [!code-vb[VbVbalrAnonymousTypes#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class1.vb#3)]  
  
 Pour plus d’informations sur le code créé par le compilateur pour un type anonyme, consultez [définition de Type anonyme](../../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-type-definition.md).  
  
> [!CAUTION]
>  Le nom du type anonyme est compilateur généré et peut varier de la compilation pour la compilation. Votre code ne doit pas utiliser ou repose sur le nom d’un type anonyme, car le nom peut changer lorsqu’un projet est recompilé.  
  
## <a name="declaring-an-anonymous-type"></a>Déclaration d’un Type anonyme  
 La déclaration d’une instance d’un type anonyme utilise une liste d’initialiseurs pour spécifier les propriétés du type. Vous pouvez spécifier uniquement des propriétés lorsque vous déclarez un type anonyme, pas autres éléments de classe tels que les méthodes ou événements. Dans l’exemple suivant, `product1` est une instance d’un type anonyme qui a deux propriétés : `Name` et `Price`.  
  
 [!code-vb[VbVbalrAnonymousTypes#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class1.vb#4)]  
  
 Si vous désignez des propriétés comme propriétés de clé, vous pouvez les utiliser pour comparer deux instances de type anonyme pour l’égalité. Toutefois, les valeurs des propriétés de clé ne peut pas être modifiés. Consultez la section Propriétés de clé plus loin dans cette rubrique pour plus d’informations.  
  
 Notez que la déclaration d’une instance d’un type anonyme est comme la déclaration d’une instance d’un type nommé à l’aide d’un initialiseur d’objet :  
  
 [!code-vb[VbVbalrAnonymousTypes#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class1.vb#5)]  
  
 Pour plus d’informations sur les autres façons de spécifier les propriétés de type anonyme, consultez [Comment : Déduire les Types dans les déclarations de types anonymes et les noms de propriété](../../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md).  
  
## <a name="key-properties"></a>Propriétés de clé  
 Propriétés de clé diffèrent des propriétés non-clé de plusieurs façons fondamentales :  
  
-   Seules les valeurs des propriétés de clé sont comparées afin de déterminer si deux instances sont égales.  
  
-   Les valeurs des propriétés de clé sont en lecture seule et ne peut pas être modifiés.  
  
-   Uniquement les valeurs de propriété de clé sont incluses dans l’algorithme de code de hachage généré par le compilateur pour un type anonyme.  
  
### <a name="equality"></a>Égalité  
 Instances de types anonymes peuvent être égales uniquement si elles sont des instances du même type anonyme. Le compilateur traite deux instances comme instances du même type s’ils répondent aux conditions suivantes :  
  
-   Ils sont déclarés dans le même assembly.  
  
-   Leurs propriétés ont les mêmes noms, les mêmes types déduits et sont déclarées dans le même ordre. Les comparaisons de noms ne respectent pas la casse.  
  
-   Les mêmes propriétés dans chacun sont marquées comme propriétés de clé.  
  
-   Au moins une propriété dans chaque déclaration est une propriété de clé.  
  
 Une instance d’un type anonyme qui ne possède aucune propriété de clé est uniquement égale à elle-même.  
  
 [!code-vb[VbVbalrAnonymousTypes#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class1.vb#6)]  
  
 Deux instances du même type anonyme sont égales si les valeurs de leurs propriétés de clé sont égales. Les exemples suivants illustrent la façon dont l’égalité est testée.  
  
 [!code-vb[VbVbalrAnonymousTypes#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class1.vb#7)]  
  
### <a name="read-only-values"></a>Valeurs en lecture seule  
 Les valeurs des propriétés de clé ne peut pas être modifiés. Par exemple, dans `prod8` dans l’exemple précédent, le `Name` et `Price` sont des champs `read-only`, mais `OnHand` peut être modifié.  
  
 [!code-vb[VbVbalrAnonymousTypes#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class1.vb#8)]  
  
## <a name="anonymous-types-from-query-expressions"></a>Types anonymes à partir d’Expressions de requête  
 Expressions de requête ne nécessitent pas toujours de la création de types anonymes. Lorsque cela est possible, ils utilisent un type existant pour contenir les données de colonne. Cela se produit lorsque la requête retourne des enregistrements entiers à partir de la source de données, ou qu’un seul champ de chaque enregistrement. Dans les exemples de code suivants, `customers` est une collection d’objets d’un `Customer` classe. La classe comporte plusieurs propriétés, et vous pouvez inclure une ou plusieurs d'entre eux dans le résultat de requête, dans n’importe quel ordre. Dans les deux premiers exemples, aucun des types anonymes ne sont requis, car les requêtes sélectionnent des éléments de types nommés :  
  
-   `custs1` contient une collection de chaînes, car `cust.Name` est une chaîne.  
  
     [!code-vb[VbVbalrAnonymousTypes#30](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#30)]  
  
-   `custs2` contient une collection de `Customer` objets, étant donné que chaque élément de `customers` est un `Customer` objet et l’élément entier est sélectionné par la requête.  
  
     [!code-vb[VbVbalrAnonymousTypes#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#31)]  
  
 Toutefois, les types nommés appropriés ne sont pas toujours disponibles. Vous souhaiterez peut-être sélectionner les noms des clients et des adresses pour un objectif, les numéros d’ID de client et les emplacements pour un autre et les noms des clients, les adresses et historiques de commande pour un tiers. Les types anonymes permettent de sélectionner n’importe quelle combinaison de propriétés, dans n’importe quel ordre, sans déclarer d’abord un nouveau type nommé pour contenir le résultat. Au lieu de cela, le compilateur crée un type anonyme pour chaque compilation de propriétés. La requête suivante sélectionne uniquement le nom du client et numéro d’identification à partir de chaque `Customer` dans l’objet `customers`. Par conséquent, le compilateur crée un type anonyme qui contient uniquement ces deux propriétés.  
  
 [!code-vb[VbVbalrAnonymousTYpes#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#32)]  
  
 Les noms et les types de données des propriétés du type anonyme sont effectuées à partir des arguments à `Select`, `cust.Name` et `cust.ID`. Les propriétés dans un type anonyme qui est créé par une requête sont toujours les propriétés de clé. Lorsque `custs3` est exécutée dans l’exemple suivant `For Each` boucle, le résultat est une collection d’instances d’un type anonyme avec deux propriétés de clé, `Name` et `ID`.  
  
 [!code-vb[VbVbalrAnonymousTypes#33](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#33)]  
  
 Les éléments dans la collection représentée par `custs3` sont fortement typés, et vous pouvez utiliser IntelliSense pour naviguer dans les propriétés disponibles et vérifier leurs types.  
  
 Pour plus d’informations, consultez [Introduction à LINQ en Visual Basic](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md).  
  
## <a name="deciding-whether-to-use-anonymous-types"></a>S’il faut utiliser des Types anonymes  
 Avant de créer un objet en tant qu’instance d’une classe anonyme, considérez si c’est la meilleure option. Par exemple, si vous souhaitez créer un objet temporaire pour contenir les données associées, et vous n’avez pas besoin d’autres champs et les méthodes susceptibles de contenir une classe complète, un type anonyme est une bonne solution. Les types anonymes sont également pratiques si vous souhaitez une autre sélection de propriétés pour chaque déclaration, ou si vous souhaitez modifier l’ordre des propriétés. Toutefois, si votre projet comprend plusieurs objets qui ont les mêmes propriétés, dans un ordre fixe, vous pouvez les déclarer plus facilement à l’aide d’un type nommé avec un constructeur de classe. Par exemple, avec un constructeur approprié, il est plus facile de déclarer plusieurs instances d’un `Product` classe plutôt que de déclarer plusieurs instances d’un type anonyme.  
  
 [!code-vb[VbVbalrAnonymousTypes#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class1.vb#9)]  
  
 Un autre avantage des types nommés est que le compilateur peut intercepter une erreur de frappe accidentelle d’un nom de propriété. Dans les exemples précédents, `firstProd2`, `secondProd2`, et `thirdProd2` sont destinées à être des instances du même type anonyme. Toutefois, si vous avez accidentellement déclarer `thirdProd2` dans une des manières suivantes, son type serait différent de celui du `firstProd2` et `secondProd2`.  
  
 [!code-vb[VbVbalrAnonymousTypes#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class1.vb#10)]  
  
 Plus important encore, il existe des limitations sur l’utilisation de types anonymes qui ne s’appliquent pas aux instances de types nommés. `firstProd2`, `secondProd2`, et `thirdProd2` sont des instances du même type anonyme. Toutefois, le nom du type anonyme partagé n’est pas disponible et ne peut pas apparaître dans lequel un nom de type est attendu dans votre code. Par exemple, un type anonyme ne peut pas être utilisé pour définir une signature de méthode, pour déclarer une autre variable ou champ ou dans une déclaration de type. Par conséquent, les types anonymes ne sont pas appropriés lorsque vous devez partager des informations sur les méthodes.  
  
## <a name="an-anonymous-type-definition"></a>Une définition de Type anonyme  
 En réponse à la déclaration d’une instance d’un type anonyme, le compilateur crée une nouvelle définition de classe qui contient les propriétés spécifiées.  
  
 Si le type anonyme contienne au moins une propriété de clé, la définition substitue à trois membres hérités de <xref:System.Object>: <xref:System.Object.Equals%2A>, <xref:System.Object.GetHashCode%2A>, et <xref:System.Object.ToString%2A>. Le code produit pour tester l’égalité et en déterminant que la valeur de code de hachage considère uniquement les propriétés de clé. Si le type anonyme ne contient aucune propriété de clé, uniquement <xref:System.Object.ToString%2A> est remplacée. Propriétés explicitement nommées d’un type anonyme ne peut pas entrer en conflit avec ces méthodes générées. Autrement dit, vous ne pouvez pas utiliser `.Equals`, `.GetHashCode`, ou `.ToString` à une propriété de nom.  
  
 Les définitions de type anonyme qui ont au moins une propriété de clé implémentent également le <xref:System.IEquatable%601?displayProperty=nameWithType> interface, où `T` est le type du type anonyme.  
  
 Pour plus d’informations sur le code créé par le compilateur et les fonctionnalités des méthodes substituées, consultez [définition de Type anonyme](../../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-type-definition.md).  
  
## <a name="see-also"></a>Voir aussi

- [Initialiseurs d’objets : Types nommés et anonymes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md)
- [Inférence de type local](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [Introduction à LINQ en Visual Basic](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Guide pratique pour Déduire les Types dans les déclarations de types anonymes et les noms de propriété](../../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md)
- [Définition du type anonyme](../../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-type-definition.md)
- [Key](../../../../visual-basic/language-reference/modifiers/key.md)
