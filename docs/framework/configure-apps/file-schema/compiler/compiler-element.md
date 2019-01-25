---
title: '&lt;compilateur&gt; élément'
ms.date: 08/14/2018
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#compiler
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.codedom/compilers/compiler
helpviewer_keywords:
- compiler configuration elements, <compiler> element
- <compiler> element
- compiler configuration attributes
- compiler element
ms.assetid: 7a151659-b803-4c27-b5ce-1c4aa0d5a823
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 40bba9f89801a75ac8c9d15e67e060714d1a29d7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54680765"
---
# <a name="ltcompilergt-element"></a><span data-ttu-id="1835a-102">&lt;compilateur&gt; élément</span><span class="sxs-lookup"><span data-stu-id="1835a-102">&lt;compiler&gt; Element</span></span>

<span data-ttu-id="1835a-103">Spécifie les attributs de configuration du compilateur pour un fournisseur de langage.</span><span class="sxs-lookup"><span data-stu-id="1835a-103">Specifies the compiler configuration attributes for a language provider.</span></span>

<span data-ttu-id="1835a-104">\<Élément de configuration > \<system.codedom élément > \<compilers, élément > \<compilateur > élément</span><span class="sxs-lookup"><span data-stu-id="1835a-104">\<configuration Element> \<system.codedom Element> \<compilers Element> \<compiler> Element</span></span>

## <a name="syntax"></a><span data-ttu-id="1835a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1835a-105">Syntax</span></span>

