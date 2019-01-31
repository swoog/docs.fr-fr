---
title: <clear> (élément de <configSections>)
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections/clear
helpviewer_keywords:
- clear Element
- <clear> Element
ms.assetid: 77f1d761-ff45-4001-8f36-3a3e5c41fa63
author: guardrex
ms.author: mairaw
ms.openlocfilehash: d824ae828dd025f3292990facaa5e423add9c282
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55254762"
---
# <a name="clear-element-for-configsections"></a>\<Désactivez >, élément pour \<configSections >

Efface toutes les sections précédemment définies et les groupes de sections.

[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md)   
&nbsp;&nbsp;[**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md)   
&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**

## <a name="syntax"></a>Syntaxe

```xml
<clear/>
```

## <a name="attribute"></a>Attribut

|           | Description |
| --------- | ----------- |
| **name**  | Attribut requis.<br><br>Spécifie le nom de la section ou le groupe de section à supprimer. |

## <a name="parent-element"></a>Élément parent

|     | Description |
| --- | ----------- |
| [**\<configSections >** élément](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) | Contient des déclarations d’espace de noms et de la section de configuration. |

## <a name="child-elements"></a>Éléments enfants

Aucun.

## <a name="remarks"></a>Notes

Le  **\<Effacer >** élément supprime toutes les sections et groupes de votre application qui ont été définis précédemment dans le fichier de configuration actuel ou à un niveau supérieur dans la hiérarchie de fichiers de configuration.

## <a name="example"></a>Exemple

Cet exemple définit un fichier de configuration d’ordinateur et un fichier de configuration d’application et montre comment utiliser le  **\<Effacer >** élément dans un fichier de configuration d’application pour effacer les sections définies précédemment dans le fichier de configuration machine.

Le code du fichier de configuration machine suivant déclare deux sections,  **\<sampleSection >** et  **\<anotherSampleSection >**, qui sont lus avant que l’application fichier de configuration :

```xml
<!-- Machine.config file -->
<configuration>
  <configSections>
    <section name="sampleSection"
             type="System.Configuration.SingleTagSectionHandler" />
    <section name="anotherSampleSection"
             type="System.Configuration.NameValueSectionHandler" />
  </configSections>
  <sampleSection setting1="Value1" 
                 setting2="value two" 
                 setting3="third value" />
</configuration>
```

Le code suivant du fichier de configuration de l’application efface toutes les sections déclarées précédemment. L’application ne peut pas utiliser ou récupérer des paramètres dans les sections qui ont été déclarées dans le fichier de configuration machine. Toutefois, il peut utiliser les paramètres à partir de  **\<anotherSection >** , car elle vient après le  **\<Effacer >** élément.

```xml
<!-- Application configuration file -->
<configuration>
  <configSections>
    <clear/>
    <section name="anotherSection"
             type="System.Configuration.NameValueSectionHandler" />
  </configSections>
  <anotherSection setting1="Value1" 
                 setting2="value two" 
                 setting3="third value" />
</configuration>
```

## <a name="configuration-file"></a>fichier de configuration

Cet élément peut être utilisé dans le fichier de configuration d’application, fichier de configuration machine (*Machine.config*), et *Web.config* fichiers qui ne sont pas au niveau du répertoire d’application.

## <a name="see-also"></a>Voir aussi

- [Schéma de fichier de configuration pour le .NET Framework](~/docs/framework/configure-apps/file-schema/index.md)
