---
title: Gestion des erreurs
ms.date: 03/30/2017
ms.assetid: c948841a-7db9-40ae-9b78-587d216cbcaf
ms.openlocfilehash: 396ad7ba6f690cedf783adcf180c92a88427a959
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54695554"
---
# <a name="error-handling"></a>Gestion des erreurs
## <a name="error-handling-in-windows-communication-foundation"></a>Gestion des erreurs dans Windows Communication Foundation  
 Lorsqu'un service rencontre une exception ou une erreur inattendue, il existe plusieurs manières de concevoir une solution de gestion des exceptions. Il n’existe aucun unique « correct » ou « meilleures pratiques » la gestion des erreurs solution, il existe plusieurs chemins d’accès valides à prendre en compte. Il est recommandé d’implémenter une solution hybride qui combine plusieurs approches de la liste ci-dessous, selon la complexité de l’implémentation de WCF, le type et la fréquence des exceptions, le texte gérées et la nature non prise en charge de la exceptions et tout suivi associé, journalisation ou exigences de la stratégie.  
  
 Ces solutions sont expliquées plus en détail dans le reste de cette section.  
  
### <a name="the-microsoft-enterprise-library"></a>Microsoft Enterprise Library  
 Le bloc d'application de gestion des exceptions Microsoft Enterprise Library permet d'implémenter des modèles communs de conception et de créer une stratégie cohérente de traitement des exceptions qui se produisent dans toutes les couches de l'architecture d'une application d'entreprise. Il est conçu pour prendre en charge le code spécifique contenu dans les instructions catch des composants de l'application. Au lieu de répéter ce code (par exemple le code qui stocke les informations sur l'exception) dans des blocs catch identiques d'une application, le bloc d'application de gestion des exceptions permet aux développeurs d'encapsuler cette logique comme gestionnaires d'exceptions réutilisables.  
  
 Cette bibliothèque comprend un gestionnaire d'exceptions du contrat d'erreur prêt à l'emploi. Ce gestionnaire d'exceptions est conçu pour une utilisation aux limites du service Windows® Communication Foundation (WCF) et génère un nouveau contrat d'erreur à partir de l'exception.  
  
 Les blocs d'application visent à incorporer les meilleures pratiques fréquemment utilisées et à fournir une approche commune pour la gestion des exceptions dans votre application. D'autre part, les gestionnaires d'erreurs personnalisés et les contrats d'erreur développés s'avèrent également très utiles. Par exemple, les gestionnaires d’erreurs personnalisés offrent la possibilité de promouvoir automatiquement toutes les exceptions en FaultExceptions et également d’ajouter des fonctionnalités de journalisation à votre application.  
  
 Pour plus d’informations, consultez [Microsoft Enterprise Library](https://msdn.microsoft.com/library/ff632023.aspx).  
  
### <a name="dealing-with-expected-exceptions"></a>Traiter les exceptions attendues  
 Le plan d’action approprié consiste à intercepter les exceptions attendues dans chaque opération ou d’un point d’extensibilité concerné, de déterminer si elles peuvent être récupérées et retournent l’erreur personnalisée appropriée dans une FaultException\<T >  
  
### <a name="dealing-with-unexpected-exceptions-using-an-ierrorhandler"></a>Traiter les exceptions inattendues à l'aide d'un IErrorHandler  
 Pour traiter les exceptions inattendues, la procédure recommandée est « connecter » un IErrorHandler. Gestionnaires d’erreurs uniquement interceptent des exceptions au niveau du runtime WCF (la couche « modèle de service »), pas au niveau de la couche de canal. La seule manière de connecter un IErrorHandler au niveau de canal consiste à créer un canal personnalisé, ce qui est déconseillé dans la plupart des scénarios.  
  
 Une exception « inattendue » n’est généralement ni une exception irrécupérable ni une exception de traitement ; Il est, au lieu de cela, une exception utilisateur inattendue. Une exception irrécupérable (par exemple, une exception de mémoire insuffisante), généralement gérée par le [Gestionnaire d’exceptions de modèle de Service](xref:System.ServiceModel.Dispatcher.ExceptionHandler) automatiquement – ne peut généralement être gérée correctement et la seule raison de gérer cette exception tout est peut-être effectuer un enregistrement supplémentaire ou de retourner une exception standard au client. Une exception de traitement se produit dans le traitement du message (par exemple, au niveau de la sérialisation, de l'encodeur ou du formateur), généralement elle ne peut pas être gérée dans un IErrorHandler, car il est trop tôt ou trop tard pour que le gestionnaire d'erreurs intervienne lorsque ces exceptions se produisent. De même, les exceptions de transport ne peuvent pas être gérées dans un IErrorHandler.  
  
 Avec un IErrorHandler, vous pouvez explicitement contrôler le comportement de votre application lorsqu'une exception est levée. Vous pouvez :  
  
1.  Déterminer s'il faut ou non envoyer une erreur au client  
  
2.  Remplacer une exception par une erreur  
  
3.  Remplacer une erreur par une autre  
  
4.  Effectuer l'enregistrement ou le suivi  
  
5.  Exécuter d'autres activités personnalisées  
  
 Pour installer un gestionnaire d'erreurs personnalisé, ajoutez-le à la propriété ErrorHandlers des répartiteurs de canal de votre service.  Il est possible d'avoir plusieurs gestionnaire d'erreurs et ils sont appelés dans l'ordre où ils sont ajoutés à cette collection.  
  
 IErrorHandler.ProvideFault contrôle le message d'erreur qui est envoyé au client. Cette méthode est appelée quel que soit le type de l'exception levée par une opération dans votre service. Si aucune opération n'est effectuée ici, WCF suppose le comportement par défaut et continue comme si aucun gestionnaire d'erreurs personnalisé n'était installé.  
  
 Un domaine dans lequel vous pouvez adopter cette approche est lorsque vous souhaitez créer une place centrale de conversion des exceptions en erreurs avant qu'elles ne soient envoyées au client (en veillant à ce que l'instance ne soit pas supprimée et le canal déplacé vers l'état d'erreur).  
  
 La méthode IErrorHandler.HandleError est généralement utilisée pour implémenter des comportements d'erreur tels que l'enregistrement des erreurs, les notifications système, la fermeture de l'application, etc. IErrorHandler.HandleError peut être appelée à plusieurs endroits dans le service, et selon l'endroit où l'erreur est retournée, la méthode HandleError peut ou non être appelée par le thread même que l'opération ; aucune garantie n'est donnée à cet égard.  
  
### <a name="dealing-with-exceptions-outside-wcf"></a>Traiter les exceptions en dehors de WCF  
 Souvent, des exceptions de configuration, des exceptions de chaîne de connexion à la base de données, et d'autres exceptions similaires peuvent se produire dans le contexte d'une application WCF, mais elles ne sont pas des exceptions provoquées par le modèle de service ou le service Web. Ces exceptions sont des exceptions « standard » externes au service web et doivent être traitées comme les autres exceptions externes dans l’environnement doivent être traités.  
  
### <a name="tracing-exceptions"></a>Suivi d'exceptions  
 Le traçage est le lieu uniquement « fourre-tout » où vous pouvez afficher toutes les exceptions. Pour plus d'informations sur le suivi et l'enregistrement des exceptions, consultez Suivi et enregistrement.  
  
### <a name="uri-template-errors-when-using-webgetattribute-and-webinvokeattribute"></a>Erreurs de modèle d'URI lors de l'utilisation de WebGetAttribute et WebInvokeAttribute  
 Les attributs WebGet et WebInvoke vous permettent de spécifier un modèle d'URI qui mappe les composants de l'adresse de requête aux paramètres d'opération. Par exemple, le modèle d'URI « weather/{state}/{city} » mappe l'adresse de requête dans les jetons de littéraux, un état de paramètre nommé et un paramètre nommé city. Ces paramètres peuvent être liés par nom à certains des paramètres formels de l'opération.  
  
 Les paramètres de modèle s'affichent au format de chaînes dans l'URI et les paramètres formels d'un contrat typé peuvent être des types non-chaînes. Par conséquent, une conversion doit avoir lieu avant que l'opération puisse être appelée. Un [tableau de formats de conversion](wcf-web-http-programming-model-overview.md) est disponible.  
  
 Cependant, si la conversion échoue, il n'existe aucun moyen d'indiquer à l'opération qu'une erreur s'est produite. Conversion de type plutôt que de surfaces sous la forme d'un échec de distribution.  
  
 Une erreur de distribution de conversion de type peut être inspectée de la même façon que d'autres types d'erreurs de distribution en installant un gestionnaire d'erreurs. Le point d'extensibilité d'IErrorHandler est appelé pour gérer les exceptions au niveau de service. À partir de là, choisissez la réponse à renvoyer à l’appelant, et effectuez des tâches et des rapports personnalisés.  
  
## <a name="see-also"></a>Voir aussi
- [Programmation WCF de base](../basic-wcf-programming.md)
