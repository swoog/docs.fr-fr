---
title: Prise en charge de haute résolution dans les Windows Forms
ms.date: 05/16/2017
helpviewer_keywords:
- High DPI in Windows Forms
- Dynamic rescaling in Windows Forms
- Windows Forms layout
- Windows Forms dynamic resizing
ms.assetid: 075ea4c3-900c-4f8a-9dd2-13ea6804346b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1641702c7b1c3d3b0e83c59a96529de70f699d17
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61966944"
---
# <a name="high-dpi-support-in-windows-forms"></a>Prise en charge de haute résolution dans les Windows Forms

À compter de .NET Framework 4.7, Windows Forms inclut des améliorations pour la haute résolution courants et scénarios de résolution dynamiques. Elles incluent notamment :

- Améliorations de la mise à l’échelle et la disposition d’un nombre de Windows Forms des contrôles, tels que le <xref:System.Windows.Forms.MonthCalendar> contrôle et le <xref:System.Windows.Forms.CheckedListBox> contrôle.

- Mise à l’échelle seul passage.  Dans le .NET Framework 4.6 et les versions antérieures, la mise à l’échelle a été effectuée via plusieurs passes, ce qui a provoqué des contrôles à l’échelle plus de données nécessaires.

- Prise en charge pour les scénarios de résolution dynamiques dans lequel l’utilisateur modifie le facteur de PPP ou mise à l’échelle après le lancement d’une application Windows Forms.

Dans les versions du .NET Framework en commençant par le .NET Framework 4.7, une prise en charge améliorée de la haute résolution est une fonctionnalité à activer. Vous devez configurer votre application pour tirer parti de celui-ci.

## <a name="configuring-your-windows-forms-app-for-high-dpi-support"></a>Configuration de votre application Windows Forms pour la prise en charge de haute résolution

Les nouvelles fonctionnalités de Windows Forms qui prennent en charge de la prise en charge DPI élevé sont disponibles uniquement dans les applications qui ciblent le .NET Framework 4.7 et sont en cours d’exécution sur les systèmes d’exploitation Windows en commençant par Windows 10 Creators Update.

En outre, pour configurer la prise en charge de haute résolution dans votre application Windows Forms, vous devez procédez comme suit :

- Déclarer la compatibilité avec Windows 10.

  Pour ce faire, ajoutez le code suivant à votre fichier manifeste :

  ```xml
  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
    <application>
      <!-- Windows 10 compatibility -->
      <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}" />
    </application>
  </compatibility>
  ```

- Activer la sensibilisation à la résolution par moniteur dans le *app.config* fichier.

  Windows Forms propose un nouveau [ `<System.Windows.Forms.ApplicationConfigurationSection>` ](../configure-apps/file-schema/winforms/index.md) élément pour prendre en charge les nouvelles fonctionnalités et les personnalisations ajoutées en commençant par le .NET Framework 4.7. Pour tirer parti des nouvelles fonctionnalités qui prennent en charge la haute résolution, ajoutez le code suivant au fichier de configuration de votre application.

  ```xml
  <System.Windows.Forms.ApplicationConfigurationSection>
    <add key="DpiAwareness" value="PerMonitorV2" />
  </System.Windows.Forms.ApplicationConfigurationSection>
  ```

  > [!IMPORTANT]
  > Dans les versions précédentes du .NET Framework, vous avez utilisé le manifeste pour ajouter la prise en charge de haute résolution. Cette approche n’est plus recommandée, car il substitue les paramètres définis dans le fichier app.config.

- Appelez la méthode statique <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> (méthode).

  Il doit s’agir du premier appel de méthode dans le point d’entrée de votre application. Exemple :

  ```csharp
  static void Main()
  {
      Application.EnableVisualStyles();
      Application.SetCompatibleTextRenderingDefault(false);
      Application.Run(new Form2());
  }
  ```

## <a name="opting-out-of-individual-high-dpi-features"></a>Désactivation de la fonctionnalités de PPP élevées individuelles

Définition de la `DpiAwareness` valeur `PerMonitorV2` Active les fonctionnalités de la reconnaissance PPP élevées tout pris en charge par les versions du .NET Framework en commençant par le .NET Framework 4.7. En règle générale, cela est suffisant pour la plupart des applications Windows Forms. Toutefois, vous souhaiterez refuser un ou plusieurs des fonctionnalités individuelles. La raison la plus importante pour cette opération est que votre code d’application existant gère déjà cette fonctionnalité.  Par exemple, si votre application gère la mise à l’échelle automatique, vous souhaiterez désactiver la fonctionnalité de redimensionnement automatique comme suit :

