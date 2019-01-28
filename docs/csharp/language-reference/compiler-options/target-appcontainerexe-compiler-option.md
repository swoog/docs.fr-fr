---
title: -target:appcontainerexe (Options du compilateur C#)
ms.date: 07/20/2015
ms.assetid: e7e62229-23ea-4e53-bef5-380d951bf95f
ms.openlocfilehash: 4f8c59d94b76dd0f3415846f7e682d62cc1771ff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54707607"
---
# <a name="-targetappcontainerexe-c-compiler-options"></a>-target:appcontainerexe (Options du compilateur C#)
Si vous utilisez l’option du compilateur **-target:appcontainerexe**, le compilateur crée un fichier exécutable Windows (.exe) qui doit être exécuté dans un conteneur d’application. Cette option est équivalente à [-target:winexe](../../../csharp/language-reference/compiler-options/target-winexe-compiler-option.md), mais elle est destinée aux applications [!INCLUDE[win8_appname_long](~/includes/win8-appname-long-md.md)].  
  
## <a name="syntax"></a>Syntaxe  
  
```console  
-target:appcontainerexe  
```  
  
## <a name="remarks"></a>Notes  
 Pour exiger que l’application s’exécute dans un conteneur d’application, cette option définit un bit dans le fichier [Portable Executable](/windows/desktop/Debug/pe-format) (PE). Lorsque ce bit est défini, une erreur se produit si la méthode CreateProcess tente de lancer l'exécutable en dehors d'un conteneur d'application.  
  
 À moins que vous utilisiez l’option [-out](../../../csharp/language-reference/compiler-options/out-compiler-option.md), le fichier de sortie prend le nom du fichier d’entrée qui contient la méthode [Main](../../../csharp/programming-guide/main-and-command-args/index.md).  
  
 Quand vous spécifiez cette option à une invite de commandes, tous les fichiers jusqu’à l’option **-out** ou **-target** suivante sont utilisés pour créer le fichier exécutable.  
  
### <a name="to-set-this-compiler-option-in-the-ide"></a>Pour définir cette option du compilateur dans l'IDE  
  
1.  Dans l’**Explorateur de solutions**, ouvrez le menu contextuel de votre projet et choisissez **Propriétés**.  
  
2.  Sous l’onglet **Application**, dans la liste **Type de sortie**, choisissez **Application Windows Store**.  
  
     Cette option est disponible uniquement pour les modèles d'applications [!INCLUDE[win8_appname_long](~/includes/win8-appname-long-md.md)].  
  
 Pour plus d'informations sur la façon de définir cette option du compilateur par programme, consultez <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.  
  
## <a name="example"></a>Exemple  
 La commande suivante compile `filename.cs` dans un fichier exécutable Windows qui peut être exécuté uniquement dans un conteneur d'application.  
  
```console  
csc -target:appcontainerexe filename.cs  
```  
  
## <a name="see-also"></a>Voir aussi

- [-target (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/target-compiler-option.md)
- [-target:winexe (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/target-winexe-compiler-option.md)
- [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)
