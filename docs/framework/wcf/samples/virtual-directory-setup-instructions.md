---
title: Instructions d'installation du répertoire virtuel
ms.date: 03/30/2017
ms.assetid: 3c62cab5-81a4-48b6-ac8c-9ce33a85a157
ms.openlocfilehash: fdff88026a49989870ee5c47f9a38a65ecad3c80
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62007550"
---
# <a name="virtual-directory-setup-instructions"></a>Instructions d'installation du répertoire virtuel
Les exemples Windows Communication Foundation (WCF) sont destinées à partager un répertoire virtuel commun nommé servicemodelsamples est mappé au dossier %SystemDrive%\inetpub\wwwroot\servicemodelsamples.  
  
> [!NOTE]
>  %SystemDrive% correspond généralement à C: ou D:, en fonction de l'emplacement de lecteur où Internet Information Services (IIS) est installé.  
  
 Vous pouvez exécuter les fichiers Setupvroot.bat et Cleanupvroot.bat à partir de la [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md) pour créer le répertoire virtuel. Si vous préférez créer le répertoire virtuel manuellement, exécutez les procédures suivantes.  
  
## <a name="procedures"></a>Procédures  
  
#### <a name="to-create-a-virtual-directory-in-iis-70-or-75"></a>Pour créer un répertoire virtuel dans IIS 7.0 ou 7.5  
  
1. À partir de la **Démarrer** menu, cliquez sur **exécuter**, puis tapez **inetmgr** pour ouvrir le composant logiciel enfichable MMC Internet Information Services (IIS).  
  
2. Dans le volet gauche, développez le nœud portant le nom d’ordinateur, puis développez le **Sites** nœud.  
  
3. Avec le bouton droit **Site Web par défaut**, puis sélectionnez **ajouter une Application** pour ouvrir le **fenêtre d’ajouter une Application**.  
  
4. Dans la fenêtre, tapez `servicemodelsamples` comme alias pour le répertoire virtuel que vous créez.  
  
5. Créez le répertoire suivant : %SystemDrive%\inetpub\wwwroot\servicemodelsamples  
  
6. Affectez la valeur %SystemDrive%\inetpub\wwwroot\servicemodelsamples au chemin d’accès physique.  La plupart des exemples WCF copient les fichiers exécutables de service dans cet emplacement une fois générés.  
  
7. Cliquez sur **OK**. L'application Web est créée pour les exemples WCF.  
  
    > [!NOTE]
    >  Cette tâche doit être exécutée qu’une seule fois, étant donné que tous les exemples WCF utilisent l’application Web même (servicemodelsamples).  
  
    > [!NOTE]
    >  Dans cette documentation, le terme `virtual directory` est synonyme du terme `Web application`.  
  
     Outre la création du répertoire virtuel, vous devez également définir ses propriétés pour permettre l’exécution des services WCF. Pour plus d'informations, consultez ce qui suit.  
  
#### <a name="to-create-a-virtual-directory-in-iis-51-or-60"></a>Pour créer un répertoire virtuel dans IIS 5.1 ou 6.0 :  
  
1. Ouvrez une fenêtre d’invite de commandes et tapez `start inetmgr` pour ouvrir le composant logiciel enfichable MMC Internet Information Services (IIS).  
  
2. Dans le volet gauche, développez le nœud portant le nom d’ordinateur, puis développez le **Sites Web** nœud.  
  
3. Avec le bouton droit **Site Web par défaut** et sélectionnez **nouveau, le répertoire virtuel** pour ouvrir l’Assistant Création de répertoire virtuel.  
  
4. Dans l’Assistant, tapez `servicemodelsamples` comme alias pour le répertoire virtuel que vous créez.  
  
5. Affectez la valeur %SystemDrive%\inetpub\wwwroot\servicemodelsamples au chemin. La plupart des exemples WCF copient les fichiers exécutables de service dans cet emplacement une fois générés.  
  
6. Cliquez sur **Suivant**.  
  
7. Les cases à cocher suivantes sont activées par défaut :  
  
    - **Read**  
  
    - **Exécuter des scripts (tels que ASP)**  
  
