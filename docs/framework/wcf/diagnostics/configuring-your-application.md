---
title: Configuration de votre application
ms.date: 03/30/2017
ms.assetid: a2f995b0-669d-4721-b00f-4561ec7eb6a4
ms.openlocfilehash: e06c428526c5383c6908521075cd2eca977ce89f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43481234"
---
# <a name="configuring-your-application"></a>Configuration de votre application
Windows Communication Foundation (WCF) utilise le système de configuration .NET et vous permet de configurer les services sur l’ordinateur et application étendue.  
  
 Paramètres de configuration définis par WCF se trouvent dans le `<system.serviceModel>` groupe de sections. Pour plus d’informations sur la façon de configurer un service WCF, consultez les rubriques suivantes :  
  
-   [Configuration des services](../../../../docs/framework/wcf/configuring-services.md)  
  
-   [\<system.serviceModel>](../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)  
  
 Les paramètres de configuration définis par l'application sont définis dans le groupe de sections `<appSettings>`. Pour plus d’informations sur les paramètres d’application dans les fichiers de configuration .NET, consultez [ \<appSettings >](https://go.microsoft.com/fwlink/?LinkId=95159).  
  
## <a name="using-the-configuration-editor"></a>Utilisation de l'Éditeur de configuration  
 WCF[l’outil Éditeur de Configuration (SvcConfigEditor.exe)](../../../../docs/framework/wcf/configuration-editor-tool-svcconfigeditor-exe.md) permet aux administrateurs et aux développeurs de créer et modifier les paramètres de configuration pour les services WCF à l’aide d’une interface utilisateur graphique. Avec cet outil, vous pouvez gérer les paramètres pour les liaisons, comportements, services et diagnostics WCF sans modifier directement les fichiers de configuration XML.  
  
## <a name="editing-configuration-files-in-visual-studio"></a>Modification des fichiers de configuration dans Visual Studio  
 Pour modifier le fichier de configuration d’un projet de service WCF dans Visual Studio, avec le bouton droit dessus dans **l’Explorateur de solutions** et choisissez le **modifier la configuration WCF** élément de menu contextuel. Cette opération lance le [l’outil Éditeur de Configuration (SvcConfigEditor.exe)](../../../../docs/framework/wcf/configuration-editor-tool-svcconfigeditor-exe.md).  
  
> [!NOTE]
>  Si vous modifiez le fichier de configuration d’un projet de Service Web WCF dans Visual Studio en double-cliquant sur dans **l’Explorateur de solutions**, notez que le **modifier la configuration WCF** élément de menu contextuel est manquant. Pour contourner ce problème, cliquez sur le **outils** menu, puis choisissez **éditeur de configuration de Service WCF**. Après cela, vous pouvez cliquez sur un fichier de configuration et utiliser le **modifier la configuration WCF** élément de menu contextuel.  
  
## <a name="see-also"></a>Voir aussi  
 [Outil Éditeur de configuration (SvcConfigEditor.exe)](../../../../docs/framework/wcf/configuration-editor-tool-svcconfigeditor-exe.md)  
 [Configuration des services](../../../../docs/framework/wcf/configuring-services.md)  
 [\<system.serviceModel>](../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)
