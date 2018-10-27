---
title: -verbose
ms.date: 03/13/2018
helpviewer_keywords:
- verbose compiler option [Visual Basic]
- -verbose compiler option [Visual Basic]
- /verbose compiler option [Visual Basic]
ms.assetid: d1aec0c1-0261-421d-9adc-5b13756100be
ms.openlocfilehash: e70496b552ced8e07cbe3cde34cda377d94da9f4
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188415"
---
# <a name="-verbose"></a>-verbose
Indique au compilateur de générer des messages d’état et d’erreur détaillés.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-verbose[+ | -]  
```  
  
## <a name="arguments"></a>Arguments  
 `+` &#124; `-`  
 Facultatif. Spécification `-verbose` est identique à la spécification `-verbose+`, ce qui entraîne le compilateur à émettre des messages détaillés. La valeur par défaut pour cette option est `-verbose-`.  
  
## <a name="remarks"></a>Notes  
 Le `-verbose` option affiche des informations sur le nombre total d’erreurs émis par le compilateur, signale les assemblys sont chargés par un module et affiche les fichiers qui sont en cours de compilation.  
  
> [!NOTE]
>  Le `-verbose` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `In.vb` et indique au compilateur d’afficher des informations d’état détaillées.  
  
```console  
vbc -verbose in.vb  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
