---
title: Composant logiciel enfichable MMC Configuration WS-AtomicTransaction
ms.date: 03/30/2017
ms.assetid: 23592973-1d51-44cc-b887-bf8b0d801e9e
ms.openlocfilehash: b1d86fa57b31d1f9be12f76c28f9d042e7e28e24
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59138203"
---
# <a name="ws-atomictransaction-configuration-mmc-snap-in"></a>Composant logiciel enfichable MMC Configuration WS-AtomicTransaction
Le composant logiciel enfichable MMC Configuration WS-AtomicTransaction est utilisé pour configurer une partie des paramètres WS-AtomicTransaction sur les ordinateurs locaux et distants.  
  
## <a name="remarks"></a>Notes  
 Si vous exécutez [!INCLUDE[wxp](../../../includes/wxp-md.md)] ou [!INCLUDE[ws2003](../../../includes/ws2003-md.md)], le composant logiciel enfichable MMC peut être recherchée en accédant à **contrôle panneau/Administrative Tools/Services de composants /**, droit **poste de travail**, et en sélectionnant **propriétés**. C'est le même emplacement que celui dans lequel vous pouvez configurer le MSDTC. Les options disponibles pour la configuration sont regroupées sous le **WS-AT** onglet.  
  
 Si vous exécutez Windows Vista ou [!INCLUDE[lserver](../../../includes/lserver-md.md)], le composant logiciel enfichable MMC est accessible en cliquant sur le **Démarrer** bouton et en tapant `dcomcnfg.exe` dans le **recherche** boîte. Lorsque la console MMC est ouverte, accédez à la **mes travail\distributed Transaction Coordinator\Local DTC** nœud, cliquez droit puis sélectionnez **propriétés**. Les options disponibles pour la configuration sont regroupées sous le **WS-AT** onglet.  
  
 Les étapes précédentes sont utilisées pour lancer le composant logiciel enfichable afin de configurer un ordinateur local. Si vous souhaitez configurer un ordinateur distant, vous devez rechercher le nom de l’ordinateur distant dans **contrôle panneau/Administrative Tools/Services de composants /** et effectuer des étapes similaires si vous exécutez [!INCLUDE[wxp](../../../includes/wxp-md.md)] ou [!INCLUDE[ws2003](../../../includes/ws2003-md.md)]. Si vous exécutez Windows Vista ou [!INCLUDE[lserver](../../../includes/lserver-md.md)], suivez les étapes précédentes pour Vista et [!INCLUDE[lserver](../../../includes/lserver-md.md)], mais utiliser le **Distributed Transaction Coordinator\Local DTC** nœud sous le nœud de l’ordinateur distant.  
  
 Pour utiliser l'interface utilisateur fournie par l'outil, vous devez enregistrer le fichier WsatUI.dll, situé à l'emplacement suivant :  
  
 **%PROGRAMFILES%\Microsoft SDKs\Windows\v6.0\Bin\WsatUI.dll**  
  
 L'inscription peut être faite par la commande suivante.  
  
```Output  
regasm.exe /codebase WsatUI.dll  
```  
  
 Vous pouvez utiliser cet outil pour modifier les paramètres de base WS-AtomicTransaction. Par exemple, vous pouvez activer et désactiver le support de protocole de WS-AtomicTransaction, configurer les ports HTTP pour WS-AT, lier un certificat SSL au port HTTP, configurer des certificats en spécifiant les noms de sujet correspondants, sélectionner le mode de suivi et définir la valeur par défaut et les délais d'attente maximum.  
  
 Si vous devez configurer uniquement le support WS-AtomicTransaction sur l'ordinateur local, vous pouvez utiliser la version de ligne de commande de cet outil. Pour plus d’informations sur l’outil de ligne de commande, consultez le [(wsatConfig.exe) de l’utilitaire de Configuration WS-AtomicTransaction](../../../docs/framework/wcf/ws-atomictransaction-configuration-utility-wsatconfig-exe.md) rubrique.  
  
 Sachez que le composant logiciel enfichable MMC et l'outil de ligne de commande ne prennent pas en charge la configuration de tous les paramètres WS-AT. Ces paramètres ne peuvent être modifiés qu'en modifiant directement le registre. Pour plus d’informations sur ces paramètres de Registre, consultez [configuration prise en charge de WS-Atomic Transaction](../../../docs/framework/wcf/feature-details/configuring-ws-atomic-transaction-support.md).  
  
### <a name="user-interface-description"></a>Description de l'interface utilisateur  
 **Activer la prise en charge du réseau WS-Atomic Transaction**:  
  
 Lorsque vous sélectionnez ou désélectionnez cette case à cocher, cela active ou désactive tous les composants d'interface utilisateur de ce composant logiciel enfichable.  
  
 Avant d'activer cette case à cocher, vous devez vous assurer que l'accès au réseau DTC est activé (communications entrantes ou sortantes, ou encore les deux). Cette valeur peut être vérifiée dans le **sécurité** onglet du composant logiciel enfichable MSDTC.  
  
#### <a name="network-group-box"></a>Zone de groupe Réseau  
 Vous pouvez spécifier le port HTTPS et des paramètres de sécurité supplémentaires, tels que le chiffrement SSL dans le groupe Réseau. Ce groupe est désactivé (grisé) si les transactions réseau DTC ne sont pas activées.  
  
 **Port HTTPS**  
  
 C'est la valeur du port HTTPS utilisée pour WS-AT. Cette valeur doit être un nombre compris dans la plage 1-65535 (pour représenter un port valide). La modification du port HTTP modifie la configuration du service HTTP, ce qui signifie que l’adresse de service WS-AT utilisée précédemment est libérée et qu’une nouvelle adresse de service WS-AT est enregistrée sur la base du nouveau port. De plus, le port que vous venez de sélectionner est chiffré avec le certificat sélectionné pour le chiffrement SSL.  
  
> [!NOTE]
>  Si vous avez déjà activé le pare-feu avant d'exécuter cet outil, le port est enregistré automatiquement dans la liste d'exceptions. Si le pare-feu est désactivé avant l'exécution de cet outil, aucun élément supplémentaire n'est configuré concernant le pare-feu.  
  
 Si vous activez le pare-feu après avoir configuré WS-AT, vous devez réexécuter cet outil et fournir le numéro de port à l'aide de ce paramètre. Si vous désactivez le pare-feu après la configuration, WS-AT continue à fonctionner sans entrée supplémentaire.  
  
 **Certificat de point de terminaison**  
  
 En cliquant sur le **sélectionnez** bouton affiche une liste avec les certificats actuellement disponibles sur l’ordinateur Local, ce qui permet de l’utilisateur de sélectionner le certificat peut être utilisé pour le chiffrement SSL. Les certificats doivent posséder une clé privée. Si ce n'est pas le cas, un message d'erreur s'affiche.  
  
> [!NOTE]
>  Lorsque vous définissez un certificat SSL pour un port sélectionné, vous remplacez le certificat SSL d’origine associé à ce port, le cas échéant.  
  
 **Comptes autorisés**  
  
 En cliquant sur le **sélectionnez** bouton appelle l’éditeur de liste de contrôle d’accès Windows, où vous pouvez spécifier l’utilisateur ou le groupe qui peut participer à WS-Atomic transactions en vérifiant la **autoriser** ou **Deny** zone le **participer** groupe d’autorisations.  
  
 **Certificats autorisés**  
  
 En cliquant sur le **sélectionnez** bouton affiche une liste des certificats actuellement disponibles sur l’ordinateur local. Vous pouvez sélectionner ensuite les identités de certificat autorisées à participer à WS-AtomicTransaction.  
  
#### <a name="timeout-group-box"></a>Zone de groupe Délai d'attente  
 Le **délai d’attente** zone de groupe vous permet de spécifier le délai d’expiration par défaut et maximale pour une transaction WS-Atomic. Les valeurs valides de délai d'attente sortant sont comprises entre 1 et 3 600. Les valeurs valides de délai d'attente entrant sont comprises entre 0 et 3 600.  
  
#### <a name="tracing-and-logging-group-box"></a>Zone de groupe Suivi et journalisation  
 Le **suivi et de journalisation** zone de groupe vous permet de configurer le souhaité de suivi et le niveau de journalisation.  
  
 En cliquant sur le **Options** bouton appelle une page où vous pouvez spécifier des paramètres supplémentaires.  
  
 Le **niveau de Trace** zone de liste déroulante vous permet de choisir parmi les valeurs valides de la <xref:System.Diagnostics.TraceLevel> énumération. Vous pouvez également utiliser les cases à cocher pour spécifier si vous souhaitez exécuter le suivi des activités, la propagation d'activité ou le rassemblement d'informations d'identification personnelles (PII).  
  
 Vous pouvez également spécifier des sessions d’enregistrement dans le **Session de journalisation** zone de groupe.  
  
> [!NOTE]
>  Lorsqu'un autre consommateur de suivi utilise le fournisseur de suivi WS-AT, vous ne pouvez pas créer de nouvelle session de journalisation pour les événements de suivi. Toute tentative de configuration de la journalisation pendant cette période aboutit à l'affichage du message d'erreur suivant : Impossible d'activer le fournisseur. Code d’erreur : 1".  
  
 Pour plus d’informations sur le suivi et la journalisation, consultez [Administration et Diagnostics](../../../docs/framework/wcf/diagnostics/index.md).  
  
## <a name="see-also"></a>Voir aussi

- [Configuration de la prise en charge WS-Atomic Transaction](../../../docs/framework/wcf/feature-details/configuring-ws-atomic-transaction-support.md)
- [Utilitaire de configuration WS-AtomicTransaction (wsatConfig.exe)](../../../docs/framework/wcf/ws-atomictransaction-configuration-utility-wsatconfig-exe.md)
- [Administration et diagnostics](../../../docs/framework/wcf/diagnostics/index.md)
