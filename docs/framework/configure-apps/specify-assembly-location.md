---
title: Spécification de l'emplacement d'un assembly
ms.date: 03/30/2017
helpviewer_keywords:
- configuration [.NET Framework], applications
- application configuration [.NET Framework]
- assemblies [.NET Framework], specifying location
ms.assetid: 1cb92bd7-6bab-44cf-8fd3-36303ce84fea
ms.openlocfilehash: b76537a347cdf30c65bfd6e56f274108e796a315
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55258988"
---
# <a name="specifying-an-assemblys-location"></a>Spécification de l'emplacement d'un assembly
Il existe deux façons de spécifier l’emplacement d’un assembly :  
  
-   À l’aide de la [ \<codeBase >](../../../docs/framework/configure-apps/file-schema/runtime/codebase-element.md) élément.  
  
-   À l’aide de la [ \<probing >](../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md) élément.  
  
 Vous pouvez également utiliser le [.NET Framework Configuration Tool (Mscorcfg.msc)](https://msdn.microsoft.com/library/a7106c52-68da-490e-b129-971b2c743764) pour spécifier les emplacements des assemblys ou spécifier des emplacements pour le common language runtime détecter les assemblys.  
  
## <a name="using-the-codebase-element"></a>À l’aide de la \<codeBase > élément  
 Vous pouvez utiliser la  **\<codeBase >** élément uniquement dans la machine serveur de publication stratégie fichiers de configuration ou qui redirigent également la version d’assembly. Lorsque le runtime détermine la version d’assembly à utiliser, elle s’applique le paramètre de base de code à partir du fichier qui détermine la version. Si aucune base de code n’est indiqué, le runtime détecte l’assembly de façon normale. Pour plus d’informations, consultez [méthode de localisation des assemblys par le Runtime](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).  
  
 L’exemple suivant montre comment spécifier l’emplacement d’un assembly.  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
       <dependentAssembly>  
         <assemblyIdentity name="myAssembly"  
                           publicKeyToken="32ab4ba45e0a69a1"  
                           culture="en-us" />  
         <codeBase version="2.0.0.0"  
                   href="http://www.litwareinc.com/myAssembly.dll"/>  
       </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 Le **version** attribut est obligatoire pour tous les assemblys avec nom fort, mais doit être omis pour les assemblys qui ne sont pas de nom fort. Le  **\<codeBase >** élément requiert le **href** attribut. Vous ne pouvez pas spécifier des plages de versions dans le  **\<codeBase >** élément.  
  
> [!NOTE]
>  Si vous fournissez un indicateur de base de code pour un assembly qui n’est pas un nom fort, l’indicateur doit pointer vers la base de l’application ou un sous-répertoire du répertoire de base de l’application.  
  
## <a name="using-the-probing-element"></a>À l’aide de la \<probing > élément  
 Le runtime localise les assemblys qui n’ont pas d’une base de code par la détection. Pour plus d’informations sur la détection, consultez [méthode de localisation des assemblys par le Runtime](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).  
  
 Vous pouvez utiliser la [ \<probing >](../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md) élément dans le fichier de configuration d’application pour spécifier le runtime doit rechercher lors de la localisation d’un assembly de sous-répertoires. L’exemple suivant montre comment spécifier le runtime doit rechercher les répertoires.  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <probing privatePath="bin;bin2\subbin;bin3"/>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 Le **privatePath** attribut contient les répertoires dans lesquels le runtime doit rechercher les assemblys. Si l’application se trouve dans C:\Program Files\MyApp, le runtime recherche les assemblys qui ne spécifient pas une base de code dans C:\Program Files\MyApp\Bin, C:\Program Files\MyApp\Bin2\Subbin et C:\Program Files\MyApp\Bin3. Les répertoires spécifiés dans **privatePath** doivent être des sous-répertoires du répertoire de base d’application.  
  
## <a name="see-also"></a>Voir aussi
- [Assemblys dans le Common Language Runtime](../../../docs/framework/app-domains/assemblies-in-the-common-language-runtime.md)
- [Programmation à l’aide d’assemblys](../../../docs/framework/app-domains/programming-with-assemblies.md)
- [Méthode de localisation des assemblys par le runtime](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
- [Configuration des applications .NET Framework](https://msdn.microsoft.com/library/d789b592-fcb5-4e3d-8ac9-e0299adaaa42)
