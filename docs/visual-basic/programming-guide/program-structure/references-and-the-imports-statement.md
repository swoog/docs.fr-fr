---
title: Références et l'instruction Imports (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- assemblies [Visual Basic], namespaces
- references [Visual Basic], assembly
- namespaces [Visual Basic], assemblies
- referencing assemblies
- Imports statement [Visual Basic], referencing assemblies
- assemblies [Visual Basic], references
ms.assetid: 38149bd4-0a6f-4b31-b5f8-94a8c33f1600
ms.openlocfilehash: 89d360e5caa3cdb0dd1ecb985ea7ba727e5a6d9d
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44208508"
---
# <a name="references-and-the-imports-statement-visual-basic"></a>Références et l'instruction Imports (Visual Basic)
Vous pouvez proposer des objets externes à votre projet en choisissant le **ajouter une référence** commande sur le **projet** menu. Les références dans Visual Basic peuvent pointer vers des assemblys qui sont semblables à des bibliothèques de types, mais contiennent plus d’informations.  
  
## <a name="the-imports-statement"></a>L’instruction Imports  
 Assemblys incluent un ou plusieurs espaces de noms. Lorsque vous ajoutez une référence à un assembly, vous pouvez également ajouter un `Imports` instruction à un module qui contrôle la visibilité des espaces de noms de l’assembly dans le module. La `Imports` instruction offre une portée qui vous permet d’utiliser uniquement la partie de l’espace de noms nécessaire pour fournir une référence unique.  
  
 La `Imports` instruction présente la syntaxe suivante :  
  
 `Imports` [`|``Aliasname` =] `Namespace`  
  
 `Aliasname` fait référence à un nom court, que vous pouvez utiliser dans du code pour faire référence à un espace de noms importé. `Namespace` est un espace de noms disponible via une référence de projet, une définition dans le projet, ou via un précédent `Imports` instruction.  
  
 Un module peut contenir un nombre quelconque de `Imports` instructions. Ils doivent apparaître après n’importe quel `Option` instructions, le cas échéant, mais avant tout autre code.  
  
> [!NOTE]
>  Ne confondez pas les références de projet avec le `Imports` instruction ou la `Declare` instruction. Références de projet à disposition des objets externes, tels que les objets dans les assemblys, aux projets Visual Basic. La `Imports` instruction permet de simplifier l’accès aux références de projet, mais ne donne pas accès à ces objets. La `Declare` instruction est utilisée pour déclarer une référence à une procédure externe dans une bibliothèque de liens dynamiques (DLL).  
  
## <a name="using-aliases-with-the-imports-statement"></a>L’utilisation d’alias avec l’instruction Imports  
 La `Imports` instruction facilite accès aux méthodes des classes en éliminant la nécessité pour typer explicitement les noms qualifiés complets de références. Les alias vous permettent d’attribuer un nom plus convivial à seulement une partie d’un espace de noms. Par exemple, la retour chariot/ligne flux séquence qui provoque un seul élément de texte à afficher sur plusieurs lignes fait partie de la <xref:Microsoft.VisualBasic.ControlChars> module dans le <xref:Microsoft.VisualBasic?displayProperty=nameWithType> espace de noms. Pour utiliser cette constante dans un programme sans alias, vous devez taper le code suivant :  
  
 [!code-vb[VbVbalrApplication#3](../../../visual-basic/programming-guide/program-structure/codesnippet/VisualBasic/references-and-the-imports-statement_1.vb)]  
  
 `Imports` instructions doivent toujours être les premières lignes immédiatement après les `Option` instructions dans un module. Le fragment de code suivant montre comment importer et affecter un alias pour le <xref:Microsoft.VisualBasic.ControlChars?displayProperty=nameWithType> module :  
  
 [!code-vb[VbVbalrApplication#4](../../../visual-basic/programming-guide/program-structure/codesnippet/VisualBasic/references-and-the-imports-statement_2.vb)]  
  
 Références ultérieures à cet espace de noms peuvent être considérablement plus courts :  
  
 [!code-vb[VbVbalrApplication#5](../../../visual-basic/programming-guide/program-structure/codesnippet/VisualBasic/references-and-the-imports-statement_3.vb)]  
  
 Si un `Imports` instruction n’inclut pas un nom d’alias, les éléments définis dans l’espace de noms importé peuvent être utilisés dans le module sans qualification. Si le nom d’alias est spécifié, il doit être utilisé comme qualificateur pour les noms contenus dans cet espace de noms.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.ControlChars>
- <xref:Microsoft.VisualBasic>
- [Espaces de noms dans Visual Basic](../../../visual-basic/programming-guide/program-structure/namespaces.md)  
- [Assemblys et le Global Assembly Cache](../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)  
- [Guide pratique : créer et utiliser des assemblys à l’aide de la ligne de commande](../../../visual-basic/programming-guide/concepts/assemblies-gac/how-to-create-and-use-assemblies-using-the-command-line.md)  
- [Imports (instruction) (espace de noms et type .NET)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
