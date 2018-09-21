---
title: Implémentation d’IEnumerable en Visual Basic
ms.date: 07/31/2018
helpviewer_keywords:
- control flow [Visual Basic]
- enumerable interfaces
- loop structures [Visual Basic], optimizing performance
- control flow [Visual Basic]
ms.assetid: c60d7589-51f2-4463-a2d5-22506bbc1554
ms.openlocfilehash: be2eefdc52d38df3071d457b7a71dbac6eaa2657
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46525498"
---
# <a name="walkthrough-implementing-ienumerableof-t-in-visual-basic"></a>Procédure pas à pas : implémentation d'IEnumerable(Of T) en Visual Basic
Le <xref:System.Collections.Generic.IEnumerable%601> interface est implémentée par les classes qui peuvent retourner une séquence de valeurs élément par élément à la fois. L’avantage de retourner des données d’un élément à la fois est que vous n’êtes pas obligé de charger l’ensemble complet des données en mémoire pour l’utiliser. Vous devez uniquement utiliser une mémoire suffisante pour charger un élément unique à partir des données. Classes qui implémentent le `IEnumerable(T)` interface peut être utilisée avec `For Each` boucles ou des requêtes LINQ.  
  
 Par exemple, considérez une application qui doit lire un fichier texte volumineux et retourner chaque ligne du fichier qui correspond aux critères de recherche spécifique. L’application utilise une requête LINQ pour retourner des lignes à partir du fichier qui correspondent aux critères spécifiés. Pour interroger le contenu du fichier à l’aide d’une requête LINQ, l’application pourrait charger le contenu du fichier dans un tableau ou une collection. Toutefois, le chargement de la totalité du fichier dans un tableau ou une collection consommerait beaucoup plus de mémoire que nécessaire. La requête LINQ pourrait à la place interroger le contenu du fichier en utilisant une classe enumerable, en retournant uniquement les valeurs qui correspondent aux critères de recherche. Requêtes qui retournent uniquement quelques valeurs correspondantes consomme beaucoup moins de mémoire.  
  
 Vous pouvez créer une classe qui implémente le <xref:System.Collections.Generic.IEnumerable%601> interface à exposer des données sources comme données énumérables. Votre classe qui implémente le `IEnumerable(T)` interface nécessitera une autre classe qui implémente le <xref:System.Collections.Generic.IEnumerator%601> interface pour itérer la source de données. Ces deux classes permettent de retourner séquentiellement comme un type spécifique des éléments de données.  
  
 Dans cette procédure pas à pas, vous allez créer une classe qui implémente le `IEnumerable(Of String)` interface et une classe qui implémente le `IEnumerator(Of String)` interface pour lire une fichier texte une ligne à la fois.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
## <a name="creating-the-enumerable-class"></a>Création de la classe Enumerable  
  
**Créer le projet de la classe enumerable**

1.  En Visual Basic, sur le **fichier** menu, pointez sur **New** puis cliquez sur **projet**.

1.  Dans la boîte de dialogue **Nouveau projet**, dans le volet **Types de projets**, vérifiez que **Windows** est sélectionné. Sélectionnez **Bibliothèque de classes** dans le volet **Modèles**. Dans la zone **Nom**, tapez `StreamReaderEnumerable`, puis cliquez sur **OK**. Le nouveau projet s’affiche.

1.  Dans **l’Explorateur de solutions**, cliquez sur le fichier Class1.vb et cliquez sur **renommer**. Renommez le fichier `StreamReaderEnumerable.vb` et appuyez sur Entrée. Quand vous renommez le fichier, la classe est également renommée `StreamReaderEnumerable`. Cette classe va implémenter l’interface `IEnumerable(Of String)`.

1.  Cliquez sur le projet StreamReaderEnumerable, pointez sur **ajouter**, puis cliquez sur **un nouvel élément**. Sélectionnez le **classe** modèle. Dans le **nom** , tapez `StreamReaderEnumerator.vb` et cliquez sur **OK**.

 La première classe dans ce projet est la classe enumerable et implémentera le `IEnumerable(Of String)` interface. Cette interface générique implémente le <xref:System.Collections.IEnumerable> interface et garantit que les consommateurs de cette classe peuvent accéder aux valeurs de type `String`.  
  
**Ajoutez le code pour implémenter IEnumerable**

1. Ouvrez le fichier StreamReaderEnumerable.vb.

