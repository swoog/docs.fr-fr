---
title: -définir (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- -d compiler option [Visual Basic]
- /d compiler option [Visual Basic]
- -define compiler option [Visual Basic]
- d compiler option [Visual Basic]
- /define compiler option [Visual Basic]
- define compiler option [Visual Basic]
ms.assetid: f735c57d-1cf9-4f2f-a26f-0de630fd4077
ms.openlocfilehash: d0a483e7a3c9e9863db39e89d655cf172c1e8c81
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61649723"
---
# <a name="-define-visual-basic"></a>-définir (Visual Basic)
Définit des constantes conditionnelles du compilateur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-define:["]symbol[=value][,symbol[=value]]["]  
' -or-  
-d:["]symbol[=value][,symbol[=value]]["]  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`symbol`|Obligatoire. Symbole à définir.|  
|`value`|Optionnel. Valeur à affecter au `symbol`. Si `value` est une chaîne, elle doit être entourée par des séquences de barre oblique inverse/guillemets (\\») au lieu des guillemets. Si aucune valeur n'est spécifiée, il prend la valeur True.|  
  
## <a name="remarks"></a>Notes  
 L'option `-define` revient à utiliser la directive de préprocesseur `#Const` dans votre fichier source, excepté que les constantes définies avec `-define` sont publiques et s'appliquent à tous les fichiers du projet.  
  
 Vous pouvez utiliser les symboles créés par cette option avec la directive `#If`...`Then`...`#Else` pour effectuer une compilation conditionnelle des fichiers sources.  
  
 `-d` est la forme abrégée de `-define`.  
  
 Vous pouvez définir plusieurs symboles avec `-define` en utilisant une virgule pour séparer les définitions de symbole.  
  
|Pour définir /define dans l'environnement de développement intégré Visual Studio|  
|---|  
|1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**. <br />2.  Cliquez sur l’onglet **Compiler**.<br />3.  Cliquez sur **Avancé**.<br />4.  Modifiez la valeur dans le **constantes personnalisées** boîte.|  
  
## <a name="example"></a>Exemple  
 Le code suivant définit deux constantes de compilation conditionnelle, puis les utilise.  
  
 [!code-vb[VbVbalrCompiler#45](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/Class1.vb#45)]  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [#If...Then...#Else, directives](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
- [#Const (directive)](../../../visual-basic/language-reference/directives/const-directive.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
