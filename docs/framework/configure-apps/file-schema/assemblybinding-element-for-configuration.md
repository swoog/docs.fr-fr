---
title: '&lt;assemblyBinding&gt; élément pour &lt;configuration&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/assemblyBinding
helpviewer_keywords:
- assemblyBinding Element
- <assemblyBinding> Element
ms.assetid: 6cc55983-b894-449b-8e26-b258e53939cd
ms.openlocfilehash: 12065d8bc484f7bbf77ae18c67df1de0845167b2
ms.sourcegitcommit: b351b0781a035616c90c68ccae6dd60aae66a953
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55083897"
---
# <a name="assemblybinding-element-for-configuration"></a>\<assemblyBinding >, élément pour \<configuration >

Spécifie la stratégie de liaison de l’assembly au niveau de la configuration.

[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md)   
&nbsp;&nbsp;**\<assemblyBinding>**

## <a name="syntax"></a>Syntaxe

```xml
<assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
  <!-- Configuration files to include. -->
</assemblyBinding>
```

## <a name="attribute"></a>Attribut

|           | Description |
| --------- | ----------- |
| **xmlns** | Attribut requis.<br><br>Spécifie l'espace de noms XML requis pour la liaison d'assembly. Utilisez la chaîne « urn:schemas-microsoft-com:asm.v1 » comme valeur. |

## <a name="parent-element"></a>Élément parent

|     | Description |
| --- | ----------- |
| [**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) | Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework. |

## <a name="child-element"></a>Élément enfant

|     | Description |
| --- | ----------- |
| [**\<linkedConfiguration>**](~/docs/framework/configure-apps/file-schema/linkedconfiguration-element.md) | Spécifie un fichier de configuration à inclure. |

## <a name="remarks"></a>Notes

Le [  **\<linkedConfiguration >** ](~/docs/framework/configure-apps/file-schema/linkedconfiguration-element.md) élément simplifie la gestion des assemblys de composant en permettant aux fichiers de configuration d’application pour inclure l’assembly dans les fichiers de configuration emplacements bien connus, plutôt que les paramètres de configuration assembly duplication.

> [!NOTE]
> Le  **\<linkedConfiguration >** élément n’est pas pris en charge pour les applications avec des manifestes côte à côte de Windows.

## <a name="example"></a>Exemple

L’exemple suivant montre comment inclure un fichier de configuration sur le disque dur local :

```xml
<configuration>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
    <linkedConfiguration href="file://c:\Program Files\Contoso\sharedConfig.xml" />
  </assemblyBinding>
</configuration>
```

## <a name="see-also"></a>Voir aussi

- [Schéma de fichier de configuration pour le .NET Framework](~/docs/framework/configure-apps/file-schema/index.md)
