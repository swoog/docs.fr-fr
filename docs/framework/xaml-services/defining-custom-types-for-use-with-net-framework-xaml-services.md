---
title: Définition de types personnalisés pour une utilisation avec les services XAML .NET Framework
ms.date: 03/30/2017
helpviewer_keywords:
- defining custom types [XAML Services]
ms.assetid: c2667cbd-2f46-4a7f-9dfc-53696e35e8e4
ms.openlocfilehash: be9c0e26574a15279ce89af2c7862abaa8713360
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59164435"
---
# <a name="defining-custom-types-for-use-with-net-framework-xaml-services"></a>Définition de types personnalisés pour une utilisation avec les services XAML .NET Framework
Lorsque vous définissez des types personnalisés qui sont des objets métier ou sont des types qui n’ont pas d’une dépendance sur des infrastructures spécifiques, il existe certaines meilleures pratiques pour XAML, vous pouvez suivre. Si vous respectez ces pratiques, les Services XAML .NET Framework et ses lecteurs XAML et les writers XAML peuvent découvrir les caractéristiques XAML de votre type et lui donner une représentation appropriée dans un flux de nœud XAML à l’aide du système de type XAML. Cette rubrique décrit les meilleures pratiques pour les définitions de type, définitions de membre et aux attributs CLR des types ou membres.  
  
## <a name="constructor-patterns-and-type-definitions-for-xaml"></a>Modèles de constructeur et définitions de Type pour XAML  
 Pour être instancié en tant qu’objet élément dans XAML, une classe personnalisée doit remplir les conditions suivantes :  
  
-   La classe personnalisée doit être publique et doit exposer un constructeur public (sans paramètre) par défaut. (Consultez la section suivante pour des remarques concernant les structures.)  
  
-   La classe personnalisée ne doit pas être une classe imbriquée. Supplémentaire « point » dans le chemin d’accès du nom complet rend la division de l’espace de noms classe ambiguë et interfère avec d’autres fonctionnalités XAML telles que les propriétés jointes.  
  
 Si un objet peut être instancié comme un élément objet, l’objet créé peut remplir le formulaire d’élément de propriété de toutes les propriétés qui acceptent l’objet comme type sous-jacent.  
  
 Vous pouvez toujours fournir des valeurs d’objet pour les types qui ne répondent pas à ces critères, si vous activez un convertisseur de valeurs. Pour plus d’informations, consultez [Type Converters and Markup Extensions for XAML](type-converters-and-markup-extensions-for-xaml.md).  
  
### <a name="structures"></a>Structures  
 Structures peuvent toujours être construites en XAML, par définition de CLR. Il s’agit, car un compilateur CLR crée implicitement un constructeur par défaut pour une structure. Ce constructeur initialise toutes les valeurs de propriétés à leurs valeurs par défaut.  
  
 Dans certains cas, le comportement de construction par défaut pour une structure n’est pas souhaitable. Cela peut être parce que la structure est destinée à remplir des valeurs et à fonctionner conceptuellement comme une union. En tant qu’union, les valeurs contenues peuvent avoir des interprétations mutuellement exclusives, et par conséquent, aucune de ses propriétés peuvent être définies. Un exemple d’une telle structure dans le vocabulaire WPF est <xref:System.Windows.GridLength>. Ces structures doivent implémenter un convertisseur de type afin que les valeurs peuvent être exprimées sous forme d’attribut, à l’aide des conventions de chaîne qui créent les différents modes ou interprétations des valeurs de structure. La structure doit également exposer un comportement similaire pour la construction de code via un constructeur non défini par défaut.  
  
### <a name="interfaces"></a>Interfaces  
 Interfaces peuvent servir de types sous-jacents des membres. Le système de type XAML vérifie la liste assignable et attend que l’objet qui est fourni en tant que la valeur peut être assigné à l’interface. Il n’existe aucun concept de la façon dont l’interface doit être présentée comme un type XAML tant un type assignable approprié prend en charge les spécifications de construction XAML.  
  
### <a name="factory-methods"></a>Méthodes de fabrique  
 Méthodes de fabrique sont une fonctionnalité de XAML 2009. Ils modifient le principe XAML que les objets doivent avoir des constructeurs par défaut. Méthodes de fabrique ne sont pas documentées dans cette rubrique. Consultez [x : FactoryMethod, Directive](x-factorymethod-directive.md).  
  
