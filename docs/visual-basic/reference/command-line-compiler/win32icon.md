---
title: -win32icon
ms.date: 03/13/2018
helpviewer_keywords:
- win32icon compiler option [Visual Basic]
- -win32icon compiler option [Visual Basic]
- /win32icon compiler option [Visual Basic]
ms.assetid: aecaab01-9353-46c5-941c-6edabd4eff92
ms.openlocfilehash: dc48a8f79aa04892c514917da00b8fd6489695b1
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65593084"
---
# <a name="-win32icon"></a>-win32icon
Insère un fichier .ico dans le fichier de sortie. Ce fichier .ico représente le fichier de sortie dans **Explorateur de fichiers**.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-win32icon:filename  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`filename`|Le fichier .ico à ajouter à votre fichier de sortie. Placez le nom de fichier entre guillemets ( » «) s’il contient un espace.|  
  
## <a name="remarks"></a>Notes  
 Vous pouvez créer un fichier .ico avec le compilateur de ressources (RC) Microsoft Windows. Le compilateur de ressources est appelé lorsque vous compilez un programme Visual C++ ; un fichier .ico est créé à partir du fichier .rc. Le `-win32icon` et `-win32resource` options s’excluent mutuellement.  
  
 Consultez [- linkresource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/linkresource.md) pour référencer un fichier de ressources .NET Framework, ou [-ressources (Visual Basic)](../../../visual-basic/reference/command-line-compiler/resource.md) pour attacher un fichier de ressources .NET Framework. Consultez [-win32resource](../../../visual-basic/reference/command-line-compiler/win32resource.md) pour importer un fichier .res.  
  
|Pour définir - win32icon dans l’IDE Visual Studio|  
|---|  
|1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**. <br />2.  Cliquez sur l’onglet **Application** .<br />3.  Modifiez la valeur dans le **icône** boîte.|  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `In.vb` et attache un fichier .ico, `Rf.ico`.  
  
```console
vbc -win32icon:rf.ico in.vb  
```  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
