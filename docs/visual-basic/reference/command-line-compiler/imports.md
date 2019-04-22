---
title: -importe (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- /imports compiler option [Visual Basic]
- imports compiler option [Visual Basic]
- -imports compiler option [Visual Basic]
ms.assetid: 9a93fb53-c080-497b-bf9b-441022dbbc39
ms.openlocfilehash: 075eeccc7d80943d2757a97b9a355bbea3ef9d4e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58833605"
---
# <a name="-imports-visual-basic"></a>-importe (Visual Basic)
Importe des espaces de noms à partir d’un assembly spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-imports:namespaceList  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`namespaceList`|Obligatoire. Liste délimitée par des virgules des espaces de noms à importer.|  
  
## <a name="remarks"></a>Notes  
 Le `-imports` option importe n’importe quel espace de noms défini dans l’ensemble des fichiers sources ou à partir de n’importe quel assembly référencé actuel.  
  
 Les membres dans un espace de noms spécifiés avec `-imports` sont disponibles pour tous les fichiers de code source dans la compilation. Utiliser le [instruction Imports (.NET Namespace et Type)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) à utiliser un espace de noms dans un fichier de code source unique.  
  
|Pour définir /Imports dans l’environnement de développement intégré Visual Studio|  
|---|  
|1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**. <br />2.  Cliquez sur l’onglet **Références**.<br />3.  Entrez le nom de l’espace de noms dans la zone en regard de la **ajouter une importation utilisateur** bouton.<br />4.  Cliquez sur le **ajouter une importation utilisateur** bouton.|  
  
## <a name="example"></a>Exemple  
 Le code suivant compile si `/imports:system.globalization` est spécifié. Sans cela, de compilation réussie nécessite qu’un `Imports System.Globalization` instruction inclus au début du fichier de code source ou que la propriété être qualifié en tant que `System.Globalization.CultureInfo.CurrentCulture.Name`.

```vb
Module Example
   Public Sub Main()
      Console.WriteLine($"The current culture is {CultureInfo.CurrentCulture.Name}")
   End Sub
End Module
```

## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Références et l’instruction Imports](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
