---
title: Profileurs CLR et les applications du Windows Store
ms.date: 03/30/2017
dev_langs:
- csharp
applies_to:
- Windows 10
- Windows 8
helpviewer_keywords:
- profiling API
- profiling API [.NET Framework]
- profiling managed code
- profiling managed code [Windows Store Apps]
ms.assetid: 1c8eb2e7-f20a-42f9-a795-71503486a0f5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 27e1433415bdc6303555ab9ae04a20e097248535
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46538006"
---
# <a name="clr-profilers-and-windows-store-apps"></a>Profileurs CLR et les applications du Windows Store

Cette rubrique explique ce que vous devez réfléchir à lorsque les outils de diagnostic d’écriture qui analysent géré code en cours d’exécution à l’intérieur d’une application Windows Store. Il fournit également des instructions pour modifier vos outils de développement existants afin qu’ils continuent de fonctionner lorsque vous les exécutez contre les applications Windows Store. Pour comprendre ces informations, il est préférable de que si vous êtes familiarisé avec l’API de profilage de Common Language Runtime, vous avez déjà utilisé cette API dans un outil de diagnostic que s’exécute correctement sur les applications de bureau Windows et vous êtes maintenant intéressé par la modification de l’outil Pour exécuter correctement sur les applications du Windows Store.

## <a name="introduction"></a>Introduction

Si vous l’avez fait après le paragraphe d’introduction, vous êtes familiarisé avec l’API de profilage CLR. Vous avez déjà écrit un outil de diagnostic qui fonctionne bien avec les applications de bureau gérées. Maintenant vous êtes curieux de savoir ce qu’il faut faire pour que votre outil fonctionne avec une application gérée par Windows Store. Vous avez peut-être déjà essayé pour y parvenir et ont découvert qu’il n’est pas une tâche simple. En effet, il existe un certain nombre de considérations qui n’est peut-être pas évident à tous les développeurs d’outils. Exemple :

- Applications du Windows Store s’exécuter dans un contexte avec des autorisations réduites considérablement.

- Fichiers de métadonnées de Windows ont des caractéristiques uniques par rapport aux modules gérés traditionnels.

- Applications du Windows Store ont l’habitude de suspension eux-mêmes lors de l’interactivité tombe en panne.

- Vos mécanismes de communication inter-processus peuvent ne plus fonctionner pour diverses raisons.

Cette rubrique répertorie les choses à connaître et comment les traiter correctement.

Si vous débutez avec l’API de profilage CLR, passez à des ressources à la fin de cette rubrique pour trouver des informations de mieux.

Qui fournit des détails sur les API Windows spécifique et comment ils doivent être utilisés est également en dehors de l’étendue de cette rubrique. Envisagez de cette rubrique, un point de départ et reportez-vous à MSDN pour en savoir plus sur les API Windows référencé ici.

## <a name="architecture-and-terminology"></a>Architecture et la terminologie

En règle générale, un outil de diagnostic possède une architecture comme celui illustré dans l’illustration suivante. Il utilise le terme « profiler », mais beaucoup de ces outils aller bien au-delà des performances standard ou de profilage de mémoire dans des domaines tels que la couverture du code, simuler les infrastructures d’objets, le débogage, l’application de surveillance et ainsi de suite-voyage. Par souci de simplicité, cette rubrique se continueront de faire référence à tous ces outils comme les profileurs.

La terminologie suivante est utilisée tout au long de cette rubrique :

**Application**

Il s’agit de l’application qui analyse le profileur. En règle générale, le développeur de cette application est maintenant en utilisant le profileur pour aider à diagnostiquer les problèmes liés à l’application. En règle générale, cette application serait une application de bureau Windows, mais dans cette rubrique, nous nous intéressons à des applications du Windows Store.

**DLL de Profiler**

C’est le composant qui se charge dans l’espace de processus de l’application en cours d’analyse. Ce composant, également connu sous le profileur « agent », implémente la [ICorProfilerCallback](icorprofilercallback-interface.md)[ICorProfilerCallback, Interface](icorprofilercallback-interface.md)(2, 3, etc.) interfaces et consomme les [ ICorProfilerInfo](icorprofilerinfo-interface.md)(2, 3, etc.) interfaces pour collecter des données relatives à l’application analysée et, potentiellement, modifier des aspects du comportement de l’application.

**Profiler l’interface utilisateur**

Il s’agit de l’utilisateur du profileur interagit avec une application de bureau. Il est responsable de l’affichage de l’état de l’application à l’utilisateur et de donner à l’utilisateur les moyens de contrôler le comportement de l’application analysée. Ce composant s’exécute toujours dans son propre espace de processus séparé à partir de l’espace de processus de l’application en cours de profilage. L’interface utilisateur de Profiler peut également agir comme le « attachement déclencheur, » qui est le processus qui appelle le [ICLRProfiling::AttachProfiler](iclrprofiling-attachprofiler-method.md) (méthode), pour charger la DLL de Profiler dans les cas où la DLL du profileur n’a pas l’application analysées charger au démarrage.

> [!IMPORTANT]
> Votre interface utilisateur de Profiler doit rester une application de bureau Windows, même quand il est utilisé pour le contrôle et les rapports sur une application Windows Store. Ne pensez pas être en mesure d’empaqueter et livrer votre outil de diagnostic dans le Windows Store. Votre outil a besoin d’effectuer des opérations qui ne peut pas les applications Windows Store, et la plupart de ces éléments se trouvent à l’intérieur de votre interface utilisateur de Profiler.

