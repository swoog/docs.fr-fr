---
title: Espaces de noms XAML pour les services XAML .NET Framework
ms.date: 03/30/2017
ms.assetid: e4f15f13-c420-4c1e-aeab-9b6f50212047
ms.openlocfilehash: ac6554cbdeb5bc6e0fe7fb96ea95d0143c293d22
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2018
ms.locfileid: "47455023"
---
# <a name="xaml-namespaces-for-net-framework-xaml-services"></a>Espaces de noms XAML pour les services XAML .NET Framework
Un espace de noms XAML est un concept qui se développe sur la définition d’un espace de noms XML. Similaire à un espace de noms XML, vous pouvez définir un espace de noms XAML à l’aide un `xmlns` attribut dans le balisage. Espaces de noms XAML sont également représentées dans le flux de nœud XAML et d’autres API de Services XAML. Cette rubrique définit le concept d’espace de noms XAML et décrit comment les espaces de noms XAML peuvent être définies et utilisées par les contextes de schéma XAML et d’autres aspects des Services XAML du .NET Framework.  
  
## <a name="xml-namespace-and-xaml-namespace"></a>Namespace XML et XAML Namespace  
 Un espace de noms XAML est un espace de noms XML spécialisé, tout comme XAML est une forme spécialisée de XML et utilise le formulaire XML de base pour son balisage. Dans le balisage, vous déclarez un espace de noms XAML et son mappage via un `xmlns` attribut appliqué à un élément. Le `xmlns` déclaration peut être faite au même élément déclaré dans l’espace de noms XAML. Une déclaration d’espace de noms XAML apportée à un élément est valide pour cet élément, tous les attributs de cet élément et tous les enfants de cet élément. Attributs peuvent utiliser un espaces de noms XAML qui n’est pas identique à l’élément qui contient l’attribut, tant que le nom de l’attribut fait référence le préfixe dans le cadre de son nom d’attribut dans le balisage.  
  
 La différence d’un espace de noms XAML par rapport à un espace de noms XML est qu’un espace de noms XML peut être utilisé pour faire référence à un schéma, ou peut servir à différencier simplement les entités. Pour XAML, les types et les membres utilisés en XAML doivent correspondre aux types de stockage et les concepts de schéma XML ne s’appliquent pas bien à cette fonction. L’espace de noms XAML contient des informations que le contexte de schéma XAML doit avoir disponible pour effectuer ce mappage de type.  
  
