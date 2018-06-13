---
title: 'Comment : écrire une boucle Parallel.ForEach avec des variables locales de thread'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- parallel foreach loop, how to use local state
ms.assetid: 24b10041-b30b-45cb-aa65-66cf568ca76d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4a89b3f25fb3d6e85c666e57f24e68c297c8c29a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33582735"
---
# <a name="how-to-write-a-parallelforeach-loop-with-thread-local-variables"></a>Comment : écrire une boucle Parallel.ForEach avec des variables locales de thread
L'exemple suivant montre comment écrire une méthode <xref:System.Threading.Tasks.Parallel.ForEach%2A> qui utilise des variables de thread local. Quand une boucle <xref:System.Threading.Tasks.Parallel.ForEach%2A> s'exécute, elle divise sa collection source en plusieurs partitions. Chaque partition obtient sa propre copie de la variable « thread local ». (Le terme « thread local » est légèrement inexact ici, car dans certains cas deux partitions peuvent s'exécuter sur le même thread.)  
  
 Le code et les paramètres dans cet exemple ressemblent beaucoup à la méthode <xref:System.Threading.Tasks.Parallel.For%2A> correspondante. Pour plus d’informations, voir [Guide pratique : écrire une boucle Parallel.For avec des variables locales de thread](../../../docs/standard/parallel-programming/how-to-write-a-parallel-for-loop-with-thread-local-variables.md).  
  
 Pour utiliser une variable de thread local dans une boucle <xref:System.Threading.Tasks.Parallel.ForEach%2A>, vous devez appeler l'une des surcharges de méthode qui accepte deux paramètres de type. Le premier paramètre de type, `TSource`, spécifie le type d'élément source, tandis que le second, `TLocal`, spécifie le type de la variable de thread local.  
  
## <a name="example"></a>Exemple  
 L'exemple suivant appelle la surcharge <xref:System.Threading.Tasks.Parallel.ForEach%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%601%7D%2CSystem.Func%7B%60%600%2CSystem.Threading.Tasks.ParallelLoopState%2C%60%601%2C%60%601%7D%2CSystem.Action%7B%60%601%7D%29?displayProperty=nameWithType> pour calculer la somme d'un tableau d'un million d'éléments. Cette surcharge possède quatre paramètres :  
  
-   `source`, qui représente la source de données. Il doit implémenter <xref:System.Collections.Generic.IEnumerable%601>. La source de données dans notre exemple est l'objet `IEnumerable<Int32>` d'un million de membres retourné par la méthode <xref:System.Linq.Enumerable.Range%2A?displayProperty=nameWithType>.  
  
-   `localInit`, fonction qui initialise la variable de thread local. Cette fonction est appelée une fois pour chaque partition dans laquelle l'opération <xref:System.Threading.Tasks.Parallel.ForEach%2A?displayProperty=nameWithType> s'exécute. Notre exemple initialise la variable de thread local à zéro.  
  
-   `body`, <xref:System.Func%604> appelé par la boucle parallèle sur chaque itération de la boucle. Sa signature est `Func\<TSource, ParallelLoopState, TLocal, TLocal>`. Vous fournissez le code pour le délégué, puis la boucle transmet les paramètres d'entrée, qui sont :  
  
    -   l'élément actuel de l'interface <xref:System.Collections.Generic.IEnumerable%601> ;  
  
    -   une variable <xref:System.Threading.Tasks.ParallelLoopState> que vous pouvez utiliser dans le code de votre délégué pour examiner l'état de la boucle ;  
  
    -   la variable de thread local.  
  
     Votre délégué retourne la variable de thread local, qui est ensuite transmise à la prochaine itération de la boucle qui s'exécute dans la partition concernée. Chaque partition de boucle tient à jour une instance distincte de cette variable.  
  
     Dans l'exemple, le délégué ajoute la valeur de chaque entier à la variable de thread local, qui tient à jour le total cumulé des valeurs des éléments d'entiers dans la partition concernée.  
  
-   `localFinally`, délégué `Action<TLocal>` que la méthode <xref:System.Threading.Tasks.Parallel.ForEach%2A?displayProperty=nameWithType> appelle quand les opérations de bouclage dans chaque partition sont terminées. La méthode <xref:System.Threading.Tasks.Parallel.ForEach%2A?displayProperty=nameWithType> transmet à votre délégué `Action<TLocal>` la valeur finale de la variable de thread local pour le thread concerné (ou partition de boucle), et vous fournissez le code qui prend en charge la combinaison du résultat de cette partition avec les résultats des autres partitions. Ce délégué peut être appelé simultanément par plusieurs tâches. C'est la raison pour laquelle l'exemple utilise la méthode <xref:System.Threading.Interlocked.Add%28System.Int32%40%2CSystem.Int32%29?displayProperty=nameWithType> pour synchroniser l'accès à la variable `total`. Comme le type de délégué est un délégué <xref:System.Action%601>, aucune valeur n'est retournée.  
  
 [!code-csharp[TPL_Parallel#04](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_parallel/cs/foreachthreadlocal.cs#04)]
 [!code-vb[TPL_Parallel#04](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_parallel/vb/foreachthreadlocal.vb#04)]  
  
## <a name="see-also"></a>Voir aussi  
 [Parallélisme de données](../../../docs/standard/parallel-programming/data-parallelism-task-parallel-library.md)  
 [Guide pratique : écrire une boucle Parallel.For avec des variables locales de thread](../../../docs/standard/parallel-programming/how-to-write-a-parallel-for-loop-with-thread-local-variables.md)  
 [Expressions lambda en PLINQ et dans la bibliothèque parallèle de tâches](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md)
