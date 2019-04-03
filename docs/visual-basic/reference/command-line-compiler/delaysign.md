---
title: -delaysign
ms.date: 03/10/2018
helpviewer_keywords:
- delaysign compiler option [Visual Basic]
- -delaysign compiler option [Visual Basic]
- -delaysign compiler option [Visual Basic]
ms.assetid: c76e61a4-1884-4252-9fb2-377f99caa690
ms.openlocfilehash: ccf569aea1363d256728e122818b70284a9e250d
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58830368"
---
# <a name="-delaysign"></a>-delaysign
Spécifie si l'assembly sera complètement ou partiellement signé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-delaysign[+ | -]  
```  
  
## <a name="arguments"></a>Arguments  
 `+` &#124; `-`  
 Optionnel. Utilisez `-delaysign-` si vous souhaitez obtenir un assembly complètement signé. Utilisez `-delaysign+` si vous souhaitez placer la clé publique dans l’espace d’assembly et réserve pour le hachage signé. La valeur par défaut est `-delaysign-`.  
  
## <a name="remarks"></a>Notes  
 Le `-delaysign` option est sans effet sauf si utilisée avec [- keyfile](../../../visual-basic/reference/command-line-compiler/keyfile.md) ou [- keycontainer](../../../visual-basic/reference/command-line-compiler/keycontainer.md).  
  
 Quand vous demandez un assembly totalement signé, le compilateur hache le fichier qui contient le manifeste (métadonnées de l’assembly) et signe ce hachage avec la clé privée. La signature numérique obtenue est stockée dans le fichier qui contient le manifeste. Lorsqu’un assembly est à signature différée, le compilateur ne calcule pas et stocker l’espace de signature mais les réserves de ressources dans le fichier pour la signature puisse être ajoutée plus tard.  
  
 Par exemple, en utilisant `-delaysign+`, un développeur d’une organisation peut distribuer des versions de test non signé d’un assembly qui les testeurs peuvent enregistrer dans le global assembly cache et utiliser. Lorsque le travail sur l’assembly est terminé, la personne responsable de la clé privée de l’organisation peut signer complètement l’assembly. Ce compartimentage protège la clé privée de l’organisation contre toute divulgation, tout en autorisant tous les développeurs de travailler sur les assemblys.  
  
 Consultez [création et assemblys avec nom fort](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) pour plus d’informations sur la signature d’un assembly.  
  
### <a name="to-set--delaysign-in-the-visual-studio-integrated-development-environment"></a>Pour définir delaysign - dans l’environnement de développement intégré Visual Studio  
  
1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**.   
  
2.  Cliquez sur l’onglet **Signature**.  
  
3.  Définissez la valeur dans le **différer la signature uniquement** boîte.  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [-keyfile](../../../visual-basic/reference/command-line-compiler/keyfile.md)
- [-keycontainer](../../../visual-basic/reference/command-line-compiler/keycontainer.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