## <a name="xaml-namespace-components"></a>Composants de Namespace XAML  
 La définition d’espace de noms XAML comporte deux composants : un préfixe et un identificateur. Chacun de ces composants sont présents, lorsqu’un espace de noms XAML est déclaré dans le balisage ou défini dans le système de type XAML.  
  
 Le préfixe peut être n’importe quelle chaîne autorisée par la [W3C des espaces de noms dans la spécification XML 1.0](https://go.microsoft.com/fwlink/?LinkID=161735) . Par convention, les préfixes sont des chaînes généralement très courtes, étant donné que le préfixe est répété plusieurs fois dans un fichier de balisage classique. Certains espaces de noms XAML qui sont destinées à être utilisées dans plusieurs implémentations XAML utilisent préfixes conventionnels particuliers. Par exemple, l’espace de noms XAML du langage XAML est généralement mappé à l’aide du préfixe `x`. Vous pouvez définir un espace de noms XAML par défaut, où le préfixe n’est pas spécifié dans la définition, mais est représenté comme une chaîne vide si défini ou interrogé by.NET API des Services XAML Framework. En règle générale, l’espace de noms XAML par défaut est délibérément choisi pour promouvoir une quantité maximum de sans préfixe balisage par une technologie de mise en œuvre de XAML et ses scénarios et des vocabulaires.  
  
 L’identificateur peut être n’importe quelle chaîne autorisée par la [W3C des espaces de noms dans la spécification XML 1.0](https://go.microsoft.com/fwlink/?LinkID=161735). Par convention, identificateurs d’espaces de noms XML ou d’espaces de noms XAML sont souvent donnés sous forme d’URI, généralement sous la forme d’un URI absolu à protocole. Souvent, les informations de version qui définissent un vocabulaire XAML particulier sont implicite dans le cadre de la chaîne de chemin d’accès. Espaces de noms XAML ajouter une convention d’identificateur supplémentaire au-delà de la convention URI XML. Pour les espaces de noms XAML, l’identificateur communique les informations requises par un contexte de schéma XAML afin de résoudre les types qui sont spécifiés en tant qu’éléments sous cet espace de noms XAML, ou pour résoudre des attributs aux membres.  
  
 À des fins de communiquer des informations à un contexte de schéma XAML, l’identificateur pour un espace de noms XAML peut toujours être sous forme URI. Toutefois, dans ce cas l’URI est également déclaré comme un identificateur correspondant dans un assembly particulier ou une liste d’assemblys. Cela est effectué dans les assemblys en attribuant l’assembly avec <xref:System.Windows.Markup.XmlnsDefinitionAttribute>. Cette méthode d’identification de l’espace de noms XAML et de prise en charge d’un comportement de résolution de type basé sur CLR dans l’assembly avec attributs est pris en charge par le contexte de schéma XAML par défaut dans les Services XAML .NET Framework. En règle générale, cette convention utilisable pour les cas où le contexte de schéma XAML incorpore le CLR ou est basé sur le contexte de schéma XAML par défaut, ce qui est nécessaire pour pouvoir lire des attributs CLR à partir d’assemblys CLR.  
  
 Espaces de noms XAML peut également être identifiée par une convention qui communique un espace de noms CLR et un assembly de définition de type. Cette convention est utilisée dans les cas où aucun <xref:System.Windows.Markup.XmlnsDefinitionAttribute> attribution existe dans les assemblys qui contiennent des types. Cette convention est potentiellement plus complexe que la convention d’URI et a également le potentiel d’ambiguïté et de duplication, car il existe plusieurs façons de faire référence à un assembly.  
  
 La forme la plus basique d’un identificateur qui utilise la convention d’espace de noms et assembly CLR est la suivante :  
  
 `clr-namespace:` *clrnsName* `; assembly=` *NomCourtAssembly*  
  
 `clr-namespace:` et `; assembly=` sont des composants de la syntaxe littérales.  
  
 *clrnsName* est le nom de chaîne qui identifie un espace de noms CLR. Ce nom de chaîne inclut tous les caractères internes de points (.) qui fournissent des conseils sur l’espace de noms CLR et sa relation à d’autres espaces de noms CLR.  
  
 *NomCourtAssembly* est le nom de chaîne d’un assembly qui définit les types qui sont utiles dans XAML. Les types seront accessibles via l’espace de noms XAML déclaré sont censés être définis par l’assembly et spécifiquement déclarés dans l’espace de noms CLR spécifié par *clrnsName*. Ce nom de chaîne met généralement en parallèle les informations comme indiqué par <xref:System.Reflection.AssemblyName.Name%2A?displayProperty=nameWithType>.  
  
 Une définition plus complète de la convention d’espace de noms et assembly CLR est la suivante :  
  
 `clr-namespace:` *clrnsName* `; assembly=` *assemblyName*  
  
 *assemblyName* représente n’importe quelle chaîne pouvant être utilisé comme un <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> d’entrée. Cette chaîne peut inclure culture, clé publique ou les informations de version (définitions de ces concepts sont définies dans la rubrique de référence <xref:System.Reflection.Assembly>). COFF format et les preuves (tel qu’utilisé par les autres surcharges de <xref:System.Reflection.Assembly.Load%2A>) ne sont pas pertinentes pour XAML chargement d’assembly à des fins ; toutes les informations sur le chargement doivent être présentées sous forme de chaîne.  
  
 Spécification d’une clé publique pour l’assembly est une technique utile pour la sécurité XAML ou pour supprimer l’ambiguïté qui peut exister si les assemblys sont chargés par nom simple ou existent préalablement dans un domaine d’application ou du cache. Pour plus d’informations, consultez [considérations sur la sécurité XAML](../../../docs/framework/xaml-services/xaml-security-considerations.md).  
  
## <a name="xaml-namespace-declarations-in-the-xaml-services-api"></a>Déclarations de Namespace XAML dans l’API des Services XAML  
 Dans l’API de Services XAML, une déclaration d’espace de noms XAML est représentée par un <xref:System.Xaml.NamespaceDeclaration> objet. Si vous déclarez un espace de noms XAML dans le code, vous appelez le <xref:System.Xaml.NamespaceDeclaration.%23ctor%28System.String%2CSystem.String%29> constructeur. Le `ns` et `prefix` paramètres sont spécifiés sous forme de chaînes, et l’entrée à fournir pour ces paramètres correspond à la définition de l’identificateur d’espace de noms XAML et le préfixe d’espace de noms XAML, comme indiqué précédemment dans cette rubrique.  
  
 Si vous examinez les informations d’espace de noms XAML dans le cadre d’un flux de nœud XAML ou par un autre accès au système de type XAML, <xref:System.Xaml.NamespaceDeclaration.Namespace%2A?displayProperty=nameWithType> signale l’identificateur d’espace de noms XAML, et <xref:System.Xaml.NamespaceDeclaration.Prefix%2A?displayProperty=nameWithType> signale le préfixe d’espace de noms XAML.  
  
 Dans un flux de nœud XAML, les informations d’espace de noms XAML peuvent apparaître sous forme de nœud XAML qui précède l’entité à laquelle elle s’applique. Cela inclut les cas où les informations d’espace de noms XAML précédant le `StartObject` de l’élément racine XAML. Pour plus d'informations, consultez [Understanding XAML Node Stream Structures and Concepts](../../../docs/framework/xaml-services/understanding-xaml-node-stream-structures-and-concepts.md).  
  
 Pour de nombreux scénarios qui utilisent les API des Services XAML .NET Framework, au moins une déclaration d’espace de noms XAML doit exister, et la déclaration doit contenir ou faire référence aux informations requises par un contexte de schéma XAML. Les espaces de noms XAML doivent spécifier les assemblys pour être chargé, ou vous permettre de résoudre des types spécifiques au sein d’espaces de noms et assemblys déjà chargés ou connus par le contexte de schéma XAML.  
  
 Pour générer un flux de nœud XAML, les informations de type XAML doivent être disponibles, par le biais du contexte de schéma XAML. Impossible de déterminer tout d’abord définir l’espace de noms XAML approprié pour chaque nœud créer les informations de type XAML. À ce stade, aucune instance de type n’est encore créé, mais le contexte de schéma XAML peut devoir consulter des informations sur la définition d’assembly et le type de stockage. Par exemple, pour traiter le balisage `<Party><PartyFavor/></Party>`, le contexte de schéma XAML doit être en mesure de déterminer le nom et le type de la `ContentProperty` de `Party`et par conséquent doit également connaître les informations d’espace de noms XAML pour `Party` et `PartyFavor`. Dans le cas le contexte de schéma XAML par défaut, la réflexion statique rapporte une grande partie des informations de système de type XAML qui sont nécessaire pour générer des nœuds de type XAML dans le flux de nœud.  
  
 Pour générer un graphique d’objet à partir d’un flux de nœud XAML, les déclarations d’espace de noms XAML doivent exister pour chaque préfixe XAML utilisé dans le balisage d’origine et enregistrée dans le flux de nœud XAML. À ce stade, sont en cours de création des instances, et true-mappage de type de comportement se produit.  
  
 Si vous avez besoin préremplir les informations d’espace de noms XAML, dans les cas où l’espace de noms XAML que vous avez l’intention de contexte de schéma XAML à utiliser n’est pas défini dans le balisage, une technique que vous pouvez utiliser consiste à déclarer des déclarations d’espace de noms XML dans le <xref:System.Xml.XmlParserContext> pour un <xref:System.Xml.XmlReader>. Utilisez ensuite <xref:System.Xml.XmlReader> en tant qu’entrée d’un constructeur de lecteur XAML, ou <xref:System.Xaml.XamlServices.Load%28System.Xml.XmlReader%29?displayProperty=nameWithType>.  
  
 Deux autres API qui sont pertinentes pour l’espace de noms XAML gestion dans les Services XAML .NET Framework sont les attributs <xref:System.Windows.Markup.XmlnsDefinitionAttribute> et <xref:System.Windows.Markup.XmlnsPrefixAttribute>. Ces attributs s’appliquent aux assemblys. <xref:System.Windows.Markup.XmlnsDefinitionAttribute> est utilisé par un contexte de schéma XAML pour interpréter toute déclaration d’espace de noms XAML qui inclut un URI. <xref:System.Windows.Markup.XmlnsPrefixAttribute> est utilisé par les outils qui émettent XAML afin qu’un espace de noms XAML particulier peut être sérialisé avec un préfixe prédictible. Pour plus d’informations, consultez [Related CLR attributs pour les Types personnalisés et les bibliothèques](../../../docs/framework/xaml-services/xaml-related-clr-attributes-for-custom-types-and-libraries.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Fonctionnement des concepts et structures du flux de nœud XAML](../../../docs/framework/xaml-services/understanding-xaml-node-stream-structures-and-concepts.md)
