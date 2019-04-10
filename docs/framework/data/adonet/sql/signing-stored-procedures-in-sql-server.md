---
title: Signature de procédures stockées dans SQL Server
ms.date: 01/05/2018
ms.assetid: eeed752c-0084-48e5-9dca-381353007a0d
ms.openlocfilehash: 2c2076294c0e06ec411ceb1f5b1238dc3d7eb304
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59313916"
---
# <a name="signing-stored-procedures-in-sql-server"></a>Signature de procédures stockées dans SQL Server
 Une signature numérique est un condensat des données qui est chiffré avec la clé privée du signataire. La clé privée garantit que la signature numérique est unique à son porteur ou propriétaire. Vous pouvez signer les assemblys, les fonctions (à l’exception des fonctions table inline), les déclencheurs et les procédures stockées.  
  
 Vous pouvez signer une procédure stockée avec un certificat ou une clé asymétrique. Cela est très utile lorsque des autorisations ne peuvent pas être héritées par le biais du chaînage des propriétés ou lorsque ce dernier est rompu, comme avec SQL dynamique. Vous pouvez ensuite créer un utilisateur mappé au certificat, octroi d’autorisations utilisateur sur les objets de que la procédure stockée doit accéder au certificat.  

 Vous pouvez également créer une connexion mappée sur le même certificat, puis accorder des autorisations au niveau du serveur nécessaires pour cette connexion ou ajouter la connexion à une ou plusieurs des rôles serveur fixes. Il est conçu pour éviter d’activer la `TRUSTWORTHY` de base de données de paramètre pour les scénarios dans lesquels des autorisations de niveau supérieur sont nécessaires.  
  
 Lorsque la procédure stockée est exécutée, SQL Server combine les autorisations de l’utilisateur du certificat et/ou de la connexion avec celles de l’appelant. Contrairement à la `EXECUTE AS` clause, elle ne modifie pas le contexte d’exécution de la procédure. Les fonctions intégrées qui retournent les noms d'accès et d'utilisateur retournent le non de l'appelant, et non celui de l'utilisateur du certificat.  
  
## <a name="creating-certificates"></a>Création de certificats  
 Lorsque vous signez une procédure stockée avec un certificat ou une clé asymétrique, un condensat des données contenant le hachage chiffré du code de procédure stockée, ainsi que l’exécution-en tant qu’utilisateur, est créé à l’aide de la clé privée. Au moment de l’exécution, le condensat des données est chiffré avec la clé publique et comparée à la valeur de hachage de la procédure stockée. Modification de l’exécution-comme utilisateur invalide la valeur de hachage afin que la signature numérique ne correspond plus à. Modification de la procédure stockée supprime la signature entièrement, ce qui empêche une personne qui n’a pas accès à la clé privée à partir de la modification du code de procédure stockée. Dans les deux cas, vous devez signer à nouveau la procédure chaque fois que vous modifiez le code ou l’exécution-en tant qu’utilisateur.  
  
 Il existe deux étapes impliquées dans la signature d’un module :  
  
1. Créez un certificat à l'aide de l'instruction Transact-SQL `CREATE CERTIFICATE [certificateName]`. Cette instruction possède plusieurs options permettant de définir une date de début et de fin, de même qu'un mot de passe. La date d’expiration par défaut est un an.  
  
1. Signez la procédure avec le certificat en utilisant l'instruction Transact-SQL `ADD SIGNATURE TO [procedureName] BY CERTIFICATE [certificateName]`.  

Une fois que le module a été signé, un ou plusieurs principaux doit être créé pour contenir les autorisations supplémentaires qui doivent être associées avec le certificat.  

Si le module a besoin des autorisations de niveau de base de données supplémentaires :  
  
1. Créez un utilisateur de base de données associé à ce certificat à l'aide de l'instruction Transact-SQL `CREATE USER [userName] FROM CERTIFICATE [certificateName]`. Cet utilisateur existe dans la base de données uniquement et n’est pas associé à un compte de connexion, sauf si une connexion a également été créée à partir de ce même certificat.  
  
1. Autorisez l’utilisateur du certificat requis au niveau de la base de données.  
  
Si le module a besoin des autorisations supplémentaires au niveau du serveur :  
  
1. Copiez le certificat à la `master` base de données.  
 
1. Créer une connexion associée à ce certificat à l’aide de l’instruction Transact-SQL `CREATE LOGIN [userName] FROM CERTIFICATE [certificateName]` instruction.  
  
1. Autorisez la connexion de certificat requis au niveau du serveur.  
  
> [!NOTE]  
>  Un certificat ne permet pas d'accorder des autorisations à un utilisateur dont les autorisations ont été révoquées à l'aide de l'instruction DENY. L'instruction DENY a toujours priorité sur l'instruction GRANT, ce qui empêche l'appelant d'hériter des autorisations accordées à l'utilisateur du certificat.  
  
## <a name="external-resources"></a>Ressources externes  
 Pour plus d'informations, voir les ressources ci-dessous.  
  
|Ressource|Description|  
|--------------|-----------------|  
|[Signature de module](https://go.microsoft.com/fwlink/?LinkId=98590) dans la documentation en ligne de SQL Server|Décrit la signature de module, en fournissant un exemple de scénario et des liens vers les rubriques pertinentes relatives à Transact-SQL.|  
|[Signature de procédures stockées avec un certificat](/sql/relational-databases/tutorial-signing-stored-procedures-with-a-certificate) dans la documentation en ligne de SQL Server|Propose un didacticiel de signature d'une procédure stockée à l'aide d'un certificat.|  
  
## <a name="see-also"></a>Voir aussi

- [Sécurisation des applications ADO.NET](../../../../../docs/framework/data/adonet/securing-ado-net-applications.md)
- [Vue d'ensemble de la sécurité SQL Server](../../../../../docs/framework/data/adonet/sql/overview-of-sql-server-security.md)
- [Scénarios de sécurité des applications dans SQL Server](../../../../../docs/framework/data/adonet/sql/application-security-scenarios-in-sql-server.md)
- [Gestion des autorisations avec les procédures stockées dans SQL Server](../../../../../docs/framework/data/adonet/sql/managing-permissions-with-stored-procedures-in-sql-server.md)
- [Écriture de Dynamic SQL sécurisé dans SQL Server](../../../../../docs/framework/data/adonet/sql/writing-secure-dynamic-sql-in-sql-server.md)
- [Personnalisation des autorisations avec l'emprunt d'identité dans SQL Server](../../../../../docs/framework/data/adonet/sql/customizing-permissions-with-impersonation-in-sql-server.md)
- [Modification des données avec les procédures stockées](../../../../../docs/framework/data/adonet/modifying-data-with-stored-procedures.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
