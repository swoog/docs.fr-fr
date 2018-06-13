---
title: Installer le .NET Framework 3.5 sur Windows 10, Windows 8.1 et Windows 8
description: Découvrez comment installer .NET Framework 3.5 sur Windows 10, Windows 8.1 et Windows 8.
author: rlander
ms.author: mairaw
ms.date: 03/30/2018
ms.openlocfilehash: 226449b8ee7c9360e6bfdc5bfa5dfeb59f19bd2b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33387414"
---
# <a name="install-the-net-framework-35-on-windows-10-windows-81-and-windows-8"></a>Installer le .NET Framework 3.5 sur Windows 10, Windows 8.1 et Windows 8

Vous pouvez avoir besoin de .NET Framework 3.5 pour exécuter une application sur Windows 10, Windows 8.1 et Windows 8. Vous pouvez également utiliser ces instructions pour les versions antérieures de Windows.

## <a name="install-the-net-framework-35-on-demand"></a>Installer .NET Framework 3.5 à la demande

Vous pouvez voir la boîte de dialogue de configuration suivante si vous essayez d’exécuter une application qui nécessite .NET Framework 3.5. Choisissez **Installer cette fonctionnalité** pour activer le .NET Framework 3.5. Cette option requiert une connexion Internet.

![Boîte de dialogue d’installation du .NET Framework](./media/dotnet-framework-installation-dialog.jpg)

### <a name="why-am-i-getting-this-pop-up"></a>Pourquoi cette fenêtre contextuelle apparaît-elle ?

Le .NET Framework est créé par Microsoft et fournit un environnement d’exécution d’applications. Différentes versions sont disponibles. De nombreuses entreprises développent leurs applications pour qu’elles s’exécutent avec le .NET Framework, et ces applications en ciblent une version spécifique. Si vous voyez cette fenêtre contextuelle, cela signifie que vous tentez d’exécuter une application qui nécessite le .NET Framework version 3.5, mais que cette version n’est pas installée sur votre système.

## <a name="enable-the-net-framework-35-in-control-panel"></a>Activer .NET Framework 3.5 dans le Panneau de configuration

Vous pouvez activer le .NET Framework 3.5 dans le Panneau de configuration de Windows. Cette option requiert une connexion Internet.

1. Appuyez sur la touche Windows ![logo Windows](https://i-msdn.sec.s-msft.com/dynimg/IC721376.jpeg) de votre clavier, tapez « Fonctionnalités Windows » puis appuyez sur Entrée. La boîte de dialogue **Activer ou désactiver des fonctionnalités Windows** apparaît.

2. Cochez la case **.NET Framework 3.5 (inclut .NET 2.0 et 3.0)**, sélectionnez **OK** et redémarrez l’ordinateur si vous y êtes invité.

   ![Installation de .NET avec le Panneau de configuration](./media/dotnet-control-panel.png)

   Vous n’avez pas besoin de sélectionner des éléments enfants pour **Activation HTTP de Windows Communication Foundation** et **Activation non-HTTP de Windows Communication Foundation**, sauf si vous êtes un développeur ou un administrateur de serveur ayant besoin de cette fonctionnalité.

## <a name="troubleshoot-the-installation-of-the-net-framework-35"></a>Résoudre les problèmes d’installation du .NET Framework 3.5

Pendant l’installation, si vous rencontrez l’erreur 0x800f0906, 0x800f0907, 0x800f081f ou 0x800F0922, consultez [Erreur d’installation de .NET Framework 3.5 : 0x800f0906, 0x800f0907 ou 0x800f081f](https://support.microsoft.com/help/2734782/net-framework-3-5-installation-error-0x800f0906--0x800f081f--0x800f09) pour découvrir comment résoudre ces problèmes.

Si vous ne pouvez toujours pas résoudre votre problème d’installation ou si vous n’avez pas de connexion Internet, vous pouvez essayer de l’installer en utilisant votre support d’installation Windows. Pour plus d’informations, consultez [Déployer le .NET Framework 3.5 à l’aide de Gestion et maintenance des images de déploiement (DISM)](/windows-hardware/manufacture/desktop/deploy-net-framework-35-by-using-deployment-image-servicing-and-management--dism). Si vous ne disposez pas du support d’installation, consultez [Créer un support d’installation pour Windows](https://support.microsoft.com/help/15088/windows-create-installation-media).
