---
title: Instructions de codage sécurisé pour .NET
ms.date: 06/28/2018
helpviewer_keywords:
- managed wrapper to native code implementation
- secure coding
- reusable components
- library code that exposes protected resources
- code, security
- code security
- secure coding, options
- components [.NET], security
- code security, options
- security-neutral code
- security [.NET], coding guidelines
ms.assetid: 4f882d94-262b-4494-b0a6-ba9ba1f5f177
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b3a8f0dfc1a2b5e09722876b73281ed1d8b6334e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62018643"
---
# <a name="secure-coding-guidelines"></a>Instructions de codage sécurisé

La sécurité basée sur les preuves et la sécurité d’accès du code fournissent des mécanismes particulièrement puissants et explicites d’implémentation de la sécurité. La plupart des codes d’application peut simplement utiliser l’infrastructure implémentée par .NET. Dans certains cas, une sécurité supplémentaire spécifique à l’application est nécessaire, générée via l’extension du système de sécurité ou via de nouvelles méthodes ad hoc.

À l’aide de .NET appliquée autorisations et autres vérifications dans votre code, vous devez ériger des barrières pour empêcher le code malveillant d’accéder aux informations que vous ne souhaitez pas qu’il ait ou effectuer d’autres actions indésirables. En outre, il vous faut trouver un compromis entre la sécurité et les possibilités d’utilisation dans tous les scénarios prévus qui utilisent du code de confiance.

Cette présentation décrit les différents procédés permettant de concevoir du code qui fonctionne avec le système de sécurité.

## <a name="securing-resource-access"></a>Sécurisation des accès aux ressources

Lorsque vous concevez et écrivez votre code, vous devez protéger et limiter l’accès du code aux ressources, tout particulièrement quand vous utilisez ou appelez un code d’une origine inconnue. Par conséquent, ayez à l’esprit les techniques suivantes afin de garantir la sécurité de votre code :

- N’utilisez pas la sécurité d’accès du code (CAS, Code Access Security).

- N’utilisez pas du code de confiance partielle.

- N’utilisez pas le [AllowPartiallyTrustedCaller](xref:System.Security.AllowPartiallyTrustedCallersAttribute) attribut (APTCA).

- N’utilisez pas .NET Remoting.

- N’utilisez pas le modèle COM distribué (Distributed Component Object Model, DCOM).

- N’utilisez pas de formateurs binaires.

Sécurité d’accès du code et le Code Transparent de sécurité ne sont pas pris en charge en tant que limite de sécurité avec du code partiellement fiable. Nous vous déconseillons de charger et d'exécuter du code d'origine inconnue sans mettre en place d'autres mesures de sécurité. Les autres mesures de sécurité sont les suivantes :

- Virtualisation

- Conteneurs d’applications

- Utilisateurs et autorisations du système d’exploitation

- Conteneurs Hyper-V

## <a name="security-neutral-code"></a>Code indépendant de la sécurité

Un code indépendant de la sécurité ne fait rien d’explicite avec le système de sécurité. Il s’exécute quelles que soient les autorisations qu’il reçoit. Bien que les applications qui ne parviennent pas à intercepter les exceptions de sécurité associées à des opérations protégées (par exemple, l’utilisation de fichiers, mise en réseau et ainsi de suite) peuvent entraîner une exception non gérée, le code indépendant de la sécurité tire néanmoins parti des technologies de sécurité dans .NET .

Une bibliothèque indépendante de la sécurité possède des caractéristiques particulières que vous devez connaître. Supposons que votre bibliothèque fournisse des éléments d’API qui utilisent des fichiers ou d’appellent du code non managé. Si votre code n’a pas l’autorisation correspondante, il ne s’exécuter comme décrit. Toutefois, même si le code possède cette autorisation, n’importe quel autre code d’application qui l’appelle doit avoir la même autorisation pour pouvoir fonctionner. Si le code appelant n’a pas l’autorisation appropriée, une <xref:System.Security.SecurityException> s’affiche à la suite le parcours de pile de code access security.

## <a name="application-code-that-isnt-a-reusable-component"></a>Code d’application qui n’est pas un composant réutilisable

Si votre code fait partie d’une application qui n’est pas appelée par un autre code, la sécurité est simple et un codage spécial peut ne pas être nécessaire. Toutefois, n’oubliez pas qu’un code malveillant peut appeler votre code. Si la sécurité d’accès du code peut empêcher le code malveillant d’accéder à des ressources, ce type de code est toutefois capable de lire les valeurs de vos champs ou propriétés susceptibles de contenir des informations confidentielles.

De plus, si votre code accepte des entrées utilisateur à partir d’Internet ou d’autres sources peu fiables, vous devez vous méfier des entrées malveillantes.

## <a name="managed-wrapper-to-native-code-implementation"></a>Wrapper managé vers l’implémentation de code natif

Dans ce scénario, certaines fonctionnalités utiles sont implémentées dans du code natif que vous souhaitez mettre à la disposition du code managé. Il est aisé d’écrire des wrappers managés en utilisant l’appel de code non managé ou COM Interop. Toutefois, si vous procédez ainsi, les appelants de vos wrappers doivent avoir des droits de code non managé pour réussir. Sous la stratégie par défaut, cela signifie que le code téléchargé à partir d’un intranet ou Internet ne fonctionne pas avec les wrappers.

Au lieu de donner des droits de code non managé sur toutes les applications qui utilisent ces wrappers, il est préférable d’accorder ces droits uniquement au code wrapper. Si les fonctionnalités sous-jacentes n’exposent aucune ressource et que l’implémentation est également sécurisée, le wrapper doit simplement déclarer ses droits, ce qui permet à n’importe quel code d’effectuer un appel via celui-ci. Lorsque des ressources sont impliquées, le codage de sécurité doit être identique à l’exemple de code de bibliothèque décrit dans la section suivante. Comme le wrapper expose potentiellement les appelants à ces ressources, une vérification minutieuse de la sécurité du code natif est nécessaire. Celle-ci relève de la responsabilité du wrapper.

## <a name="library-code-that-exposes-protected-resources"></a>Code de bibliothèque qui expose des ressources protégées

L’approche suivante est la plus puissante et donc potentiellement dangereuse (si effectuée correctement) pour le codage de sécurité : votre bibliothèque sert d’une interface pour un autre code accéder à certaines ressources qui ne sont pas autrement disponibles, tout comme les classes .NET appliquent autorisations pour les ressources qu’ils utilisent. Chaque fois que vous exposez une ressource, votre code doit en premier lieu demander l’autorisation appropriée à la ressource (autrement dit, il doit effectuer une vérification de sécurité), puis généralement déclarer ses droits pour effectuer l’opération proprement dite.

## <a name="related-topics"></a>Rubriques connexes

|Titre|Description|
|-----------|-----------------|
|[Sécurisation des données d’état](securing-state-data.md)|Décrit comment protéger les membres privés.|
|[Sécurité et entrées d’utilisateur](security-and-user-input.md)|Décrit les problèmes de sécurité liés à des applications qui acceptent les entrées utilisateur.|
|[Sécurité et conditions de concurrence](security-and-race-conditions.md)|Décrit comment éviter des conditions de concurrence critique dans votre code.|
|[Sécurité et génération de code immédiate](security-and-on-the-fly-code-generation.md)|Décrit les problèmes de sécurité liés à des applications qui génèrent du code dynamique.|
|[Sécurité basée sur les rôles](role-based-security.md)|Décrit la sécurité des rôles .NET en détail et explique comment l’utiliser dans votre code.|