```xml
<compiler
  language="languageName[;...;...]"
  extension="fileExtension[;...;...]"
  type="typeName, assemblyName"
  warningLevel="number"
  compilerOptions="option1 option2"
/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="1835a-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1835a-106">Attributes and Elements</span></span>

<span data-ttu-id="1835a-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1835a-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="1835a-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="1835a-108">Attributes</span></span>

|<span data-ttu-id="1835a-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="1835a-109">Attribute</span></span>|<span data-ttu-id="1835a-110">Description</span><span class="sxs-lookup"><span data-stu-id="1835a-110">Description</span></span>|
|---------------|-----------------|
|`compilerOptions`|<span data-ttu-id="1835a-111">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="1835a-111">Optional attribute.</span></span><br /><br /> <span data-ttu-id="1835a-112">Spécifie des arguments supplémentaires spécifiques au compilateur pour la compilation.</span><span class="sxs-lookup"><span data-stu-id="1835a-112">Specifies additional compiler-specific arguments for compilation.</span></span> <span data-ttu-id="1835a-113">Les valeurs pour le `compilerOptions` attribut sont généralement répertoriées dans une rubrique d’options du compilateur pour le compilateur.</span><span class="sxs-lookup"><span data-stu-id="1835a-113">The values for the `compilerOptions` attribute are typically listed in a compiler options topic for the compiler.</span></span>|
|`extension`|<span data-ttu-id="1835a-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="1835a-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="1835a-115">Fournit une liste délimitée par des points-virgules des extensions de nom de fichier utilisé par les fichiers de code source pour le fournisseur de langages.</span><span class="sxs-lookup"><span data-stu-id="1835a-115">Provides a semicolon-separated list of file name extensions used by source files for the language provider.</span></span> <span data-ttu-id="1835a-116">Par exemple, « .cs ».</span><span class="sxs-lookup"><span data-stu-id="1835a-116">For example, ".cs".</span></span>|
|`language`|<span data-ttu-id="1835a-117">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="1835a-117">Required attribute.</span></span><br /><br /> <span data-ttu-id="1835a-118">Fournit une liste délimitée par des points-virgules de noms de langages pris en charge par le fournisseur de langages.</span><span class="sxs-lookup"><span data-stu-id="1835a-118">Provides a semicolon-separated list of language names supported by the language provider.</span></span> <span data-ttu-id="1835a-119">Par exemple, « c# ; cs ; csharp ».</span><span class="sxs-lookup"><span data-stu-id="1835a-119">For example, "c#;cs;csharp".</span></span>|
|`type`|<span data-ttu-id="1835a-120">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="1835a-120">Required attribute.</span></span><br /><br /> <span data-ttu-id="1835a-121">Spécifie le nom de type fournisseur de langages, y compris le nom de l’assembly contenant l’implémentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1835a-121">Specifies the type name of the language provider, including the name of the assembly containing the provider implementation.</span></span> <span data-ttu-id="1835a-122">Le nom de type doit respecter les exigences définies dans [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span><span class="sxs-lookup"><span data-stu-id="1835a-122">The type name must meet the requirements defined in [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|
|`warningLevel`|<span data-ttu-id="1835a-123">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="1835a-123">Optional attribute.</span></span><br /><br /> <span data-ttu-id="1835a-124">Spécifie le niveau d’avertissement du compilateur par défaut ; Détermine le niveau auquel le fournisseur de langages traite les avertissements de compilation comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="1835a-124">Specifies the default compiler warning level; determines the level at which the language provider treats compilation warnings as errors.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="1835a-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1835a-125">Child Elements</span></span>

|<span data-ttu-id="1835a-126">Élément</span><span class="sxs-lookup"><span data-stu-id="1835a-126">Element</span></span>|<span data-ttu-id="1835a-127">Description</span><span class="sxs-lookup"><span data-stu-id="1835a-127">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="1835a-128">\<providerOption > élément</span><span class="sxs-lookup"><span data-stu-id="1835a-128">\<providerOption> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/provideroption-element.md)|<span data-ttu-id="1835a-129">Spécifie les attributs de version du compilateur pour un fournisseur de langage.</span><span class="sxs-lookup"><span data-stu-id="1835a-129">Specifies compiler version attributes for a language provider.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="1835a-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1835a-130">Parent Elements</span></span>

|<span data-ttu-id="1835a-131">Élément</span><span class="sxs-lookup"><span data-stu-id="1835a-131">Element</span></span>|<span data-ttu-id="1835a-132">Description</span><span class="sxs-lookup"><span data-stu-id="1835a-132">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="1835a-133">\<configuration>, élément</span><span class="sxs-lookup"><span data-stu-id="1835a-133">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="1835a-134">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="1835a-134">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|[<span data-ttu-id="1835a-135">\<System.CodeDom > élément</span><span class="sxs-lookup"><span data-stu-id="1835a-135">\<system.codedom> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)|<span data-ttu-id="1835a-136">Spécifie les paramètres de configuration du compilateur pour les fournisseurs de langages disponibles.</span><span class="sxs-lookup"><span data-stu-id="1835a-136">Specifies compiler configuration settings for available language providers.</span></span>|
|[<span data-ttu-id="1835a-137">\<compilateurs > élément</span><span class="sxs-lookup"><span data-stu-id="1835a-137">\<compilers> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|<span data-ttu-id="1835a-138">Conteneur pour les éléments de configuration de compilateur ; contient zéro ou plusieurs `<compiler>` éléments.</span><span class="sxs-lookup"><span data-stu-id="1835a-138">Container for compiler configuration elements; contains zero or more `<compiler>` elements.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1835a-139">Notes</span><span class="sxs-lookup"><span data-stu-id="1835a-139">Remarks</span></span>

<span data-ttu-id="1835a-140">Chaque `<compiler>` élément spécifie les attributs de configuration du compilateur pour un fournisseur de langage spécifique.</span><span class="sxs-lookup"><span data-stu-id="1835a-140">Each `<compiler>` element specifies the compiler configuration attributes for a specific language provider.</span></span> <span data-ttu-id="1835a-141">Étend le fournisseur le <xref:System.CodeDom.Compiler.CodeDomProvider?displayProperty=nameWithType> classe pour une langue spécifique ; la `<compiler>` élément définit le compilateur et les paramètres de générateur de code pour le fournisseur de langages.</span><span class="sxs-lookup"><span data-stu-id="1835a-141">The provider extends the <xref:System.CodeDom.Compiler.CodeDomProvider?displayProperty=nameWithType> class for a specific language; the `<compiler>` element defines the compiler and code generator settings for the language provider.</span></span>

<span data-ttu-id="1835a-142">Le .NET Framework définit les paramètres de compilateur initiaux dans le fichier de configuration de l’ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="1835a-142">The .NET Framework defines the initial compiler settings in the machine configuration file (Machine.config).</span></span> <span data-ttu-id="1835a-143">Les développeurs et les éditeurs de compilateurs peuvent ajouter des paramètres de configuration pour une nouvelle implémentation <xref:System.CodeDom.Compiler.CodeDomProvider>.</span><span class="sxs-lookup"><span data-stu-id="1835a-143">Developers and compiler vendors can add configuration settings for a new <xref:System.CodeDom.Compiler.CodeDomProvider> implementation.</span></span> <span data-ttu-id="1835a-144">Utilisez la méthode <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> pour énumérer par programmation les paramètres de configuration du compilateur et du fournisseur de langage sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1835a-144">Use the <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> method to programmatically enumerate language provider and compiler configuration settings on a computer.</span></span>

<span data-ttu-id="1835a-145">Éléments du compilateur dans l’application ou le fichier de configuration Web peuvent compléter ou remplacer les paramètres dans le fichier de configuration machine.</span><span class="sxs-lookup"><span data-stu-id="1835a-145">Compiler elements in the application or Web configuration file can supplement or override the settings in the machine configuration file.</span></span> <span data-ttu-id="1835a-146">Si plus d’une implémentation de fournisseur est configurée pour le même nom de langage ou la même extension de fichier, la dernière configuration correspondante remplace n’importe quel précédentes fournisseurs configurés pour cette extension de fichier ou le nom de langage.</span><span class="sxs-lookup"><span data-stu-id="1835a-146">If more than one provider implementation is configured for the same language name or the same file extension, the last matching configuration overrides any previous configured providers for that language name or file extension.</span></span>

## <a name="configuration-file"></a><span data-ttu-id="1835a-147">Fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="1835a-147">Configuration File</span></span>

<span data-ttu-id="1835a-148">Cet élément peut être utilisé dans le fichier de configuration machine et le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="1835a-148">This element can be used in the machine configuration file and the application configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="1835a-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="1835a-149">Example</span></span>

<span data-ttu-id="1835a-150">L’exemple suivant illustre un élément de configuration de compilateur classique :</span><span class="sxs-lookup"><span data-stu-id="1835a-150">The following example illustrates a typical compiler configuration element:</span></span>

```xml
<configuration>
  <system.codedom>
    <compilers>
      <!-- zero or more compiler elements -->
      <compiler
        language="c#;cs;csharp"
        extension=".cs"
        type="Microsoft.CSharp.CSharpCodeProvider, System,
          Version=2.0.3600.0, Culture=neutral,
          PublicKeyToken=b77a5c561934e089"
        compilerOptions="/optimize"
        warningLevel="1" />
    </compilers>
  </system.codedom>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="1835a-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1835a-151">See also</span></span>

- <xref:System.CodeDom.Compiler.CompilerInfo>
- <xref:System.CodeDom.Compiler.CodeDomProvider>
- [<span data-ttu-id="1835a-152">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="1835a-152">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="1835a-153">\<compilateurs > élément</span><span class="sxs-lookup"><span data-stu-id="1835a-153">\<compilers> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)
- [<span data-ttu-id="1835a-154">Spécification des noms de types complets</span><span class="sxs-lookup"><span data-stu-id="1835a-154">Specifying Fully Qualified Type Names</span></span>](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)
- <span data-ttu-id="1835a-155">[compiler, élément de compilers pour compilation (schéma des paramètres ASP.NET)](https://msdn.microsoft.com/library/f7d6b078-5d42-4134-b3f7-62e1aba1df1e(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1835a-155">[compiler Element for compilers for compilation (ASP.NET Settings Schema)](https://msdn.microsoft.com/library/f7d6b078-5d42-4134-b3f7-62e1aba1df1e(v=vs.100))</span></span>
