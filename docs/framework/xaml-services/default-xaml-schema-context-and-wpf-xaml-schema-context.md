---
title: Contexte de schéma XAML par défaut et contexte de schéma XAML WPF
ms.date: 03/30/2017
ms.assetid: 04e06a15-09b3-4210-9bdf-9a64c2eccb83
ms.openlocfilehash: 0d6a0aa80d8490c509fa9036f88d4f6863ff040c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61689396"
---
# <a name="default-xaml-schema-context-and-wpf-xaml-schema-context"></a>Contexte de schéma XAML par défaut et contexte de schéma XAML WPF
Un contexte de schéma XAML est une entité conceptuelle qui qualifie la façon dont une production XAML qui utilise un vocabulaire XAML particulier interagit avec l’objet de comportement, y compris le mappage de type est résolu, comment les assemblys sont chargés, comment certains lecteur et enregistreur d’écriture les paramètres sont interprétés. Cette rubrique décrit les fonctionnalités des Services XAML .NET Framework et le contexte de schéma XAML par défaut associé, qui est basé sur le système de type CLR. Cette rubrique décrit également le contexte de schéma XAML utilisé pour WPF.  
  
## <a name="default-xaml-schema-context"></a>Contexte de schéma XAML par défaut  
 Les Services XAML .NET framework à la fois implémente et utilise un contexte de schéma XAML par défaut. Le comportement de contexte de schéma XAML par défaut n’est pas toujours entièrement visible dans l’API de la <xref:System.Xaml.XamlSchemaContext> classe. Toutefois, dans de nombreux cas le comportement qui influence le contexte de schéma XAML par défaut est observable dans l’API commune du système de type XAML, tels que les membres de <xref:System.Xaml.XamlMember> ou <xref:System.Xaml.XamlType>, ou via les API exposées sur les lecteurs XAML et les writers XAML qui sont à l’aide le contexte de schéma XAML par défaut.  
  
 Vous pouvez créer un <xref:System.Xaml.XamlSchemaContext> qui encapsule le comportement par défaut en appelant le <xref:System.Xaml.XamlSchemaContext> constructeur. Cela crée explicitement le contexte de schéma XAML par défaut. Le même contexte de schéma XAML par défaut est créé implicitement, si vous initialisez un lecteur XAML ou un writer XAML à l’aide des API qui ne prennent pas explicitement un <xref:System.Xaml.XamlSchemaContext> paramètre d’entrée.  
  
 Le contexte de schéma XAML par défaut s’appuie sur la réflexion CLR pour son comportement de mappage de type. Cela comprend l’examen de la définition du CLR <xref:System.Type>et connexes <xref:System.Reflection.PropertyInfo> ou <xref:System.Reflection.MethodInfo>. En outre, les attributs CLR sur les types ou membres est utilisé afin de remplir les détails pour le type XAML ou des informations sur le membre XAML qui utilise le type de stockage CLR. Le contexte de schéma XAML par défaut ne nécessite pas de type système extension techniques telles que le `Invoker` de modèle, car les informations nécessaires sont disponibles dans le système de type CLR.  
  
 Pour la logique de chargement des assemblys, le contexte de schéma XAML par défaut s’appuie principalement sur les valeurs de l’assembly fournis dans les mappages d’espace de noms XAML. En outre, <xref:System.Xaml.XamlReaderSettings.LocalAssembly%2A> peut conseiller un assembly à charger, pour des scénarios tels que le chargement de types internes.  
  
