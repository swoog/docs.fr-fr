---
title: Dispose, modèle
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- Dispose method
- class library design guidelines [.NET Framework], Dispose method
- class library design guidelines [.NET Framework], Finalize method
- customizing Dispose method name
- Finalize method
ms.assetid: 31a6c13b-d6a2-492b-9a9f-e5238c983bcb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ff52e17cfe4a4236e4d165c0961ca3a23fed9a72
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43864642"
---
# <a name="dispose-pattern"></a>Dispose, modèle
Tous les programmes d’acquérir une ou plusieurs ressources système, telles que la mémoire, les handles du système ou les connexions de base de données, au cours de leur exécution. Les développeurs doivent être prudent lorsque vous utilisez ces ressources système, car ils doivent être libérées après que qu’ils ont été acquis et utilisés.  
  
 Le CLR prend en charge pour la gestion de mémoire automatique. Gestion de la mémoire (mémoire allouée à l’aide de l’opérateur c# `new`) n’a pas besoin être explicitement libéré. Il est automatiquement libéré par le garbage collector (GC). Cela évite aux développeurs de la tâche fastidieuse et difficile de libération de mémoire et a été une des principales raisons de la productivité sans précédent offerte par le .NET Framework.  
  
 Malheureusement, la mémoire managée est juste un des nombreux types de ressources système. Ressources autres que la mémoire managée toujours doivent être libérées explicitement et sont désignés comme des ressources non managées. Le GC a été pas spécifiquement conçu pour gérer ces ressources non managées, ce qui signifie que la responsabilité de la gestion des ressources non managées est située entre les mains des développeurs.  
  
 Le CLR fournit d’aide pour libérer les ressources non managées. <xref:System.Object?displayProperty=nameWithType> déclare une méthode virtuelle <xref:System.Object.Finalize%2A> (également appelé le finaliseur) qui est appelée par le garbage collector avant que la mémoire de l’objet ne soit récupérée par le garbage collector et peut être substituée pour libérer les ressources non managées. Les types qui substituent le finaliseur sont appelés types finalisables.  
  
 Bien que les finaliseurs sont efficaces dans certains scénarios de nettoyage, ils ont deux des inconvénients importants :  
  
-   Le finaliseur est appelé lorsque le garbage collector détecte qu’un objet est éligible pour la collection. Cela se produit sur une période indéterminée une fois que la ressource n’est plus nécessaire. Le délai entre lorsque le développeur pourrait et pourrait être mise en production de la ressource et l’heure lorsque la ressource est libérée en fait par le finaliseur peut être inacceptable dans les programmes qui acquièrent de nombreuses ressources rares (les ressources qui peuvent être utilisées intégralement facilement) ou dans cas dans lequel les ressources sont coûteux à maintenir en cours d’utilisation (par exemple, les tampons de grande taille de mémoire non managée).  
  
-   Lorsque le CLR doit appeler un finaliseur, il doit reporter la collecte de la mémoire de l’objet jusqu'à ce que la prochaine arrondir du garbage collection (les finaliseurs s’exécutent entre les collections). Cela signifie que le mémoire de l’objet (et tous les objets qu’il fait référence à) ne seront pas disponible pour une période plus longue.  
  
 Par conséquent, s’appuyer exclusivement sur les finaliseurs peut ne pas convenir dans de nombreux scénarios quand il est important de libérer des ressources non managées aussi rapidement que possible, lorsque vous traitez des ressources rares ou dans hautement performante scénarios dans lesquels la surcharge de garbage collection ajoutée de la finalisation est inacceptable.  
  
 Le Framework fournit la <xref:System.IDisposable?displayProperty=nameWithType> interface qui doit être implémentée pour fournir aux développeurs une méthode manuelle de libérer des ressources non managées, dès qu’ils ne sont pas nécessaires. Il fournit également la <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> méthode qui peut indiquer au GC qui un objet a été supprimé manuellement et n’a pas besoin d’être finalisée de plus, auquel cas la mémoire de l’objet peut être récupérée de précédemment. Types qui implémentent le `IDisposable` interface sont appelés types jetables.  
  
 Le modèle Dispose est destiné à normaliser l’utilisation et l’implémentation des finaliseurs et `IDisposable` interface.  
  
 La motivation principale pour le modèle est de réduire la complexité de l’implémentation de la <xref:System.Object.Finalize%2A> et <xref:System.IDisposable.Dispose%2A> méthodes. La complexité vient du fait que les méthodes partagent certains, mais pas tous les chemins de code (les différences sont décrites plus loin dans ce chapitre). En outre, il existe des raisons historiques pour certains éléments du modèle liés à l’évolution de la prise en charge linguistique pour la gestion des ressources déterministe.  
  
 **✓ DO** implémenter le modèle de suppression de base sur les types contenant des instances de types pouvant être supprimés. Consultez le [base modèle Dispose](#basic_pattern) section pour plus d’informations sur le modèle de base.  
  
 Si un type est chargé de la durée de vie d’autres objets jetables, les développeurs ont besoin d’un moyen de les supprimer, trop. À l’aide du conteneur `Dispose` méthode est un moyen pratique pour rendre cela possible.  
  
 **✓ DO** implémenter le modèle de suppression de base et de fournir un finaliseur sur les types de ressources d’exploitation qui doivent être libérées explicitement et qui n’ont pas de finaliseurs.  
  
 Par exemple, le modèle doit être implémenté sur les types de stockage des mémoires tampons de mémoire non managée. Le [Types finalisables](#finalizable_types) section traite des recommandations relatives à l’implémentation des finaliseurs.  
  
 **✓ CONSIDER** implémentant le modèle de suppression de base sur les classes qu’eux-mêmes ne contiennent pas les ressources non managées ou les objets à supprimer, mais sont susceptibles d’avoir les sous-types de font.  
  
 Un bon exemple de ceci est le <xref:System.IO.Stream?displayProperty=nameWithType> classe. Bien qu’il soit une classe de base abstraite qui ne contiennent pas toutes les ressources, la plupart de ses sous-classes, et pour cette raison, il implémente ce modèle.  
  
<a name="basic_pattern"></a>   
## <a name="basic-dispose-pattern"></a>Modèle de suppression de base  
 L’implémentation de base du modèle implique l’implémentation la `System.IDisposable` interface et en déclarant le `Dispose(bool)` méthode qui implémente la logique de nettoyage toutes les ressources d’être partagées entre le `Dispose` (méthode) et le finaliseur facultatif.  
  
 L’exemple suivant montre une implémentation simple du modèle de base :  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
  
    private SafeHandle resource; // handle to a resource  
  
    public DisposableResourceHolder() {  
        this.resource = ... // allocates the resource  
    }  
  
    public void Dispose() {  
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
  
    protected virtual void Dispose(bool disposing) {  
        if (disposing) {  
            if (resource!= null) resource.Dispose();  
        }  
    }  
}  
```  
  
 Le paramètre booléen `disposing` indique si la méthode a été appelée à partir de la `IDisposable.Dispose` implémentation ou à partir du finaliseur. Le `Dispose(bool)` implémentation doit vérifier le paramètre avant d’accéder à d’autres objets de référence (par exemple, le champ ressource dans l’exemple précédent). Ces objets doivent uniquement accessible lorsque la méthode est appelée à partir de la `IDisposable.Dispose` implémentation (lorsque le `disposing` paramètre est égal à true). Si la méthode est appelée à partir du finaliseur (`disposing` a la valeur false), autres objets ne doivent pas être accessibles. La raison est que les objets sont finalisés dans un ordre imprévisible et par conséquent, elles, ou l’un de leurs dépendances, peut déjà avoir été finalisé.  
  
 En outre, cette section s’applique aux classes avec une base qui n’implémente pas déjà le modèle Dispose. Si vous héritez d’une classe qui implémente déjà le modèle, il vous suffit de remplacer le `Dispose(bool)` méthode pour fournir la logique de nettoyage des ressources supplémentaires.  
  
 **✓ DO** déclarer un `protected virtual void Dispose(bool disposing)` méthode pour centraliser toute la logique associée à la libération des ressources non managées.  
  
 Nettoyage des ressources doit se produire dans cette méthode. La méthode est appelée depuis les deux le finaliseur et la `IDisposable.Dispose` (méthode). Le paramètre est false si appelé à partir d’un finaliseur. Il doit être utilisé afin de n’importe quel code en cours d’exécution lors de la finalisation n’accède pas aux autres objets finalisables. Détails de l’implémentation des finaliseurs sont décrits dans la section suivante.  
  
```csharp
protected virtual void Dispose(bool disposing) {  
    if (disposing) {  
        if (resource!= null) resource.Dispose();  
    }  
}  
```  
  
 **✓ DO** implémenter la `IDisposable` interface en appelant simplement `Dispose(true)` suivie `GC.SuppressFinalize(this)`.  
  
 L’appel à `SuppressFinalize` doit uniquement se produire si `Dispose(true)` s’exécute avec succès.  
  
```csharp
public void Dispose(){  
    Dispose(true);  
    GC.SuppressFinalize(this);  
}  
```  
  
 **X DO NOT** rendre sans paramètre `Dispose` méthode virtuelle.  
  
 Le `Dispose(bool)` méthode est celle qui doit être substituée par les sous-classes.  
  
```csharp
// bad design  
public class DisposableResourceHolder : IDisposable {  
    public virtual void Dispose() { ... }  
    protected virtual void Dispose(bool disposing) { ... }  
}  
  
// good design  
public class DisposableResourceHolder : IDisposable {  
    public void Dispose() { ... }  
    protected virtual void Dispose(bool disposing) { ... }  
}  
```  
  
 **X DO NOT** déclarer toutes les surcharges de la `Dispose` autrement que `Dispose()` et `Dispose(bool)`.  
  
 `Dispose` Prenez en compte un mot réservé pour codifier ce modèle et éviter toute confusion entre les implémenteurs, les utilisateurs et les compilateurs. Certains langages peuvent choisir d’implémenter automatiquement ce modèle sur certains types.  
  
 **✓ DO** autoriser la `Dispose(bool)` méthode à être appelée plusieurs fois. La méthode peut choisir de ne rien faire après le premier appel.  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
  
    bool disposed = false;  
  
    protected virtual void Dispose(bool disposing) {  
        if (disposed) return;  
        // cleanup  
        ...  
        disposed = true;  
    }  
}  
```  
  
 **X AVOID** lever une exception depuis `Dispose(bool)` sauf dans les situations où le processus de conteneur a été endommagé critiques (fuites, un état partagé incohérent, etc.).  
  
 Les utilisateurs s’attendent à qui un appel à `Dispose` ne lève pas d’exception.  
  
 Si `Dispose` peut lever une exception, la logique de nettoyage de bloc finally supplémentaire ne s’exécutera pas. Pour contourner ce problème, l’utilisateur aurait besoin encapsuler chaque appel à `Dispose` (dans le bloc finally !) dans un bloc try, ce qui entraîne des gestionnaires de nettoyage très complexe. Si l’exécution un `Dispose(bool disposing)` (méthode), jamais lever une exception si disposing a la valeur false. Cela terminera le processus si l’exécution à l’intérieur d’un contexte de finaliseur.  
  
 **✓ DO** lever un <xref:System.ObjectDisposedException> à partir de n’importe quel membre qui ne peut pas être utilisé une fois que l’objet a été supprimé.  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
    bool disposed = false;  
    SafeHandle resource; // handle to a resource  
  
    public void DoSomething() {  
        if (disposed) throw new ObjectDisposedException(...);  
        // now call some native methods using the resource   
        ...  
    }  
    protected virtual void Dispose(bool disposing) {  
        if (disposed) return;  
        // cleanup  
        ...  
        disposed = true;  
    }  
}  
```  
  
 **✓ CONSIDER** en fournissant la méthode `Close()`, en plus de la `Dispose()`, si proche est une terminologie standard dans la zone.  
  
 Ce cas, il est important de faire la `Close` implémentation identique à `Dispose` et envisagez d’implémenter la `IDisposable.Dispose` méthode explicitement.  
  
```csharp
public class Stream : IDisposable {  
    IDisposable.Dispose() {  
        Close();  
    }  
    public void Close() {  
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
}  
```  
  
<a name="finalizable_types"></a>   
## <a name="finalizable-types"></a>Types finalisables  
 Types finalisables sont des types qui étendent le modèle de base Dispose en remplaçant le finaliseur et en fournissant le chemin d’accès du code de finalisation dans le `Dispose(bool)` (méthode).  
  
 Les finaliseurs sont notoirement difficiles à implémenter correctement, principalement parce que vous ne pouvez pas avancez certaines hypothèses (normalement valides) sur l’état du système pendant leur exécution. Les instructions suivantes doivent être prises en considération prudente.  
  
 Notez que certaines instructions s’appliquent pas uniquement à la `Finalize` (méthode), mais à tout code appelé à partir d’un finaliseur. Dans le cas le modèle Dispose base défini précédemment, cela signifie que la logique qui s’exécute à l’intérieur de `Dispose(bool disposing)` lorsque le `disposing` paramètre a la valeur false.  
  
 Si la classe de base est finalisable déjà et implémente le modèle Dispose de base, vous ne devez pas substituer `Finalize` à nouveau. Vous devez substituer à la place simplement la `Dispose(bool)` méthode pour fournir la logique de nettoyage des ressources supplémentaires.  
  
 Le code suivant montre un exemple d’un type finalisable :  
  
```csharp
public class ComplexResourceHolder : IDisposable {  
  
    private IntPtr buffer; // unmanaged memory buffer  
    private SafeHandle resource; // disposable handle to a resource  
  
    public ComplexResourceHolder() {  
        this.buffer = ... // allocates memory  
        this.resource = ... // allocates the resource  
    }  
  
    protected virtual void Dispose(bool disposing) {  
            ReleaseBuffer(buffer); // release unmanaged memory  
        if (disposing) { // release other disposable objects  
            if (resource!= null) resource.Dispose();  
        }  
    }  
  
    ~ComplexResourceHolder() {
        Dispose(false);  
    }  
  
    public void Dispose() {
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
}  
```  
  
 **X AVOID** rendre types finalisables.  
  
 Étudiez attentivement tous les cas dans lequel vous pensez qu'un finaliseur est nécessaire. Il existe une véritable coût associé aux instances avec des finaliseurs, une performance et le code de point de vue de la complexité. Préférer à l’aide des wrappers de ressource comme <xref:System.Runtime.InteropServices.SafeHandle> pour encapsuler les ressources non managées lorsque cela est possible, auquel cas un finaliseur devienne inutile, car le wrapper est responsable de son propre nettoyage des ressources.  
  
 **X DO NOT** rendre des types valeur finalisables.  
  
 Seuls les types référence réellement obtient finalisés par le CLR, et par conséquent, toute tentative pour placer un finaliseur sur un type valeur sera ignorée. Les compilateurs c# et C++ appliquent cette règle.  
  
 **✓ DO** rendre un type finalisables si le type est responsable de la libération d’une ressource non managée qui n’a pas son propre finaliseur.  
  
 Lorsque vous implémentez le finaliseur, appelez simplement `Dispose(false)` et placer la logique de nettoyage toutes les ressources à l’intérieur de la `Dispose(bool disposing)` (méthode).  
  
```csharp
public class ComplexResourceHolder : IDisposable {  
  
    ~ComplexResourceHolder() {
        Dispose(false);  
    }  
  
    protected virtual void Dispose(bool disposing) {
        ...  
    }  
}  
```  
  
 **✓ DO** implémenter le modèle de suppression de base sur chaque type finalisable.  
  
 Ainsi, les utilisateurs du type d’un moyen pour effectuer explicitement le nettoyage déterministe de ces mêmes ressources dont le finaliseur est responsable.  
  
 **X DO NOT** accéder à tous les objets finalisables dans le chemin d’accès du code finaliseur, étant donné le risque qu’ils seront déjà avoir été finalisés.  
  
 Par exemple, un objet finalisable A qui a une référence à un autre objet finalisable B ne peut pas utiliser fiable de B dans une suite de finaliseur, ou vice versa. Les finaliseurs sont appelés dans un ordre aléatoire (pas une garantie de classement faible pour la finalisation critique).  
  
 En outre, n’oubliez pas que les objets stockés dans des variables statiques seront collectés à certains points pendant un déchargement du domaine d’application ou lors de la sortie du processus. L’accès à une variable statique qui fait référence à un objet finalisable (ou en appelant une méthode statique qui peut utiliser des valeurs stockées dans des variables statiques) ne peut pas être sécurisé if <xref:System.Environment.HasShutdownStarted%2A?displayProperty=nameWithType> retourne la valeur true.  
  
 **✓ DO** rendre votre `Finalize` méthode protégée.  
  
 Les développeurs c#, C++ et VB.NET est inutile à vous soucier de cela, étant donné que les compilateurs aider à appliquer cette recommandation.  
  
 **X DO NOT** échappement permettent d’exceptions à partir de la logique de finaliseur, à l’exception des défaillances système critiques.  
  
 Si une exception est levée à partir d’un finaliseur, le CLR s’arrête à l’ensemble du processus (à compter de .NET Framework version 2.0), empêchant les autres finaliseurs d’exécuter et de ressources à partir de libéré de manière contrôlée.  
  
 **✓ CONSIDER** création et utilisation d’un objet finalisable critiques (un type avec une hiérarchie de type qui contient <xref:System.Runtime.ConstrainedExecution.CriticalFinalizerObject>) pour les situations dans lesquelles un finaliseur absolument doit s’exécuter même en cas de déchargement de domaine d’application forcé et de thread abandonne.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType>  
- <xref:System.Object.Finalize%2A?displayProperty=nameWithType>  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
- [Modèles de design courants](../../../docs/standard/design-guidelines/common-design-patterns.md)  
- [Nettoyage de la mémoire](../../../docs/standard/garbage-collection/index.md)
