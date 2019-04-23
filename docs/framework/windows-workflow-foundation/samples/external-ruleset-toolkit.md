---
title: External RuleSet Toolkit
ms.date: 03/30/2017
ms.assetid: a306d283-a031-475e-aa01-9ae86e7adcb0
ms.openlocfilehash: c453c6137beeae8eee0e356734a1f9cdf8d8568b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59978612"
---
# <a name="external-ruleset-toolkit"></a>External RuleSet Toolkit

Généralement, lorsque des règles sont utilisées dans une application de workflow, elles font partie de l'assembly. Dans certains cas, il peut être préférable de gérer les RuleSets séparément de l'assembly afin qu'ils soient mis à jour sans que la génération et le déploiement de l'assembly de workflow ne soient nécessaires. Cet exemple vous permet de gérer et de modifier des RuleSets dans une base de données et d'accéder à ceux-ci à partir d'un workflow au moment de son exécution, opération qui permet aux instances de workflow en cours d'intégrer automatiquement des modifications de RuleSets.

L'exemple External RuleSet Toolkit contient un utilitaire basé sur les Windows Forms pouvant être utilisé pour gérer et modifier les versions d'un RuleSet dans une base de données. Il inclut également une activité et un service hôte permettant d'exécuter ces règles.

> [!NOTE]
> Cet exemple requiert [Microsoft SQL Server](https://go.microsoft.com/fwlink/?LinkId=96181).

Visual Studio fournit un outil RuleSet editor dans le cadre de Windows Workflow Foundation (WF). Vous pouvez démarrer cet éditeur en double-cliquant sur l'activité `Policy` dans un workflow ; cette opération sérialise l'objet RuleSet défini au fichier .rules associé au workflow (une activité `Policy` exécute une instance RuleSet sur le workflow). Le fichier .rules est compilé dans l'assembly en tant que ressource lors de la génération du projet de workflow.

Les composants de cet exemple incluent les éléments suivants :

- Un outil GUI RuleSet pouvant être utilisé pour modifier et gérer des versions de RuleSets dans la base de données.

- Un service de RuleSet configuré dans l'application hôte et accédant aux RuleSets de la base de données.

- Une activité `ExternalPolicy` nécessitant un RuleSet du service de RuleSet et exécutant ce RuleSet sur le workflow.

L’interaction des composants est présentée dans l’image suivante. Les sections qui suivent décrivent chacun de ces composants.

![Diagramme montrant la présentation de l’exemple External RuleSet Toolkit.](./media/external-ruleset-toolkit/ruleset-toolkit-overview.gif)

> [!IMPORTANT]
> Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ExternalRuleSetToolKit`

## <a name="ruleset-tool"></a>Outil RuleSet

L’illustration suivante est une capture d’écran de l’outil RuleSet. À partir de la **règle Store** menu, vous pouvez charger les RuleSets disponibles à partir de la base de données et enregistrer des groupes de règles modifié dans le magasin. Un fichier de configuration d'application contient une chaîne de connexion pour la base de données RuleSet. Lorsque vous démarrez l'outil, ce dernier charge automatiquement les RuleSets à partir de la base de données configurée.

![Capture d’écran montrant le navigateur de RuleSet.](./media/external-ruleset-toolkit/ruleset-browser-dialog.gif)

L’outil RuleSet applique aux RuleSets des numéros de version principaux et secondaires, vous permettant de gérer et de stocker simultanément plusieurs versions. Il ne dispose pas de fonctionnalités de verrouillage ou de contrôle de configuration en plus de ces fonctionnalités de versions. Cet outil vous permet de créer des versions de RuleSets ou de supprimer des versions existantes. Lorsque vous cliquez sur **New**, l’outil crée un nouveau nom de RuleSet et lui applique la version 1.0. Lorsque vous copiez une version, l'outil crée une copie de la version de l'ensemble de règles sélectionné, y compris les règles qu'il contient, et assigne de nouveaux numéros de version uniques. Ces numéros sont basés sur ceux de RuleSets existants. Vous pouvez changer le nom d'un RuleSet et ses numéros de version en utilisant les champs associés sur le formulaire.

Lorsque vous cliquez sur **modifier les règles de**, l’outil RuleSet editor démarre, comme illustré dans l’image suivante :

![Capture d’écran montrant l’outil RuleSet Editor.](./media/external-ruleset-toolkit/ruleset-editor-dialog.gif)

Il s’agit d’une ré-hébergement de la boîte de dialogue d’éditeur qui fait partie du complément Visual Studio de Windows Workflow Foundation. Elle contient les mêmes fonctionnalités, y compris la prise en charge Intellisense. Les règles sont créées par rapport à un type de cible (par exemple, un flux de travail) qui est associé à l’ensemble de règles dans l’outil ; Lorsque vous cliquez sur **Parcourir** dans la boîte de dialogue principale de l’outil, le **Workflow/Type Selector** boîte de dialogue s’affiche, comme illustré dans la Figure 4.

![Flux de travail &#47;tapez sélection](./media/71f08d57-e8f2-499e-8151-ece2cbdcabfd.gif "71f08d57-e8f2-499e-8151-ece2cbdcabfd")

Figure 4 : Workflow/Type Selector

Vous pouvez utiliser la **Workflow/Type Selector** boîte de dialogue pour spécifier un assembly et un type spécifique au sein de cet assembly. Ce type correspond au type de cible pour lequel les règles sont créées (et exécutées). Dans de nombreux cas, le type de cible est un workflow ou un autre type d'activité. Toutefois, il est possible d'exécuter un RuleSet sur tout type .NET.

Le chemin d’accès pour le fichier d’assembly et le type `name are stored with the` RuleSet dans la base de données, afin que lorsque le RuleSet est récupéré à partir de la base de données, l’outil tente de charger automatiquement le type de cible.

Lorsque vous cliquez sur **OK** dans le **Workflow/Type Selector** boîte de dialogue, il valide le type sélectionné pour l’ensemble de règles pour vous assurer que le type de cible a tous les membres référencés par les règles. Erreurs sont affichées dans un **erreurs de Validation** boîte de dialogue. Vous pouvez choisir de poursuivre la modification malgré ces erreurs, ou cliquez sur **Annuler**. À partir de la **outils** menu dans la boîte de dialogue principale de l’outil, vous pouvez cliquer sur **Validate** pour valider à nouveau la version du RuleSet à l’activité cible.

![Capture d’écran montrant la boîte de dialogue erreurs de Validation.](./media/external-ruleset-toolkit/validation-errors-dialog.png)

À partir de la **données** menu dans l’outil, vous pouvez importer et exporter des ensembles de règles. Lorsque vous cliquez sur **importation**, une boîte de dialogue Sélecteur de fichiers s’affiche, dans laquelle vous pouvez sélectionner un fichier .rules. Cela peut ou ne peut pas être un fichier initialement créé dans Visual Studio. Le fichier .rules doit contenir une instance de `RuleDefinitions` sérialisée qui dispose d’une collection de conditions et d’une collection de RuleSets. L’outil n’utilise pas la collection de conditions, mais il n’utilise pas le `RuleDefinitions` format .rules pour permettre l’interaction avec l’environnement Visual Studio.

Après avoir sélectionné un fichier .rules, un **RuleSet Selector** boîte de dialogue apparaît. Celle-ci permet de sélectionner les ensembles de règles que vous souhaitez importer à partir du fichier (par défaut, tous les ensembles de règles sont sélectionnés). Les RuleSets d'un fichier .rules ne disposent pas de numéros de version, car leur version dans un projet WF est identique à celle de l'assembly. Pendant le processus d’importation, l’outil assigne automatiquement le numéro de version principal disponible suivant (que vous pouvez le modifier après l’importation) ; Vous pouvez voir les numéros de version attribué dans le **RuleSet Selector** liste.

Pour chaque RuleSet importé, l’outil tente de localiser le type associé dans le dossier bin\Debug qui se trouve sous l’emplacement du fichier .rules (s’il existe), en fonction des membres utilisés dans le RuleSet. Si l'outil détecte plusieurs types correspondants, il essaie d'en choisir un en fonction d'une correspondance entre le nom de fichier .rules et celui du type (par exemple, le type `Workflow1` correspond au fichier Workflow1.rules). Si plusieurs noms concordent, vous êtes invité à sélectionner le type. Si ce mécanisme d’identification automatique ne parvient pas à localiser un assembly ou un type correspondant, après l’importation vous pouvez ensuite cliquer sur **Parcourir** dans la boîte de dialogue principale de l’outil pour accéder au type associé. L’illustration suivante montre le sélecteur de groupe de règles :

![Capture d’écran montrant la boîte de dialogue du sélecteur de groupe de règles.](./media/external-ruleset-toolkit/ruleset-selector-dialog.gif)

Lorsque vous cliquez sur **Data-Export** à partir du menu principale de l’outil, le **RuleSet Selector** boîte de dialogue s’affiche de nouveau, à partir de laquelle vous pouvez déterminer les ensembles de règles à partir de la base de données qui doit être exporté. Lorsque vous cliquez sur **OK**, un **enregistrer le fichier** boîte de dialogue s’affiche, dans laquelle vous pouvez spécifier le nom et l’emplacement du fichier .rules. Le fichier .rules ne contenant aucune information sur la version, vous pouvez sélectionner une seule version de RuleSet répondant à un nom donné.

## <a name="policyfromservice-activity"></a>Activité PolicyFromService

Le code correspondant à l'activité `PolicyFromService` est très simple. Il fonctionne exactement comme l'activité `Policy` fournie avec WF, mais au lieu de récupérer le RuleSet cible dans le fichier .rules, il appelle un service hôte pour obtenir l'instance de ce RuleSet. Il exécute ensuite le RuleSet sur l'instance de l'activité du workflow racine.

Pour utiliser l'activité dans un workflow, ajoutez une référence aux assemblys `PolicyActivities` et `RuleSetService` de votre projet de workflow. Consultez la procédure située à la fin de cette rubrique pour savoir comment ajouter une activité à la boîte à outils.

Après avoir ajouté l'activité à votre workflow, vous devez indiquer le nom du RuleSet à exécuter. Vous pouvez indiquer ce nom en tant que valeur littérale ou le lier à la variable ou à la propriété de workflow d'une autre activité. Vous pouvez également indiquer des numéros de version pour le RuleSet à exécuter (facultatif). Si vous laissez la valeur par défaut (0) comme numéro de version principal ou secondaire, le numéro de version le plus récent figurant dans la base de données sera automatiquement assigné à l'activité.

## <a name="ruleset-service"></a>Service de RuleSet

Ce service est chargé de récupérer dans la base de données la version indiquée du RuleSet et de la renvoyer à l'activité appelante. Comme indiqué précédemment, si la valeur des versions principales et secondaires passées dans l'appel `GetRuleSet` est de 0, le service récupère la version la plus récente. À ce stade, aucune mise en cache des définitions ou des instances de RuleSets n’est effectuée ; de la même façon, aucune fonctionnalité visant à marquer certaines versions de RuleSets comme étant « déployées » (afin de les différencier des RuleSets en cours) n’est appliquée.

La base de données devant être consultée par le service doit être configurée sur l'hôte à l'aide d'un fichier de configuration d'application.

#### <a name="to-run-the-tool"></a>Pour exécuter l'outil

1. Le dossier de configuration de la table RuleSet utilisée par l’outil et par le service contient un fichier Setup.sql. Vous pouvez exécuter le fichier de commandes Setup.cmd pour créer la base de données Rules dans SQL Express et configurer la table RuleSet.

2. Si vous modifiez le fichier de commandes ou Setup.sql et indiquez de ne pas utiliser SQL Express ou d'ajouter la table dans une base de données autre que `Rules`, les fichiers de configuration d'application de l'outil RuleSet et les projets `UsageSample` doivent être modifiés pour contenir les mêmes informations.

3. Après avoir exécuté le script Setup.sql, vous pouvez générer la solution `ExternalRuleSetToolkit` puis exécuter l'outil RuleSet à partir du projet ExternalRuleSetTool.

4. La solution `RuleSetToolkitUsageSample` Sequential Workflow Console Application contient un exemple de workflow. Ce dernier se compose d'une activité `PolicyFromService` et de deux variables (`orderValue` et `discount`) sur lesquelles le RuleSet cible s'exécute.

5. Pour utiliser cet exemple, générez la solution `RuleSetToolkitUsageSample`. Puis, dans le menu principal outil de l’ensemble de règles, cliquez sur **-importation des données** et pointer vers le fichier discountruleset.Rules qui se trouve dans le dossier RuleSetToolkitUsageSample. Cliquez sur le **Rule Store-Save** option de menu pour enregistrer le RuleSet importé dans la base de données.

6. L'assembly `PolicyActivities` étant référencé à partir du projet de workflow exemple, l'activité `PolicyFromService` apparaît dans le workflow. Toutefois, elle ne s'affiche pas par défaut dans la boîte à outils. Pour l'ajouter à la boîte à outils, procédez comme suit :

    - Avec le bouton droit de la boîte à outils et sélectionnez **choisir des éléments** (Cela peut prendre un certain temps).

    - Lorsque le **Choose Toolbox Items** boîte de dialogue s’affiche, cliquez sur le **activités** onglet.

    - Accédez à la `PolicyActivities` assembly dans le `ExternalRuleSetToolkit` solution et cliquez sur **Open**.

    - Vérifiez que le `PolicyFromService` activité est sélectionnée dans le **Choose Toolbox Items** boîte de dialogue, puis cliquez sur **OK**.

    - L’activité doit maintenant apparaître dans la boîte à outils dans le **RuleSetToolkitUsageSample Components** catégorie.

7. Le service de RuleSet est déjà configuré dans l'application console hôte via l'instruction suivante dans Program.cs.

    ```csharp
    workflowRuntime.AddService(new RuleSetService());
    ```

8. Vous pouvez également configurer le service sur l'hôte en utilisant un fichier de configuration ; consultez la documentation du kit de développement logiciel (SDK) pour plus de détails.

9. Un fichier de configuration d'application est ajouté au projet de workflow afin d'indiquer la chaîne de connexion correspondant à la base de données devant être utilisée par le service. Cette chaîne doit être la même que celle utilisée par l'outil RuleSet, laquelle cible la base de données contenant la table RuleSet.

10. Vous pouvez désormais exécuter le projet `RuleSetToolkitUsageSample` comme s'il s'agissait de toute autre application console de workflow. Appuyez sur F5 ou Ctrl + F5 dans Visual Studio ou le fichier RuleSetToolkitUsageSample.exe directement.

    > [!NOTE]
    > Vous devez fermer l'outil RuleSet pour recompiler l'exemple d'utilisation, car l'outil charge l'assembly correspondant à cet exemple.