8. Cliquez sur **suivant**, puis cliquez sur **Terminer** pour terminer l’Assistant.  
  
    > [!NOTE]
    >  Cette tâche doit être exécutée qu’une seule fois, car tous les exemples WCF utilisent le même répertoire virtuel servicemodelsamples.  
  
#### <a name="to-set-additional-virtual-directory-properties-in-iis-70-or-75"></a>Pour définir les propriétés de répertoire virtuel supplémentaire dans IIS 7.0 ou 7.5  
  
1. Cliquez sur le nœud servicemodelsamples. Deux vues figurent au bas de la fenêtre. Sélectionnez **affichage des fonctionnalités** s’il n’est pas déjà sélectionné.  
  
2. Double-cliquez sur l’entrée **exploration des répertoires**.  
  
3. Dans le volet Actions, sélectionnez le **activer** option. Cela permet d'accéder au répertoire du répertoire à l'aide d'Internet Explorer, ce qui est utile lors du débogage d'un service.  
  
 Enfin, vous devez définir les propriétés de sécurité du dossier servicemodelsamples afin d’autoriser son accès. Pour plus d'informations, consultez ce qui suit.  
  
#### <a name="to-set-additional-virtual-directory-properties-in-iis-51-or-60"></a>Pour définir des propriétés de répertoire virtuel supplémentaires dans IIS 5.1 ou 6.0  
  
1. Cliquez sur le nœud servicemodelsamples, puis sur **propriétés**.  
  
2. Les cases à cocher suivantes sont activées par défaut :  
  
    - **Read**  
  
    - **Accès au journal**  
  
    - **Indexer cette ressource**  
  
3. Sélectionnez le **exploration des répertoires** case à cocher. Cela permet d'accéder au répertoire du répertoire à l'aide d'Internet Explorer, ce qui est utile lors du débogage d'un service.  
  
#### <a name="to-set-security-properties-of-the-folder-in-iis-70-or-75"></a>Pour définir les propriétés de sécurité du dossier dans IIS 7.0 ou 7.5  
  
1. Ouvrez le répertoire %SystemDrive%\inetpub\wwwroot\servicemodelsamples.  
  
2. Cliquez sur le dossier servicemodelsamples et cliquez sur **partage** ou **partage avec**.  
  
3. Cliquez sur la flèche bas à gauche de la **ajouter** bouton.  
  
4. Sélectionnez le **trouver** entrée. Le **sélectionner des utilisateurs ou groupes** fenêtre s’ouvre.  
  
5. Cliquez sur **Avancé**.  
  
6. Cliquez sur **emplacements**. Le **emplacements** fenêtre est maintenant ouverte.  
  
7. Sélectionnez l'entrée correspondant à l'ordinateur en cours d'utilisation. Il est important de sélectionner l'ordinateur local et non une entrée correspondant à tous les domaines ou réseaux répertoriés. Une fois que vous avez sélectionné l’ordinateur, cliquez sur **OK**.  
  
8. Cliquez sur **trouver maintenant**. Cela permet d'inclure dans les résultats de la recherche les objets associés à l'ordinateur local.  
  
9. Rechercher la **IIS_IUSRS** entrée dans le **nom (nom unique relatif)** colonne. Sélectionnez cette entrée et cliquez sur **OK** fenêtre des résultats pour fermer la recherche.  
  
10. Cliquez sur **OK** pour fermer la **sélectionner des utilisateurs ou groupes** fenêtre.  
  
11. Cliquez sur **partage** pour conserver les modifications.  
  
12. Une fois les modifications apportées à activer le partage sont terminées, cliquez sur **fait** pour fermer la **le partage de fichiers** fenêtre.  
  
#### <a name="to-set-security-properties-of-the-folder-in-iis-51-or-60"></a>Pour définir les propriétés de sécurité de ce dossier dans IIS 5.1 ou 6.0 :  
  
1. Ouvrez le répertoire %SystemDrive%\inetpub\wwwroot\servicemodelsamples.  
  
2. Cliquez sur le **servicemodelsamples** dossier, puis cliquez sur **partage et sécurité.**  
  
