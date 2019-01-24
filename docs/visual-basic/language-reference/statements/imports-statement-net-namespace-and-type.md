---
title: Imports, instruction - Namespace de .NET et de Type (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Imports
- imports
helpviewer_keywords:
- declared element names [Visual Basic], qualification
- imports [Visual Basic]
- Imports statement [Visual Basic]
- aliases [Visual Basic], Imports statement
- container elements [Visual Basic]
- namespaces [Visual Basic], importing
- Imports statement [Visual Basic], syntax
- import aliases [Visual Basic]
- aliases [Visual Basic], import
- declared elements [Visual Basic], container elements
ms.assetid: 7062f8aa-d890-4232-9eed-92836e13fb6e
ms.openlocfilehash: ecb75e71225d2b6705d6235a941ecd83b3aab75b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54699803"
---
# <a name="imports-statement-net-namespace-and-type"></a>Imports, instruction (espace de noms et type .NET)
Active les noms d’être référencés sans qualification d’espace de noms de type.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Imports [ aliasname = ] namespace  
-or-  
Imports [ aliasname = ] namespace.element  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`aliasname`|Facultatif. Un *alias d’importation* ou le nom par lequel le code peut faire référence à `namespace` au lieu de la chaîne de qualification complète. Consultez [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).|  
|`namespace`|Obligatoire. Le nom qualifié complet de l’espace de noms importé. Une chaîne d’espaces de noms imbriquée à n’importe quel niveau.|  
|`element`|Facultatif. Le nom d’un élément de programmation déclaré dans l’espace de noms. Peut être n’importe quel élément de conteneur.|  
  
## <a name="remarks"></a>Notes  
 La `Imports` instruction permet aux types qui sont contenus dans un espace de noms donné pour être référencé directement.  
  
 Vous pouvez fournir un nom d’espace de noms unique ou une chaîne d’espaces de noms imbriqués. Chaque espace de noms imbriqué est séparé de l’espace de noms au niveau supérieur suivant par une période (`.`), comme l’illustre l’exemple suivant.  
  
 `Imports System.Collections.Generic`  
  
 Chaque fichier source peut contenir un nombre quelconque de `Imports` instructions. Ces derniers doivent respecter les déclarations d’option, tel que le `Option Strict` instruction et elles doivent précéder les déclarations d’élément de programmation, telles que `Module` ou `Class` instructions.  
  
 Vous pouvez utiliser `Imports` uniquement au niveau fichier. Cela signifie que le contexte de déclaration pour l’importation doit être un fichier source et ne peut pas être un espace de noms, classe, structure, module, interface, procédure ou bloc.  
  
 Notez que la `Imports` instruction ne rend pas les éléments à partir d’autres projets et assemblys disponibles à votre projet. L’importation ne prend pas la place de la définition d’une référence. Elle supprime uniquement la nécessité pour qualifier des noms qui sont déjà disponibles pour votre projet. Pour plus d’informations, consultez « Importation d’éléments conteneurs » dans [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).  
  
> [!NOTE]
>  Vous pouvez définir implicite `Imports` instructions à l’aide de la [Page références, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/references-page-project-designer-visual-basic). Pour plus d'informations, voir [Procédure : Ajouter ou supprimer des espaces de noms importés (Visual Basic)](/visualstudio/ide/how-to-add-or-remove-imported-namespaces-visual-basic).  
  
## <a name="import-aliases"></a>Alias d’importation  
 Un *alias d’importation* définit l’alias pour un espace de noms ou un type. Alias d’importation sont utiles lorsque vous avez besoin d’utiliser des éléments portant le même nom sont déclarées dans un ou plusieurs espaces de noms. Pour plus d’informations et un exemple, consultez « Qualification d’un nom d’élément » dans [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).  
  
 Vous ne devez pas déclarer un membre au niveau du module avec le même nom que `aliasname`. Si vous le faites, le compilateur Visual Basic utilise `aliasname` uniquement pour le membre déclaré et n’est plus le reconnaît comme un alias d’importation.  
  
 Bien que la syntaxe utilisée pour déclarer un alias d’importation est utilisée comme celle-ci pour l’importation d’un préfixe d’espace de noms XML, les résultats sont différents. Un alias d’importation peut être utilisé en tant qu’expression dans votre code, tandis qu’un préfixe d’espace de noms XML peut être utilisé uniquement dans les littéraux XML ou les propriétés d’axe XML comme préfixe pour un élément qualifié ou un nom d’attribut.  
  
### <a name="element-names"></a>Noms des éléments  
 Si vous fournissez `element`, il doit représenter un *élément conteneur*, autrement dit, un élément de programmation qui permettre contenir d’autres éléments. Éléments conteneurs incluent les classes, structures, modules, interfaces et énumérations.  
  
 La portée des éléments mis à disposition par un `Imports` instruction varie selon que vous spécifiez `element`. Si vous spécifiez uniquement `namespace`, tous les identifie de façon unique nommé membres de cet espace de noms et d’éléments de conteneur au sein de cet espace de noms, sont disponibles sans qualification. Si vous spécifiez à la fois `namespace` et `element`, seuls les membres de cet élément sont disponibles sans qualification.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant retourne tous les dossiers dans le répertoire C:\ à l’aide de la <xref:System.IO.DirectoryInfo> classe.  
  
 Le code n’a aucun `Imports` instructions en haut du fichier. Par conséquent, le `DirectoryInfo`, <xref:System.Text.StringBuilder>, et <xref:Microsoft.VisualBasic.ControlChars.CrLf> références sont entièrement qualifiées avec les espaces de noms.  
  
 [!code-vb[VbVbalrStatements#152](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_1.vb)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant inclut `Imports` instructions pour les espaces de noms référencé. Par conséquent, les types n’ont pas à être complet avec les espaces de noms.  
  
 [!code-vb[VbVbalrStatements#153](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_2.vb)]  
  
 [!code-vb[VbVbalrStatements#154](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_3.vb)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant inclut `Imports` instructions qui créent des alias pour les espaces de noms référencé. Les types sont qualifiées avec l’alias.  
  
 [!code-vb[VbVbalrStatements#155](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_4.vb)]  
  
 [!code-vb[VbVbalrStatements#156](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_5.vb)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant inclut `Imports` instructions qui créent des alias pour les types référencés. Alias sont utilisés pour spécifier les types.  
  
 [!code-vb[VbVbalrStatements#157](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_6.vb)]  
  
 [!code-vb[VbVbalrStatements#158](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_7.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Namespace (instruction)](../../../visual-basic/language-reference/statements/namespace-statement.md)
- [Espaces de noms dans Visual Basic](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [Références et l’instruction Imports](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)
- [Imports (instruction) (espace de noms XML)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md)
- [Références aux éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