```xml
<System.Windows.Forms.ApplicationConfigurationSection>
  <add key="DpiAwareness" value="PerMonitorV2" />
  <add key="EnableWindowsFormsHighDpiAutoResizing" value="false" />
</System.Windows.Forms.ApplicationConfigurationSection>
```

Pour obtenir la liste des clés individuelles et leurs valeurs, consultez [élément de Configuration Add Windows Forms](../configure-apps/file-schema/winforms/windows-forms-add-configuration-element.md).

## <a name="new-dpi-change-events"></a>Nouveaux événements de modification de PPP

À compter de .NET Framework 4.7, trois nouveaux événements vous autorise à gérer par programme les modifications de résolution dynamiques :

- <xref:System.Windows.Forms.Control.DpiChangedAfterParent>, qui est déclenché quand le paramètre DPI d’un contrôle est modifié par programme après un événement de modification de PPP pour le contrôle de son parent ou formulaire s’est produite.
- <xref:System.Windows.Forms.Control.DpiChangedBeforeParent>, qui est déclenché lorsque le paramètre DPI d’un contrôle est modifié par programme avant qu’un événement de modification de PPP pour son contrôle parent ou le formulaire s’est produite.
- <xref:System.Windows.Forms.Form.DpiChanged>, qui est déclenché lorsque le paramètre DPI est modifié sur le périphérique d’affichage dans lequel le formulaire est actuellement affiché.

## <a name="new-helper-methods-and-properties"></a>Propriétés et nouvelles méthodes d’assistance

Le .NET Framework 4.7 ajoute également un nombre de nouvelles méthodes d’assistance et des propriétés qui fournissent des informations sur la mise à l’échelle PPP et que vous puissiez effectuer la mise à l’échelle PPP. Elles incluent notamment :

- <xref:System.Windows.Forms.Control.LogicalToDeviceUnits%2A>, qui convertit une valeur exprimé en coordonnées logiques en pixels de périphérique.

- <xref:System.Windows.Forms.Control.ScaleBitmapLogicalToDevice%2A>, qui met à l’échelle d’une image bitmap à la valeur PPP logique pour un périphérique.

- <xref:System.Windows.Forms.Control.DeviceDpi%2A>, qui retourne la valeur PPP pour l’appareil en cours.

## <a name="versioning-considerations"></a>Considérations relatives à la gestion des versions

Outre l’exécution sur .NET Framework 4.7 et Windows 10 Creators Update, votre application peut également exécuter dans un environnement dans lequel il n’est pas compatible avec les améliorations de PPP élevées. Dans ce cas, vous devez développer une procédure de secours pour votre application. Vous pouvez le faire pour effectuer [dessin personnalisé](./controls/user-drawn-controls.md) pour gérer la mise à l’échelle.

Pour ce faire, vous devez également déterminer le système d’exploitation sur lequel votre application est en cours d’exécution. Vous pouvez le faire avec un code semblable au suivant :

```csharp
// Create a reference to the OS version of Windows 10 Creators Update.
Version OsMinVersion = new Version(10, 0, 15063, 0);

// Access the platform/version of the current OS.
Console.WriteLine(Environment.OSVersion.Platform.ToString());
Console.WriteLine(Environment.OSVersion.VersionString);

// Compare the current version to the minimum required version.
Console.WriteLine(Environment.OSVersion.Version.CompareTo(OsMinVersion));
```

Notez que votre application ne détecte avec succès Windows 10 si elle n’a pas été répertoriée comme un système d’exploitation pris en charge dans le manifeste d’application.

Vous pouvez également vérifier la version du .NET Framework que l’application a été développée pour :

```csharp
Console.WriteLine(AppDomain.CurrentDomain.SetupInformation.TargetFrameworkName);
```

## <a name="see-also"></a>Voir aussi

- [Windows Forms Add, élément de Configuration](../configure-apps/file-schema/winforms/windows-forms-add-configuration-element.md)
- [Réglage de la taille et de l'échelle des Windows Forms](adjusting-the-size-and-scale-of-windows-forms.md)