2. Sur la ligne après `Public Class StreamReaderEnumerable`, tapez la commande suivante et appuyez sur ENTRÉE.

   [!code-vb[VbVbalrIteratorWalkthrough#1](../../../../visual-basic/programming-guide/language-features/control-flow/codesnippet/VisualBasic/walkthrough-implementing-ienumerable-of-t_1.vb)]

   Visual Basic remplit automatiquement la classe avec les membres qui sont requis par le `IEnumerable(Of String)` interface.
  
3. Cette classe énumérable lira les lignes à partir d’une fichier texte une ligne à la fois. Ajoutez le code suivant à la classe pour exposer un constructeur public qui prend un chemin d’accès de fichier comme paramètre d’entrée.

   [!code-vb[VbVbalrIteratorWalkthrough#2](../../../../visual-basic/programming-guide/language-features/control-flow/codesnippet/VisualBasic/walkthrough-implementing-ienumerable-of-t_2.vb)]

4. Votre implémentation de la <xref:System.Collections.Generic.IEnumerable%601.GetEnumerator%2A> méthode de la `IEnumerable(Of String)` interface retourne une nouvelle instance de la `StreamReaderEnumerator` classe. L’implémentation de la `GetEnumerator` méthode de la `IEnumerable` interface peut devenir `Private`, car vous devez exposer uniquement les membres de la `IEnumerable(Of String)` interface. Remplacez le code généré par Visual Basic pour le `GetEnumerator` méthodes avec le code suivant.

   [!code-vb[VbVbalrIteratorWalkthrough#3](../../../../visual-basic/programming-guide/language-features/control-flow/codesnippet/VisualBasic/walkthrough-implementing-ienumerable-of-t_3.vb)]  
  
**Ajoutez le code pour implémenter IEnumerator**

1. Ouvrez le fichier StreamReaderEnumerator.vb.

2. Sur la ligne après `Public Class StreamReaderEnumerator`, tapez la commande suivante et appuyez sur ENTRÉE.

   [!code-vb[VbVbalrIteratorWalkthrough#4](../../../../visual-basic/programming-guide/language-features/control-flow/codesnippet/VisualBasic/walkthrough-implementing-ienumerable-of-t_4.vb)]

   Visual Basic remplit automatiquement la classe avec les membres qui sont requis par le `IEnumerator(Of String)` interface.

3. La classe d’énumérateur ouvre le fichier texte et exécute le fichier d’e/s pour lire les lignes à partir du fichier. Ajoutez le code suivant à la classe pour exposer un constructeur public qui prend un chemin d’accès de fichier comme paramètre d’entrée et ouvrez le fichier texte pour la lecture.

   [!code-vb[VbVbalrIteratorWalkthrough#5](../../../../visual-basic/programming-guide/language-features/control-flow/codesnippet/VisualBasic/walkthrough-implementing-ienumerable-of-t_5.vb)]

4. Le `Current` propriétés à la fois pour le `IEnumerator(Of String)` et `IEnumerator` interfaces retournent l’élément actuel à partir du fichier texte comme un `String`. L’implémentation de la `Current` propriété de la `IEnumerator` interface peut devenir `Private`, car vous devez exposer uniquement les membres de la `IEnumerator(Of String)` interface. Remplacez le code généré par Visual Basic pour le `Current` propriétés avec le code suivant.

   [!code-vb[VbVbalrIteratorWalkthrough#6](../../../../visual-basic/programming-guide/language-features/control-flow/codesnippet/VisualBasic/walkthrough-implementing-ienumerable-of-t_6.vb)]

5. Le `MoveNext` méthode de la `IEnumerator` interface accède à l’élément suivant dans le fichier texte et met à jour la valeur retournée par la `Current` propriété. S’il en existe aucun élément à lire, le `MoveNext` retourne de la méthode `False`; sinon la `MoveNext` retourne de la méthode `True`. Ajoutez le code suivant à la méthode `MoveNext` .

   [!code-vb[VbVbalrIteratorWalkthrough#7](../../../../visual-basic/programming-guide/language-features/control-flow/codesnippet/VisualBasic/walkthrough-implementing-ienumerable-of-t_7.vb)]

6. Le `Reset` méthode de la `IEnumerator` interface ordonne à l’itérateur pour pointer vers le début du fichier texte et efface la valeur de l’élément actuel. Ajoutez le code suivant à la méthode `Reset` .

   [!code-vb[VbVbalrIteratorWalkthrough#8](../../../../visual-basic/programming-guide/language-features/control-flow/codesnippet/VisualBasic/walkthrough-implementing-ienumerable-of-t_8.vb)]

7. Le `Dispose` méthode de la `IEnumerator` interface garantit que toutes les ressources non managées sont libérées avant la destruction de l’itérateur. Le handle de fichier qui est utilisé par le `StreamReader` objet est une ressource non managée et doit être fermé avant la destruction de l’instance de l’itérateur. Remplacez le code généré par Visual Basic pour le `Dispose` méthode avec le code suivant.

   [!code-vb[VbVbalrIteratorWalkthrough#9](../../../../visual-basic/programming-guide/language-features/control-flow/codesnippet/VisualBasic/walkthrough-implementing-ienumerable-of-t_9.vb)] 
  
## <a name="using-the-sample-iterator"></a>À l’aide de l’itérateur d’exemple

 Vous pouvez utiliser une classe énumérable dans votre code avec des structures de contrôle qui nécessitent un objet qui implémente `IEnumerable`, comme un `For Next` boucle ou une requête LINQ. L’exemple suivant montre le `StreamReaderEnumerable` dans une requête LINQ.  
  
 [!code-vb[VbVbalrIteratorWalkthrough#10](../../../../visual-basic/programming-guide/language-features/control-flow/codesnippet/VisualBasic/walkthrough-implementing-ienumerable-of-t_10.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Introduction à LINQ en Visual Basic](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [Flux de contrôle](../../../../visual-basic/programming-guide/language-features/control-flow/index.md)  
 [Structures de boucle](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)  
 [For Each...Next (instruction)](../../../../visual-basic/language-reference/statements/for-each-next-statement.md)