## <a name="enumerations"></a>Énumérations  
 Les énumérations ont un comportement de conversion de type natif XAML. Noms de constantes d’énumération spécifiées dans XAML sont résolus par rapport au type énumération sous-jacent et retournent la valeur d’énumération à un writer d’objet XAML.  
  
 XAML prend en charge une utilisation d’indicateurs de style pour les énumérations avec <xref:System.FlagsAttribute> appliquée. Pour plus d’informations, consultez [syntaxe de XAML en détail](../wpf/advanced/xaml-syntax-in-detail.md). ([Syntaxe de XAML en détail](../wpf/advanced/xaml-syntax-in-detail.md) est rédigée pour les utilisateurs WPF, mais la plupart des informations dans cette rubrique s’applique pour XAML qui n’est pas spécifique à une infrastructure d’implémentation particulière.)  
  
## <a name="member-definitions"></a>Définitions de membre  
 Types peuvent définir des membres pour l’utilisation XAML. Il est possible de définir des membres qui sont utilisables à XAML même si ce type spécifique n’est pas utilisable en XAML. Cela est possible en raison de l’héritage du CLR. Tant que certains type qui hérite du membre prend en charge l’utilisation XAML en tant que type, et le membre prend en charge l’utilisation XAML pour son type sous-jacent ou a une syntaxe XAML native disponible, ce membre est utilisable en XAML.  
  
### <a name="properties"></a>Properties  
 Si vous définissez les propriétés comme une propriété CLR publique à l’aide du CLR standard `get` et `set` modèles d’accesseur et mots-clés approprié à la langue, le système de type XAML peut signaler fournie par la propriété en tant que membre avec les informations appropriées pour <xref:System.Xaml.XamlMember> propriétés, telles que <xref:System.Xaml.XamlMember.IsReadPublic%2A> et <xref:System.Xaml.XamlMember.IsWritePublic%2A>.  
  
 Propriétés spécifiques peuvent activer une syntaxe de texte en appliquant <xref:System.ComponentModel.TypeConverterAttribute>. Pour plus d’informations, consultez [Type Converters and Markup Extensions for XAML](type-converters-and-markup-extensions-for-xaml.md).  
  
 En l’absence d’une syntaxe de texte ou d’une conversion XAML native et en l’absence d’indirection supplémentaire, comme une extension de balisage, le type d’une propriété (<xref:System.Xaml.XamlMember.TargetType%2A> système de type dans le XAML) doit être en mesure de retourner une instance à un writer d’objet XAML en traitant le t type de cible comme un type CLR.  
  
 L’utilisation de XAML 2009, [x : Reference Markup Extension](x-reference-markup-extension.md) peut être utilisé pour fournir des valeurs si les considérations précédentes ne sont pas remplies ; Toutefois, qui est plus un problème d’utilisation qu’un problème de définition de type.  
  
### <a name="events"></a>Événements  
 Si vous définissez des événements en tant qu’événement CLR public, le système de type XAML peut signaler l’événement en tant que membre avec <xref:System.Xaml.XamlMember.IsEvent%2A> comme `true`. Les gestionnaires d’événements de câblage n’est pas dans l’étendue des fonctionnalités de Services XAML du .NET Framework ; en revanche, implémentations et les infrastructures spécifiques.  
  
### <a name="methods"></a>Méthodes  
 Code inline des méthodes n’est pas une fonctionnalité XAML par défaut. Dans la plupart des cas vous ne référencez pas directement les membres de méthode à partir de XAML, et le rôle des méthodes dans XAML est uniquement pour prendre en charge des modèles XAML spécifiques. [x : FactoryMethod Directive](x-factorymethod-directive.md) est une exception.  
  
### <a name="fields"></a>Champs  
 Instructions de conception CLR décourager les champs non statiques. Pour les champs statiques, vous pouvez accéder à des valeurs de champ statique uniquement via [x : Static, Extension de balisage](x-static-markup-extension.md); dans ce cas vous ne font rien de spécial dans la définition du CLR pour exposer un champ pour [x : Static](x-static-markup-extension.md) utilisations.  
  
