---
title: 'Procédure : Créer une stratégie d’éditeur'
ms.date: 03/30/2017
helpviewer_keywords:
- publisher policy assembly
- publisher policy files
- GAC (global assembly cache), publisher policy assembly
- global assembly cache, publisher policy assembly
ms.assetid: 8046bc5d-2fa9-4277-8a5e-6dcc96c281d9
ms.openlocfilehash: b98d3ef62fc9dda48920d32fed6f6acf797334d6
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55758987"
---
# <a name="how-to-create-a-publisher-policy"></a>Procédure : Créer une stratégie d’éditeur
Les fournisseurs d’assemblys peuvent indiquer que les applications doivent utiliser une version plus récente d’un assembly en incluant un fichier de stratégie de serveur de publication avec l’assembly mis à niveau. Le fichier de stratégie d’éditeur spécifie la redirection d’assembly et les paramètres de base de code et utilise le même format qu’un fichier de configuration d’application. Le fichier de stratégie d’éditeur est compilé dans un assembly et placé dans le global assembly cache.  
  
 Il existe trois étapes impliquées dans la création d’une stratégie d’éditeur :  
  
1.  Créez un fichier de stratégie de serveur de publication.  
  
2.  Créer un assembly de stratégie de serveur de publication.  
  
3.  Ajoutez l’assembly de stratégie de serveur de publication dans le global assembly cache.  
  
 Le schéma pour la stratégie d’éditeur est décrit dans [redirection des Versions d’Assembly](../../../docs/framework/configure-apps/redirect-assembly-versions.md). L’exemple suivant montre un serveur de publication des fichiers de stratégie qui redirige une version de `myAssembly` vers un autre.  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
       <dependentAssembly>  
         <assemblyIdentity name="myAssembly"  
                           publicKeyToken="32ab4ba45e0a69a1"  
                           culture="en-us" />  
         <!-- Redirecting to version 2.0.0.0 of the assembly. -->  
         <bindingRedirect oldVersion="1.0.0.0"  
                          newVersion="2.0.0.0"/>  
       </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 Pour savoir comment spécifier une base de code, consultez [spécifiant l’emplacement d’un Assembly](../../../docs/framework/configure-apps/specify-assembly-location.md).  
  
## <a name="creating-the-publisher-policy-assembly"></a>Création de l’Assembly de stratégie de serveur de publication  
 Utilisez le [Assembly Linker (Al.exe)](../../../docs/framework/tools/al-exe-assembly-linker.md) pour créer l’assembly de stratégie de serveur de publication.  
  
#### <a name="to-create-a-publisher-policy-assembly"></a>Pour créer un assembly de stratégie de serveur de publication  
  
1.  Tapez la commande suivante à l’invite de commandes :  
  
     **al /link:** *publisherPolicyFile* **/out:** *publisherPolicyAssemblyFile* **/keyfile:** *keyPairFile* **/platform:** *processorArchitecture*  
  
     Dans cette commande :  
  
    -   Le *publisherPolicyFile* argument est le nom du fichier de stratégie de serveur de publication.  
  
    -   Le *publisherPolicyAssemblyFile* argument est le nom de l’assembly de stratégie d’éditeur qui résulte de cette commande. Le nom de fichier d’assembly doit respecter le format :  
  
         **policy.** *majorNumber* **.** *minorNumber* **.** *mainAssemblyName* **.dll**  
  
    -   Le *keyPairFile* argument est le nom du fichier contenant la paire de clés. Vous devez signer l’assembly et l’assembly de stratégie d’éditeur avec la même paire de clés.  
  
    -   Le *processorArchitecture* argument identifie la plateforme ciblée par un assembly spécifique au processeur.  
  
        > [!NOTE]
        >  La possibilité de cibler une architecture de processeur spécifique est une nouveauté dans le .NET Framework version 2.0.  
  
     La commande suivante crée un assembly de stratégie d’éditeur appelé `policy.1.0.myAssembly` à partir d’un fichier de stratégie de serveur de publication nommé `pub.config`, assigne un nom fort à l’assembly à l’aide de la paire de clés dans le `sgKey.snk` de fichiers et spécifie que l’assembly cible la x86 architecture de processeur.  
  
    ```  
    al /link:pub.config /out:policy.1.0.myAssembly.dll /keyfile:sgKey.snk /platform:x86  
    ```  
  
     L’assembly de stratégie de serveur de publication doit correspondre à l’architecture de processeur de l’assembly qui s’applique à. Par conséquent, si l’assembly comporte un <xref:System.Reflection.AssemblyName.ProcessorArchitecture%2A> valeur <xref:System.Reflection.ProcessorArchitecture.MSIL>, l’assembly de stratégie d’éditeur pour cet assembly doit être créé avec `/platform:anycpu`. Vous devez fournir un distinct assembly de stratégie d’éditeur pour chaque assembly spécifique au processeur.  
  
     Une conséquence de cette règle est que, pour modifier l’architecture de processeur pour un assembly, vous devez modifier le composant majeur ou mineurs du numéro de version, afin que vous pouvez fournir un nouvel assembly de stratégie de serveur de publication avec l’architecture de processeur correcte. L’ancien assembly de stratégie de serveur de publication ne peut pas traiter votre assembly une fois que votre assembly dispose d’une architecture de processeur différente.  
  
     Une autre conséquence est que l’éditeur de liens version 2.0 ne peut pas être utilisé pour créer un assembly de stratégie de serveur de publication pour un assembly compilé à l’aide de versions antérieures du .NET Framework, car elle spécifie toujours architecture de processeur.  
  
## <a name="adding-the-publisher-policy-assembly-to-the-global-assembly-cache"></a>Ajout de l’Assembly de stratégie de serveur de publication dans le Global Assembly Cache  
 Utilisez le [outil Global Assembly Cache (Gacutil.exe)](../../../docs/framework/tools/gacutil-exe-gac-tool.md) pour ajouter l’assembly de stratégie de serveur de publication dans le global assembly cache.  
  
#### <a name="to-add-the-publisher-policy-assembly-to-the-global-assembly-cache"></a>Pour ajouter l’assembly de stratégie de serveur de publication dans le global assembly cache  
  
1.  Tapez la commande suivante à l’invite de commandes :  
  
     **gacutil /i**  *publisherPolicyAssemblyFile*  
  
     La commande suivante ajoute `policy.1.0.myAssembly.dll` dans le global assembly cache.  
  
    ```  
    gacutil /i policy.1.0.myAssembly.dll  
    ```  
  
    > [!IMPORTANT]
    >  L’assembly de stratégie de serveur de publication ne peut pas être ajouté au global assembly cache, sauf si le fichier de stratégie de serveur de publication d’origine se trouve dans le même répertoire que l’assembly.  
  
## <a name="see-also"></a>Voir aussi
- [Programmation à l’aide d’assemblys](../../../docs/framework/app-domains/programming-with-assemblies.md)
- [Méthode de localisation des assemblys par le runtime](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
- [Configuration d’applications à l’aide de fichiers de Configuration](../../../docs/framework/configure-apps/index.md)
- [Schéma des paramètres d’exécution](../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [Schéma des fichiers de configuration](../../../docs/framework/configure-apps/file-schema/index.md)
- [Redirection des versions d'assemblys](../../../docs/framework/configure-apps/redirect-assembly-versions.md)
