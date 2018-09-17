---
title: Diagnostic d'erreurs avec les Assistants de débogage managés
ms.date: 08/14/2018
f1_keywords:
- EHMDA
helpviewer_keywords:
- run-time error debugging
- managed code, run-time debugging
- resource debugging
- registry, MDAs
- common language runtime, debugging
- MDAs (managed debugging assistants)
- configuration files [.NET Framework], debugging runtime events
- messages, managed debugging assistants
- application configuration files, managed debugging assistants
- debugging [.NET Framework], managed debugging assistants
- environment variables, MDAs
- access violation debugging [.NET Framework]
- diagnostics, managed debugging assistants
- unmanaged code, run-time debugging
- default debug output stream
- memory, debugging
- app.config files, managed debugging assistants
- managed debugging assistants (MDAs)
- debugging [.NET Framework], run-time errors
- trapping events
- runtime, error debugging
- disabling MDAs
- output, managed debugging assistants
- errors [.NET Framework], managed debugging assistants
ms.assetid: 76994ee6-9fa9-4059-b813-26578d24427c
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b745fa6a78ab2a7ab0b3a94c9921883d3c56c1b7
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45750282"
---
# <a name="diagnose-errors-with-managed-debugging-assistants"></a>Diagnostiquer des erreurs avec les Assistants Débogage managé

Les Assistants Débogage managé sont des aides au débogage qui fonctionnent conjointement avec le Common Language Runtime (CLR) pour fournir des informations sur l'état d'exécution. Les Assistants génèrent des messages d'information sur les événements du runtime que vous ne pouvez pas intercepter en temps normal. Vous pouvez utiliser les Assistants Débogage managé pour isoler les bogues d'application difficiles à déceler qui se produisent pendant les phases de transition entre un code managé et un code non managé.

