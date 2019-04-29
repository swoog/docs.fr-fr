---
title: Considérations sur la sécurité XAML
ms.date: 03/30/2017
helpviewer_keywords:
- security [XAML Services], .NET XAML services
- XAML security [XAML Services]
ms.assetid: 544296d4-f38e-4498-af49-c9f4dad28964
ms.openlocfilehash: 124310497cc2a8e8a816ba90b2c68a16ed342ae6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61938786"
---
# <a name="xaml-security-considerations"></a>Considérations sur la sécurité XAML
Cette rubrique décrit les meilleures pratiques pour la sécurité dans les applications lorsque vous utilisez XAML et les API des Services XAML .NET Framework.  
  
## <a name="untrusted-xaml-in-applications"></a>XAML non fiable dans les Applications  
 Dans le sens de la plus général, XAML non approuvé est n’importe quelle source XAML qui votre application ne sont pas spécifiquement inclure ou émettre.  
  
 XAML qui est compilé ou stocké en tant qu’un `resx`-ressource de type dans un assembly signé et approuvé n’est pas fondamentalement non fiable. Vous pouvez approuver le XAML que vous faites confiance à l’assembly dans son ensemble. Dans la plupart des cas, vous intéressent uniquement les aspects de l’approbation du XAML libre, qui est une source XAML que vous chargez à partir d’un flux de données ou d’autres d’e/s. XAML libre n’est pas un composant spécifique ou une fonctionnalité d’un modèle d’application avec une infrastructure de l’empaquetage et le déploiement. Toutefois, un assembly peut implémenter un comportement qui implique le chargement XAML libre.  
  
 Pour le XAML non approuvé, vous devez considérer il généralement le même comme s’il s’agissait de code non fiable. Utilisez sandboxing ou autres métaphores pour empêcher le XAML non fiable d’accéder à votre code de confiance.  
  
 La nature des fonctionnalités XAML autorise le XAML à construire des objets et définir leurs propriétés. Ces fonctions incluent également l’accès aux convertisseurs de type, le mappage et l’accès aux assemblys dans le domaine d’application à l’aide des extensions de balisage, `x:Code` blocs et ainsi de suite.  
  
 En plus de ses fonctionnalités au niveau du langage, XAML est utilisé pour la définition de l’interface utilisateur dans de nombreuses technologies. Le chargement XAML non fiable peut signifier le chargement d’une interface d’utilisateur d’usurpation de contenu malveillant.  
  
## <a name="sharing-context-between-readers-and-writers"></a>Partage du contexte entre les lecteurs et Writers  
 L’architecture de Services XAML du .NET Framework pour les lecteurs XAML et les writers XAML requiert souvent le partage d’un lecteur XAML pour un writer XAML ou un contexte de schéma XAML partagé. Partage d’objets ou les contextes peut être nécessaire si vous écrivez la logique de boucle de nœud XAML, ou en fournissant un personnalisé de chemin d’enregistrement. Vous ne devez partager que les instances de lecteur XAML, le contexte de schéma XAML par défaut ou des paramètres pour les classes de lecteur/writer XAML entre le code et non approuvé.  
  
 La plupart des scénarios et les opérations impliquant l’écriture d’un stockage basé sur CLR de type d’objet XAML peuvent simplement utiliser le contexte de schéma XAML par défaut. Le contexte de schéma XAML par défaut n’inclut pas explicitement les paramètres qui pourraient compromettre la confiance totale. Par conséquent, il est sûr de partager le contexte entre les composants de lecteur/writer XAML approuvés et non approuvés. Toutefois, si vous procédez ainsi, il est toujours recommandé de conserver ces lecteurs et les writers dans distinct <xref:System.AppDomain> étendues, à l’aide d’un d’eux spécifiquement prévu/sandbox pour la confiance partielle.  
  
## <a name="xaml-namespaces-and-assembly-trust"></a>Espaces de noms XAML et l’approbation de l’Assembly  
 La syntaxe non qualifié de base et la définition de la façon dont XAML interprète un mappage d’espace de noms XAML personnalisé à un assembly ne fait pas la distinction entre un assembly approuvé et non approuvés chargés dans le domaine d’application. Par conséquent, il est techniquement possible pour un assembly non fiable d’usurper le mappage d’espace de noms XAML prévu d’un assembly de confiance et de capturer l’objet déclaré d’une source XAML et les informations de propriété. Si vous avez des exigences de sécurité afin d’éviter cette situation, votre mappage d’espace de noms XAML souhaité doit être créée en utilisant l’une des techniques suivantes :  
  
- Utilisez un nom qualifié complet d’assembly avec nom fort dans un mappage d’espace de noms XAML effectué par votre application XAML.  
  
- Restreindre le mappage à un ensemble fixe d’assemblys de référence, en construisant un spécifique de l’assembly <xref:System.Xaml.XamlSchemaContext> pour votre XAML lecteurs XAML et les writers d’objets. Consultez <xref:System.Xaml.XamlSchemaContext.%23ctor%28System.Collections.Generic.IEnumerable%7BSystem.Reflection.Assembly%7D%29>.  
  
## <a name="xaml-type-mapping-and-type-system-access"></a>Mappage de Type XAML et accès au système de Type  
 XAML prend en charge son propre système de type, qui est un homologue de la façon dont le CLR implémente le système de type CLR base à bien des égards. Toutefois, pour certains aspects de la reconnaissance de type où vous prenez des décisions d’approbation sur un type en fonction de ses informations de type, vous devez retarder aux informations de type dans le CLR, types de stockage. Il s’agit, puisque les fonctions de rapport spécifiques du système de type XAML restent ouverts en tant que méthodes virtuelles et sont par conséquent, pas entièrement sous le contrôle des implémentations de Services XAML du .NET Framework d’origine. Ces points d’extensibilité existent car le système de type XAML est extensible, pour correspondre à l’extensibilité de XAML lui-même et de ses stratégies de mappage de type alternatives possibles par rapport à l’implémentation de CLR par défaut et le contexte de schéma XAML par défaut. Pour plus d’informations, consultez les remarques spécifiques sur les différentes propriétés de <xref:System.Xaml.XamlType> et <xref:System.Xaml.XamlMember>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Xaml.Permissions.XamlAccessLevel>