## <a name="attachable-members"></a>Membres pouvant être attachés  
 Membres pouvant être attachés sont exposées à XAML via un modèle de méthode d’accesseur sur un type de définition. Le type de définition lui-même est inutile être utilisable par le XAML en tant qu’objet. En fait, il est courant de déclarer une classe de service dont le rôle est propriétaire du membre et implémenter les comportements associés, mais autre fonction comme une représentation de l’interface utilisateur. Pour les sections suivantes, l’espace réservé *PropertyName* représente le nom de votre membre pouvant être attaché. Ce nom doit être valide dans le [XamlName, grammaire](xamlname-grammar.md).  
  
 Méfiez-vous des collisions de noms entre ces modèles et d’autres méthodes d’un type. Si un membre existant qui correspond à l’un des modèles, il peut être interprété comme une voie d’accès au membre pouvant être attaché par un processeur XAML même si ce n’était pas votre intention.  
  
#### <a name="the-getpropertyname-accessor"></a>L’accesseur GetPropertyName  
 La signature pour l’accesseur `Get`*NomPropriété* doit être :  
  
 `public static object Get` *NomPropriété* `(object`  `target` `)`  
  
-   L’objet `target` peut être défini comme un type plus spécifique dans votre implémentation. Vous pouvez l’utiliser pour limiter l’utilisation de votre membre pouvant être attaché ; utilisations en dehors de votre portée prévue lève des exceptions de cast non valide qui sont ensuite signalées par une erreur d’analyse XAML. Le nom du paramètre `target` n’est pas obligatoire, mais est nommé `target` par convention dans la plupart des implémentations.  
  
-   La valeur de retour peut être spécifiée comme un type plus spécifique dans votre implémentation.  
  
 Pour prendre en charge un <xref:System.ComponentModel.TypeConverter> appliquer de la syntaxe de texte est activée pour l’utilisation des attributs du membre pouvant être attachée, <xref:System.ComponentModel.TypeConverterAttribute> à la `Get` *PropertyName* accesseur. Application à la `get` au lieu du `set` peut sembler non intuitive ; Toutefois, cette convention peut prendre en charge le concept de membres en lecture seule pouvant être attachés qui sont sérialisables, ce qui est utile dans les scénarios de concepteur.  
  
#### <a name="the-setpropertyname-accessor"></a>L’accesseur SetPropertyName  
 La signature pour l’ensemble*PropertyName* accesseur doit être :  
  
 `public static void Set` *NomPropriété* `(object`  `target` `, object`  `value` `)`  
  
-   Le `target` objet peut être spécifié comme un type plus spécifique dans votre implémentation, avec la même logique et les conséquences, comme décrit dans la section précédente.  
  
-   L’objet `value` peut être défini comme un type plus spécifique dans votre implémentation.  
  
 N’oubliez pas que la valeur de cette méthode est l’entrée provenant de l’utilisation XAML, généralement sous la forme d’attribut. À partir de la forme d’attribut doit être prise en charge de convertisseur de valeur pour une syntaxe de texte, et vous attribut sur le `Get` *PropertyName* accesseur.  
  
### <a name="attachable-member-stores"></a>Magasins de membres pouvant être attachée  
 Les méthodes d’accesseur ne sont généralement pas suffisamment pour fournir un moyen de placer des valeurs de membre pouvant être attaché dans un graphique d’objet, ou pour extraire des valeurs de graphique d’objet et les sérialiser correctement. Pour offrir cette fonctionnalité, le `target` objets dans les signatures d’accesseur précédentes doivent être capables de stocker des valeurs. Le mécanisme de stockage doit être conforme au principe de membre pouvant être attaché constituant le membre pouvant être attaché aux cibles où le membre pouvant être attaché n’est pas dans la liste des membres. Les Services XAML .NET framework fournit une technique d’implémentation pour le membre pouvant être attaché stocke via les API <xref:System.Xaml.IAttachedPropertyStore> et <xref:System.Xaml.AttachablePropertyServices>. <xref:System.Xaml.IAttachedPropertyStore> est utilisé par les writers XAML pour découvrir l’implémentation de magasin et doit être implémenté sur le type qui est la `target` des accesseurs. La méthode statique <xref:System.Xaml.AttachablePropertyServices> API sont utilisées dans le corps des accesseurs et faire référence au membre pouvant être attaché par son <xref:System.Xaml.AttachableMemberIdentifier>.  
  
