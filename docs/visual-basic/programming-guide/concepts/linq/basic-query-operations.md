---
title: Opérations de requête de base (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- data sources [LINQ in Visual Basic]
- Join clause [LINQ in Visual Basic]
- ordering data [LINQ in Visual Basic]
- projections [LINQ in Visual Basic]
- LINQ [Visual Basic], query operations
- Order By clause [LINQ in Visual Basic]
- joining data [LINQ in Visual Basic]
- queries [LINQ in Visual Basic], basic operations
- selecting data [LINQ in Visual Basic]
- Group By clause [LINQ in Visual Basic]
- grouping data [LINQ in Visual Basic]
- Select clause [LINQ in Visual Basic]
ms.assetid: 1146f6d0-fcb8-4f4d-8223-c9db52620d21
ms.openlocfilehash: 5ca92324dec1d4fa8885a610a6e246640f4a5752
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56973026"
---
# <a name="basic-query-operations-visual-basic"></a>Opérations de requête de base (Visual Basic)
Cette rubrique fournit une brève introduction aux [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] expressions en Visual Basic et certains types d’opérations que vous effectuez dans une requête classiques. Pour plus d’informations, consultez les rubriques suivantes :  
  
 [Introduction à LINQ en Visual Basic](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
  
 [Requêtes](../../../../visual-basic/language-reference/queries/index.md)  
  
 [Procédure pas à pas : Écriture de requêtes dans Visual Basic](../../../../visual-basic/programming-guide/concepts/linq/walkthrough-writing-queries.md)  
  
## <a name="specifying-the-data-source-from"></a>Spécification de la Source de données (à partir de)  
 Dans un [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] requête, la première étape consiste à spécifier la source de données que vous souhaitez interroger. Par conséquent, le `From` clause dans une requête toujours en premier. Opérateurs de requête sélectionnent et mettre en forme le résultat en fonction du type de la source.  
  
 [!code-vb[VbLINQBasicOps#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#1)]  
  
 Le `From` clause spécifie la source de données `customers`et un *variable de portée*, `cust`. La variable de portée est comme une variable d’itération de boucle, à ceci près que dans une expression de requête, aucune itération réelle ne se produit. Lorsque la requête est exécutée, souvent à l’aide un `For Each` boucle, la variable de portée sert de référence pour chaque élément consécutif dans `customers`. Comme le compilateur déduit le type de `cust`, vous n’avez pas à le spécifier explicitement. Pour obtenir des exemples de requêtes écrites avec et sans type explicite, consultez [relations des types dans les opérations de requête (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/type-relationships-in-query-operations.md).  
  
 Pour plus d’informations sur l’utilisation de la `From` clause en Visual Basic, consultez [Clause From](../../../../visual-basic/language-reference/queries/from-clause.md).  
  
## <a name="filtering-data-where"></a>Filtrage des données (où)  
 Probablement l’opération de requête plus courante consiste à appliquer un filtre sous la forme d’une expression booléenne. Puis, la requête retourne uniquement les éléments pour lesquels l’expression est vraie. Un `Where` clause est utilisée pour effectuer le filtrage. Le filtre spécifie les éléments de la source de données à inclure dans la séquence résultante. Dans l’exemple suivant, que les clients qui ont une adresse à Londres sont inclus.  
  
 [!code-vb[VbLINQBasicOps#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#2)]  
  
 Vous pouvez utiliser des opérateurs logiques tels que `And` et `Or` pour combiner des expressions de filtre dans un `Where` clause. Par exemple, pour retourner uniquement les clients de Londres et dont le nom est Devon, utilisez le code suivant :  
  
```vb  
Where cust.City = "London" And cust.Name = "Devon"   
```  
  
 Pour retourner les clients de Londres ou Paris, utilisez le code suivant :  
  
```vb  
Where cust.City = "London" Or cust.City = "Paris"   
```  
  
 Pour plus d’informations sur l’utilisation de la `Where` clause en Visual Basic, consultez [une Clause Where](../../../../visual-basic/language-reference/queries/where-clause.md).  
  
## <a name="ordering-data-order-by"></a>Classer des données (Order By)  
 Il est souvent utile de trier les données retournées dans un ordre particulier. Le `Order By` clause triera les éléments de la séquence retournée à trier sur un ou plusieurs champs spécifiés. Par exemple, la requête suivante trie les résultats selon la `Name` propriété. Étant donné que `Name` est une chaîne, les données retournées seront triées par ordre alphabétique, de A à Z.  
  
 [!code-vb[VbLINQBasicOps#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#3)]  
  
 Pour trier les résultats dans l’ordre inverse, de Z à A, utilisez la clause `Order By...Descending`. La valeur par défaut est `Ascending` lorsque ni `Ascending` ni `Descending` est spécifié.  
  
 Pour plus d’informations sur l’utilisation de la `Order By` clause en Visual Basic, consultez [Clause Order By](../../../../visual-basic/language-reference/queries/order-by-clause.md).  
  
## <a name="selecting-data-select"></a>Sélection de données (Select)  
 Le `Select` clause spécifie la forme et le contenu des éléments retournés. Par exemple, vous pouvez spécifier si vos résultats comprendra complète `Customer` d’objets, seul `Customer` propriété, un sous-ensemble de propriétés, une combinaison de propriétés à partir de diverses sources de données ou un nouveau type de résultat basé sur un calcul. Quand la clause `Select` produit autre chose qu’une copie de l’élément source, l’opération est appelée *projection*.  
  
 Pour récupérer une collection qui se compose de complet `Customer` objets, sélectionnez la variable de portée elle-même :  
  
 [!code-vb[VbLINQBasicOps#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#4)]  
  
 Si un `Customer` instance est un objet qui compte de nombreux champs, et tout ce que vous souhaitez récupérer est le nom, vous pouvez sélectionner `cust.Name`, comme illustré dans l’exemple suivant. Inférence de type local reconnaît que cela modifie le type de résultat d’une collection de `Customer` objets à une collection de chaînes.  
  
 [!code-vb[VbLINQBasicOps#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#5)]  
  
 Pour sélectionner plusieurs champs à partir de la source de données, vous avez deux possibilités :  
  
-   Dans le `Select` clause, spécifiez les champs que vous souhaitez inclure dans le résultat. Le compilateur définira un type anonyme qui a ces champs en tant que ses propriétés. Pour plus d’informations, consultez [Types anonymes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md).  
  
     Étant donné que les éléments retournés dans l’exemple suivant sont des instances d’un type anonyme, vous ne pouvez pas faire référence au type par nom ailleurs dans votre code. Le nom désigné par le compilateur pour le type contient des caractères qui ne sont pas valides dans du code Visual Basic normal. Dans l’exemple suivant, les éléments dans la collection retournée par la requête dans `londonCusts4` sont des instances d’un type anonyme  
  
     [!code-vb[VbLINQBasicOps#6](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/basic-query-operations_6.vb)]  
  
     ou  
  
-   Définir un type nommé qui contient les champs spécifiques que vous souhaitez inclure dans le résultat et créer et initialiser les instances du type dans le `Select` clause. Utilisez cette option uniquement si vous devez utiliser des résultats individuels en dehors de la collection dans laquelle ils sont retournés, ou si vous devez les passer en tant que paramètres dans les appels de méthode. Le type de `londonCusts5` dans l’exemple suivant est IEnumerable (Of NamePhone).  
  
     [!code-vb[VbLINQBasicOps#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#7)]  
  
     [!code-vb[VbLINQBasicOps#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#8)]  
  
 Pour plus d’informations sur l’utilisation de la `Select` clause en Visual Basic, consultez [Clause Select](../../../../visual-basic/language-reference/queries/select-clause.md).  
  
## <a name="joining-data-join-and-group-join"></a>Jointure de données (jointure et jointure groupée)  
 Vous pouvez combiner plusieurs sources de données dans le `From` clause de plusieurs façons. Par exemple, le code suivant utilise deux sources de données et associe implicitement les propriétés des deux dans le résultat. La requête sélectionne les étudiants dont le nom commence par une voyelle.  
  
 [!code-vb[VbLINQBasicOps#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#9)]  
  
> [!NOTE]
>  Vous pouvez exécuter ce code avec la liste d’étudiants créée dans [Comment : Créer une liste d’éléments](../../../../visual-basic/programming-guide/concepts/linq/how-to-create-a-list-of-items.md).  
  
 Le `Join` mot clé est équivalente à une `INNER JOIN` dans SQL. Il combine deux collections en fonction des valeurs de clés correspondantes entre les éléments dans les deux collections. La requête retourne tout ou partie des éléments de collection qui ont des valeurs de clés correspondantes. Par exemple, le code suivant reproduit l’action de la jointure implicite précédente.  
  
 [!code-vb[VbLINQBasicOps#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#10)]  
  
 `Group Join` combine des collections en une collection hiérarchique unique, comme un `LEFT JOIN` dans SQL. Pour plus d’informations, consultez [Clause Join](../../../../visual-basic/language-reference/queries/join-clause.md) et [Group Join, Clause](../../../../visual-basic/language-reference/queries/group-join-clause.md).  
  
## <a name="grouping-data-group-by"></a>Regroupement de données (Group By)  
 Vous pouvez ajouter un `Group By` clause pour regrouper les éléments dans un résultat de requête en fonction d’un ou plusieurs champs des éléments. Par exemple, le code suivant regroupe les étudiants par année de la classe.  
  
 [!code-vb[VbLINQBasicOps#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#11)]  
  
 Si vous exécutez ce code à l’aide de la liste d’étudiants créée dans [Comment : Créer une liste d’éléments](../../../../visual-basic/programming-guide/concepts/linq/how-to-create-a-list-of-items.md), la sortie de la `For Each` instruction est :  
  
 Année : « Junior »  
  
 Tucker, Michael  
  
 Garcia, Hugo  
  
 Garcia, Marie  
  
 Tucker, Lance  
  
 Année : Senior  
  
 Omelchenko, Svetlana remarque  
  
 Osada, Michiko  
  
 Fakhouri, Fadi  
  
 Feng, Hanying  
  
 Adams, Terry  
  
 Année : Freshman  
  
 Mortensen, Sven  
  
 Garcia, Cesar  
  
 La variante indiquée dans le code suivant trie les années de classe, puis trie les étudiants de chaque année par nom de famille.  
  
 [!code-vb[VbLINQBasicOps#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQBasicOps/VB/Class1.vb#12)]  
  
 Pour plus d’informations sur `Group By`, consultez [Group By Clause](../../../../visual-basic/language-reference/queries/group-by-clause.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Collections.Generic.IEnumerable%601>
- [Bien démarrer avec LINQ en Visual Basic](../../../../visual-basic/programming-guide/concepts/linq/getting-started-with-linq.md)
- [Requêtes](../../../../visual-basic/language-reference/queries/index.md)
- [Vue d’ensemble des opérateurs de requête standard (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [LINQ](../../../../visual-basic/programming-guide/language-features/linq/index.md)
