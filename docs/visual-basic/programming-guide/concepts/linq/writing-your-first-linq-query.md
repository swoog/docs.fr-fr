---
title: Écriture de votre première requête LINQ (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- queries [LINQ in Visual Basic], writing
- LINQ queries [Visual Basic]
- LINQ [Visual Basic], writing queries
ms.assetid: 4affb732-3e9b-4479-aa31-1f9bd8183cbe
ms.openlocfilehash: 4c04c00c5392d8ba363346b06c806ec79041c439
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44708528"
---
# <a name="writing-your-first-linq-query-visual-basic"></a>Écriture de votre première requête LINQ (Visual Basic)
Une *requête* est une expression qui récupère des données d’une source de données. Les requêtes sont exprimées dans un langage de requête dédié. Au fil du temps, différents langages ont été développées pour différents types de sources de données, par exemple, SQL pour les bases de données relationnelles et XQuery pour XML. Cela rend nécessaire pour le développeur d’applications à apprendre un nouveau langage de requête pour chaque type de source de données ou format de données qui est pris en charge.  
  
 [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] simplifie la situation en proposant un modèle cohérent pour l’utilisation des données entre les différents types de sources de données et formats. Dans une requête [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)], vous travaillez toujours avec des objets. Vous utilisez les mêmes modèles de codage de base pour interroger et transformer des données dans des documents XML, bases de données SQL, les jeux de données ADO.NET et entités, collections .NET Framework et n’importe quel autre source ou le format pour lequel un [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] fournisseur n’est disponible. Ce document décrit les trois phases de la création et l’utilisation de basic [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] requêtes.  
  
## <a name="three-stages-of-a-query-operation"></a>Trois phases d’une opération de requête  
 [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] opérations de requête se composent de trois actions :  
  
1.  Obtenir la source de données ou des sources.  
  
2.  Création de la requête  
  
3.  Exécution de la requête  
  
 Dans [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)], l’exécution d’une requête est distincte de la création de la requête. Vous ne récupérez pas toutes les données simplement en créant une requête. Ce point est abordé en détail plus loin dans cette rubrique.  
  
 L’exemple suivant illustre les trois parties d’une opération de requête. L’exemple utilise un tableau d’entiers comme source de données à des fins de démonstration. Toutefois, les mêmes concepts s’appliquent également à d’autres sources de données.  
  
