---
title: Using, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.using
helpviewer_keywords:
- resource disposal
- Try...Catch...Finally statements, equivalent to Using statement
- resources [Visual Basic], disposing
- Using statement [Visual Basic]
ms.assetid: 665d1580-dd54-4e96-a9a9-6be2a68948f1
ms.openlocfilehash: fe53ea58dc98a4de793fe9dad1c3ceeac71622fc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61698653"
---
# <a name="using-statement-visual-basic"></a>Using, instruction (Visual Basic)
Déclare le début d’un `Using` bloquer et acquiert éventuellement les ressources système qui contrôle le bloc.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Using { resourcelist | resourceexpression }  
    [ statements ]  
End Using  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`resourcelist`|Requis si vous ne fournissez pas `resourceexpression`. Liste d’une ou plusieurs ressources système que ce `Using` bloquer des contrôles, séparés par des virgules.|  
|`resourceexpression`|Requis si vous ne fournissez pas `resourcelist`. Variable de référence ou une expression faisant référence à une ressource système à être contrôlé par ce `Using` bloc.|  
|`statements`|Optionnel. Bloc d’instructions qui la `Using` bloquer s’exécute.|  
|`End Using`|Obligatoire. Termine la définition de la `Using` bloc et supprime toutes les ressources qu’il contrôle.|  
  
 Chaque ressource dans le `resourcelist` partie a la syntaxe et les éléments suivants :  
  
 `resourcename As New resourcetype [ ( [ arglist ] ) ]`  
  
 - ou -  
  
 `resourcename As resourcetype = resourceexpression`  
  
## <a name="resourcelist-parts"></a>Éléments resourcelist  
  
|Terme|Définition|  
|---|---|  
|`resourcename`|Obligatoire. Variable de référence qui fait référence à une ressource système qui le `Using` bloquer les commandes.|  
|`New`|Obligatoire si le `Using` instruction acquiert la ressource. Si vous avez déjà acquis la ressource, utilisez la deuxième possibilité de syntaxe.|  
|`resourcetype`|Obligatoire. La classe de la ressource. La classe doit implémenter la <xref:System.IDisposable> interface.|  
|`arglist`|Optionnel. Liste des arguments que vous passez au constructeur pour créer une instance de `resourcetype`. Consultez [liste de paramètres](../../../visual-basic/language-reference/statements/parameter-list.md).|  
|`resourceexpression`|Obligatoire. Variable ou une expression faisant référence à une ressource système répondant aux exigences de `resourcetype`. Si vous utilisez la deuxième possibilité de syntaxe, vous devez acquérir la ressource avant de passer le contrôle à la `Using` instruction.|  
  
## <a name="remarks"></a>Notes  
 Parfois, votre code requiert une ressource non managée, comme un descripteur de fichier, un wrapper COM ou une connexion SQL. Un `Using` bloc garantit la suppression d’un ou plusieurs de ces ressources lorsque votre code a fini avec eux. Cela les rend disponibles pour tout autre code à utiliser.  
  
 Ressources managées sont supprimées par le garbage collector (GC) du .NET Framework sans codage supplémentaire de votre part. Vous n’avez pas besoin un `Using` bloc pour les ressources managées. Toutefois, vous pouvez toujours utiliser un `Using` bloc pour forcer la suppression d’une ressource managée au lieu d’attendre le garbage collector.  
  
 Un `Using` bloc comprend trois parties : acquisition, de l’utilisation et de suppression.  
  
- *Acquisition* signifie que la création d’une variable et l’initialiser pour faire référence à la ressource du système. Le `Using` instruction peut acquérir une ou plusieurs ressources, ou vous pouvez acquérir exactement une ressource avant d’entrer dans le bloc et lui fournir à la `Using` instruction. Si vous fournissez `resourceexpression`, vous devez acquérir la ressource avant de passer le contrôle à la `Using` instruction.  
  
- *Utilisation* signifie que l’accès des ressources et d’exécuter des opérations. Les instructions entre `Using` et `End Using` représentent l’utilisation des ressources.  
  
- *Élimination* signifie appeler le <xref:System.IDisposable.Dispose%2A> méthode sur l’objet dans `resourcename`. Cela permet à l’objet arrêter correctement ses ressources. Le `End Using` instruction supprime les ressources sous le `Using` contrôle du bloc.  
  
## <a name="behavior"></a>Comportement  
 Un `Using` bloc se comporte comme un `Try`... `Finally` dans laquelle le `Try` bloc utilise les ressources et le `Finally` bloc supprime d'entre eux. Pour cette raison, le `Using` bloc garantit l’élimination des ressources, quel que soit la manière dont vous quittez le bloc. Cela est vrai même en cas d’une exception non gérée, sauf pour un <xref:System.StackOverflowException>.  
  
 La portée de chaque variable de ressource acquise par le `Using` instruction est limitée à la `Using` bloc.  
  
 Si vous spécifiez plusieurs ressources système dans le `Using` instruction, l’effet est le même que si vous imbriquez `Using` bloque une fois dans un autre.  
  
 Si `resourcename` est `Nothing`, aucun appel à <xref:System.IDisposable.Dispose%2A> est effectuée, et aucune exception n’est levée.  
  
## <a name="structured-exception-handling-within-a-using-block"></a>Structurée des exceptions dans un bloc à l’aide de  
 Si vous avez besoin gérer une exception qui peut-être se produire dans le `Using` bloc, vous pouvez ajouter un `Try`... `Finally` construction à celui-ci. Si vous avez besoin gérer le cas où le `Using` instruction n’a pas réussie à acquérir une ressource, vous pouvez tester pour voir si `resourcename` est `Nothing`.  
  
## <a name="structured-exception-handling-instead-of-a-using-block"></a>Structurée des exceptions au lieu d’un bloc à l’aide de  
 Si vous avez besoin d’un contrôle plus précis sur l’acquisition des ressources, ou si vous avez besoin de code supplémentaire dans le `Finally` bloc, vous pouvez réécrire la `Using` bloquer comme un `Try`... `Finally` construction. L’exemple suivant montre la structure `Try` et `Using` constructions qui sont équivalentes dans l’acquisition et l’élimination des `resource`.  
  
```vb  
Using resource As New resourceType   
    ' Insert code to work with resource.  
End Using  
  
' For the acquisition and disposal of resource, the following  
' Try construction is equivalent to the Using block.  
Dim resource As New resourceType  
Try   
    ' Insert code to work with resource.  
Finally   
    If resource IsNot Nothing Then  
        resource.Dispose()   
    End If  
End Try   
```  
  
> [!NOTE]
>  Le code à l’intérieur de la `Using` bloc ne doit pas affecter l’objet dans `resourcename` à une autre variable. Lorsque vous quittez le `Using` bloc, la ressource est supprimée, et l’autre variable ne peut pas accéder à la ressource vers laquelle il pointe.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée un fichier nommé log.txt et écrit deux lignes de texte dans le fichier. L’exemple lit ce même fichier également et affiche les lignes de texte.  
  
 Étant donné que le <xref:System.IO.TextWriter> et <xref:System.IO.TextReader> classes implémentent le <xref:System.IDisposable> interface, le code peut utiliser `Using` instructions pour vous assurer que le fichier est correctement fermé lors de l’écriture et les opérations de lecture.  
  
 [!code-vb[VbVbalrStatements#50](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#50)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IDisposable>
- [Try...Catch...Finally (instruction)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [Guide pratique pour Supprimer une ressource système](../../../visual-basic/programming-guide/language-features/control-flow/how-to-dispose-of-a-system-resource.md)
