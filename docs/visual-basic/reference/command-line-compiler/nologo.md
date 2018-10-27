---
title: -nologo (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- -nologo compiler option [Visual Basic]
- banners [Visual Basic], suppressing startup
- nologo compiler option [Visual Basic]
- /nologo compiler option [Visual Basic]
ms.assetid: 25ef54b6-d676-4639-a2d2-a747a158bc07
ms.openlocfilehash: 21c708ef632cc0ed923713cd49e22d44848b4db3
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50037280"
---
# <a name="-nologo-visual-basic"></a>-nologo (Visual Basic)
Supprime l’affichage de la bannière de copyright et les messages d’information pendant la compilation.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-nologo  
```  
  
## <a name="remarks"></a>Notes  
 Si vous spécifiez `-nologo`, le compilateur n’affiche pas la bannière de copyright. Par défaut, l'option `-nologo` n'est pas activée.  
  
> [!NOTE]
>  Le `-nologo` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `T2.vb` et n’affiche pas la bannière de copyright.  
  
```console
vbc -nologo t2.vb  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