Tout au long de ce document, l’exemple de code suppose que :

- Votre DLL de Profiler est écrit en C++, car il doit être une DLL native, conformément à la configuration requise de l’API de profilage CLR.

- Votre interface utilisateur de Profiler est écrit en c#. Cela n’est pas nécessaire, mais comme il n’y a aucune exigence sur le langage pour les processus de l’interface utilisateur de votre Profiler, pourquoi ne pas choisir un langage simple et concise ?

### <a name="windows-rt-devices"></a>Périphériques Windows RT

Périphériques Windows RT sont assez verrouillés. Profileurs tiers ne peut pas être simplement chargés sur ces appareils. Ce document se concentre sur les PC Windows 8.

## <a name="consuming-windows-runtime-apis"></a>Utilisation des API de Windows Runtime

Dans un nombre de scénarios présentés dans les sections suivantes, votre application de bureau de l’interface utilisateur du Profiler doit utiliser certaines nouvelles Windows Runtime APIs. Vous souhaitez consulter la documentation pour comprendre lesquelles API de Runtime Windows peuvent être utilisées à partir d’applications de bureau, et si leur comportement diffère lorsque appelé à partir d’applications de bureau et Windows Store d’applications.

Si votre interface utilisateur de Profiler est écrit en code managé, il y aura quelques étapes, que vous devez faire pour que la consommation de ces Windows APIs Runtime facile. Consultez le [gérés des applications de bureau et Windows Runtime](https://go.microsoft.com/fwlink/?LinkID=271858) article pour plus d’informations.

## <a name="loading-the-profiler-dll"></a>Le chargement de la DLL de Profiler

Cette section décrit la façon dont votre interface utilisateur de Profiler entraîne l’application du Windows Store charger la DLL à Profiler. Le code présenté dans cette section appartienne dans votre application de bureau de l’interface utilisateur du Profiler et par conséquent implique l’utilisation des API Windows qui sont sécurisés pour les applications de bureau, mais pas nécessairement sécurisés pour les applications du Windows Store.

Votre interface utilisateur de Profiler peut entraîner la DLL de Profiler à charger dans l’espace de processus de l’application de deux manières :

- Au démarrage de l’application, contrôlé par les variables d’environnement.

- En attachant à l’application après le démarrage est terminé en appelant le [ICLRProfiling::AttachProfiler](iclrprofiling-attachprofiler-method.md) (méthode).

Un de votre première obstacles obtiendrez chargement au démarrage et chargement par attachement de votre DLL de Profiler fonctionne correctement avec les applications du Windows Store. Les deux formes de chargement partagent certaines considérations particulières en commun, par conséquent, nous allons commencer avec eux.

### <a name="common-considerations-for-startup-and-attach-loads"></a>Considérations générales pour le démarrage et d’attachement des charges

**Signature de votre DLL de Profiler**

Lorsque Windows tente de charger votre DLL de Profiler, il vérifie que votre DLL de Profiler est correctement signé. Si ce n’est pas le cas, le chargement échoue par défaut. Il existe deux façons d'effectuer cette opération :

- Assurez-vous que votre DLL de Profiler est signé.

- Indiquez votre utilisateur qu’ils doivent installer à une licence de développeur sur leur ordinateur Windows 8, avant d’utiliser votre outil. Cela est possible automatiquement à partir de Visual Studio ou manuellement à partir d’une invite de commandes. Pour plus d’informations, consultez [obtenir une licence de développeur](https://msdn.microsoft.com/library/windows/apps/Hh974578.aspx).

**Autorisations de système de fichiers**

L’application du Windows Store doit être autorisé à charger et exécuter votre DLL de Profiler à partir de l’emplacement sur le système de fichiers dans lequel il residesBy défaut, l’application du Windows Store n’a pas cette autorisation sur la plupart des répertoires et ayant échoué, toute tentative de charger votre DLL de Profiler génère une entrée dans le journal des événements Windows Application qui ressemble à ceci :

```Output
NET Runtime version 4.0.30319.17929 - Loading profiler failed during CoCreateInstance.  Profiler CLSID: '{xxxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}'.  HRESULT: 0x80070005.  Process ID (decimal): 4688.  Message ID: [0x2504].
```

En règle générale, les applications Windows Store sont uniquement autorisées à accéder à un ensemble limité d’emplacements sur le disque. Chaque application du Windows Store permettre accéder à ses propres dossiers de données d’application, ainsi que quelques autres zones du système de fichiers pour lequel toutes les applications du Windows Store ont accès. Il est préférable d’installer la DLL de Profiler et ses dépendances quelque part sous Program Files ou Program Files (x86), étant donné que toutes les applications du Windows Store ont lu et il les autorisations d’exécution par défaut.

### <a name="startup-load"></a>Chargement au démarrage

En règle générale, dans une application de bureau, votre interface utilisateur de Profiler vous invite à entrer un chargement au démarrage de votre DLL à Profiler en initialisant un bloc d’environnement qui contient les variables d’environnement API de profilage CLR requis (par exemple, `COR_PROFILER`, `COR_ENABLE_PROFILING`, et `COR_PROFILER_PATH`), et puis en créant un nouveau processus avec ce bloc d’environnement. Va de même pour les applications du Windows Store, mais les mécanismes sont différents.

**Ne pas exécuter avec élévation de privilèges**

Si le processus tente de générer dynamiquement le Windows Store app B de processus, le processus A doit être exécuté avec une intégrité moyenne niveau, non au niveau de haut niveau d’intégrité (qui est, pas avec privilège élevé). Cela signifie que votre interface utilisateur de Profiler doit être en cours d’exécution au niveau d’intégrité moyen, ou il doit générer un autre processus bureau au niveau d’intégrité moyen pour prendre en charge du lancement de l’application du Windows Store.

**Choix d’une application de Store Windows au profil**

Tout d’abord, vous souhaitez demander à votre utilisateur de profileur quelle application Windows Store pour lancer. Pour les applications de bureau, peut-être vous affiche une boîte de dialogue Parcourir, et l’utilisateur serait rechercher et sélectionner un fichier .exe. Mais les applications du Windows Store sont différentes, et à l’aide d’une boîte de dialogue Parcourir n’est pas pertinent. Au lieu de cela, il est préférable d’afficher la liste des applications Windows Store installées pour cet utilisateur à sélectionner à partir de l’utilisateur.

Vous pouvez utiliser la [PackageManager classe](https://msdn.microsoft.com/library/windows/apps/windows.management.deployment.packagemanager.aspx) pour générer cette liste. `PackageManager` est une classe Windows Runtime qui est disponible pour les applications de bureau, et il est en fait *uniquement* disponibles pour les applications de bureau.

L’exemple de code suivant à partir d’une interface utilisateur du Profiler hypothétique écrit sous la forme d’une application de bureau dans c# yses le `PackageManager` pour générer une liste d’applications de Windows :

```csharp
string currentUserSID = WindowsIdentity.GetCurrent().User.ToString();
IAppxFactory appxFactory = (IAppxFactory) new AppxFactory();
PackageManager packageManager = new PackageManager();
IEnumerable<Package> packages = packageManager.FindPackagesForUser(currentUserSID);
```

**En spécifiant le bloc environnement personnalisé**

Une nouvelle interface COM, [IPackageDebugSettings](https://msdn.microsoft.com/library/hh438393\(v=vs.85\).aspx), vous permet de personnaliser le comportement de l’exécution d’une application Windows Store pour simplifier certaines formes de diagnostics. Une de ses méthodes, [EnableDebugging](https://msdn.microsoft.com/library/hh438395\(v=vs.85\).aspx), vous permet de passer un bloc d’environnement à l’application du Windows Store lorsqu’elle est lancée, ainsi que d’autres effets utiles comme la désactivation de suspension de processus automatique. Le bloc d’environnement est important car il s’agit d’où vous devez spécifier les variables d’environnement (`COR_PROFILER`, `COR_ENABLE_PROFILING`, et `COR_PROFILER_PATH)`) utilisé par le CLR pour charger votre DLL de Profiler.

Examinez l’extrait de code suivant :

```csharp
IPackageDebugSettings pkgDebugSettings = new PackageDebugSettings();
pkgDebugSettings.EnableDebugging(packgeFullName, debuggerCommandLine, 
                                                                 (IntPtr)fixedEnvironmentPzz);
```

Il existe deux éléments, que vous devez obtenir le droit :

- `packageFullName` Vous pouvez déterminer tout en effectuant une itération sur les packages et en saisissant `package.Id.FullName`.

- `debuggerCommandLine` est un peu plus intéressant. Pour transmettre le bloc environnement personnalisé à l’application du Windows Store, vous devez écrire votre propre, débogueur factice simpliste. Génère de Windows, l’application du Windows Store suspendu et joint ensuite votre débogueur en lançant votre débogueur de ligne de commande, comme dans cet exemple :

    ```Output
    MyDummyDebugger.exe -p 1336 -tid 1424
    ```

     où `-p 1336` signifie que l’application du Windows Store a 1336 d’ID de processus, et `-tid 1424` signifie 1424 d’ID de Thread est le thread est suspendu. Votre débogueur factice voulez-vous analyser ThreadID à partir de la ligne de commande, reprendre ce thread, puis quittez.

     Voici quelques exemples de code C++ pour ce faire (veillez à ajouter la vérification des erreurs !) :

    ```cpp
    int wmain(int argc, wchar_t* argv[])
    {
        // …
        // Parse command line here
        // …

        HANDLE hThread = OpenThread(THREAD_SUSPEND_RESUME, 
                                                                  FALSE /* bInheritHandle */, nThreadID);
        ResumeThread(hThread);
        CloseHandle(hThread);
        return 0;
    }
    ```

     Vous aurez besoin déployer ce débogueur factice dans le cadre de votre installation de l’outil diagnostics, puis spécifiez le chemin d’accès à ce débogueur dans le `debuggerCommandLine` paramètre.

**Lancement de l’application du Windows Store**

Le moment pour lancer l’application du Windows Store est enfin arrivé. Si vous avez déjà déjà essayé de faire vous-même, vous avez peut-être remarqué que [CreateProcess](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) pas comment vous créer un processus d’application Windows Store. Au lieu de cela, vous devez utiliser le [IApplicationActivationManager::ActivateApplication](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) (méthode). Pour ce faire, vous devez obtenir l’ID de modèle d’application utilisateur de l’application Windows Store que vous lancez. Et cela signifie que vous devez effectuer quelques rentrer via le manifeste.

Lors de l’itération sur vos packages (consultez « Choix d’un Windows Store App à profiler » dans le [chargement au démarrage](#startup-load) section précédemment), vous devrez vous procurer l’ensemble des applications contenues dans le manifeste du package actuel :

```csharp
string manifestPath = package.InstalledLocation.Path + "\\AppxManifest.xml";

AppxPackaging.IStream manifestStream;
SHCreateStreamOnFileEx(
                    manifestPath,
                    0x00000040,     // STGM_READ | STGM_SHARE_DENY_NONE
                    0,              // file creation attributes
                    false,          // fCreate
                    null,           // reserved
                    out manifestStream);

IAppxManifestReader manifestReader = appxFactory.CreateManifestReader(manifestStream);

IAppxManifestApplicationsEnumerator appsEnum = manifestReader.GetApplications();
```

Oui, un package peut avoir plusieurs applications, et chaque application possède son propre ID de modèle d’Application utilisateur. Par conséquent, vous souhaitez demander à votre utilisateur quelle application au profil et récupérer l’ID de modèle Application utilisateur à partir de cette application en particulier :

```csharp
while (appsEnum.GetHasCurrent() != 0)
{
    IAppxManifestApplication app = appsEnum.GetCurrent();
    string appUserModelId = app.GetAppUserModelId();
    //...
}
```

Enfin, vous devez maintenant ce dont vous avez besoin lancer l’application du Windows Store :

```csharp
IApplicationActivationManager appActivationMgr = new ApplicationActivationManager();
appActivationMgr.ActivateApplication(appUserModelId, appArgs, ACTIVATEOPTIONS.AO_NONE, out pid);
```

**N’oubliez pas d’appeler DisableDebugging**

Lorsque vous avez appelé [IPackageDebugSettings::EnableDebugging](https://msdn.microsoft.com/library/hh438395\(v=VS.85\).aspx), effectuées une promesse qui vous nettoyez après vous-même en appelant le [IPackageDebugSettings::DisableDebugging](https://msdn.microsoft.com/library/hh438394\(v=vs.85\).aspx) (méthode), veillez à faire que lorsque la session de profilage terminée.

### <a name="attach-load"></a>Attacher la charge

Lorsque votre interface utilisateur de Profiler souhaite joindre ses DLL à Profiler à une application qui a déjà démarré, il utilise [ICLRProfiling::AttachProfiler](iclrprofiling-attachprofiler-method.md). Il en va de même avec les applications du Windows Store. Mais en plus les considérations courantes répertoriées plus haut, assurez-vous que l’application du Windows Store cible n’est pas interrompue.

**EnableDebugging**

À l’instar de chargement au démarrage, appelez le [IPackageDebugSettings::EnableDebugging](https://msdn.microsoft.com/library/hh438395\(v=VS.85\).aspx) (méthode). Vous n’en avez pas besoin pour le passage d’un bloc d’environnement, mais vous avez besoin d’un de ses autres fonctionnalités : la désactivation de suspension de processus automatique. Sinon, lorsque votre interface utilisateur de Profiler appelle [AttachProfiler](iclrprofiling-attachprofiler-method.md), l’application du Windows Store cible peut être suspendue. En fait, c’est probablement si l’utilisateur est maintenant interagit avec votre interface utilisateur de Profiler et l’application Windows Store n’est pas active sur un des écrans de l’utilisateur. Et si le Windows Store app est suspendu, il sera en mesure de répondre à certaines signalent que le CLR lui envoie pour attacher votre DLL à Profiler.

Vous devez donc faire quelque chose comme ceci :

```csharp
IPackageDebugSettings pkgDebugSettings = new PackageDebugSettings();
pkgDebugSettings.EnableDebugging(packgeFullName, null /* debuggerCommandLine */, 
                                                                 IntPtr.Zero /* environment */);
```

Il s’agit de l’appel de même que vous comptez le faire dans le cas de charge de démarrage, mais vous ne spécifiez pas une ligne de commande du débogueur ou un bloc d’environnement.

**DisableDebugging**

Comme toujours, n’oubliez pas d’appeler [IPackageDebugSettings::DisableDebugging](https://msdn.microsoft.com/library/hh438394\(v=vs.85\).aspx) lorsque votre session de profilage est terminée.

## <a name="running-inside-the-windows-store-app"></a>En cours d’exécution à l’intérieur de l’application du Windows Store

Par conséquent, l’application du Windows Store a chargé votre DLL à Profiler. Maintenant votre DLL de Profiler doit être appris à lire par les différentes règles requises par les applications du Windows Store, y compris les API qui sont autorisées et exécuter avec des autorisations réduites.

### <a name="stick-to-the-windows-store-app-apis"></a>Respectez les API d’application Windows Store

Lorsque vous parcourez l’API Windows, vous remarquerez que toutes les API est documenté comme étant applicables aux applications de bureau, les applications du Windows Store ou les deux. Par exemple, le **exigences** section de la documentation pour le [InitializeCriticalSectionAndSpinCount](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) fonction indique que la fonction s’applique aux applications de bureau uniquement. En revanche, le [InitializeCriticalSectionEx](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsectionex) fonction n’est disponible pour les applications de bureau et les applications du Windows Store.

Lorsque vous développez votre DLL de Profiler, traitez-le comme s’il s’agit d’une application Windows Store et utilisent uniquement les API sont documentées comme étant disponibles pour les applications du Windows Store. Analyser vos dépendances (par exemple, vous pouvez exécuter `link /dump /imports` par rapport à votre DLL de Profiler pour audit), puis recherchez la documentation pour voir lequel de vos dépendances sont OK et qui ne sont pas. Dans la plupart des cas, les violations de votre peuvent être résolues en simplement en les remplaçant par une forme plus récente de l’API est documenté comme sécurisé (par exemple, en remplaçant [InitializeCriticalSectionAndSpinCount](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) avec [ InitializeCriticalSectionEx](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsectionex)).

Vous pouvez remarquer que votre DLL de Profiler appelle certaines API qui s’appliquent aux applications de bureau uniquement, et encore qu’ils semblent fonctionner même lorsque votre DLL de Profiler est chargée à l’intérieur d’une application Windows Store. N’oubliez pas qu’il est risqué d’utiliser n’importe quelle API non documenté pour une utilisation avec les applications du Windows Store dans votre DLL de Profiler lors du chargement dans un processus d’application Windows Store :

- Ces API n’est pas garanties fonctionne lorsqu’elle est appelée dans le contexte unique qui s’exécutent des applications du Windows Store dans.

- Ces API ne fonctionnera ne peut-être pas régulièrement lorsque appelée à partir de différents processus d’application Windows Store.

- Ces API peut-être sembler fonctionner sans problème à partir d’applications du Windows Store dans la version actuelle de Windows, mais peut cesser de fonctionner ou être désactivé dans les versions futures de Windows.

Le meilleur conseil est de résoudre toutes les violations de votre et éviter le risque.

Vous constaterez peut-être que vous ne pouvez pas faire sans une API particulière absolument et ne peut pas trouver un remplacement adapté pour les applications du Windows Store. Dans ce cas, au minimum :

- Tester, de test, de tester les daylights vivant en dehors de votre utilisation de cette API.

- Comprendre que l’API peut soudainement interrompre ou disparaître si elle est appelée à partir de Windows Store à l’intérieur d’applications dans les versions futures de Windows. Cela ne soit considéré comme un problème de compatibilité par Microsoft, et prise en charge de votre utilisation de celui-ci ne sera pas une priorité.

### <a name="reduced-permissions"></a>Autorisations réduites

Il est en dehors de l’étendue de cette rubrique pour répertorier toutes les méthodes qui diffèrent des autorisations d’application Windows Store à partir d’applications de bureau. Mais certainement le comportement sera différent chaque fois que votre DLL de Profiler (lorsqu’il est chargé dans une application Windows Store par rapport à une application de bureau) tente d’accéder aux ressources. Le système de fichiers est l’exemple le plus courant. Il existe, mais quelques place sur le disque une application Windows Store donnée est autorisée à accéder (consultez [accès et les autorisations de fichiers (applications Windows Runtime](https://msdn.microsoft.com/library/windows/apps/hh967755.aspx)), et votre DLL de Profiler seront sous les mêmes restrictions. Testez minutieusement votre code.

### <a name="inter-process-communication"></a>Communication entre processus

Comme indiqué dans le diagramme au début de ce document, votre DLL de Profiler (chargées dans l’espace de processus d’application Windows Store) aurez probablement besoin de communiquer avec votre Profiler une interface utilisateur (en cours d’exécution dans un espace de processus d’application de bureau distincte) via votre propre processus entre personnalisé canal de communication (IPC). L’interface utilisateur de Profiler envoie des signaux à la DLL de Profiler pour modifier son comportement, et la DLL de Profiler envoie des données à partir de l’application Windows Store analysée vers l’interface utilisateur de Profiler de post-traitement et d’affichage à l’utilisateur du profileur.

La plupart des profileurs besoin de cette manière, mais vos choix de mécanismes IPC est plus limitées lorsque votre DLL de Profiler est chargé dans une application Windows Store. Par exemple, ce canaux nommés ne font pas partie de l’application du Windows Store Kit de développement logiciel, vous ne pouvez pas les utiliser.

Mais bien sûr, les fichiers sont toujours dans, bien que de manière plus limitée. Les événements sont également disponibles.

**Communication via des fichiers**

La plupart de vos données est probablement passer entre la DLL de Profiler et l’interface utilisateur du Profiler via des fichiers. La clé est de choisir un emplacement de fichier que votre DLL de Profiler (dans le contexte d’une application Windows Store) et l’interface utilisateur du Profiler lus et d’un accès en écriture au. Par exemple, le chemin d’accès du dossier temporaire est un emplacement accessible par votre DLL de Profiler et l’interface utilisateur du Profiler, mais aucun autre package d’application Windows Store ne permettre accéder (ce qui protège les informations que vous vous connectez à partir d’autres packages d’application Windows Store).

Votre interface utilisateur du Profiler et la DLL de Profiler peuvent déterminer ce chemin d’accès indépendamment. Votre interface utilisateur du Profiler, lorsqu’il itère tous les packages installés pour l’utilisateur actuel (voir l’exemple de code précédemment), obtient l’accès à la `PackageId` (classe), à partir duquel le chemin d’accès du dossier temporaire peut être dérivée avec un code similaire à cet extrait de code. (Comme toujours, la vérification des erreurs est omise par souci de concision.)

```csharp
// C# code for the Profiler UI.
ApplicationData appData =
    ApplicationDataManager.CreateForPackageFamily(
        packageId.FamilyName);

tempDir = appData.TemporaryFolder.Path;
```

Pendant ce temps, votre DLL de Profiler peut faire la même chose en fait, même si elle peut plus facilement accéder à la [ApplicationData](https://msdn.microsoft.com/library/windows/apps/windows.storage.applicationdata.aspx) classe à l’aide de la [ApplicationData.Current](https://msdn.microsoft.com/library/windows/apps/windows.storage.applicationdata.current.aspx) propriété.

**Communiquant via des événements**

Si vous souhaitez la sémantique de signalisation simple entre votre interface utilisateur de Profiler et de la DLL de Profiler, vous pouvez utiliser des événements à l’intérieur d’applications du Windows Store, ainsi que des applications de bureau.

À partir de votre DLL à Profiler, vous pouvez simplement appeler le [CreateEventEx](/windows/desktop/api/synchapi/nf-synchapi-createeventexa) fonction permettant de créer un événement nommé avec le nom de votre choix. Exemple :

```cpp
// Profiler DLL in Windows Store app (C++).
CreateEventEx(
    NULL,  // Not inherited
    "MyNamedEvent"
    CREATE_EVENT_MANUAL_RESET, /* explicit ResetEvent() required; leave initial state unsignaled */
    EVENT_ALL_ACCESS);
```

Votre interface utilisateur de Profiler doit ensuite rechercher cet événement nommé sous espace de noms de l’application Windows Store. Par exemple, votre interface utilisateur de Profiler pourrait appeler [CreateEventEx](/windows/desktop/api/synchapi/nf-synchapi-createeventexa), en spécifiant le nom de l’événement en tant que

`AppContainerNamedObjects\<acSid>\MyNamedEvent`

`<acSid>` est AppContainer SID l’application Windows Store. Une section précédente de cette rubrique vous a montré comment effectuer une itération sur les packages installés pour l’utilisateur actuel. À partir de cet exemple de code, vous pouvez obtenir l’ID de package. Et à partir de l’ID de package, vous pouvez obtenir le `<acSid>` avec un code similaire à ce qui suit :

```csharp
IntPtr acPSID;
DeriveAppContainerSidFromAppContainerName(packageId.FamilyName, out acPSID);

string acSid;
ConvertSidToStringSid(acPSID, out acSid);

string acDir;
GetAppContainerFolderPath(acSid, out acDir);
```

### <a name="no-shutdown-notifications"></a>Aucune notification d’arrêt

Lors de l’exécution à l’intérieur d’une application Windows Store, votre DLL à Profiler ne doivent pas dépendre soit [ICorProfilerCallback::Shutdown](icorprofilercallback-shutdown-method.md) , voire [DllMain](/windows/desktop/Dlls/dllmain) (avec `DLL_PROCESS_DETACH`) qui est appelé pour avertir votre DLL de Profiler que l’application du Windows Store va s’arrêter. Vous devriez en fait, qu'ils ne seront jamais appelées. Historiquement, nombreuses DLL Profiler ont utilisé ces notifications en tant qu’emplacements pratiques pour vider les caches pour le disque, de fermer les fichiers, d’envoyer des notifications à l’interface utilisateur du Profiler, etc. Mais maintenant votre DLL de Profiler doit être organisé un peu différemment.

Votre DLL à Profiler doivent être des informations de journalisation tandis qu’elle passe. Pour des raisons de performances, vous souhaiterez batch les informations en mémoire et de vidage sur le disque que le lot augmente en taille après un certain seuil. Mais supposons que toutes les informations ne sont pas encore vidées sur le disque peuvent être perdues. Cela signifie que vous voudrez choisir votre seuil avec soin, et que votre interface utilisateur de Profiler doit être renforcé pour gérer des informations incomplètes écrites par la DLL à Profiler.

## <a name="windows-runtime-metadata-files"></a>Fichiers de métadonnées Windows Runtime

Il est en dehors de la portée de ce document aborde en détail sur les métadonnées Windows Runtime (WinMD) sont des fichiers. Cette section est limitée à la façon dont l’API de profilage CLR réagit lorsque des fichiers WinMD sont chargés par l’application du Windows Store que l’analyse de votre DLL à Profiler.

### <a name="managed-and-non-managed-winmds"></a>Winmd gérés et non gérés

Si un développeur utilise Visual Studio pour créer un nouveau projet de composant d’exécution de Windows, une build du projet produit un fichier WinMD qui décrit les métadonnées (les descriptions de types de classes, interfaces, etc.) créée par le développeur. Si ce projet est un projet de langage managé écrit en c# ou VB, ce même fichier WinMD contient également l’implémentation de ces types (c'est-à-dire qu’il contient le langage intermédiaire compilé à partir du code source du développeur). Ces fichiers sont appelés fichiers WinMD gérés. Ils sont intéressants, car elles contiennent des métadonnées Windows Runtime et l’implémentation sous-jacente.

En revanche, si un développeur crée un projet de composant de Windows Runtime pour C++, une build du projet produit un fichier WinMD qui contient uniquement les métadonnées et l’implémentation est compilée dans une DLL native distincte. De même, les fichiers WinMD sont fournis dans le Kit de développement logiciel Windows contiennent uniquement des métadonnées, avec l’implémentation compilée dans des DLL natives distincts qui font partie de Windows.

Les informations ci-dessous s’applique aux deux Winmd managée, qui contiennent des métadonnées et implémentation, aux Winmd non managé, qui contiennent uniquement des métadonnées.

### <a name="winmd-files-look-like-clr-modules"></a>Fichiers WinMD ressembler aux modules CLR

Autant que le CLR est concerné, tous les fichiers WinMD sont des modules. Par conséquent, l’API de profilage CLR indique votre DLL de Profiler lors de la chargent des fichiers WinMD et quelles est leurs ID de module, de la même façon que pour d’autres modules managés.

Votre DLL de Profiler peut distinguer les fichiers WinMD provenant d’autres modules en appelant le [ICorProfilerInfo3::GetModuleInfo2](icorprofilerinfo3-getmoduleinfo2-method.md) (méthode) et en inspectant le `pdwModuleFlags` de sortie de paramètre pour le [COR_PRF_MODULE_WINDOWS_ RUNTIME](cor-prf-module-flags-enumeration.md) indicateur. (Il est défini si et seulement si l’ID de module représente un fichier WinMD).

### <a name="reading-metadata-from-winmds"></a>Lecture des métadonnées Winmd

Les fichiers WinMD, tels que les modules standards, contiennent des métadonnées qui peuvent être lues via le [Metadata APIs](../../../../docs/framework/unmanaged-api/metadata/index.md). Toutefois, le CLR mappe les types Windows Runtime en types .NET Framework lorsqu’il lit que les fichiers WinMD afin que les développeurs qui programmer dans le code managé et de consomment le fichier WinMD peuvent avoir une expérience en programmation plus naturelle. Pour obtenir des exemples de ces mappages, consultez [prise en charge pour Windows Store d’applications .NET Framework et Windows Runtime](../../../../docs/standard/cross-platform/support-for-windows-store-apps-and-windows-runtime.md).

Par conséquent, la vue qui sera votre profileur obtenir lorsqu’il utilise les API de métadonnées : l’affichage brut de Windows Runtime, ou de la vue de .NET Framework mappée ?  La réponse : c’est à vous.

Lorsque vous appelez le [ICorProfilerInfo::GetModuleMetaData](icorprofilerinfo-getmodulemetadata-method.md) méthode sur un fichier WinMD pour obtenir une interface de métadonnées, telles que [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md), vous pouvez choisir de définir [ofNoTransform](../../../../docs/framework/unmanaged-api/metadata/coropenflags-enumeration.md)dans le `dwOpenFlags` paramètre pour désactiver ce mappage. Sinon, par défaut, le mappage est activé. En règle générale, un profileur conserve le mappage est activé, afin que les chaînes qui obtient de la DLL à Profiler à partir des métadonnées WinMD (par exemple, les noms de types) recherche familière et naturelle à l’utilisateur du profileur.

### <a name="modifying-metadata-from-winmds"></a>Modification des métadonnées à partir de Winmd

Modification des métadonnées dans Winmd n’est pas pris en charge. Si vous appelez le [ICorProfilerInfo::GetModuleMetaData](icorprofilerinfo-getmodulemetadata-method.md) méthode pour un fichier WinMD fichier et spécifiez [ofWrite](../../../../docs/framework/unmanaged-api/metadata/coropenflags-enumeration.md) dans le `dwOpenFlags` paramètre ou demandez à une interface de métadonnées inscriptible comme [ IMetaDataEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md), [GetModuleMetaData](icorprofilerinfo-getmodulemetadata-method.md) échouera. Il s’agit d’un aspect important pour les profileurs de réécriture en langage intermédiaire, qui doivent modifier les métadonnées pour prendre en charge leur instrumentation (par exemple, pour ajouter AssemblyRefs ou nouvelles méthodes). Vous devez donc vérifier pour [COR_PRF_MODULE_WINDOWS_RUNTIME](cor-prf-module-flags-enumeration.md) tout d’abord (comme indiqué dans la section précédente) et en évitant de vous demander pour les interfaces de métadonnées accessibles en écriture sur ces modules.

### <a name="resolving-assembly-references-with-winmds"></a>Résolution des références d’assembly avec Winmd

Les profileurs de nombreux besoin résoudre les références de métadonnées manuellement à l’aide avec l’instrumentation ou l’inspection de type. Les profileurs de ce type doivent être conscient de comment le CLR résout les références d’assembly qui pointent vers Winmd, étant donné que ces références sont résolues dans totalement différemment des autres références d’assembly standard.

## <a name="memory-profilers"></a>Profileurs de mémoire

Le garbage collector et le tas managé ne sont pas fondamentalement différents dans une application Windows Store et une application de bureau. Toutefois, il existe quelques différences subtiles qui les auteurs de profileur doivent connaître.

### <a name="forcegc-creates-a-managed-thread"></a>ForceGC crée un thread managé

Lorsque vous effectuez le profilage de mémoire, votre DLL de Profiler crée généralement un thread séparé à partir de laquelle appeler la [ForceGC, méthode](icorprofilerinfo-forcegc-method.md) (méthode). Cela n’est pas nouveau. Mais ce qui peut être étonnant est que le fait d’effectuer un garbage collection à l’intérieur d’une application Windows Store peut-être transformer votre thread dans un thread managé (par exemple, un API ThreadID de profilage est créé pour ce thread).

Pour comprendre les conséquences de cela, il est important de comprendre les différences entre les appels synchrones et asynchrones, comme défini par l’API de profilage CLR. Notez que cela est très différent du concept des appels asynchrones dans les applications du Windows Store. Consultez le blog [pourquoi nous avons CORPROF_E_UNSUPPORTED_CALL_SEQUENCE](https://blogs.msdn.microsoft.com/davbr/2008/12/23/why-we-have-corprof_e_unsupported_call_sequence/) pour plus d’informations.

Le point approprié est que les appels effectués sur les threads créés par votre profileur sont toujours considérés comme synchrones, même si ces appels sont effectués à partir en dehors d’une implémentation d’un de votre DLL Profiler [ICorProfilerCallback](icorprofilercallback-interface.md) méthodes. Au moins, qui permet d’être le cas. Maintenant que le CLR a transformée thread de votre profileur par un thread managé en raison de votre appel à [ForceGC, méthode](icorprofilerinfo-forcegc-method.md), que thread ne soit plus considéré thread de votre profileur. Par conséquent, le CLR applique une définition plus stricte de qu’est-ce que synchrone pour ce thread, à savoir qui doit provenir d’un appel à l’intérieur d’un de votre DLL Profiler [ICorProfilerCallback](icorprofilercallback-interface.md) méthodes pour qualifier comme synchrone.

Que cela signifie dans la pratique ? La plupart des [ICorProfilerInfo](icorprofilerinfo-interface.md) méthodes permettent uniquement à être appelé de façon synchrone et immédiatement échoue dans le cas contraire. Par conséquent, si votre DLL de Profiler réutilise votre [ForceGC, méthode](icorprofilerinfo-forcegc-method.md) thread pour les autres appels effectués en général sur les threads créés par le profileur (par exemple, pour [RequestProfilerDetach](icorprofilerinfo3-requestprofilerdetach-method.md), [RequestReJIT](icorprofilerinfo4-requestrejit-method.md), ou [RequestRevert](icorprofilerinfo4-requestrevert-method.md)), vous allez rencontrer des difficultés. Même une fonction asynchrone safe telle que [DoStackSnapshot](icorprofilerinfo2-dostacksnapshot-method.md) possède des règles spéciales lorsqu’elle est appelée à partir de threads managés. (Consultez le blog [parcours de pile Profiler : principes de base et au-delà](https://blogs.msdn.microsoft.com/davbr/2005/10/06/profiler-stack-walking-basics-and-beyond/) pour plus d’informations.)

Par conséquent, nous recommandons que n’importe quel thread de votre DLL de Profiler crée pour appeler [ForceGC, méthode](icorprofilerinfo-forcegc-method.md) doit être utilisé *uniquement* en vue de déclencher le catalogues globaux et de répondre aux rappels GC. Il ne doit pas appeler dans l’API de profilage pour effectuer d’autres tâches telles que pile d’échantillonnage ou de détachement.

### <a name="conditionalweaktablereferences"></a>ConditionalWeakTableReferences

À compter de .NET Framework 4.5, il existe un nouveau rappel GC, [ConditionalWeakTableElementReferences](icorprofilercallback5-conditionalweaktableelementreferences-method.md), qui donne le profileur terminer plus d’informations sur *handles dépendants*. Ces descripteurs ajouter efficacement une référence à partir d’un objet de source à un objet de cible pour les besoins de gestion de durée de vie de GC. Handles dépendants sont rien de nouveau, et les développeurs qui programment dans du code managé ont été en mesure de créer leurs propres handles dépendants à l’aide de la <xref:System.Runtime.CompilerServices.ConditionalWeakTable%602?displayProperty=nameWithType> classe même avant Windows 8 et le .NET Framework 4.5.

Toutefois, les applications XAML Windows Store gérées maintenant utilisent beaucoup de handles dépendants. En particulier, le CLR les utilise pour faciliter la gestion des cycles de références entre des objets gérés et les objets Windows Runtime non managés. Cela signifie qu’il est désormais plus importe que jamais pour les profileurs de mémoire être informé de ces handles dépendants afin qu’ils peuvent être visualisés avec le reste des bords dans le graphique de segment de mémoire. Votre DLL de Profiler doit utiliser [RootReferences2](icorprofilercallback2-rootreferences2-method.md), [ObjectReferences](icorprofilercallback-objectreferences-method.md), et [ConditionalWeakTableElementReferences](icorprofilercallback5-conditionalweaktableelementreferences-method.md) pour former une vue complète du graphique de segment de mémoire .

## <a name="conclusion"></a>Conclusion

Il est possible d’utiliser l’API de profilage CLR pour analyser le code managé en cours d’exécution à l’intérieur d’applications du Windows Store. En fait, vous pouvez prendre un profileur existant que vous développez et apporter des modifications spécifiques afin qu’il peut cibler les applications du Windows Store. Votre interface utilisateur de Profiler doit utiliser les nouvelles API pour l’activation de l’application du Windows Store en mode débogage. Assurez-vous que votre DLL de Profiler consomme des seules API applicable pour les applications du Windows Store. Le mécanisme de communication entre votre DLL de Profiler et l’interface utilisateur du Profiler doit être écrits avec les restrictions de API d’applications Windows Store à l’esprit et avec la reconnaissance des autorisations restreintes en place pour les applications du Windows Store. Votre DLL de Profiler doit être conscient de la manière dont le CLR traite Winmd, et comment le comportement du Garbage Collector est différent en ce qui concerne les threads managés.

## <a name="resources"></a>Ressources

**Le Common Language Runtime**

- [Profilage (référence des API non managées)](index.md)

- [Métadonnées (référence des API non managées)](../metadata/index.md)

**Interaction du CLR avec le Runtime de Windows**

- [Prise en charge .NET Framework pour les applications Windows Store et Windows Runtime](../../../../docs/standard/cross-platform/support-for-windows-store-apps-and-windows-runtime.md)

**Applications Windows Store**

- [Accès aux fichiers et les autorisations (applications Windows Runtime](https://msdn.microsoft.com/library/windows/apps/hh967755.aspx)

- [Obtenir une licence de développeur](https://msdn.microsoft.com/library/windows/apps/Hh974578.aspx)

- [Interface de IPackageDebugSettings](https://msdn.microsoft.com/library/hh438393\(v=vs.85\).aspx)
