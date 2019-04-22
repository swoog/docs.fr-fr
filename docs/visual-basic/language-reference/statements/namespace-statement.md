---
title: Namespace, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Namespace
helpviewer_keywords:
- namespaces [Visual Basic], root
- Namespace statement [Visual Basic]
- namespaces [Visual Basic], nested
- declaring namespaces [Visual Basic], syntax
- namespaces [Visual Basic], declaring
- root namespaces
- declarations [Visual Basic], namespaces
ms.assetid: a31fbd95-9ace-4c3d-bbb1-51222a2272b2
ms.openlocfilehash: 7f6b976af7933b3895f6992488d2d1532a8fc2f7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58820930"
---
# <a name="namespace-statement"></a>Namespace, instruction
Déclare le nom d’un espace de noms et oblige le code source qui suit la déclaration à être compilé dans cet espace de noms.  
  
## <a name="syntax"></a>Syntaxe  
  
```vb  
Namespace [Global.] { name | name.name }  
    [ componenttypes ]  
End Namespace  
```  
  
## <a name="parts"></a>Composants  
 Global  
 Optionnel. Vous permet de définir un espace de noms en dehors de l’espace de noms racine de votre projet. Consultez [espaces de noms dans Visual Basic](../../../visual-basic/programming-guide/program-structure/namespaces.md).  
  
 `name`  
 Obligatoire. Un nom unique qui identifie l’espace de noms. Doit être un identificateur Visual Basic valide. Pour plus d’informations, consultez [noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).  
  
 `componenttypes`  
 Optionnel. Éléments qui composent l’espace de noms. Cela inclut, mais ne sont pas limités à, énumérations, structures, interfaces, classes, modules, délégués et autres espaces de noms.  
  
 `End Namespace`  
 Met fin à une `Namespace` bloc.  
  
## <a name="remarks"></a>Notes  
 Espaces de noms sont utilisés comme un système d’organisation. Ils permettent de classer et présenter des éléments de programmation qui sont exposés à d’autres programmes et les applications. Notez qu’un espace de noms n’est pas un *type* en ce sens qu’une classe ou structure est — vous ne pouvez pas déclarer un élément de programmation comme ayant le type de données d’un espace de noms.  
  
 Tous les éléments de programmation déclarés après une `Namespace` instruction appartiennent à cet espace de noms. Visual Basic continue à compiler les éléments dans le dernier espace de noms déclaré jusqu'à ce qu’il rencontre un `End Namespace` instruction ou un autre `Namespace` instruction.  
  
 Si un espace de noms est déjà défini, même en dehors de votre projet, vous pouvez ajouter des éléments de programmation à ce dernier. Pour ce faire, vous utilisez un `Namespace` instruction pour indiquer à Visual Basic pour compiler les éléments dans cet espace de noms.  
  
 Vous pouvez utiliser un `Namespace` instruction uniquement au niveau du fichier ou l’espace de noms. Cela signifie que le *contexte de déclaration* pour un espace de noms doit être un fichier source ou un autre espace de noms et ne peut pas être une classe, structure, module, interface ou une procédure. Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).  
  
 Vous pouvez déclarer un espace de noms dans une autre. Il n’existe aucune limite stricte aux niveaux d’imbrication, vous pouvez déclarer, mais n’oubliez pas que tout autre code qui accède aux éléments déclarés dans l’espace de noms plus profond, il doit utiliser une chaîne de qualification qui contient tous les noms d’espace de noms dans la hiérarchie d’imbrication.  
  
## <a name="access-level"></a>Niveau d’accès  
 Espaces de noms sont traités comme s’ils ont un `Public` niveau d’accès. Un espace de noms est accessible à partir du code n’importe où dans le même projet, à partir d’autres projets qui référencent le projet et à partir de n’importe quel assembly construit à partir du projet.  
  
 Les éléments de programmation déclarés au niveau de l’espace de noms, ce qui signifie que dans un espace de noms mais pas à l’intérieur d’un autre élément, peuvent avoir `Public` ou `Friend` accès. Si non spécifié, le niveau d’accès de telles un élément utilise `Friend` par défaut. Vous pouvez déclarer au niveau de l’espace de noms des éléments incluent des classes, structures, modules, interfaces, énumérations et les délégués. Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).  
  
