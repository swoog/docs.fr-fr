---
title: -nostdlib (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- nostdlib compiler option [Visual Basic]
- -nostdlib compiler option [Visual Basic]
- /nostdlib compiler option [Visual Basic]
ms.assetid: 140381b8-dc96-4ad5-ae11-792c9ed0be4d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3764409f13a00f6d8a050bfbdd0f59e537a5ded3
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43456290"
---
# <a name="-nostdlib-visual-basic"></a>-nostdlib (Visual Basic)
Indique au compilateur pour ne pas automatiquement de référencer les bibliothèques standards.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-nostdlib  
```  
  
## <a name="remarks"></a>Notes  
 Le `-nostdlib` option supprime la référence automatique à l’assembly System.dll et empêche le compilateur de lire le fichier Vbc.rsp. Le fichier Vbc.rsp, qui se trouve dans le même répertoire que le fichier Vbc.exe, référence couramment utilisées [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] assemblys et des importations le `System` et `Microsoft.VisualBasic` espaces de noms.  
  
> [!NOTE]
>  Les assemblys Mscorlib.dll et de Microsoft.VisualBasic.dll sont toujours référencés.  
  
> [!NOTE]
>  Le `-nostdlib` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `T2.vb` sans référencer les bibliothèques standards. Vous devez définir le `_MYTYPE` constante de compilation conditionnelle à la chaîne « Vide » si vous souhaitez supprimer le `My` objet.  
  
```console
vbc -nostdlib -define:_MYTYPE=\"Empty\" T2.vb  
```  
  
## <a name="see-also"></a>Voir aussi  
 [-noconfig](../../../visual-basic/reference/command-line-compiler/noconfig.md)  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [Personnalisation de la disponibilité ou non des objets dans My](../../../visual-basic/developing-apps/customizing-extending-my/customizing-which-objects-are-available-in-my.md)