## <a name="wpf-xaml-schema-context"></a>Contexte de schéma XAML de WPF  
 Le contexte de schéma WPF XAML est décrite dans cette rubrique, car l’implémentation WPF fournit une illustration intéressante des types de fonctionnalités qui peuvent être introduites en implémentant un contexte de schéma XAML par défaut. En outre, le concept de contexte de schéma XAML n’est pas abordé beaucoup dans la documentation WPF qui traite de WPF XAML ; le comportement qui permet le contexte de schéma XAML peut uniquement être entièrement compréhensible si intégré à une discussion sur le fonctionnement du contexte de schéma XAML par défaut. Le contexte de schéma WPF XAML implémente le comportement suivant.  
  
 **Substitutions de recherche :** WPF dispose de quelques modèles de contenu pour XAML où il existe des propriétés de contenu XAML qui fonctionnent sans être <xref:System.Windows.Markup.ContentPropertyAttribute> attribuée. <xref:System.Xaml.XamlType.LookupContentProperty%2A> remplacements pour WPF implémentent ce comportement.  
  
 **Report pour les expressions de WPF :** WPF propose plusieurs classes d’expressions qui diffèrent d’une valeur jusqu'à ce qu’un contexte d’exécution est disponible. En outre, expansion de modèle est un comportement d’exécution qui s’appuie sur les techniques de différé.  
  
 **Tapez les optimisations de recherche du système :** WPF a un étendue XAML vocabulaire et le modèle objet, y compris les définitions de membre de classe de base qui héritent des centaines de classes définies par WPF. En outre, WPF est répartie sur plusieurs assemblys. WPF optimise sa recherche de type à l’aide de tables de recherche et d’autres techniques. Cela fournit des améliorations des performances sur le contexte de schéma XAML par défaut et sa recherche de type basé sur CLR. Dans les cas où les types n’existent pas dans une table de recherche, le comportement utilise des techniques de contexte de schéma XAML sont similaires au contexte de schéma XAML par défaut.  
  
 **Extension de XamlType et XamlMember :** WPF étend les concepts de propriété avec les propriétés de dépendance et les concepts d’événements avec des événements routés. Pour donner une plus grande visibilité à ces concepts pour les opérations de traitement de XAML, WPF étend <xref:System.Xaml.XamlType> et <xref:System.Xaml.XamlMember>et ajoute les propriétés internes qui signalent la propriété de dépendance et acheminé les caractéristiques de l’événement.  
  
### <a name="accessing-the-wpf-xaml-schema-context"></a>L’accès au contexte de schéma XAML de WPF  
 Si vous utilisez des techniques XAML qui sont basées sur WPF <xref:System.Windows.Markup.XamlReader?displayProperty=nameWithType> ou <xref:System.Windows.Markup.XamlWriter?displayProperty=nameWithType>, le contexte de schéma WPF XAML est déjà en cours d’utilisation sur ces lecteur XAML et les implémentations de writer XAML.  
  
 Si vous utilisez un autre lecteur XAML ou les implémentations de writer XAML n’initialisent pas avec le contexte de schéma WPF XAML, vous pouvez être en mesure d’obtenir un contexte de schéma à partir de WPF XAML <xref:System.Windows.Markup.XamlReader.GetWpfSchemaContext%2A?displayProperty=nameWithType>. Vous pouvez ensuite utiliser cette valeur en tant que l’initialisation pour les autres API qui utilisent un <xref:System.Xaml.XamlSchemaContext>. Par exemple, vous pouvez appeler <xref:System.Xaml.XamlXmlReader.%23ctor%2A> pour l’initialisation et transmettre le contexte de schéma WPF XAML. Ou vous pouvez utiliser le contexte de schéma WPF XAML pour les opérations de système de type XAML. Cela peut inclure l’initialisation de construction d’un <xref:System.Xaml.XamlType> ou <xref:System.Xaml.XamlMember>, ou en appelant <xref:System.Xaml.XamlSchemaContext.GetXamlType%2A?displayProperty=nameWithType>.  
  
 Notez que si vous accédez à certains aspects de WPF XAML une pure perspectives de flux de nœud XAML, certaines des fonctionnalités de framework WPF ne peuvent pas avoir encore été utilisées. Par exemple, les modèles WPF pour les contrôles ne sont pas appliquées encore. Par conséquent, si vous accédez à une propriété qui peut être remplie avec une arborescence visuelle complète en cours d’exécution, vous pouvez uniquement voir une valeur de propriété qui fait référence à un modèle. Le contexte de service fourni pour les extensions de balisage WPF peut également être inexact si fourni à partir d’une situation non-runtime et peut entraîner des exceptions lorsque vous tentez d’écrire un graphique d’objet.  
  