> [!NOTE]
>  Sur le [Page Compiler, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/compile-page-project-designer-visual-basic), vérifiez que **Option infer** a la valeur **sur**.  
  
 [!code-vb[VbLINQFirstQuery#1](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/writing-your-first-linq-query_1.vb)]  
  
 Sortie :  
  
 `0 2 4 6`  
  
## <a name="the-data-source"></a>Source de données  
 Étant donné que la source de données dans l’exemple précédent est un tableau, il prend en charge implicitement générique <xref:System.Collections.Generic.IEnumerable%601> interface. Il est fait qui vous permet d’utiliser un tableau comme source de données pour un [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] requête. Les types qui prennent en charge <xref:System.Collections.Generic.IEnumerable%601> ou une interface dérivée, comme l’interface générique <xref:System.Linq.IQueryable%601>, sont appelés des *types requêtables*.  
  
 Comme un type implicitement requêtable, le tableau ne nécessite aucune modification ni traitement spécial pour servir une [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] source de données. Vaut également pour n’importe quel type de collection qui prend en charge <xref:System.Collections.Generic.IEnumerable%601>, y compris le générique <xref:System.Collections.Generic.List%601>, <xref:System.Collections.Generic.Dictionary%602>et d’autres classes dans la bibliothèque de classes .NET Framework.  
  
 Si la source de données n’implémente pas déjà <xref:System.Collections.Generic.IEnumerable%601>, un [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] fournisseur est nécessaire pour implémenter les fonctionnalités de la *opérateurs de requête standard* pour cette source de données. Par exemple, [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] gère les tâches de chargement d’un document XML dans un requêtable <xref:System.Xml.Linq.XElement> type, comme illustré dans l’exemple suivant. Pour plus d’informations sur les opérateurs de requête standard, consultez [présentation des opérateurs de requête Standard (Visual Basic)](standard-query-operators-overview.md).  
  
 [!code-vb[VbLINQFirstQuery#2](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/writing-your-first-linq-query_2.vb)]  
  
 Avec [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)], vous créez tout d’abord un mappage objet / relationnel au moment du design, manuellement ou en utilisant le [outils LINQ to SQL dans Visual Studio](/visualstudio/data-tools/linq-to-sql-tools-in-visual-studio2) dans Visual Studio. Vous écrivez vos requêtes pour des objets. Ensuite, au moment de l’exécution, [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] gère la communication avec la base de données. Dans l’exemple suivant, `customers` représente une table spécifique dans la base de données, et <xref:System.Data.Linq.Table%601> prend en charge générique <xref:System.Linq.IQueryable%601>.  
  
```vb  
' Create a data source from a SQL table.  
Dim db As New DataContext("C:\Northwind\Northwnd.mdf")  
Dim customers As Table(Of Customer) = db.GetTable(Of Customer)  
```  
  
 Pour plus d’informations sur la création de types de sources de données spécifiques, consultez la documentation relative aux différents fournisseurs [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)]. (Pour obtenir la liste de ces fournisseurs, consultez [LINQ (Language-Integrated Query)](../../../../visual-basic/programming-guide/concepts/linq/index.md).) La règle de base est simple : un [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] source de données est n’importe quel objet qui prend en charge le modèle générique <xref:System.Collections.Generic.IEnumerable%601> interface ou une interface qui hérite de celle-ci.  
  
> [!NOTE]
>  Types tels que <xref:System.Collections.ArrayList> qui prennent en charge le non générique <xref:System.Collections.IEnumerable> interface peut également être utilisée en tant que [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] des sources de données. Pour obtenir un exemple qui utilise un <xref:System.Collections.ArrayList>, consultez [Comment : interroger un ArrayList avec LINQ (Visual Basic)](how-to-query-an-arraylist-with-linq.md).  
  
## <a name="the-query"></a>La requête  
 Dans la requête, vous spécifiez les informations que vous souhaitez récupérer à partir de la source de données ou des sources. Vous avez également la possibilité de spécifier comment ces informations doivent être triées, regroupées ou structurées avant d’être retournée. Pour activer la création de requête, Visual Basic a incorporé nouvelle syntaxe de requête dans le langage.  
  
 Lorsqu’elle est exécutée, la requête dans l’exemple suivant retourne tous les nombres pairs à partir d’un tableau d’entiers, `numbers`.  
  
 [!code-vb[VbLINQFirstQuery#1](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/writing-your-first-linq-query_1.vb)]  
  
 L’expression de requête contient trois clauses : `From`, `Where`, et `Select`. La fonction spécifique et l’objectif de chaque clause d’expression de requête est abordée dans [opérations de requête de base (Visual Basic)](basic-query-operations.md). Pour plus d’informations, consultez [requêtes](../../../../visual-basic/language-reference/queries/index.md). Notez que dans [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)], une définition de requête est souvent stockée dans une variable et exécutée ultérieurement. La requête variable, comme `evensQuery` dans l’exemple précédent, doit être un type requêtable. Le type de `evensQuery` est `IEnumerable(Of Integer)`, attribué par le compilateur à l’aide de l’inférence de type local.  
  
 Il est important de se rappeler que la variable de requête n’effectue aucune action et ne retourne aucune donnée. Il stocke uniquement la définition de requête. Dans l’exemple précédent, il est le `For Each` boucle qui exécute la requête.  
  
## <a name="query-execution"></a>Exécution de la requête  
 Exécution de la requête est distincte de la création de requête. Création de requête définit la requête, mais l’exécution est déclenchée par un mécanisme différent. Une requête peut être exécutée dès qu’il est défini (*l’exécution immédiate*), ou la définition peut être stockée et la requête peut être exécutée ultérieurement (*exécution différée*).  
  
### <a name="deferred-execution"></a>Exécution différée  
 Classique [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] requête ressemble à celui de l’exemple précédent, dans lequel `evensQuery` est défini. Il crée la requête, mais sans l’exécuter immédiatement. Au lieu de cela, la définition de la requête est stockée dans la variable de requête `evensQuery`. Vous exécutez la requête ultérieurement, généralement en utilisant un `For Each` boucle, ce qui retourne une séquence de valeurs, ou en appliquant un opérateur de requête standard, tels que `Count` ou `Max`. Ce processus est appelé *exécution différée*.  
  
 [!code-vb[VbLINQFirstQuery#7](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/writing-your-first-linq-query_3.vb)]  
  
 Pour une séquence de valeurs, vous accédez aux données récupérées à l’aide de la variable d’itération dans le `For Each` boucle (`number` dans l’exemple précédent). Étant donné que la variable de requête, `evensQuery`, conserve la définition de requête plutôt que les résultats de requête, vous pouvez exécuter une requête aussi souvent que vous le souhaitez à l’aide de la variable de requête plusieurs fois. Par exemple, vous pouvez avoir une base de données dans votre application en cours de mise à jour en permanence par une application distincte. Une fois que vous avez créé une requête qui Récupère des données à partir de cette base de données, vous pouvez utiliser un `For Each` boucle pour exécuter la requête à plusieurs reprises, la récupération des données les plus récentes chaque fois.  
  
 L’exemple suivant montre comment l’exécution fonctionne. Après avoir `evensQuery2` est définie et exécutée avec un `For Each` boucle, comme dans les exemples précédents, certains éléments dans la source de données `numbers` sont modifiés. Ensuite, une deuxième `For Each` s’exécute en boucle `evensQuery2` à nouveau. Les résultats sont différents la deuxième fois, étant donné que le `For Each` boucle s’exécute la requête à nouveau, en utilisant les nouvelles valeurs dans `numbers`.  
  
 [!code-vb[VbLINQFirstQuery#3](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/writing-your-first-linq-query_4.vb)]  
  
 Sortie :  
  
 `Evens in original array:`  
  
 `0  2  4  6`  
  
 `Evens in changed array:`  
  
 `0  10  2  22  8`  
  
### <a name="immediate-execution"></a>Exécution immédiate  
 Dans l’exécution différée des requêtes, la définition de la requête est stockée dans une variable de requête pour une exécution ultérieure. Dans l’exécution immédiate, la requête est exécutée au moment de sa définition. L’exécution est déclenchée lorsque vous appliquez une méthode qui requiert l’accès aux éléments individuels du résultat de requête. Fréquence à laquelle l’exécution immédiate est forcée à l’aide d’un des opérateurs de requête standard qui retournent des valeurs uniques. Sont des exemples `Count`, `Max`, `Average`, et `First`. Ces opérateurs de requête standard exécutent la requête dès qu’ils sont appliqués pour calculer et retourner un résultat singleton. Pour plus d’informations sur les opérateurs de requête standard qui retournent des valeurs uniques, consultez [opérations d’agrégation](aggregation-operations.md), [opérations d’élément](element-operations.md), et [opérations de quantificateur](quantifier-operations.md).  
  
 La requête suivante retourne un nombre de chiffres pairs dans un tableau d’entiers. La définition de requête n’est pas enregistrée, et `numEvens` est un simple `Integer`.  
  
 [!code-vb[VbLINQFirstQuery#4](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/writing-your-first-linq-query_5.vb)]  
  
 Vous pouvez obtenir le même résultat à l’aide de la `Aggregate` (méthode).  
  
 [!code-vb[VbLINQFirstQuery#5](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/writing-your-first-linq-query_6.vb)]  
  
 Vous pouvez également forcer l’exécution d’une requête en appelant le `ToList` ou `ToArray` méthode sur une requête (immédiat) ou d’une variable de requête (différé), comme indiqué dans le code suivant.  
  
 [!code-vb[VbLINQFirstQuery#6](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/writing-your-first-linq-query_7.vb)]  
  
 Dans les exemples précédents, `evensQuery3` est une requête, mais `evensList` est une liste et `evensArray` est un tableau.  
  
 À l’aide de `ToList` ou `ToArray` pour forcer immédiatement l’exécution est particulièrement utile dans les scénarios dans lesquels vous souhaitez exécuter immédiatement la requête et mettre en cache les résultats dans un objet de collection unique. Pour plus d’informations sur ces méthodes, consultez [conversion des Types de données](converting-data-types.md).  
  
 Vous pouvez également provoquer une requête doit être exécutée à l’aide un `IEnumerable` méthode telle que la <xref:Microsoft.VisualBasic.Collection.System%23Collections%23IEnumerable%23GetEnumerator%2A> (méthode).  
  
## <a name="see-also"></a>Voir aussi

- [Bien démarrer avec LINQ en Visual Basic](getting-started-with-linq.md)  
- [Inférence de type local](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)  
- [Vue d’ensemble des opérateurs de requête standard (Visual Basic)](standard-query-operators-overview.md)  
- [Introduction à LINQ en Visual Basic](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
- [LINQ](../../../../visual-basic/programming-guide/language-features/linq/index.md)  
- [Requêtes](../../../../visual-basic/language-reference/queries/index.md)
