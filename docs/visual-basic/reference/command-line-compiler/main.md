---
title: -main
ms.date: 03/13/2018
helpviewer_keywords:
- main compiler option [Visual Basic]
- /main compiler option [Visual Basic]
- -main compiler option [Visual Basic]
ms.assetid: 83fc339d-6652-415d-b205-b5133319b5b0
ms.openlocfilehash: fd6240faf702ccb5e543bfd6a7779284f38d8850
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793911"
---
# <a name="-main"></a>-main
Spécifie la classe ou le module qui contient la procédure `Sub Main`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-main:location  
```  
  
## <a name="arguments"></a>Arguments  
 `location`  
 Obligatoire. Le nom de la classe ou le module qui contient le `Sub Main` procédure à appeler lorsque le programme démarre. Cela peut être sous la forme **-module : principal** ou **-main:namespace.module**.  
  
## <a name="remarks"></a>Notes  
 Utilisez cette option lorsque vous créez un fichier exécutable ou un programme exécutable Windows. Si le **-principal** option est omise, le compilateur recherche les valide partagé `Sub Main` dans tous les modules et les classes publiques.  
  
 Consultez [procédure Main dans Visual Basic](../../../visual-basic/programming-guide/program-structure/main-procedure.md) pour une description des différentes formes de la `Main` procédure.  
  
 Lorsque `location` est une classe qui hérite de <xref:System.Windows.Forms.Form>, le compilateur fournit une valeur par défaut `Main` procédure qui démarre l’application si la classe n’a pas `Main` procédure. Cela vous permet de compiler du code à la ligne de commande qui a été créée dans l’environnement de développement.  
  
 [!code-vb[VbVbalrCompiler#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/Class1.vb#16)]  
  
### <a name="to-set--main-in-the-visual-studio-integrated-development-environment"></a>Pour définir - main dans l’environnement de développement intégré Visual Studio  
  
1. Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**.  
  
2. Cliquez sur l’onglet **Application** .  
  
3. Assurez-vous que le **activer l’infrastructure application** case à cocher n’est pas activée.  
  
4. Modifiez la valeur dans le **objet de démarrage** boîte.  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `T2.vb` et `T3.vb`, en spécifiant que le `Sub Main` procédure se trouve dans le `Test2` classe.  
  
```console
vbc t2.vb t3.vb -main:Test2  
```  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [-target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [Procédure Main dans Visual Basic](../../../visual-basic/programming-guide/program-structure/main-procedure.md)
