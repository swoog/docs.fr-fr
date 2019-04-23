---
title: Désactiver la prise en charge-DPI dans Visual Studio
description: Présente les limitations du Concepteur de Windows Forms sur les écrans HDPI et l’exécution de Visual Studio comme un processus dépendant PPP.
ms.date: 04/05/2019
ms.prod: visual-studio-windows
ms.technology: vs-ide-designers
author: gewarren
ms.author: gewarren
ms.custom: seoapril2019
ms.openlocfilehash: e52debea382033417afe0bd47f899af1666192bc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181378"
---
# <a name="disable-dpi-awareness-in-visual-studio"></a>Désactiver la prise en charge-DPI dans Visual Studio

Visual Studio est un points par pouce (PPP) application prenant en charge, ce qui signifie que les échelles affichage automatiquement. Si une application indique qu’il n’est pas reconnaissant les résolutions, le système d’exploitation met à l’échelle de l’application sous forme de bitmap. Ce comportement est également appelé virtualisation de PPP. L’application croit toujours qu’il s’exécute à la mise à l’échelle de 100 % ou 96 PPP.

Cet article décrit les limitations du Concepteur de formulaires Windows sur les écrans HDPI et l’exécution de Visual Studio comme un processus dépendant PPP.

## <a name="windows-forms-designer-on-hdpi-monitors"></a>Concepteur Windows Forms sur les écrans HDPI

Le **Windows Forms Designer** dans Visual Studio n’a pas prise en charge de mise à l’échelle. Cela entraîne des problèmes d’affichage lorsque vous ouvrez des formulaires dans le **Windows Forms Designer** sur élevé de points par pouce (HDPI) moniteurs. Pour obtenir des exemples, les contrôles peuvent semblent se chevaucher comme indiqué dans l’image suivante :

![Concepteur de formulaires Windows sur le moniteur HDPI](./media/disable-dpi-awareness-visual-studio/win-forms-designer-hdpi.png)

Lorsque vous ouvrez un formulaire dans le **Windows Forms Designer** dans Visual Studio sur un moniteur HDPI, Visual Studio affiche un jaune d’information de la barre en haut du concepteur :

![Barre d’information dans Visual Studio à redémarrer en mode dépendant PPP](./media/disable-dpi-awareness-visual-studio/scaling-gold-bar.png)

Lit le message **mise à l’échelle sur votre écran d’affichage principal est défini à 200 % (192 PPP). Cela peut entraîner des problèmes de rendu dans la fenêtre du concepteur.**

> [!NOTE]
> Cette barre d’information a été introduite dans Visual Studio 2017 version 15.8.

