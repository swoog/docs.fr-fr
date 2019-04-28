---
title: Élément <loadFromRemoteSources>
ms.date: 05/24/2018
helpviewer_keywords:
- loadFromRemoteSources element
- <loadFromRemoteSources> element
ms.assetid: 006d1280-2ac3-4db6-a984-a3d4e275046a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7568129f30267b212737ec8aa688cf882e19bbff
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704594"
---
# <a name="loadfromremotesources-element"></a>\<loadFromRemoteSources > élément
Spécifie si les assemblys chargés à partir de sources distantes doivent être accordés une confiance totale dans .NET Framework 4 et versions ultérieures.
  
> [!NOTE]
>  Si vous avez été redirigé vers cet article en raison d’un message d’erreur dans la liste d’erreurs de projet Visual Studio ou une erreur de build, consultez [Comment : Utiliser un Assembly à partir du Web dans Visual Studio](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee890038(v=vs.100)).  
  
 \<configuration>  
\<runtime>  
\<loadFromRemoteSources>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<loadFromRemoteSources    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`enabled`|Attribut requis.<br /><br /> Spécifie si un assembly est chargé à partir d’une source distante doit être de confiance totale.|  
  
## <a name="enabled-attribute"></a>attribut activé  
  
|Value|Description|  
|-----------|-----------------|  
|`false`|N’accordez pas une confiance totale aux applications à partir de sources distantes. Il s'agit de la valeur par défaut.|  
|`true`|Accorder une confiance totale aux applications à partir de sources distantes.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les options d'initialisation du runtime.|  
  
## <a name="remarks"></a>Notes

Dans le .NET Framework 3.5 et les versions antérieures, si vous chargez un assembly à partir d’un emplacement distant, le code dans l’assembly s’exécute en confiance partielle avec un jeu d’autorisations qui dépend de la zone à partir de laquelle il est chargé. Par exemple, si vous chargez un assembly à partir d’un site Web, il est chargé dans la zone Internet et accordé le jeu d’autorisations Internet. En d’autres termes, il s’exécute dans un bac à sable d’Internet.

À compter de .NET Framework 4, la stratégie de sécurité (CA) d’accès au code est désactivée et les assemblys sont chargés avec une confiance totale. En règle générale, cela revient à accorder une confiance totale aux assemblys chargés avec le <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType> méthode avait été précédemment sandbox. Pour éviter ce problème, la possibilité d’exécuter du code dans les assemblys chargés à partir d’une source distante est désactivée par défaut. Par défaut, si vous essayez de charger un assembly distant, un <xref:System.IO.FileLoadException> avec un message d’exception, comme ce qui suit est levé :

```text
System.IO.FileNotFoundException: Could not load file or assembly 'file:assem.dll' or one of its dependencies. Operation is not supported. 
(Exception from HRESULT: 0x80131515)
File name: 'file:assem.dll' ---> 
System.NotSupportedException: An attempt was made to load an assembly from a network location which would have caused the assembly 
to be sandboxed in previous versions of the .NET Framework. This release of the .NET Framework does not enable CAS policy by default, 
so this load may be dangerous. If this load is not intended to sandbox the assembly, please enable the loadFromRemoteSources switch. 
```

Pour charger l’assembly et exécuter son code, vous devez :

- Créer explicitement un bac à sable pour l’assembly (consultez [Comment : Exécuter le Code de confiance partiel dans un bac à sable](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md)).

- Exécutez le code de l’assembly avec une confiance totale. Pour cela, vous devez configurer le `<loadFromRemoteSources>` élément. Il vous permet de spécifier que les assemblys qui s’exécutent en confiance partielle dans les versions antérieures du .NET Framework s’exécutent maintenant en mode confiance totale dans le .NET Framework 4 et versions ultérieures.

> [!IMPORTANT]
> Si l’assembly ne doit pas s’exécuter en mode confiance totale, ne définissez pas cet élément de configuration. Au lieu de cela, créez un bac à sable <xref:System.AppDomain> dans lequel charger l’assembly.

Le `enabled` d’attribut pour le `<loadFromRemoteSources>` élément est efficace uniquement lorsque la sécurité d’accès de code (CAS) est désactivée. Par défaut, la stratégie CAS est désactivée dans le .NET Framework 4 et versions ultérieures. Si vous définissez `enabled` à `true`, une confiance totale est accordée aux assemblys à distance.

Si `enabled` n’a pas la valeur `true`, un <xref:System.IO.FileLoadException> est levée dans l’une des conditions suivantes :

- Le comportement de bac à sable du domaine actuel est différent de son comportement dans le .NET Framework 3.5. Cela nécessite la stratégie CAS doit être désactivée et le domaine actuel ne pas à sable (sandbox).

- L’assembly en cours de chargement n’est pas à partir de la `MyComputer` zone.

Définition de la `<loadFromRemoteSources>` élément à `true` empêche cette exception ne soit levée. Il vous permet de spécifier que vous ne comptez pas sur le common language runtime pour le bac à sable les assemblys chargés pour la sécurité, et qu’il peut être autorisé à exécuter dans une confiance totale.

## <a name="notes"></a>Notes

- Dans le .NET Framework 4.5 et les versions ultérieures, les assemblys sur des partages de réseau local s’exécutent en confiance totale par défaut ; vous n’avez pas à activer le `<loadFromRemoteSources>` élément.

- Si une application a été copiée à partir du web, il est signalé par Windows comme étant une application web, même s’il se trouve sur l’ordinateur local. Vous pouvez modifier cette désignation en modifiant ses propriétés de fichier, ou vous pouvez utiliser le `<loadFromRemoteSources>` élément à accorder à l’assembly de confiance totale. Comme alternative, vous pouvez utiliser la <xref:System.Reflection.Assembly.UnsafeLoadFrom%2A> méthode pour charger un assembly local que le système d’exploitation a signalé comme ayant été chargé à partir du web.

- Vous risquez d’obtenir un <xref:System.IO.FileLoadException> dans une application qui s’exécute dans une application Windows Virtual PC. Cela peut se produire lorsque vous essayez de charger un fichier à partir des dossiers liés sur l’ordinateur hôte. Il peut également se produire lorsque vous essayez de charger un fichier à partir d’un dossier lié au fil du [Services Bureau à distance](https://go.microsoft.com/fwlink/?LinkId=182775) (Terminal Services). Pour éviter l’exception, définissez `enabled` à `true`.

## <a name="configuration-file"></a>fichier de configuration

Cet élément est généralement utilisé dans le fichier de configuration d’application, mais il peut être utilisé dans d’autres fichiers de configuration selon le contexte. Pour plus d’informations, consultez l’article [plus implicite utilise de stratégie CAS : loadFromRemoteSources](https://go.microsoft.com/fwlink/p/?LinkId=266839) dans le blog de sécurité .NET.  

## <a name="example"></a>Exemple

L’exemple suivant montre comment accorder une confiance totale aux assemblys chargés à partir de sources distantes.

```xml
<configuration>  
   <runtime>  
      <loadFromRemoteSources enabled="true"/>  
   </runtime>  
</configuration>  
```

## <a name="see-also"></a>Voir aussi

- [Utilise plus implicite de stratégie CAS : loadFromRemoteSources](https://go.microsoft.com/fwlink/p/?LinkId=266839)
- [Guide pratique pour exécuter du code d’un niveau de confiance partiel dans un bac à sable (sandbox)](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md)
- [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
- <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType>