## <a name="xaml-and-assembly-loading"></a>XAML et le chargement d’assemblys  
 Chargement d’assemblys pour XAML et les Services XAML .NET Framework s’intègre avec le concept défini par le CLR de <xref:System.AppDomain>. Un contexte de schéma XAML interprète la manière de charger les assemblys ou rechercher des types au moment de l’exécution ou au moment du design, en fonction de l’utilisation de <xref:System.AppDomain> et d’autres facteurs. La logique est légèrement différente selon que le XAML est XAML libre pour un lecteur XAML, est le XAML compilé dans une DLL par `XamlBuildTask`, ou est BAML généré par WPF de `PresentationBuildTask`.  
  
 Le contexte de schéma XAML pour WPF s’intègre avec le modèle d’application WPF, qui à son tour utilise <xref:System.AppDomain> , ainsi que d’autres facteurs sont les détails d’implémentation WPF.  
  
#### <a name="xaml-reader-input-loose-xaml"></a>Entrée de lecteur XAML (XAML libre)  
  
1. Le contexte de schéma XAML effectue une itération dans le <xref:System.AppDomain> de l’application, en recherchant un assembly déjà chargé qui correspond à tous les aspects du nom, à partir de la plus récemment assembly chargé. Si une correspondance est trouvée, cet assembly est utilisé pour la résolution.  
  
2. Sinon, une des techniques suivantes basée sur le CLR <xref:System.Reflection.Assembly> API sont utilisées pour charger un assembly :  
  
    - Si le nom est qualifié dans le mappage, appelez <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> sur le nom qualifié.  
  
    - Si l’étape précédente échoue, utilisez le nom court (et le jeton de clé publique le cas échéant) pour appeler <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType>.  
  
    - Si le nom est non qualifié dans le mappage, appelez <xref:System.Reflection.Assembly.LoadWithPartialName%2A?displayProperty=nameWithType>.  
  
#### <a name="xamlbuildtask"></a>XamlBuildTask  
 `XamlBuildTask` est utilisé pour Windows Communication Foundation (WCF) et Windows Workflow Foundation.  
  
 Notez que les références d’assembly via `XamlBuildTask` sont toujours entièrement qualifiés.  
  
1. Appeler <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> sur le nom qualifié.  
  
2. Si l’étape précédente échoue, utilisez le nom court (et le jeton de clé publique le cas échéant) pour appeler <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType>.  
  
#### <a name="baml-presentationbuildtask"></a>BAML (intermédiaire de PresentationBuildTask)  
 Il existe deux aspects de chargement d’assemblys pour BAML : chargement de l’assembly initial qui contient le BAML en tant que composant et le chargement des assemblys de stockage de type pour tous les types référencés par la production BAML.  
  
##### <a name="assembly-load-for-initial-markup"></a>Chargement d’assembly pour le balisage initial :  
 La référence à l’assembly à charger le balisage d’est toujours non qualifiée.  
  
1. Le contexte de schéma WPF XAML effectue une itération dans le <xref:System.AppDomain> de l’application WPF, en recherchant un assembly déjà chargé qui correspond à tous les aspects du nom, à partir de la plus récemment assembly chargé. Si une correspondance est trouvée, cet assembly est utilisé pour la résolution.  
  
2. Si l’étape précédente échoue, utilisez le nom court (et le jeton de clé publique le cas échéant) pour appeler <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType>.  
  
##### <a name="assembly-references-by-baml-types"></a>Références d’assembly par types BAML :  
 Références d’assembly pour les types utilisés dans la production BAML sont toujours entièrement qualifiés en tant que sortie de la tâche de génération.  
  
1. Le contexte de schéma WPF XAML effectue une itération dans le <xref:System.AppDomain> de l’application WPF, en recherchant un assembly déjà chargé qui correspond à tous les aspects du nom, à partir de la plus récemment assembly chargé. Si une correspondance est trouvée, cet assembly est utilisé pour la résolution.  
  
2. Sinon, une des techniques suivantes est utilisée pour charger un assembly :  
  
    - Appeler <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> sur le nom qualifié.  
  
    - Si un nom court + la combinaison de jetons clé publique correspond à l’assembly qui le BAML a été chargé à partir de, utilisez cet assembly.  
  
    - Utilisez le nom court + jeton de clé publique pour appeler <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnement des concepts et structures du flux de nœud XAML](understanding-xaml-node-stream-structures-and-concepts.md)