## <a name="root-namespace"></a>Racine Namespace  
 Tous les noms d’espace de noms dans votre projet sont basés sur un *espace de noms racine*. Visual Studio définit le nom de votre projet comme espace de noms racine par défaut pour l’ensemble du code de votre projet. Par exemple, si votre projet est nommé `Payroll`, ses éléments de programmation appartiennent à l’espace de noms `Payroll`. Si vous déclarez `Namespace funding`, le nom complet de cet espace de noms est `Payroll.funding`.  
  
 Si vous souhaitez spécifier un espace de noms dans un `Namespace` instruction, comme dans l’exemple de classe de liste générique, vous pouvez définir votre espace de noms racine pour une valeur null. Pour ce faire, cliquez sur **propriétés du projet** à partir de la **projet** menu et puis désactivez le **espace de noms racine** entrée afin que la zone est vide. Si vous n’avez pas cela dans l’exemple de classe de liste générique, le compilateur Visual Basic prend `System.Collections.Generic` en tant qu’un nouvel espace de noms dans le projet `Payroll`, avec le nom complet de `Payroll.System.Collections.Generic`.  
  
 Vous pouvez également utiliser le `Global` mot clé pour faire référence aux éléments des espaces de noms définis en dehors de votre projet. Cela vous permet de conserver le nom de votre projet en tant que l’espace de noms racine. Cela réduit le risque de fusion involontaire de vos éléments de programmation avec ceux des espaces de noms existants. Pour plus d’informations, consultez la section « Mot clé dans entièrement qualifié noms globaux » dans [espaces de noms dans Visual Basic](../../../visual-basic/programming-guide/program-structure/namespaces.md).  
  
 Le `Global` mot clé peut également être utilisé dans une instruction Namespace. pour définir un espace de noms hors de l’espace de noms racine de votre projet. Pour plus d’informations, consultez la section « Mot clé Global dans instructions Namespace » dans [espaces de noms dans Visual Basic](../../../visual-basic/programming-guide/program-structure/namespaces.md).  
  
 **Résolution des problèmes.** L’espace de noms racine peut entraîner des concaténations inattendues de l’espace de noms. Si vous faites référence aux espaces de noms définis en dehors de votre projet, le compilateur Visual Basic peut les interpréter comme des espaces de noms imbriqués dans l’espace de noms racine. Dans ce cas, le compilateur ne reconnaît pas les types qui ont déjà été définis dans les espaces de noms externe. Pour éviter ce problème, définissez votre espace de noms racine pour une valeur null, comme décrit dans « Namespace racine », ou utiliser le `Global` mot clé pour accéder aux éléments des espaces de noms externe.  
  
## <a name="attributes-and-modifiers"></a>Attributs et modificateurs  
 Vous ne pouvez pas appliquer des attributs à un espace de noms. Un attribut fournit des informations aux métadonnées de l’assembly qui n’est pas significatif pour les classifieurs source tels que des espaces de noms.  
  
 Vous ne pouvez pas appliquer tout accès ou les modificateurs de procédure ou d’autres modificateurs, à un espace de noms. Comme il n’est pas un type, ces modificateurs ne sont pas significatifs.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant déclare deux espaces de noms, un étant imbriqué dans l’autre.  
  
 [!code-vb[VbVbalrStatements#43](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#43)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant déclare plusieurs espaces de noms imbriqués sur une seule ligne, et il est équivalent à l’exemple précédent.  
  
 [!code-vb[VbVbalrStatements#41](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#41)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant accède à la classe définie dans les exemples précédents.  
  
 [!code-vb[VbVbalrStatements#42](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#42)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit la structure d’une nouvelle classe de liste générique et l’ajoute à la <xref:System.Collections.Generic?displayProperty=nameWithType> espace de noms.  
  
```vb  
Namespace System.Collections.Generic  
    Class specialSortedList(Of T)  
        Inherits List(Of T)  
        ' Insert code to define the special generic list class.  
    End Class  
End Namespace  
```  
  
## <a name="see-also"></a>Voir aussi

- [Imports (instruction) (espace de noms et type .NET)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
- [Noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [Espaces de noms dans Visual Basic](../../../visual-basic/programming-guide/program-structure/namespaces.md)
