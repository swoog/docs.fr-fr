---
title: Modèles Visual Studio WCF
ms.date: 03/30/2017
ms.assetid: 6a608575-3535-4190-89da-911e24c8374f
ms.openlocfilehash: b0cca0cd585a45b795db4d573659e0d19ecd78dc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61780664"
---
# <a name="wcf-visual-studio-templates"></a>Modèles Visual Studio WCF
Modèles Visual Studio de Windows Communication Foundation (WCF) sont prédéfinis et des modèles d’élément que vous pouvez utiliser dans Visual Studio pour créer rapidement des services WCF et les applications s’y rapportant.  
  
## <a name="using-the-wcf-templates"></a>Utilisation des modèles WCF  
 Modèles WCF Visual Studio fournissent une structure de classe de base pour le développement de service. Spécifiquement, ces modèles fournissent les définitions de base pour les contrats de service, les contrats de données, les implémentations de services et les configurations. Vous pouvez utiliser ces modèles pour créer un service simple avec une interaction minimale du code, ainsi qu'un bloc de création pour des services plus avancés.  
  
### <a name="wcf-service-library-project-template"></a>Modèle de projet Bibliothèque du service WCF  
 Le modèle de projet bibliothèque du Service WCF est disponible dans la boîte de dialogue Nouveau projet sous **Visual C# \WCF** et **Visual Basic\WCF**.  
  
 Lorsque vous créez un projet à l’aide du **Service WCF** modèle, le nouveau projet inclut automatiquement les trois fichiers suivants :  
  
- Fichier de contrat de service (IService1.cs ou IService1.vb). Le fichier de contrat de service est une interface qui possède les attributs de service WCF appliqués. Ce fichier contient la définition d'un service simple destinée à vous aider à définir vos services et inclut des opérations basées des paramètres, ainsi qu'un exemple de contrat de données simple. Il s’agit du fichier par défaut affiché dans l’éditeur de code après avoir créé un projet de service WCF.  
  
- Fichier d'implémentation de service (Service1.cs ou Service1.vb). Le fichier d'implémentation de service implémente le contrat défini dans le fichier de contrat de service.  
  
- Fichier de configuration de l'application (App.config). Le fichier de configuration fournit les éléments de base d’un modèle de service WCF avec une liaison HTTP sécurisée. Il inclut également un point de terminaison applicable au service et active l'échange de métadonnées.  
  