## <a name="xaml-related-clr-attributes"></a>Attributs CLR XAML  
 Attribution correctement vos types, membres et des assemblys est important dans l’ordre à signaler les informations de système de type XAML pour les Services XAML .NET Framework. Cela est utile si vous avez l’intention d’utiliser avec les systèmes XAML qui sont directement basés sur les lecteurs XAML de Services XAML .NET Framework et les writers XAML vos types, ou si vous définissez ou utilisez une infrastructure utilisent XAML qui repose sur ces lecteurs XAML et les writers XAML.  
  
 Pour obtenir la liste de chaque attribut de XAML qui est pertinente pour la prise en charge XAML de vos types personnalisés, consultez [Related CLR attributs pour les bibliothèques et Types personnalisés](xaml-related-clr-attributes-for-custom-types-and-libraries.md).  
  
## <a name="usage"></a>Utilisation  
 L’utilisation de types personnalisés requiert que l’auteur du balisage doit mapper un préfixe pour l’assembly et l’espace de noms CLR qui contiennent le type personnalisé. Cette procédure n’est pas documentée dans cette rubrique.  
  
## <a name="access-level"></a>Niveau d’accès  
 XAML fournit un moyen pour charger et instancier des types qui ont un `internal` niveau d’accès. Cette fonctionnalité est fournie afin que le code utilisateur peut définir ses propres types, puis instancier les classes à partir du balisage qui fait également partie de la même portée de code utilisateur.  
  
 Par exemple à partir de WPF, chaque fois que le code de l’utilisateur définit un <xref:System.Windows.Controls.UserControl> qui est conçu comme un moyen de refactoriser un comportement de l’interface utilisateur, mais pas dans le cadre de n’importe quel mécanisme d’extension possible qui peut être déduite d’une déclaration de la classe de prise en charge avec `public` niveau d’accès. Tel un <xref:System.Windows.Controls.UserControl> peuvent être déclarés avec `internal` accéder si le code de stockage est compilé dans le même assembly à partir duquel il est référencé comme un type XAML.  
  
 Pour une application qui charge le XAML sous confiance totale et utilise <xref:System.Xaml.XamlObjectWriter>, chargement de classes avec `internal` niveau d’accès est toujours activé.  
  
 Pour une application qui charge le XAML sous confiance partielle, vous pouvez contrôler les caractéristiques de niveau d’accès à l’aide de la <xref:System.Xaml.Permissions.XamlAccessLevel> API. En outre, des mécanismes de différé (par exemple, le système de modèle de WPF) doivent pouvoir propager les autorisations de niveau d’accès et de les conserver pour les évaluations éventuelle exécution ; Ceci est géré en interne en passant le <xref:System.Xaml.Permissions.XamlAccessLevel> plus d’informations.  
  
### <a name="wpf-implementation"></a>Implémentation de WPF  
 WPF XAML utilise un modèle d’accès de niveau de confiance partiel où Si BAML est chargé en confiance partielle, l’accès est limité à <xref:System.Xaml.Permissions.XamlAccessLevel.AssemblyAccessTo%2A> pour l’assembly qui est la source BAML. Report, WPF utilise <xref:System.Xaml.IXamlObjectWriterFactory.GetParentSettings%2A?displayProperty=nameWithType> comme un mécanisme pour passer les informations au niveau d’accès.  
  
 Dans la terminologie de WPF XAML, un *type interne* est un type qui est défini par le même assembly qui inclut également le XAML de référencement. Ce type peut être mappé par un espace de noms XAML qui omet délibérément l’assembly = partie d’un mappage, par exemple, `xmlns:local="clr-namespace:WPFApplication1"`.  Si BAML fait référence à un type interne et que le type a `internal` accéder à niveau, cela génère un `GeneratedInternalTypeHelper` classe pour l’assembly. Si vous souhaitez éviter `GeneratedInternalTypeHelper`, vous devez utiliser `public` niveau d’accès ou doit tenir compte de la classe appropriée dans un assembly distinct et créez une dépendance entre cet assembly.  
  
## <a name="see-also"></a>Voir aussi

- [Attributs CLR XAML pour les bibliothèques et types personnalisés](xaml-related-clr-attributes-for-custom-types-and-libraries.md)
- [Services XAML](index.md)
