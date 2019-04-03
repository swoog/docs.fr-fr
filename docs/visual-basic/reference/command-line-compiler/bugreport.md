---
title: -bugreport
ms.date: 03/08/2018
helpviewer_keywords:
- -bugreport compiler option [Visual Basic]
- bugreport compiler option [Visual Basic]
- /bugreport compiler option [Visual Basic]
ms.assetid: e4325406-8dbd-4b48-b311-9ee0799e48bb
ms.openlocfilehash: e7b4ebc58b6fe9850b92ef945cb0d715e4369efe
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58820905"
---
# <a name="-bugreport"></a>-bugreport
Crée un fichier que vous pouvez utiliser quand vous archivez un rapport de bogue.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-bugreport:file  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`file`|Obligatoire. Le nom du fichier qui contiendra votre rapport de bogue. Placez le nom de fichier entre guillemets ( » «) si le nom contient un espace.|  
  
## <a name="remarks"></a>Notes  
 Les informations suivantes sont ajoutées à `file`:  
  
-   Une copie de tous les fichiers de code source dans la compilation.  
  
-   Une liste des options du compilateur utilisé dans la compilation.  
  
-   Informations de version concernant votre compilateur, le common language runtime et le système d’exploitation.  
  
-   Les résultats de la compilation, le cas échéant.  
  
-   Une description du problème pour lequel vous êtes invité.  
  
-   Une description de la façon dont vous pensez que le problème doit être corrigée, pour lequel vous êtes invité.  
  
 Car une copie de tous les fichiers de code source est incluse dans `file`, vous pouvez souhaiter reproduire l’erreur de code (supposée) dans le programme le plus court possible.  
  
> [!IMPORTANT]
>  Le `-bugreport` option génère un fichier qui contient des informations potentiellement sensibles. Cela inclut l’heure actuelle, la version du compilateur, [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] version, version du système d’exploitation, nom d’utilisateur, les arguments de ligne de commande avec laquelle le compilateur a été exécuté, tout le code source, et la forme binaire de tout assembly référencé. Cette option est accessible en spécifiant des options de ligne de commande dans le fichier Web.config pour une compilation côté serveur d’un [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] application. Pour éviter ce problème, modifiez le fichier Machine.config pour interdire aux utilisateurs de se compiler sur le serveur.  
  
 Si cette option est utilisée avec `-errorreport:prompt`, `-errorreport:queue`, ou `-errorreport:send`, et votre application rencontre une erreur interne du compilateur, les informations contenues dans `file` sont envoyées à Microsoft Corporation. Ces informations aideront les ingénieurs Microsoft à identifier la cause de l’erreur et peuvent contribuer à améliorer la prochaine version de Visual Basic. Par défaut, aucune information n’est envoyée à Microsoft. Toutefois, lorsque vous compilez une application à l’aide de `-errorreport:queue`, qui est activé par défaut, l’application rassemble ses rapports d’erreurs. Ensuite, lorsque l’administrateur de l’ordinateur se connecte, le système de création de rapports d’erreurs affiche une fenêtre contextuelle qui permet à l’administrateur à envoyer à Microsoft signale toute erreur qui se sont produites depuis l’ouverture de session.  
  
> [!NOTE]
>  Le `/bugreport` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lorsque vous compilez à partir de la ligne de commande.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant compile `T2.vb` et place toutes les informations de rapport de bogue dans le fichier `Problem.txt`.  
  
```  
vbc -bugreport:problem.txt t2.vb  
```  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [-debug (Visual Basic)](../../../visual-basic/reference/command-line-compiler/debug.md)
- [-errorreport](../../../visual-basic/reference/command-line-compiler/errorreport.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [trustLevel, élément de securityPolicy (schéma des paramètres ASP.NET)](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/as399f0x(v=vs.100))