3. Cliquez sur l'onglet **Sécurité** .  
  
4. Si vous utilisez IIS 6.0, dans le **noms d’utilisateur ou groupe** boîte, vérifiez si **compte Invité Internet** est répertorié.  
  
     Si ce n'est pas le cas :  
  
    1. Cliquez sur **Démarrer**, puis sur **Panneau de configuration**.  
  
    2. Si vous ne voyez pas le **comptes d’utilisateur** icône, cliquez sur **basculer vers l’affichage de la catégorie**.  
  
    3. Cliquez sur le **comptes d’utilisateur** icône.  
  
    4. Sous « ou une icône du Panneau de configuration, » cliquez sur **comptes d’utilisateur**.  
  
    5. Dans le **comptes d’utilisateur** boîte de dialogue, cliquez sur le **avancé** onglet.  
  
    6. Cliquez sur **Avancé**.  
  
    7. Dans le **utilisateurs et groupes locaux** boîte de dialogue, cliquez pour développer le **utilisateurs** dossier.  
  
    8. Dans le volet droit, double-cliquez sur **compte Invité Internet**.  
  
    9. Dans le **propriétés** boîte de dialogue, copiez le nom utilisé en tant que compte Invité Internet. Par défaut, le nom commence par « USR_ » suivi du nom de l'ordinateur.  
  
    10. Fermez la boîte de dialogue **Propriétés** .  
  
    11. Fermer le **utilisateurs et groupes locaux** boîte de dialogue.  
  
    12. Fermer le **comptes d’utilisateur** boîte de dialogue.  
  
    13. Fermez l’autre **comptes d’utilisateur** boîte de dialogue.  
  
    14. Dans le **propriétés de servicemodelsamples** boîte de dialogue le **sécurité** , cliquez sur **ajouter**.  
  
    15. Tapez le nom de l’ordinateur suivi d’une barre oblique inverse, puis collez le nom du compte d’utilisateur Internet, par exemple, myMachineName\\InternetGuestAccountName %  
  
    16. Cliquez sur **vérifier les noms** pour vérifier l’ajout. S'il est valide, ce nom figure en majuscules soulignées.  
  
5. Pour IIS 6.0, vérifiez également que le SERVICE réseau est répertorié dans le **noms d’utilisateur ou groupe** boîte.  
  
     Si SERVICE RÉSEAU n'est pas répertorié :  
  
    1. Cliquez sur **Ajouter**.  
  
    2. Dans le **sélectionner des utilisateurs ou groupes** boîte de dialogue, tapez le nom de l’ordinateur suivi d’une barre oblique inverse.  
  
    3. Type **service** après la barre oblique inverse (sans espace).  
  
    4. Cliquez sur **vérifier les noms**.  
  
    5. Si plusieurs noms sont trouvés, sélectionnez **SERVICE réseau** et cliquez sur **OK**.  
  
    6. Cliquez sur **OK** pour fermer la **sélectionner des utilisateurs ou groupes** boîte de dialogue.  
  
6. Si vous utilisez Windows XP SP2 avec IIS 5.1, vérifiez que le compte Invité Internet et ASPNET sont répertoriés dans le **noms d’utilisateur ou groupe** boîte.  
  
     Notez que l’utilisateur ASPNET peut être un membre d’intégrés **utilisateurs** groupe de sécurité. Dans ce cas, puis si le **utilisateurs** groupe est répertorié dans la boîte de dialogue, vous n’avez pas besoin pour l’ajouter en tant qu’élément distinct à la liste des utilisateurs autorisés.  
  
     Pour vérifier qu’ASPNET fait partie de la **utilisateurs** groupe de sécurité :  
  
    1. Sur le **Démarrer** menu, cliquez sur **le panneau de configuration**.  
  
    2. Cliquez sur le **comptes d’utilisateur** icône.  
  
    3. Dans le **groupe** colonne, vérifiez que la valeur de **ASPNET** est « Utilisateurs ».  
  
## <a name="see-also"></a>Voir aussi

- [Instructions relatives à l’hébergement dans Internet Information Services](../../../../docs/framework/wcf/samples/internet-information-service-hosting-instructions.md)
