---
title: Join, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryJoinIn
- vb.QueryJoin
- vb.QueryJoinOn
helpviewer_keywords:
- queries [Visual Basic], Join
- Join statement [Visual Basic]
- Join clause [Visual Basic]
ms.assetid: 6dd37936-b27c-4e00-98ad-154b23f4de64
ms.openlocfilehash: 21432b95b30ae38ac2cbc9e55b5a3066f0bef665
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58825844"
---
# <a name="join-clause-visual-basic"></a>Join, clause (Visual Basic)
Combine deux collections en une collection unique. L’opération de jointure est basée sur les clés correspondantes et utilise le `Equals` opérateur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Join element In collection _  
  [ joinClause _ ]   
  [ groupJoinClause ... _ ]   
On key1 Equals key2 [ And key3 Equals key4 [... ]  
```  
  
## <a name="parts"></a>Composants  
 `element`  
 Obligatoire. La variable de contrôle pour la collection jointe.  
  
 `collection`  
 Obligatoire. La collection à combiner avec la collection identifiée sur le côté gauche de la `Join` opérateur. Un `Join` clause peut être imbriquée dans une autre `Join` clause, ou dans un `Group Join` clause.  
  
 `joinClause`  
 Optionnel. Un ou plus supplémentaires `Join` clauses pour en savoir plus affiner la requête.  
  
 `groupJoinClause`  
 Optionnel. Un ou plus supplémentaires `Group Join` clauses pour en savoir plus affiner la requête.  
  
 `key1` `Equals` `key2`  
 Obligatoire. Identifie les clés pour les collections qui sont jointes. Vous devez utiliser le `Equals` opérateur pour comparer les clés à partir des collections qui sont jointes. Vous pouvez combiner des conditions de jointure à l’aide de la `And` opérateur afin d’identifier plusieurs clés. `key1` doit être de la collection sur le côté gauche de la `Join` opérateur. `key2` doit être de la collection sur le côté droit de la `Join` opérateur.  
  
 Les clés utilisées dans la condition de jointure peuvent être des expressions incluant plusieurs éléments de la collection. Toutefois, chaque expression clé peut contenir uniquement des éléments à partir de sa collection respectif.  
  
## <a name="remarks"></a>Notes  
 Le `Join` clause combine deux collections en fonction des valeurs de clés correspondantes des collections qui sont jointes. La collection résultante peut contenir n’importe quelle combinaison de valeurs de la collection identifiée sur le côté gauche de la `Join` opérateur et la collection identifiée dans le `Join` clause. La requête retournera uniquement des résultats pour lesquels la condition spécifiée par la `Equals` opérateur est remplie. Cela équivaut à un `INNER JOIN` dans SQL.  
  
 Vous pouvez utiliser plusieurs `Join` clauses dans une requête pour joindre deux collections ou plus en une collection unique.  
  
 Vous pouvez effectuer une jointure implicite pour combiner des collections sans la `Join` clause. Pour ce faire, inclure plusieurs `In` clauses dans votre `From` clause et spécifiez un `Where` clause qui identifie les clés que vous souhaitez utiliser pour la jointure.  
  
 Vous pouvez utiliser le `Group Join` clause pour combiner des collections en une collection hiérarchique unique. Il s’agit comme un `LEFT OUTER JOIN` dans SQL.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant effectue une jointure implicite pour combiner une liste de clients avec leurs commandes.  
  
 [!code-vb[VbSimpleQuerySamples#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#13)]  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant joint deux collections à l’aide de la `Join` clause.  
  
 [!code-vb[VbSimpleQuerySamples#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples2.vb#12)]  
  
 Cet exemple produira un résultat similaire à ce qui suit :  
  
 `winlogon (968), Windows Logon`  
  
 `explorer (2424), File Explorer`  
  
 `cmd (5136), Command Window`  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant joint deux collections à l’aide de la `Join` clause avec deux colonnes clés.  
  
 [!code-vb[VbSimpleQuerySamples#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples3.vb#17)]  
  
 L’exemple de sortie produite est semblable à ce qui suit :  
  
 `winlogon (968), Windows Logon, Priority = 13`  
  
 `cmd (700), Command Window, Priority = 8`  
  
 `explorer (2424), File Explorer, Priority = 8`  
  
## <a name="see-also"></a>Voir aussi

- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Requêtes](../../../visual-basic/language-reference/queries/index.md)
- [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
- [Group Join (clause)](../../../visual-basic/language-reference/queries/group-join-clause.md)
- [Where (clause)](../../../visual-basic/language-reference/queries/where-clause.md)
