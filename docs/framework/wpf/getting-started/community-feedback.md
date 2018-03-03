---
title: "Commentaires de la Communauté WPF"
ms.date: 03/01/2018
ms.prod: .net-framework
ms.technology:
- dotnet-wpf
ms.topic: article
helpviewer_keywords:
- community resources [WPF]
- forums [WPF]
- bug descriptions [WPF]
ms.assetid: 468b060a-d54b-4900-a74a-9faccb554045
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 243e40b1b16fd88a786398c15cd29a5baeacd6ac
ms.sourcegitcommit: ba765893e3efcece67d99fd6d5ce0074b050d1d9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2018
---
# <a name="wpf-community-feedback"></a>Commentaires de la Communauté WPF

Microsoft expose une variété de ressources de communauté pour vous permettre d’en savoir plus sur, de discuter et de fournir des commentaires sur Windows Presentation Foundation (WPF). Ces ressources incluent des forums et le [Communauté de développeurs Visual Studio](https://developercommunity.visualstudio.com/) site. Chaque ressource de la communauté offre un ensemble d’avantages différents. Ces avantages sont décrits ici, ainsi qu’un ensemble de meilleures pratiques pour utiliser chacun pour garantir la meilleure réponse à partir de la Communauté et Microsoft en particulier.

> [!NOTE]
> Ne permet d’envoyer des commentaires la section Commentaires située en bas de chaque page. Ces liens sont réservés aux commentaires sur la documentation.

## <a name="forums"></a>Forums

Le [forum WPF](https://social.msdn.microsoft.com/Forums/vstudio/en-US/home?forum=wpf) est la ressource de communauté principal pour discuter et de résolution des problèmes. Les forums facilitent la discussion et la résolution des problèmes en offrant un ensemble complet de fonctionnalités, notamment :

- la recherche ;
- le suivi de discussion ;
- la mise en forme enrichie de texte et de code ;
- Intégration de Visual Studio.
- l’implication des MVP (Most Valued Professionals) et de la Communauté ;
- une surveillance visant à garantir la réponse la plus rapide aux publications.

Une autre option pour vous permettre de poser des questions à la Communauté sur WPF est [débordement de pile](https://stackoverflow.com/questions/tagged/wpf).

### <a name="forum-best-practices"></a>Forum des meilleures pratiques

À l’aide de la meilleure suivante pratiques permettent de résoudre les problèmes publiés sur le forum WPF dans le plus rapidement possible. Ces pratiques s’appliquent à tous les forums.

#### <a name="search-existing-posts"></a>Recherche de publications existantes

Certains problèmes se produisent si souvent que d’autres utilisateurs y ont déjà été confrontés avant vous. Vous pouvez donc résoudre rapidement votre problème ou apporter votre contribution à une discussion existante.

#### <a name="use-meaningful-titles"></a>Utiliser des titres explicites

Titres concis et explicites améliorent la détectabilité de vos publications. Ils facilitent également pour les autres membres de la Communauté forum WPF déterminer s’ils peuvent résoudre votre problème.

#### <a name="include-appropriate-content"></a>Inclure le contenu approprié

Décrivez le problème et comment vous avez essayé de travail par son biais. Si possible, ajoutez des extraits de code ou un exemple très simple qui illustre le problème. Tous ces détails augmenter vos chances d’obtenir une réponse rapide à votre question.

## <a name="visual-studio-developer-community"></a>Communauté de développeurs Visual Studio

Certains problèmes peuvent parfois être difficiles, voire impossibles à résoudre. De telles situations sont liées à des bogues au niveau de la technologie, à la difficulté à appliquer la technologie à des scénarios particuliers, ou encore à un manque de prise en charge de certains scénarios particuliers. Cette information est importante de Microsoft et peut être fournie la [Communauté de développeurs Visual Studio](https://developercommunity.visualstudio.com/) site.

Les articles publiés sur le centre de commentaires produit WPF sont acheminés vers la base de données interne de bogue de l’équipe WPF. Par conséquent, il est le moyen le plus fiable pour obtenir vos commentaires au propriétaire de la fonctionnalité WPF. En outre, vous pouvez valider et suivre des suggestions et des bogues ainsi voter, ce qui contribue à l’équipe WPF pour hiérarchiser les problèmes.

### <a name="developer-community-best-practices"></a>Meilleures pratiques de communauté des développeurs

Lors de la validation à la Communauté de développeurs Visual Studio, rechercher des publications existantes, fournir un intitulé explicite et de contenu approprié sont les meilleures pratiques, tout comme pour les publications sur le forum WPF. Vous trouverez ci-dessous d’autres pratiques à adopter.

#### <a name="search-existing-posts"></a>Recherche de publications existantes

Certains problèmes se produisent si souvent que d’autres utilisateurs y ont déjà été confrontés avant vous. Par conséquent, vous pouvez résoudre votre problème rapidement, ou vous pouvez ajouter votre entrée à un problème existant.

#### <a name="use-meaningful-titles"></a>Utiliser des titres explicites

Titres concis et explicites, augmentez le risque que votre problème est dirigé vers l’équipe WPF plus approprié dans le délai le plus court. Cela est particulièrement important pour une technologie comme WPF, qui contient de nombreuses fonctionnalités reliées entre elles.

#### <a name="describe-how-to-reproduce-your-bug"></a>Décrivent la façon de reproduire le bogue

Lorsque vous publiez sur un bogue, il est important d’inclure les éléments suivants, le cas échéant :

- Fournir une description claire du bogue.
- Utiliser des extraits de code pour étayer la description du bogue.
- Fournir une liste d’étapes montrant comment reproduire le bogue.
- Inclure le plus petit exemple de code possible qui reproduit le bogue.
- Préciser si le bogue se reproduit constamment ou non.
- Inclure les informations d’exception appropriées.

 Si le bogue est lié à l’installation ou à la configuration, joignez les journaux d’installation et les captures instantanées (fichiers comportant le préfixe « dd_ » qui se trouvent dans votre dossier %temp%).

 Dans le cas de problèmes de compilation ou de génération, joignez les journaux de génération. MSBuild système peut être configuré pour prend en charge l’enregistrement avec différents commentaires en utilisant le commutateur/v: à partir de la ligne de commande ou en configurant le niveau approprié d’un environnement de développement intégré (IDE) tel que Visual Studio.

#### <a name="provide-environment-information"></a>Fournir des informations sur l’environnement

Les informations générales peuvent souvent être utiles pour ajouter du contexte à votre publication. En particulier, mentionnez la plateforme de système d’exploitation, famille de processeurs et architecture, tels que « Version de Windows 10 1709, Intel (r) Xeon, x64 ».

Si vous rencontrez un problème de rendu, vous devez également fournir des détails sur la carte et le pilote graphiques, si possible. Ces informations sont importantes, car WPF est une infrastructure de présentation.

#### <a name="provide-solution-or-project-information"></a>Fournir des informations de solution ou un projet

Les bogues peuvent être liés à des outils utilisés pour développer et générer vos applications et les types d’applications que vous créez. Par conséquent, il peut être utile de spécifier :

- Le type d’application que vous générez, par exemple :
  - Application (*.exe*) ou bibliothèque (*.dll*)
  - Application de navigateur Extensible Application Markup Language (XAML) (XBAP)
  - Applications XAML
  - Applications autonomes installé
  - Applications autonomes déployées par ClickOnce
- L’outil de développement, par exemple :
  - MSBuild
  - Concepteur graphique d’expression
  - Expression Interactive Designer
  - Visual Studio
- La configuration de la solution, par exemple :
  - Une solution
  - Un seul projet
  - Une solution avec plusieurs projets dépendants
- Si votre application dispose de ressources associées ou non à un langage spécifique. Par exemple, avez-vous spécifié la propriété `UICulture` du projet ou des métadonnées localisables pour les types `Application`, `Page` et `Resource` ?
- Si vous avez utilisé le paramètre de langue neutre dans le fichier AssemblyInfo.cs ou AssemblyInfo.vb.

#### <a name="provide-scenario-and-impact-information"></a>Fournir des informations de scénario et l’impact

Fournissent des informations sur le scénario que les manifestes le bogue et son impact. Cette information est très importante de l’équipe WPF lorsqu’elle décide si, quand et comment un problème doit être corrigé, ou si une solution acceptable peut être utilisée à la place.

En règle générale, les scénarios de plantage et de perte de données ont un impact important et sont, par conséquent, facilement prioritaires. Certains bogues, toutefois, se produisent uniquement dans des scénarios rares, mais qui peuvent aussi parfois devenir des scénarios courants. Qui fournit le contexte dans le scénario et l’impact aide l’équipe WPF à faire le bon choix.

## <a name="see-also"></a>Voir aussi

[Guide pratique pour signaler un problème avec Visual Studio 2017](/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017)