> [!NOTE]
>  Visual Studio est configuré pour reconnaître le fichier App.config comme fichier de configuration pour le projet lorsqu’il est exécuté à l’aide de la [hôte de Service WCF (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md), qui est la configuration par défaut. Si la bibliothèque de services se trouve dans un fichier exécutable, vous devez déplacer le code de configuration vers le fichier de configuration du fichier exécutable : en effet, les fichiers de configuration des DLL ne sont pas valides.  
  
### <a name="wcf-service-application-template"></a>Modèle d'application de service WCF  
 Le modèle d’Application de Service WCF est disponible dans la boîte de dialogue Nouveau projet sous **Visual C# \WCF** et **Visual Basic\WCF**.  
  
 Lorsque vous créez un projet à l’aide du **Service d’Application Web WCF** modèle, le projet inclut les quatre fichiers suivants :  
  
- Fichier d'hôte de service (service1.svc).  
  
- Fichier de contrat de service (IService1.cs ou IService1.vb).  
  
- Fichier d'implémentation de service (Service1.svc.cs ou Service1.svc.vb).  
  
- Fichier de configuration Web (Web.config).  
  
 Le modèle crée automatiquement un site Web (à déployer dans un répertoire virtuel) et y héberge un service.  
  
### <a name="wcf-web-site-template"></a>Modèle de site Web WCF  
 Le modèle de Site Web de WCF est disponible dans la boîte de dialogue Nouveau projet sous **Visual C# \Web Site\WCF Service** et **Visual Basic\Web Site\WCF Service**. Cela crée les mêmes fichiers que ceux du modèle d’application de service WCF, mais les classe comme s’il s’agissait d’un site web ASP.NET. Les dossiers App_Code et App_Data sont créés.  
  
### <a name="wcf-service-item-template"></a>Modèle d'élément de service WCF  
 Le modèle d’élément de Service WCF est un modèle personnalisé qui fournit un moyen rapide d’ajouter des services WCF à vos projets Visual Studio existants.  
  
 Pour utiliser ce modèle, accédez à la **l’Explorateur de solutions** volet, cliquez sur le nom de votre projet, pointez sur **ajouter**, puis cliquez sur **un nouvel élément** pour lancer le **Ajouter nouveau Élément** boîte de dialogue.  
  
 L'interface de service et les fichiers d'implémentation sont placés dans le dossier du projet racine.  
  
 Le modèle tente de fusionner la section de configuration du nouveau service avec le fichier de configuration existant, si leurs types sont compatibles.  
  
 Un fichier d'hôte de service (service1.svc) est également créé si le projet existant est un projet Web.  
  
### <a name="wcf-wf-service-project-and-item-template"></a>Modèles d'élément et de projet de service WF WCF.  
 Ces modèles créent des services WCF qui hébergent un Service de Workflow, qui est un flux de travail qui est accessible comme un service web. Différents modèles existent pour les XAML et les modèles de programmation impératifs. À l'aide des modèles, vous pouvez créer des workflows séquentiels ou des workflows de l'ordinateur d'état. Pour plus d’informations sur ces types de flux de travail, consultez [Comment : Créer un flux de travail](../windows-workflow-foundation/how-to-create-a-workflow.md). Pour plus d’informations sur la création de projets de workflow, consultez [création de projets de flux de travail hérité](/visualstudio/workflow-designer/creating-legacy-workflow-projects).  
  
 Concepteur de Visual Studio est plus réactif lorsque type XOML workflows sont utilisés à la place du code en fonction ceux. Le workflow XOML est le type de workflow par défaut à créer.  
  
### <a name="wcf-syndication-service-library-template"></a>Modèle de la bibliothèque du service de syndication WCF  
 Ce modèle vous permet d’exposer votre flux au format RSS ou ATOM en tant qu’un service WCF. Pour plus d’informations, consultez [Syndication WCF](../../../docs/framework/wcf/feature-details/wcf-syndication.md).  
  
#### <a name="changing-the-address-of-the-feed"></a>Modification de l'adresse du flux  
 Le modèle de syndication utilise Internet Explorer au cours de l'exécution. Lorsque vous cliquez sur votre projet dans **l’Explorateur de Solutions** dans Visual Studio, sélectionnez **propriétés**, puis sélectionnez le **déboguer** onglet et vous pouvez voir l’adresse par défaut de la modèle. Internet Explorer tente d'ouvrir le flux à cette adresse.  
  
 Si vous modifiez l’adresse de votre flux, vous devez également modifier l’adresse dans le **déboguer** onglet. Sinon, Internet Explorer tente d'ouvrir le flux à l'adresse par défaut et échoue.  
  
### <a name="ajax-enabled-wcf-service-item-template"></a>Modèle d'élément de service WCF AJAX  
 Ce modèle expose un contrôle AJAX comme un service WCF. Pour plus d’informations sur les contrôles AJAX, consultez le [documentation sur le contrôle AJAX](https://go.microsoft.com/fwlink/?LinkId=96717).  
  
### <a name="silverlight-enabled-wcf-service-item-template"></a>Modèle d'élément de service WCF compatible Silverlight  
 Ce modèle crée un service Web qui fournit des données à un client Silverlight ou frontal. Le modèle peut être ajouté à un projet d’application Web ou site Web pour créer un service WCF, qui inclut le code de service et de configuration qui prennent en charge la communication avec un client Silverlight. Vous pouvez ensuite utiliser **ajouter une référence de Service** pour ajouter un proxy client du service au client et échanger des données entre le client Silverlight et le service WCF compatible Silverlight.  
  
 Pour accéder à ce modèle, cliquez sur un projet d’application Web ou site Web dans **l’Explorateur de solutions**, cliquez sur **ajouter un nouvel élément**, puis cliquez sur **Service WCF compatible Silverlight**.  
  
> [!NOTE]
>  Le service WCF compatible Silverlight expose un point de terminaison `basicHttpBinding` sans activer de paramètre de sécurité. Par conséquent, les informations concernant le service peuvent être obtenues par tous les clients qui s'y connectent. Les messages échangés entre le service et le client ne sont pas signés ni chiffrés. Pour sécuriser correctement le point de terminaison, vous devez utiliser l'authentification ASP.NET, HTTPS ou d'autres mécanismes.  
  
## <a name="see-also"></a>Voir aussi

- [WCF Service Host (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)
- [Client test WCF (WcfTestClient.exe)](../../../docs/framework/wcf/wcf-test-client-wcftestclient-exe.md)