Si vous ne travaillez pas dans le concepteur et que vous n’avez pas besoin d’ajuster la disposition de votre formulaire, vous pouvez ignorer la barre d’information et continuer à travailler dans l’éditeur de code ou dans d’autres types de concepteurs. (Vous pouvez également [désactiver les notifications](#disable-notifications) afin que la barre d’information ne continue de s’afficher.) Uniquement les **Windows Forms Designer** est affecté. Si vous n’avez pas besoin de travailler dans le **Windows Forms Designer**, la section suivante vous aide à [résoudre le problème](#to-resolve-the-display-problem).

## <a name="to-resolve-the-display-problem"></a>Pour résoudre le problème d’affichage

Il existe trois options pour résoudre le problème d’affichage :

1. [Redémarrez Visual Studio comme un processus dépendant PPP](#restart-visual-studio-as-a-dpi-unaware-process)
2. [Ajouter une entrée de Registre](#add-a-registry-entry)
3. [Définissez votre affichage mise à l’échelle à 100 %](#set-your-display-scaling-setting-to-100)

### <a name="restart-visual-studio-as-a-dpi-unaware-process"></a>Redémarrez Visual Studio comme un processus dépendant PPP

Vous pouvez redémarrer Visual Studio en tant que PPP ne dépendant pas processus en sélectionnant l’option dans la barre d’information jaune. Il s’agit de la meilleure façon de résoudre le problème.

Lorsque Visual Studio s’exécute comme un processus dépendant PPP, les problèmes de disposition de concepteur sont résolus, mais les polices peuvent produire un flous. Visual Studio affiche un message d’information jaune différent lorsqu’elle s’exécute comme un processus dépendant PPP indiquant **Visual Studio s’exécute comme un processus dépendant PPP. Les concepteurs WPF et XAML peuvent ne pas s’afficher correctement.** La barre d’information fournit également une option permettant de **redémarrer Visual Studio en tant que reconnaissant les résolutions processus**.

> [!NOTE]
> - Si vous aviez désancrée fenêtres Outil dans Visual Studio lorsque vous avez sélectionné l’option de redémarrage en tant que PPP ne dépendant pas processus, la position de ces fenêtres Outil peut changer.
> - Si vous utilisez le profil de Visual Basic par défaut, ou si vous avez le **enregistrer les nouveaux projets lors de la création** option désélectionnée dans **outils** > **Options**  >  **Projets et Solutions**, Visual Studio ne peut pas rouvrir votre projet lorsqu’elle redémarre comme un processus dépendant PPP. Toutefois, vous pouvez ouvrir le projet en le sélectionnant sous **fichier** > **projets et Solutions récents**.

Il est important de redémarrer Visual Studio en tant que reconnaissant les résolutions processus lorsque vous avez fini de travailler le **Windows Forms Designer**. Lorsqu’il s’exécute comme un processus dépendant PPP, polices peuvent floues et que vous pouvez voir les problèmes dans les autres concepteurs tels que le **le concepteur XAML**. Si vous fermez et rouvrez Visual Studio lorsqu’il s’exécute en mode PPP ne dépendant pas, il devient reconnaissant à nouveau. Vous pouvez également cliquer sur le **redémarrer Visual Studio en tant que reconnaissant les résolutions processus** option dans la barre d’information.

### <a name="add-a-registry-entry"></a>Ajouter une entrée de Registre

Vous pouvez marquer Visual Studio comme dépendant PPP en modifiant le Registre. Ouvrez **Éditeur du Registre** et ajouter une entrée à la **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows NT\CurrentVersion\AppCompatFlags\Layers** sous-clé :

**Entrée**: Selon que vous utilisez Visual Studio 2017 ou 2019, utilisez une des valeurs suivantes :

- C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\devenv.exe
- C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\Common7\IDE\devenv.exe

> [!NOTE]
> Si vous utilisez l’édition Professional ou Enterprise de Visual Studio, remplacez **Communauté** avec **Professionnel** ou **Enterprise** dans l’entrée. Remplacez la lettre de lecteur en fonction des besoins.

**Type**: REG_SZ

**Valeur** : DPIUNAWARE

> [!NOTE]
> Visual Studio reste en mode PPP ne dépendant pas jusqu'à ce que vous supprimez l’entrée de Registre.

### <a name="set-your-display-scaling-setting-to-100"></a>Définissez votre affichage mise à l’échelle à 100 %

Pour définir l’affichage de votre mise à l’échelle de paramètre à 100 % dans Windows 10, tapez **paramètres d’affichage** dans la barre de zone de recherche, puis sélectionnez des tâches **modifier les paramètres d’affichage**. Dans le **paramètres** fenêtre, définissez **modifier la taille du texte, les applications et les autres éléments** à **100 %**.

Paramétrage de votre affichage mise à l’échelle à 100 % est peut-être pas souhaitable, car cela peut rendre l’interface utilisateur trop petite pour être utilisable.

## <a name="disable-notifications"></a>Désactiver les notifications

Vous pouvez choisir ne pas d’être averti de PPP mise à l’échelle des problèmes dans Visual Studio. Vous souhaiterez peut-être désactiver les notifications si vous ne travaillez pas dans le concepteur, par exemple.

Pour désactiver les notifications, choisissez **outils** > **Options** pour ouvrir le **Options** boîte de dialogue. Ensuite, choisissez **Windows Forms Designer** > **général**et définissez **Notifications de mise à l’échelle PPP** à **False**.

![Résolution de mise à l’échelle d’option de notifications dans Visual Studio](./media/disable-dpi-awareness-visual-studio/notifications-option.png)

Si vous souhaitez réactiver ultérieurement les notifications de mise à l’échelle, définissez la propriété sur **True**.

## <a name="troubleshoot"></a>Résoudre les problèmes

Si la transition prise en charge DPI ne fonctionne pas comme prévu dans Visual Studio, vérifiez si vous avez le `dpiAwareness` valeur dans le **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image fichier exécution Options\devenv.exe**  sous-clé dans l’Éditeur du Registre. Supprimez la valeur si elle est présente.

## <a name="see-also"></a>Voir aussi

- [Automatique mise à l’échelle dans les Windows Forms](automatic-scaling-in-windows-forms.md)
