---
title: -resource (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- /resource compiler option [Visual Basic]
- -resource compiler option [Visual Basic]
- /res compiler option [Visual Basic]
- res compiler option [Visual Basic]
- -res compiler option [Visual Basic]
- resource compiler option [Visual Basic]
ms.assetid: eee2f227-91f2-4f2b-a9d6-1c51c5320858
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ab5593455546e65bdd760d9e60532031dc1f12a9
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42931444"
---
# <a name="-resource-visual-basic"></a>-resource (Visual Basic)
Incorpore une ressource managée dans un assembly.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-resource:filename[,identifier[,public|private]]  
' -or-  
-res:filename[,identifier[,public|private]]  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`filename`|Obligatoire. Le nom du fichier de ressources à incorporer dans le fichier de sortie. Par défaut, `filename` est public dans l’assembly. Placez le nom de fichier entre guillemets ( » «) s’il contient un espace.|  
|`identifier`|Facultatif. Le nom logique de la ressource ; nom utilisé pour le charger. La valeur par défaut est le nom du fichier. Si vous le souhaitez, vous pouvez spécifier si la ressource est publique ou privée dans le manifeste d’assembly, comme avec les éléments suivants : `-res:filename.res, myname.res, public`|  
  
## <a name="remarks"></a>Notes  
 Utilisez `-linkresource` pour lier une ressource à un assembly sans placer le fichier de ressources dans le fichier de sortie.  
  
 Si `filename` est un [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fichier de ressources créé, par exemple, par le [Resgen.exe (Resource File Generator)](http://msdn.microsoft.com/library/8ef159de-b660-4bec-9213-c3fbc4d1c6f4) ou dans l’environnement de développement, il est accessible à l’aide des membres de la <xref:System.Resources> (voir del’espacedenoms<xref:System.Resources.ResourceManager> pour plus d’informations). Pour accéder à toutes les autres ressources au moment de l’exécution, utilisez une des méthodes suivantes : <xref:System.Reflection.Assembly.GetManifestResourceInfo%2A>, <xref:System.Reflection.Assembly.GetManifestResourceNames%2A>, ou <xref:System.Reflection.Assembly.GetManifestResourceStream%2A>.  
  
 La forme abrégée de `-resource` est `-res`.  
  
 Pour plus d’informations sur la définition `-resource` dans l’IDE de Visual Studio, consultez [gestion des ressources Application (.NET)](/visualstudio/ide/managing-application-resources-dotnet).  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `In.vb` et le fichier de ressources attache `Rf.resource`.  
  
```console
vbc -res:rf.resource in.vb  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [-win32resource](../../../visual-basic/reference/command-line-compiler/win32resource.md)  
 [-linkresource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/linkresource.md)  
 [-target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
