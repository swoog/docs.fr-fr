---
title: '&lt;providerOption&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- provideroption
helpviewer_keywords:
- <provideroption> element
- providerOptions
- provideroption element
ms.assetid: 014f2e0b-c0b5-4fc4-92d3-73f02978b2a1
author: mcleblanc
ms.author: markl
ms.openlocfilehash: fab681042055edac0291b917f55656350261d6af
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47201034"
---
# <a name="ltprovideroptiongt-element"></a>&lt;providerOption&gt; élément
Spécifie les attributs de version du compilateur pour un fournisseur de langage.  
  
 \<Élément de configuration >  
\<System.CodeDom (élément) >  
\<compilers, élément >  
\<compilateur > élément  
\<providerOption > élément  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<providerOption  
  name="option-name"  
  value="option-value"  
/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`name`|Attribut requis.<br /><br /> Spécifie le nom de l’option ; par exemple, « CompilerVersion ».|  
|`value`|Attribut requis.<br /><br /> Spécifie la valeur de l’option ; par exemple, « v3.5 ».|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<configuration>, élément](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|Élément racine dans chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|[\<System.CodeDom > élément](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)|Spécifie les paramètres de configuration du compilateur pour les fournisseurs de langages disponibles.|  
|[\<compilateurs > élément](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|Conteneur pour les éléments de configuration de compilateur ; contient zéro ou plusieurs `<compiler>` éléments.|  
|[\<compiler> Element](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)|Spécifie les attributs de configuration du compilateur pour un fournisseur de langage.|  
  
## <a name="remarks"></a>Notes  
 Dans le .NET Framework version 3.5, les fournisseurs de code Code Document Object Model (CodeDOM) peuvent prendre en charge les options spécifiques au fournisseur à l’aide de la `<providerOption>` élément.  
  
 Le .NET Framework 3.5 inclut des assemblys .NET Framework 2.0 mis à jour et fournit des assemblys 3.5 qui contiennent de nouveaux types. Les fournisseurs de code Microsoft c# et Visual Basic sont contenus dans les assemblys .NET Framework 2.0, mais ont été mis à jour pour prendre en charge les compilateurs de la version 3.5. Par défaut, les fournisseurs de code mis à jour génèrent du code pour les compilateurs de la version 2.0. Vous pouvez utiliser le `<providerOption>` élément pour modifier la version de compilateur cible en 3.5. Pour ce faire, spécifiez « CompilerVersion » pour le `name` attribut et « v3.5 » pour le `value` attribut. Vous devez faire précéder le numéro de version avec un « v » en minuscules.  
  
 Vous pouvez rendre la spécification de version global en ajoutant le `<providerOption>` élément au fichier racine Web.config ou Machine.config de .NET Framework 2.0. Si vous mettez à jour la version de compilateur par défaut à 3.5 dans le fichier Machine.config, vous pouvez le modifier à 2.0 sur chaque application à l’aide de la `<providerOption>` élément dans le fichier de configuration d’application.  
  
 Les implémenteurs de fournisseur de code codeDOM peuvent traiter des options personnalisées en fournissant un constructeur qui accepte un `providerOptions` paramètre de type <xref:System.Collections.Generic.IDictionary%602>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment spécifier la version 3.5 du fournisseur de code c# doit être utilisée.  
  
```xml  
<configuration>  
  <system.codedom>  
    <compilers>  
      <!-- zero or more compiler elements -->  
      <compiler  
        language="c#;cs;csharp"  
        extension=".cs"  
        type="Microsoft.CSharp.CSharpCodeProvider, System,   
          Version=2.0.3600.0, Culture=neutral,   
          PublicKeyToken=b77a5c561934e089"  
        compilerOptions="/optimize"  
        warningLevel="1" >  
          <providerOption  
            name="CompilerVersion"  
            value="v3.5" />  
      </compiler>  
    </compilers>  
  </system.codedom>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.CodeDom.Compiler.CompilerInfo>  
 <xref:System.CodeDom.Compiler.CodeDomProvider>  
 [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [\<compilateurs > élément](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)  
 [Spécification des noms de types complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)  
 [compiler, élément de compilers pour compilation (schéma des paramètres ASP.NET)](https://msdn.microsoft.com/library/f7d6b078-5d42-4134-b3f7-62e1aba1df1e)