Vous pouvez [activer ou désactiver](#enable-and-disable-mdas) tous les Assistants Débogage managé en ajoutant une clé au Registre Windows ou en définissant une variable d’environnement. Vous pouvez activer des Assistants Débogage managé spécifiques à l'aide de paramètres de configuration d'application. Vous pouvez définir des paramètres de configuration supplémentaires pour certains Assistants Débogage managé dans le fichier de configuration de l'application. Comme ces fichiers de configuration sont analysés au chargement du runtime, vous devez activer l'Assistant Débogage managé avant que l'application managée ne démarre. Vous ne pouvez pas l'activer pour les applications qui ont déjà démarré.

Le tableau suivant répertorie les Assistants Débogage managé fournis avec le .NET Framework :

|||
|-|-|
|[asynchronousThreadAbort](../../../docs/framework/debug-trace-profile/asynchronousthreadabort-mda.md)|[bindingFailure](../../../docs/framework/debug-trace-profile/bindingfailure-mda.md)|
|[callbackOnCollectedDelegate](../../../docs/framework/debug-trace-profile/callbackoncollecteddelegate-mda.md)|[contextSwitchDeadlock](../../../docs/framework/debug-trace-profile/contextswitchdeadlock-mda.md)|
|[dangerousThreadingAPI](../../../docs/framework/debug-trace-profile/dangerousthreadingapi-mda.md)|[dateTimeInvalidLocalFormat](../../../docs/framework/debug-trace-profile/datetimeinvalidlocalformat-mda.md)|
|[dirtyCastAndCallOnInterface](../../../docs/framework/debug-trace-profile/dirtycastandcalloninterface-mda.md)|[disconnectedContext](../../../docs/framework/debug-trace-profile/disconnectedcontext-mda.md)|
|[dllMainReturnsFalse](../../../docs/framework/debug-trace-profile/dllmainreturnsfalse-mda.md)|[exceptionSwallowedOnCallFromCom](../../../docs/framework/debug-trace-profile/exceptionswallowedoncallfromcom-mda.md)|
|[failedQI](../../../docs/framework/debug-trace-profile/failedqi-mda.md)|[fatalExecutionEngineError](../../../docs/framework/debug-trace-profile/fatalexecutionengineerror-mda.md)|
|[gcManagedToUnmanaged](../../../docs/framework/debug-trace-profile/gcmanagedtounmanaged-mda.md)|[gcUnmanagedToManaged](../../../docs/framework/debug-trace-profile/gcunmanagedtomanaged-mda.md)|
|[illegalPrepareConstrainedRegion](../../../docs/framework/debug-trace-profile/illegalprepareconstrainedregion-mda.md)|[invalidApartmentStateChange](../../../docs/framework/debug-trace-profile/invalidapartmentstatechange-mda.md)|
|[invalidCERCall](../../../docs/framework/debug-trace-profile/invalidcercall-mda.md)|[invalidFunctionPointerInDelegate](../../../docs/framework/debug-trace-profile/invalidfunctionpointerindelegate-mda.md)|
|[invalidGCHandleCookie](../../../docs/framework/debug-trace-profile/invalidgchandlecookie-mda.md)|[invalidIUnknown](../../../docs/framework/debug-trace-profile/invalidiunknown-mda.md)|
|[invalidMemberDeclaration](../../../docs/framework/debug-trace-profile/invalidmemberdeclaration-mda.md)|[invalidOverlappedToPinvoke](../../../docs/framework/debug-trace-profile/invalidoverlappedtopinvoke-mda.md)|
|[invalidVariant](../../../docs/framework/debug-trace-profile/invalidvariant-mda.md)|[jitCompilationStart](../../../docs/framework/debug-trace-profile/jitcompilationstart-mda.md)|
|[loaderLock](../../../docs/framework/debug-trace-profile/loaderlock-mda.md)|[loadFromContext](../../../docs/framework/debug-trace-profile/loadfromcontext-mda.md)|
|[marshalCleanupError](../../../docs/framework/debug-trace-profile/marshalcleanuperror-mda.md)|[marshaling](../../../docs/framework/debug-trace-profile/marshaling-mda.md)|
|[memberInfoCacheCreation](../../../docs/framework/debug-trace-profile/memberinfocachecreation-mda.md)|[moduloObjectHashcode](../../../docs/framework/debug-trace-profile/moduloobjecthashcode-mda.md)|
|[nonComVisibleBaseClass](../../../docs/framework/debug-trace-profile/noncomvisiblebaseclass-mda.md)|[notMarshalable](../../../docs/framework/debug-trace-profile/notmarshalable-mda.md)|
|[openGenericCERCall](../../../docs/framework/debug-trace-profile/opengenericcercall-mda.md)|[overlappedFreeError](../../../docs/framework/debug-trace-profile/overlappedfreeerror-mda.md)|
|[pInvokeLog](../../../docs/framework/debug-trace-profile/pinvokelog-mda.md)|[pInvokeStackImbalance](../../../docs/framework/debug-trace-profile/pinvokestackimbalance-mda.md)|
|[raceOnRCWCleanup](../../../docs/framework/debug-trace-profile/raceonrcwcleanup-mda.md)|[reentrancy](../../../docs/framework/debug-trace-profile/reentrancy-mda.md)|
|[releaseHandleFailed](../../../docs/framework/debug-trace-profile/releasehandlefailed-mda.md)|[reportAvOnComRelease](../../../docs/framework/debug-trace-profile/reportavoncomrelease-mda.md)|
|[streamWriterBufferedDataLost](../../../docs/framework/debug-trace-profile/streamwriterbuffereddatalost-mda.md)|[virtualCERCall](../../../docs/framework/debug-trace-profile/virtualcercall-mda.md)|

Par défaut, le .NET Framework active une partie des Assistants Débogage managé pour tous les débogueurs managés. Vous pouvez afficher l’ensemble par défaut dans Visual Studio en choisissant **Windows** > **paramètres d’Exception** sur le **déboguer** menu, puis en développant le **Assistants Débogage managé** liste.

![Fenêtre Paramètres d’exception dans Visual Studio](media/diagnosing-errors-with-managed-debugging-assistants/exception-settings-mdas.png)

## <a name="enable-and-disable-mdas"></a>Activation et désactivation des Assistants Débogage managé

Vous pouvez activer et désactiver les Assistants Débogage managé en utilisant une clé de Registre, une variable d'environnement et des paramètres de configuration d'application. Vous devez activer la clé de Registre ou la variable d'environnement pour utiliser les paramètres de configuration d'application.

> [!TIP]
> Au lieu de désactiver les Assistants Débogage managé, vous pouvez empêcher Visual Studio d’afficher la boîte de dialogue d’Assistant Débogage MANAGÉ chaque fois qu’une notification de l’Assistant Débogage MANAGÉ est reçue. Pour ce faire, choisissez **Windows** > **paramètres d’Exception** sur le **déboguer** menu, développez le **Assistants Débogage managé**liste, puis activez ou désactivez le **arrêter lorsque levée** case à cocher pour l’Assistant Débogage MANAGÉ concerné.

### <a name="registry-key"></a>Clé de Registre

Pour activer les Assistants Débogage managé, ajoutez le **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\\. NETFramework\MDA** sous-clé (type REG_SZ, valeur 1) dans le Registre Windows. Copiez l’exemple suivant dans un fichier texte nommé *MDAEnable.reg*. Ouvrez l’Éditeur du Registre Windows (RegEdit.exe) et à partir de la **fichier** menu Choisissez **importation**. Sélectionnez le *MDAEnable.reg* fichier pour activer les Assistants Débogage managé sur cet ordinateur. Définir la sous-clé sur la valeur de chaîne de **1** (pas la valeur DWORD de **1**) permet la lecture des paramètres de l’Assistant Débogage MANAGÉ à partir de la *nom_application.suffixe*. mda.config fichier. Par exemple, le fichier de configuration MDA pour le bloc-notes serait nommé notepad.exe.mda.config.

```text
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework]
"MDA"="1"
```

Si l'ordinateur exécute une application 32 bits sur un système d'exploitation 64 bits, la clé MDA doit être définie comme suit :

```text
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\.NETFramework]
"MDA"="1"
```

Consultez [les paramètres de Configuration spécifiques à l’Application](#application-specific-configuration-settings) pour plus d’informations. Le paramétrage du Registre peut être remplacé par la variable d'environnement COMPLUS_MDA. Consultez [Variable d’environnement](#environment-variable) pour plus d’informations.

Pour désactiver les Assistants Débogage managé, définissez la sous-clé MDA sur **0** (zéro) à l’aide de l’Éditeur du Registre Windows.

Par défaut, certains Assistants Débogage managé sont activés quand vous exécutez une application qui est attachée à un débogueur, même sans que la clé de Registre soit ajoutée. Vous pouvez désactiver ces assistants en exécutant le *MDADisable.reg* comme décrit précédemment dans cette section du fichier.

### <a name="environment-variable"></a>Variable d’environnement

L'activation des Assistants Débogage managé peut également être contrôlée par la variable d'environnement COMPLUS_MDA, qui remplace la clé de Registre. La chaîne COMPLUS_MDA est une liste de noms d'Assistant Débogage managé ou d'autres chaînes de contrôle spéciales séparés par des points-virgules et sans distinction minuscules/majuscules. Démarrer sous un débogueur managé ou non managé active par défaut un ensemble d'Assistants Débogage managé. Pour ce faire, la valeur de la variable d'environnement ou de la clé de Registre doit être implicitement ajoutée au début de la liste délimitée par des points-virgules qui répertorie les Assistants Débogage managé activés par défaut sous les débogueurs. Les chaînes de contrôle spéciales sont les suivantes :

- `0` : désactive tous les Assistants Débogage managé.

- `1` : lit les paramètres d’Assistant Débogage managé dans le fichier *nom_application*.mda.config.

- `managedDebugger` : active explicitement tous les Assistants Débogage managé qui sont implicitement activés quand un exécutable managé est démarré sous un débogueur.

- `unmanagedDebugger` : active explicitement tous les Assistants Débogage managé qui sont implicitement activés quand un exécutable non managé est démarré sous un débogueur.

En cas de conflit de paramètres, les paramètres les plus récents remplacent les paramètres antérieurs :

- `COMPLUS_MDA=0` désactive tous les Assistants Débogage managé, y compris ceux qui sont implicitement activés sous un débogueur.

- `COMPLUS_MDA=gcUnmanagedToManaged` active `gcUnmanagedToManaged` outre tout Assistant Débogage managé implicitement activé sous un débogueur.

- `COMPLUS_MDA=0;gcUnmanagedToManaged` active `gcUnmanagedToManaged`, mais désactive tout Assistant Débogage managé implicitement activé sous un débogueur.

### <a name="application-specific-configuration-settings"></a>Paramètres de Configuration spécifiques à l’application

Vous pouvez activer, désactiver et configurer certains Assistants séparément dans le fichier de configuration d'Assistant Débogage managé propre à l'application. Vous ne pouvez utiliser un fichier de configuration d'application pour configurer des Assistants Débogage managé que si la clé de Registre MDA ou la variable d'environnement COMPLUS_MDA est définie. En règle générale, le fichier de configuration d'application se trouve dans le même répertoire que le fichier exécutable (.exe) de l'application. Le format du nom de fichier est *nom_application*.mda.config ; par exemple, notepad.exe.mda.config. Les Assistants qui sont activés dans le fichier de configuration d'application peuvent avoir des attributs ou des éléments qui permettent de contrôler le comportement de l'Assistant concerné.

L’exemple suivant montre comment activer et configurer le [marshaling](../../../docs/framework/debug-trace-profile/marshaling-mda.md):

```xml
<mdaConfig>
  <assistants>
    <marshaling>
      <methodFilter>
        <match name="*"/>
      </methodFilter>
      <fieldFilter>
        <match name="*"/>
      </fieldFilter>
    </marshaling>
  </assistants>
</mdaConfig>
```

L'Assistant Débogage managé `Marshaling` émet des informations sur le type managé qui est marshalé en un type non managé pour chaque transition de code managé vers un code non managé dans l'application. Le `Marshaling` peut également filtrer les noms de la méthode et les champs de structure fournis dans le **methodFilter** et **fieldFilter** éléments enfants, respectivement.

L’exemple suivant montre comment activer plusieurs Assistants Débogage managé à l’aide de leurs paramètres par défaut :

```xml
<mdaConfig>
  <assistants>
    <illegalPrepareConstrainedRegion />
    <invalidCERCall />
    <openGenericCERCall />
    <virtualCERCall />
  </assistants>
</mdaConfig>
```

> [!IMPORTANT]
> Quand vous spécifiez plusieurs Assistants dans un fichier de configuration, vous devez les répertorier dans l'ordre alphabétique. Par exemple, pour activer les Assistants Débogage managé `virtualCERCall` et `invalidCERCall`, vous devez ajouter l'entrée `<invalidCERCall />` avant l'entrée `<virtualCERCall />`. Si vous n'indiquez pas les entrées dans l'ordre alphabétique, vous obtenez un message d'exception non gérée liée à un fichier de configuration non valide.

## <a name="mda-exceptions"></a>Exceptions de l’Assistant Débogage MANAGÉ

Quand un Assistant Débogage MANAGÉ est activé, il est actif même lorsque votre code ne s’exécute pas sous un débogueur. Si un événement d'Assistant Débogage managé est déclenché en l'absence de débogueur, le message de l'événement est présenté dans une boîte de dialogue d'exception non gérée, bien qu'il ne s'agisse pas d'une exception non gérée. Pour éviter l'affichage de la boîte de dialogue, supprimez les paramètres de désactivation de l'Assistant Débogage managé quand votre code ne s'exécute pas dans un environnement de débogage.

Lorsque votre code s’exécute dans l’environnement de développement intégré (IDE) Visual Studio, vous pouvez éviter la boîte de dialogue d’exception qui s’affiche pour les événements de débogage MANAGÉ spécifiques. Pour ce faire, dans le **déboguer** menu, choisissez **Windows** > **paramètres d’Exception**. Dans le **paramètres d’Exception** fenêtre, développez le **Assistants Débogage managé** liste, puis décochez la **arrêter lorsque levée** case à cocher pour l’Assistant Débogage MANAGÉ concerné. Vous pouvez également utiliser la boîte de dialogue *activer* l’affichage des boîtes de dialogue d’exception (MDA).

## <a name="mda-output"></a>Sortie de l'Assistant Débogage managé

Sortie de l’Assistant Débogage MANAGÉ est similaire à l’exemple suivant, qui montre la sortie de le `PInvokeStackImbalance` Assistant Débogage MANAGÉ :

**Un appel à la fonction PInvoke ' MDATest ! MDATest.Program::StdCall' a ait déséquilibré la pile. Cela est probablement parce que la signature PInvoke managée ne correspond pas à la signature cible non managée. Vérifiez que la convention d’appel et les paramètres de la signature PInvoke correspondent à la signature non managée cible.**

## <a name="see-also"></a>Voir aussi

- [Débogage, traçage et profilage](../../../docs/framework/debug-trace-profile/index.md)
