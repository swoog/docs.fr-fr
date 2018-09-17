---
title: -publicsign (Options du compilateur C#)
ms.date: 05/15/2018
f1_keywords:
- /publicsign
helpviewer_keywords:
- -publicsign compiler option [C#]
- publicsign compiler option [C#]
- /publicsign compiler option [C#]
ms.openlocfilehash: 01ce30b9ac5997f56f29dcbbfa43a27738fa5556
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45678957"
---
# <a name="-publicsign-c-compiler-options"></a>-publicsign (Options du compilateur C#)

Cette option force le compilateur à appliquer une clé publique sans signer l’assembly. L’option **-publicsign** définit également un bit dans l’assembly qui indique au runtime que le fichier est signé.

## <a name="syntax"></a>Syntaxe

```console
-publicsign
```

## <a name="arguments"></a>Arguments

Aucun.

## <a name="remarks"></a>Notes

L’option **-publicsign** nécessite l’utilisation de l’option [-keyfile](keyfile-compiler-option.md) ou [-keycontainer](keycontainer-compiler-option.md). Les options **keyfile** ou **keycontainer** spécifient la clé publique.

Les options **-publicsign** et **-delaysign** s’excluent mutuellement.

Parfois appelée « fausse signature » ou « signature OSS », la signature publique inclut la clé publique dans un assembly de sortie et définit l’indicateur « signé ». Toutefois, elle ne signe pas l’assembly avec une clé privée. Cette approche est utile dans le cadre de projets open source. Vous pouvez en effet générer des assemblys compatibles avec les assemblys publiés « totalement signés », même si vous n’avez pas accès à la clé privée utilisée pour les signer. Puisque pratiquement aucun consommateur ne doit vérifier si l’assembly est totalement signé, ces assemblys générés publiquement peuvent être utilisés dans la quasi-totalité des scénarios employant des assemblys totalement signés.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Pour définir cette option du compilateur dans l'environnement de développement Visual Studio

1. Ouvrez la page **Propriétés** du projet.
1. Modifiez la propriété **Différer la signature uniquement**.

## <a name="see-also"></a>Voir aussi

- [Option -delaysign du compilateur C#](delaysign-compiler-option.md)  
- [Option -keyfile du compilateur C#](keyfile-compiler-option.md)  
- [Option -keycontainer du compilateur C#](keycontainer-compiler-option.md)  
- [Options du compilateur C#](index.md)  
- [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)
