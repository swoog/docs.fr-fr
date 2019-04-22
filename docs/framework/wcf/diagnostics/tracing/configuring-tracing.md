---
title: Configuration du traçage
ms.date: 03/30/2017
helpviewer_keywords:
- tracing [WCF]
ms.assetid: 82922010-e8b3-40eb-98c4-10fc05c6d65d
ms.openlocfilehash: 8702091c185ba3d4956d3bd5d13ca191c12fce82
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59162879"
---
# <a name="configuring-tracing"></a>Configuration du traçage
Cette rubrique décrit comment activer le suivi, configurer des sources de suivi pour émettre des suivis et définir des niveaux de suivi, définir le suivi et la propagation d'activité afin de prendre en charge la corrélation de suivi de bout en bout, et définir des écouteurs de suivi pour accéder aux suivis.  
  
 Pour des recommandations de paramètres de suivi dans l’environnement de production ou débogage, reportez-vous à [paramètres recommandés pour le suivi et la journalisation des messages](../../../../../docs/framework/wcf/diagnostics/tracing/recommended-settings-for-tracing-and-message-logging.md).  
  
> [!IMPORTANT]
>  Sur Windows 8 vous devez exécuter votre application avec élévation de privilèges (Exécuter en tant qu'administrateur) pour que votre application génère des journaux de traces.  
  
## <a name="enabling-tracing"></a>Activation du suivi  
 Windows Communication Foundation (WCF) génère les données suivantes pour le suivi de diagnostic :  
  
-   Suivis des jalons de processus dans l'ensemble des composants des applications, tels que les appels d'opération, les exceptions de code, les avertissements et d'autres événements de traitement significatifs.  
  
-   Événements d’erreur Windows en cas de dysfonctionnement de la fonctionnalité de suivi. Consultez [journalisation des événements](../../../../../docs/framework/wcf/diagnostics/event-logging/index.md).  
  
 Le suivi WCF repose sur <xref:System.Diagnostics>. Pour utiliser le traçage, vous devez définir des sources de trace dans le fichier de configuration ou dans le code. WCF définit une source de suivi pour chaque assembly WCF. Le `System.ServiceModel` source de suivi est la source de suivi WCF plus générale et enregistre des jalons de traitement dans la pile de communication WCF, à partir de l’entrée/sortie de transport pour l’entrée/sortie de code utilisateur. La source de suivi `System.ServiceModel.MessageLogging` enregistre tous les messages qui circulent dans le système.  
  
 Le suivi est désactivé par défaut. Pour activer le suivi, vous devez créer un écouteur de suivi et définir un niveau de trace autre que « Off » pour la source de trace sélectionné dans la configuration ; Sinon, WCF ne génère pas de suivi. Si vous ne spécifiez pas d'écouteur, le suivi est automatiquement désactivé. Si un écouteur est défini mais qu'aucun niveau n'est spécifié, le niveau a la valeur « Désactivé » par défaut, ce qui signifie qu'aucun suivi n'est émis.  
  
 Si vous utilisez des points d’extensibilité WCF tels que les appelants d’opération personnalisé, vous devez émettre vos propres suivis. Il s’agit, car si vous implémentez un point d’extensibilité, WCF peut ne plus émettre les suivis standard dans le chemin d’accès par défaut. Si vous n'implémentez par la prise en charge du suivi manuel à l'aide de l'émission de suivis, les suivis peuvent ne pas s'afficher comme prévu.  
  
 Vous pouvez configurer le suivi en modifiant le fichier de configuration de l'application : Web.config pour les applications hébergées sur le Web, ou Appname.exe.config pour les applications auto-hébergées. Vous trouverez ci-dessous un exemple de ce type de modification : Pour plus d’informations sur ces paramètres, consultez la section « Configuration de Trace écouteurs pour consommer des suivis ».  
  
```xml  
<configuration>  
   <system.diagnostics>  
      <sources>  
            <source name="System.ServiceModel"   
                    switchValue="Information, ActivityTracing"  
                    propagateActivity="true">  
            <listeners>  
               <add name="traceListener"   
                   type="System.Diagnostics.XmlWriterTraceListener"   
                   initializeData= "c:\log\Traces.svclog" />  
            </listeners>  
         </source>  
      </sources>  
   </system.diagnostics>  
</configuration>  
```  
  
> [!NOTE]
>  Pour modifier le fichier de configuration d’un projet de service WCF dans Visual Studio, cliquez avec le bouton droit sur le fichier de configuration application : Web.config pour les applications hébergées sur le Web, ou Appname.exe.config pour les applications auto-hébergées dans **l’Explorateur de solutions** . Puis choisissez le **modifier la Configuration WCF** élément de menu contextuel. Cette opération lance le [l’outil Éditeur de Configuration (SvcConfigEditor.exe)](../../../../../docs/framework/wcf/configuration-editor-tool-svcconfigeditor-exe.md), qui vous permet de modifier les paramètres de configuration pour les services WCF à l’aide d’une interface utilisateur graphique.  
  
## <a name="configuring-trace-sources-to-emit-traces"></a>Configuration de sources de suivi de façon à émettre des suivis  
 WCF définit une source de suivi pour chaque assembly. Les écouteurs définis pour cette source accèdent aux suivis générés dans un assembly. Les sources de suivi suivantes sont définies :  
  
-   System.ServiceModel : Enregistre toutes les phases de traitement de WCF, chaque fois que la configuration est lue, un message est traité dans le transport, traitement de sécurité, un message est distribuée dans le code utilisateur et ainsi de suite.  
  
-   System.ServiceModel.MessageLogging: Enregistre tous les messages qui transitent par le système.  
  
-   System.IdentityModel.  
  
-   System.ServiceModel.Activation.  
  
-   System.IO.Log : Journalisation de l’interface .NET Framework pour le fichier système CLFS (Common Log).  
  
-   System.Runtime.Serialization: Enregistre les objets sont lues ou écrites.  
  
-   CardSpace.  
  
 Vous pouvez configurer chaque source de suivi de façon à utiliser le même écouteur (partagé), comme indiqué dans l'exemple de configuration suivant :  
  
```xml  
<configuration>  
    <system.diagnostics>  
        <sources>  
            <source name="System.ServiceModel"   
                    switchValue="Information, ActivityTracing"  
                    propagateActivity="true">  
                <listeners>  
                    <add name="xml" />  
                </listeners>  
            </source>  
            <source name="CardSpace">  
                <listeners>  
                    <add name="xml" />  
                </listeners>  
            </source>  
            <source name="System.IO.Log">  
                <listeners>  
                    <add name="xml" />  
                </listeners>  
            </source>  
            <source name="System.Runtime.Serialization">  
                <listeners>  
                    <add name="xml" />  
                </listeners>  
            </source>  
            <source name="System.IdentityModel">  
                <listeners>  
                    <add name="xml" />  
                </listeners>  
            </source>  
        </sources>  
  
        <sharedListeners>  
            <add name="xml"  
                 type="System.Diagnostics.XmlWriterTraceListener"  
                 initializeData="c:\log\Traces.svclog" />  
        </sharedListeners>  
    </system.diagnostics>  
</configuration>  
```  
  
 De plus, vous pouvez ajouter des sources de suivi définies par l'utilisateur, comme illustré par l'exemple suivant, de façon à émettre des suivis de code utilisateur :  
  
```xml  
<system.diagnostics>  
   <sources>  
       <source name="UserTraceSource" switchValue="Warning, ActivityTracing" >  
          <listeners>  
              <add name="xml"  
                 type="System.Diagnostics.XmlWriterTraceListener"  
                 initializeData="C:\logs\UserTraces.svclog" />  
          </listeners>  
       </source>  
   </sources>  
   <trace autoflush="true" />   
</system.diagnostics>  
```  
  
 Pour plus d’informations sur la création des sources de trace défini par l’utilisateur, consultez [extension suivi](../../../../../docs/framework/wcf/samples/extending-tracing.md).  
  
## <a name="configuring-trace-listeners-to-consume-traces"></a>Configuration d'écouteurs de suivi pour consommer des suivis  
 Lors de l’exécution, WCF de flux de données de trace dans les écouteurs qui traitent les données. WCF fournit plusieurs écouteurs prédéfinis pour <xref:System.Diagnostics>, qui diffèrent dans le format qu’ils utilisent pour la sortie. Vous pouvez également ajouter des types d'écouteurs personnalisés.  
  
 Vous pouvez utiliser `add` pour indiquer les nom et type de l'écouteur de suivi à utiliser. Dans notre exemple de configuration, nous avons nommé l'écouteur `traceListener` et ajouté l'écouteur de suivi standard .NET Framework (`System.Diagnostics.XmlWriterTraceListener`) comme type à utiliser. Vous pouvez ajouter un nombre quelconque d'écouteurs de suivi pour chaque source. Si l'écouteur de suivi émet le suivi dans un fichier, vous devez spécifier le nom et l'emplacement du fichier de sortie dans le fichier de configuration. Pour cela, vous devez affecter à `initializeData` le nom du fichier pour cet écouteur. Si vous ne spécifiez pas de nom de fichier, un nom de fichier aléatoire est généré en fonction du type d'écouteur utilisé. Si <xref:System.Diagnostics.XmlWriterTraceListener> est utilisé, un nom de fichier sans extension est généré. Si vous implémentez un écouteur personnalisé, vous pouvez également utiliser cet attribut pour recevoir des données d'initialisation autres qu'un nom de fichier. Par exemple, vous pouvez spécifier un identificateur de base de données pour cet attribut.  
  
 Vous pouvez configurer un écouteur de suivi personnalisé pour envoyer des suivis sur le câble, par exemple à une base de données distante. En tant que responsable du déploiement d'applications, vous devez appliquer un contrôle d'accès approprié sur les journaux de suivi sur l'ordinateur distant.  
  
 Vous pouvez également configurer un écouteur de suivi par programmation. Pour plus d'informations, voir [Procédure : Créer et initialiser des écouteurs de Trace](https://go.microsoft.com/fwlink/?LinkId=94648) et [création d’un TraceListener personnalisé](https://go.microsoft.com/fwlink/?LinkId=96239).  
  
> [!CAUTION]
>  `System.Diagnostics.XmlWriterTraceListener` n'étant pas thread-safe, la source de suivi peut verrouiller des ressources exclusivement lors de la sortie de suivis. Lorsque de nombreux threads sortent des suivis vers une source de suivi configurée pour utiliser cet écouteur, un conflit de ressource peut se produire, provoquant une dégradation significative des performances. Pour résoudre ce problème, vous devez implémenter un écouteur personnalisé thread-safe.  
  
## <a name="trace-level"></a>Niveau de suivi  
 Le niveau de suivi est contrôlé par le paramètre `switchValue` de la source de suivi. Les niveaux de suivi disponibles sont décrits dans le tableau suivant.  
  
|Niveau de suivi|Nature des événements suivis|Contenu des événements suivis|Événements suivis|Cible utilisateur|  
|-----------------|----------------------------------|-----------------------------------|--------------------|-----------------|  
|Off|N/A|N/A|Aucun suivi n'est émis.|N/A|  
|Critique|Événements « négatifs » : événements qui indiquent un traitement inattendu ou une condition d’erreur.||Les exceptions non prises en charge, notamment les suivantes, sont enregistrées :<br /><br /> -   OutOfMemoryException<br />-ThreadAbortException (le CLR appelle tout ThreadAbortExceptionHandler)<br />-StackOverflowException (interception impossible)<br />-   ConfigurationErrorsException<br />-   SEHException<br />-Erreurs de de l’application<br />-Événements Failfast<br />-Blocages du système<br />-Messages incohérents : suivis de messages qui provoquent l’échec de l’application.|Administrateurs<br /><br /> Développeurs d'applications|  
|Error|Événements « négatifs » : événements qui indiquent un traitement inattendu ou une condition d’erreur.|Un traitement inattendu s'est produit. L’application n’a pas pu effectuer une tâche comme prévu. Toutefois, l'application s'exécute encore.|Toutes les exceptions sont enregistrées.|Administrateurs<br /><br /> Développeurs d'applications|  
|Warning|Événements « négatifs » : événements qui indiquent un traitement inattendu ou une condition d’erreur.|Un problème possible s'est produit ou peut se produire, mais l'application fonctionne encore correctement. Toutefois, elle risque de ne plus fonctionner correctement.|-L’application reçoit davantage de demandes que ses paramètres de limitation ne l’autorisent.<br />-La file d’attente de réception est proche de sa capacité maximale configurée.<br />-Délai d’attente a été dépassé.<br />-Informations d’identification sont rejetées.|Administrateurs<br /><br /> Développeurs d'applications|  
|Information|Événements « Positifs » : événements qui marquent des jalons|Jalons importants et atteints relatifs à l'exécution d'application, indépendamment du fonctionnement correct de l'application.|En général, des messages d'aide au contrôle et au diagnostic de l'état système, à la mesure des performances ou au profilage sont générés. Vous pouvez utiliser ces informations pour la planification de capacité et la gestion des performances :<br /><br /> -Les canaux sont créés.<br />-Écouteurs de point de terminaison sont créés.<br />-Message pénètre/quitte le transport.<br />-Jeton de sécurité est récupéré.<br />-Paramètre de configuration est en lecture.|Administrateurs<br /><br /> Développeurs d'applications<br /><br /> Développeurs de produits.|  
|Verbose|Événements « Positifs » : événements qui marquent des jalons.|Des événements de bas niveau pour le code utilisateur et la maintenance sont émis.|En général, vous pouvez utiliser ce niveau pour le débogage ou l'optimisation d'application.<br /><br /> -En-tête de message compris.|Administrateurs<br /><br /> Développeurs d'applications<br /><br /> Développeurs de produits.|  
|ActivityTracing||Transfert d'événements entre des activités de traitement et des composants.|Ce niveau permet aux administrateurs et aux développeurs de corréler des applications dans le même domaine d'application :<br /><br /> -Effectue le suivi des limites d’activité, tels que Démarrer/arrêter.<br />-Suivis pour les transferts.|Tous|  
|Tous||L'application peut fonctionner correctement. Tous les événements sont émis.|Tous les événements précédents.|Tous|  
  
 Les niveaux compris entre Verbose et Critique sont empilés les uns sur les autres, autrement dit chaque niveau de suivi inclut tous les niveaux supérieurs hormis le niveau Désactivé. Par exemple, un écouteur qui écoute au niveau Avertissement reçoit les suivis des niveaux Critique, Erreur et Avertissement. Le niveau Tout inclut les événements du niveau Verbose au niveau Critique et les événements ActivityTracing.  
  
> [!CAUTION]
>  Les niveaux Informations, Commentaires et ActivityTracing génèrent de nombreux suivis, ce qui peut avoir un impact négatif sur le débit des messages si vous avez utilisé toutes les ressources disponibles sur l'ordinateur.  
  
## <a name="configuring-activity-tracing-and-propagation-for-correlation"></a>Configuration du suivi d'activité et de la propagation pour la corrélation  
 La valeur `activityTracing` spécifiée pour l'attribut `switchValue` est utilisée pour activer le suivi d'activité, qui émet des suivis pour les transferts et limites d'activité dans les points de terminaison.  
  
> [!NOTE]
>  Lorsque vous utilisez certaines fonctionnalités d’extensibilité dans WCF, vous pouvez obtenir un <xref:System.NullReferenceException> lorsque le suivi des activités est activé. Pour résoudre ce problème, vérifiez le fichier de configuration de votre application et assurez-vous que l'attribut `switchValue` de votre source de suivi n'a pas la valeur `activityTracing`.  
  
 L'attribut `propagateActivity` indique si l'activité doit être propagée vers d'autres points de terminaison qui participent à l'échange de messages. En affectant à cet attribut la valeur `true`, vous pouvez prendre des fichiers de suivi générés par deux points de terminaison quelconque et observer comment un ensemble de suivis sur un point de terminaison a été transféré vers un ensemble de suivis sur un autre point de terminaison.  
  
 Pour plus d’informations sur le suivi des activités et de propagation, consultez [Propagation](../../../../../docs/framework/wcf/diagnostics/tracing/propagation.md).  
  
 Les deux `propagateActivity` et `ActivityTracing` valeurs booléennes s’appliquent à System.ServiceModel TraceSource. Le `ActivityTracing` valeur s’applique également à n’importe quelle source de trace, y compris ceux définis par l’utilisateur ou WCF.  
  
 Vous ne pouvez pas utiliser l'attribut `propagateActivity` avec des sources de suivi définies par l'utilisateur. Pour la propagation d'ID d'activité de code utilisateur, assurez-vous de ne pas définir ServiceModel `ActivityTracing`, tout en ayant encore l'attribut `propagateActivity` ServiceModel défini à `true`.  
  
## <a name="see-also"></a>Voir aussi

- [Suivi](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
- [Guide pratique pour Créer et initialiser des écouteurs de Trace](https://go.microsoft.com/fwlink/?LinkId=94648)
- [Création d’un TraceListener personnalisé](https://go.microsoft.com/fwlink/?LinkId=96239)
