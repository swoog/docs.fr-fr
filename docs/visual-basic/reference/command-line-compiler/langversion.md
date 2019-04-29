---
title: -langversion (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- /langversion compiler option [Visual Basic]
- langversion compiler option [Visual Basic]
- -langversion compiler option [Visual Basic]
ms.assetid: 59b7b0c8-2dde-4e9b-94e7-0237f7e0bafb
ms.openlocfilehash: db2cb1eb107973e9ce60ecb0d669c677d4fa2c51
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793952"
---
# <a name="-langversion-visual-basic"></a>-langversion (Visual Basic)
Indique au compilateur à accepter uniquement la syntaxe qui est incluse dans la version de langage Visual Basic spécifiée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-langversion:version  
```  
  
## <a name="arguments"></a>Arguments  
 `version`  
 Obligatoire. La version de langage à utiliser lors de la compilation. Valeurs acceptées sont `9`, `10`, `11`, `12`, `14`, `15`, `15.3`, `15.5`, `default` et `latest`.

 Aucun nombre entier peut également être spécifié à l’aide de `.0` la version secondaire, par exemple, `11.0`.

 Vous pouvez voir la liste de toutes les valeurs possibles en spécifiant `-langversion:?` sur la ligne de commande.  
  
## <a name="remarks"></a>Notes  
 Le `-langversion` option spécifie la syntaxe le compilateur accepte. Par exemple, si vous spécifiez que la version est 9.0, le compilateur génère des erreurs de syntaxe qui est valide uniquement dans la version 10.0 et versions ultérieures.  
  
 Vous pouvez utiliser cette option lorsque vous développez des applications qui ciblent différentes versions du .NET Framework. Par exemple, si vous ciblez .NET Framework 3.5, vous pouvez utiliser cette option pour vous assurer que vous n’utilisez pas la syntaxe de la version de langage 10.0.  
  
 Vous pouvez définir `-langversion` directement uniquement à l’aide de la ligne de commande. Pour plus d’informations, consultez [Ciblage d’une version spécifique du .NET Framework](/visualstudio/ide/targeting-a-specific-dotnet-framework-version).  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `sample.vb` pour Visual Basic 9.0.  
  
```console  
vbc -langversion:9.0 sample.vb  
```  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [Cibler une version spécifique du .NET Framework](/visualstudio/ide/targeting-a-specific-dotnet-framework-version)
