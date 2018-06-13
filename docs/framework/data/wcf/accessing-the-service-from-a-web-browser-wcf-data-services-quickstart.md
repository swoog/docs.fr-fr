---
title: Accès au service à partir d'un navigateur Web (démarrage rapide des services de données WCF)
ms.date: 03/30/2017
ms.assetid: 5a6fa180-3094-4e6e-ba2b-8c80975d18d1
ms.openlocfilehash: b7fcead5eed2dd4c0c779d9a881563a39f88d094
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33364003"
---
# <a name="accessing-the-service-from-a-web-browser-wcf-data-services-quickstart"></a>Accès au service à partir d'un navigateur Web (démarrage rapide des services de données WCF)
Dans cette tâche, vous allez démarrer [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] à partir de Visual Studio et éventuellement désactiver la lecture de flux dans le navigateur Web. Vous serez ensuite extraire le document de définition de service ainsi accéder aux ressources du service de données en soumettant des demandes HTTP GET via un navigateur Web aux ressources exposées.  
  
> [!NOTE]
>  Par défaut, Visual Studio affecte automatiquement un numéro de port à l'URI `localhost` sur votre ordinateur. Cette tâche utilise le numéro de port `12345` dans les exemples d'URI. Pour plus d’informations sur la définition d’un numéro de port spécifique dans votre projet Visual Studio, consultez [création du Service de données](../../../../docs/framework/data/wcf/creating-the-data-service.md).  
  
### <a name="to-request-the-default-service-document-by-using-internet-explorer"></a>Pour demander le document de service par défaut à l'aide d'Internet Explorer  
  
1.  Dans Internet Explorer, à partir de la **outils** menu, sélectionnez **Options Internet**, cliquez sur le **contenu** , cliquez sur **paramètres**et désactivez  **Activer la lecture du flux**.  
  
     Cette opération garantit que la lecture de flux est désactivée. Si vous ne désactivez pas cette fonctionnalité, le navigateur Web traitera le document encodé AtomPub retourné comme un flux XML au lieu d'afficher les données XML brutes.  
  
    > [!NOTE]
    >  Si votre navigateur ne peut pas afficher le flux sous forme de données XML brutes, vous devriez encore être en mesure de voir le flux sous forme de code source de la page.  
  
2.  Dans Visual Studio, appuyez sur la touche F5 pour démarrer le débogage de l'application.  
  
3.  Ouvrez un navigateur Web sur l'ordinateur local. Dans la barre d'adresses, entrez l'URI suivant :  
  
    ```  
    http://localhost:12345/northwind.svc  
    ```  
  
     Cette opération retourne le document du service par défaut qui contient une liste des jeux d'entités exposés par ce service de données.  
  
### <a name="to-access-entity-set-resources-from-a-web-browser"></a>Pour accéder aux ressources de jeu d'entités depuis un navigateur Web  
  
1.  Dans la barre d'adresse de votre navigateur Web, entrez l'URI suivant :  
  
    ```  
    http://localhost:12345/northwind.svc/Customers  
    ```  
  
     Cette opération retourne un jeu de tous les clients dans l'exemple de base de données Northwind.  
  
2.  Dans la barre d'adresse de votre navigateur Web, entrez l'URI suivant :  
  
    ```  
    http://localhost:12345/northwind.svc/Customers('ALFKI')  
    ```  
  
     Cette opération retourne une instance d'entité pour le client spécifique, `ALFKI`.  
  
3.  Dans la barre d'adresse de votre navigateur Web, entrez l'URI suivant :  
  
    ```  
    http://localhost:12345/northwind.svc/Customers('ALFKI')/Orders  
    ```  
  
     Cette opération parcourt la relation entre les clients et les ordres pour retourner un jeu de tous les ordres pour le client `ALFKI` spécifique.  
  
4.  Dans la barre d'adresse de votre navigateur Web, entrez l'URI suivant :  
  
    ```  
    http://localhost:12345/northwind.svc/Customers('ALFKI')/Orders?$filter=OrderID eq 10643  
    ```  
  
     Cette opération filtre des ordres qui appartiennent au client `ALFKI` spécifique afin que seul un ordre spécifique soit retourné selon la valeur `OrderID` fournie.  
  
## <a name="next-steps"></a>Étapes suivantes  
 Vous avez correctement accédé à [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] depuis un navigateur Web, et le navigateur a émis des demandes HTTP GET aux ressources spécifiées. Un navigateur Web fournit un moyen simple d'expérimenter la syntaxe d'adressage des demandes et d'afficher les résultats. Toutefois, un service des données de production n'est pas accessible en général par cette méthode. Généralement, les applications interagissent avec le service de données par le biais de code d'application ou de langages de script. Ensuite, vous allez créer une application cliente qui utilise des bibliothèques clientes pour accéder aux ressources du service des données comme s'il s'agissait d'objets CLR (Common Language runtime) :  
  
 [Création de l’application cliente du .NET Framework](../../../../docs/framework/data/wcf/creating-the-dotnet-client-application-wcf-data-services-quickstart.md)  
  
## <a name="see-also"></a>Voir aussi  
 [Accès aux ressources d’un service de données](../../../../docs/framework/data/wcf/accessing-data-service-resources-wcf-data-services.md)
