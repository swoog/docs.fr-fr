---
title: Guide pratique pour utiliser les fonctionnalités de la documentation XML (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- XML documentation [C#]
- C# language, XML documentation features
ms.assetid: 8f33917b-9577-4c9a-818a-640dbbb0b399
ms.openlocfilehash: 6c7e30d23868959145e8941057f1c633fe6e374e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-use-the-xml-documentation-features-c-programming-guide"></a><span data-ttu-id="681a1-102">Guide pratique pour utiliser les fonctionnalités de la documentation XML (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="681a1-102">How to: Use the XML Documentation Features (C# Programming Guide)</span></span>
<span data-ttu-id="681a1-103">L’exemple suivant montre un type qui a été documenté.</span><span class="sxs-lookup"><span data-stu-id="681a1-103">The following sample provides a basic overview of a type that has been documented.</span></span>  
  
## <a name="example"></a><span data-ttu-id="681a1-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="681a1-104">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#15](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/how-to-use-the-xml-documentation-features_1.cs)]  
  
 <span data-ttu-id="681a1-105">**// Ce fichier .xml a été généré avec l’exemple de code précédent.**</span><span class="sxs-lookup"><span data-stu-id="681a1-105">**// This .xml file was generated with the previous code sample.**</span></span>  
<span data-ttu-id="681a1-106">**\<?xml version="1.0"?>**</span><span class="sxs-lookup"><span data-stu-id="681a1-106">**\<?xml version="1.0"?>**</span></span>  
<span data-ttu-id="681a1-107">**\<doc>**</span><span class="sxs-lookup"><span data-stu-id="681a1-107">**\<doc>**</span></span>  
 <span data-ttu-id="681a1-108">**\<assembly>**</span><span class="sxs-lookup"><span data-stu-id="681a1-108">**\<assembly>**</span></span>  
 <span data-ttu-id="681a1-109">**\<name>xmlsample\</name>**</span><span class="sxs-lookup"><span data-stu-id="681a1-109">**\<name>xmlsample\</name>**</span></span>  
 <span data-ttu-id="681a1-110">**\</assembly>**</span><span class="sxs-lookup"><span data-stu-id="681a1-110">**\</assembly>**</span></span>  
 <span data-ttu-id="681a1-111">**\<members>**</span><span class="sxs-lookup"><span data-stu-id="681a1-111">**\<members>**</span></span>  
 <span data-ttu-id="681a1-112">**\<member name="T:SomeClass">**</span><span class="sxs-lookup"><span data-stu-id="681a1-112">**\<member name="T:SomeClass">**</span></span>  
 <span data-ttu-id="681a1-113">**\<summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-113">**\<summary>**</span></span>  
 <span data-ttu-id="681a1-114">**Insérer ici les informations récapitulatives relatives à la classe.\</summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-114">**Class level summary documentation goes here.\</summary>**</span></span>  
 <span data-ttu-id="681a1-115">**\<remarks>**</span><span class="sxs-lookup"><span data-stu-id="681a1-115">**\<remarks>**</span></span>  
 <span data-ttu-id="681a1-116">**Des commentaires plus longs peuvent être associés à un type ou à un membre**</span><span class="sxs-lookup"><span data-stu-id="681a1-116">**Longer comments can be associated with a type or member**</span></span>  
 <span data-ttu-id="681a1-117">**grâce à la balise remarks\</remarks>**</span><span class="sxs-lookup"><span data-stu-id="681a1-117">**through the remarks tag\</remarks>**</span></span>  
 <span data-ttu-id="681a1-118">**\</member>**</span><span class="sxs-lookup"><span data-stu-id="681a1-118">**\</member>**</span></span>  
 <span data-ttu-id="681a1-119">**\<member name="F:SomeClass.m_Name">**</span><span class="sxs-lookup"><span data-stu-id="681a1-119">**\<member name="F:SomeClass.m_Name">**</span></span>  
 <span data-ttu-id="681a1-120">**\<summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-120">**\<summary>**</span></span>  
 <span data-ttu-id="681a1-121">**Stocke la propriété name\</summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-121">**Store for the name property\</summary>**</span></span>  
 <span data-ttu-id="681a1-122">**\</member>**</span><span class="sxs-lookup"><span data-stu-id="681a1-122">**\</member>**</span></span>  
 <span data-ttu-id="681a1-123">**\<member name="M:SomeClass.#ctor">**</span><span class="sxs-lookup"><span data-stu-id="681a1-123">**\<member name="M:SomeClass.#ctor">**</span></span>  
 <span data-ttu-id="681a1-124">**\<summary>Le constructeur de classe.\</summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-124">**\<summary>The class constructor.\</summary>**</span></span>  
 <span data-ttu-id="681a1-125">**\</member>**</span><span class="sxs-lookup"><span data-stu-id="681a1-125">**\</member>**</span></span>  
 <span data-ttu-id="681a1-126">**\<member name="M:SomeClass.SomeMethod(System.String)">**</span><span class="sxs-lookup"><span data-stu-id="681a1-126">**\<member name="M:SomeClass.SomeMethod(System.String)">**</span></span>  
 <span data-ttu-id="681a1-127">**\<summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-127">**\<summary>**</span></span>  
 <span data-ttu-id="681a1-128">**Description de la méthode SomeMethod.\</summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-128">**Description for SomeMethod.\</summary>**</span></span>  
 <span data-ttu-id="681a1-129">**\<param name="s"> Insérer ici la description du paramètre s.\</param>**</span><span class="sxs-lookup"><span data-stu-id="681a1-129">**\<param name="s"> Parameter description for s goes here\</param>**</span></span>  
 <span data-ttu-id="681a1-130">**\<seealso cref="T:System.String">**</span><span class="sxs-lookup"><span data-stu-id="681a1-130">**\<seealso cref="T:System.String">**</span></span>  
 <span data-ttu-id="681a1-131">**Vous pouvez utiliser l’attribut cref sur n’importe quelle étiquette pour référencer un type ou un membre**</span><span class="sxs-lookup"><span data-stu-id="681a1-131">**You can use the cref attribute on any tag to reference a type or member**</span></span>  
 <span data-ttu-id="681a1-132">**et le compilateur vérifiera que cette référence existe. \</seealso>**</span><span class="sxs-lookup"><span data-stu-id="681a1-132">**and the compiler will check that the reference exists. \</seealso>**</span></span>  
 <span data-ttu-id="681a1-133">**\</member>**</span><span class="sxs-lookup"><span data-stu-id="681a1-133">**\</member>**</span></span>  
 <span data-ttu-id="681a1-134">**\<member name="M:SomeClass.SomeOtherMethod">**</span><span class="sxs-lookup"><span data-stu-id="681a1-134">**\<member name="M:SomeClass.SomeOtherMethod">**</span></span>  
 <span data-ttu-id="681a1-135">**\<summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-135">**\<summary>**</span></span>  
 <span data-ttu-id="681a1-136">**Autre méthode quelconque. \</summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-136">**Some other method. \</summary>**</span></span>  
 <span data-ttu-id="681a1-137">**\<returns>**</span><span class="sxs-lookup"><span data-stu-id="681a1-137">**\<returns>**</span></span>  
 <span data-ttu-id="681a1-138">**Les résultats retournés sont décrits grâce à la balise returns.\</returns>**</span><span class="sxs-lookup"><span data-stu-id="681a1-138">**Return results are described through the returns tag.\</returns>**</span></span>  
 <span data-ttu-id="681a1-139">**\<seealso cref="M:SomeClass.SomeMethod(System.String)">**</span><span class="sxs-lookup"><span data-stu-id="681a1-139">**\<seealso cref="M:SomeClass.SomeMethod(System.String)">**</span></span>  
 <span data-ttu-id="681a1-140">**Remarquez l’utilisation de l’attribut cref pour référencer une méthode spécifique \</seealso>**</span><span class="sxs-lookup"><span data-stu-id="681a1-140">**Notice the use of the cref attribute to reference a specific method \</seealso>**</span></span>  
 <span data-ttu-id="681a1-141">**\</member>**</span><span class="sxs-lookup"><span data-stu-id="681a1-141">**\</member>**</span></span>  
 <span data-ttu-id="681a1-142">**\<member name="M:SomeClass.Main(System.String[])">**</span><span class="sxs-lookup"><span data-stu-id="681a1-142">**\<member name="M:SomeClass.Main(System.String[])">**</span></span>  
 <span data-ttu-id="681a1-143">**\<summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-143">**\<summary>**</span></span>  
 <span data-ttu-id="681a1-144">**Point d’entrée de l’application.**</span><span class="sxs-lookup"><span data-stu-id="681a1-144">**The entry point for the application.**</span></span>  
 <span data-ttu-id="681a1-145">**\</summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-145">**\</summary>**</span></span>  
 <span data-ttu-id="681a1-146">**\<param name="args"> Liste d’arguments de la ligne de commande\</param>**</span><span class="sxs-lookup"><span data-stu-id="681a1-146">**\<param name="args"> A list of command line arguments\</param>**</span></span>  
 <span data-ttu-id="681a1-147">**\</member>**</span><span class="sxs-lookup"><span data-stu-id="681a1-147">**\</member>**</span></span>  
 <span data-ttu-id="681a1-148">**\<member name="P:SomeClass.Name">**</span><span class="sxs-lookup"><span data-stu-id="681a1-148">**\<member name="P:SomeClass.Name">**</span></span>  
 <span data-ttu-id="681a1-149">**\<summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-149">**\<summary>**</span></span>  
 <span data-ttu-id="681a1-150">**Propriété Name \</summary>**</span><span class="sxs-lookup"><span data-stu-id="681a1-150">**Name property \</summary>**</span></span>  
 <span data-ttu-id="681a1-151">**\<value>**</span><span class="sxs-lookup"><span data-stu-id="681a1-151">**\<value>**</span></span>  
 <span data-ttu-id="681a1-152">**Une balise value sert à décrire la valeur de la propriété\</value>**</span><span class="sxs-lookup"><span data-stu-id="681a1-152">**A value tag is used to describe the property value\</value>**</span></span>  
 <span data-ttu-id="681a1-153">**\</member>**</span><span class="sxs-lookup"><span data-stu-id="681a1-153">**\</member>**</span></span>  
 <span data-ttu-id="681a1-154">**\</members>**</span><span class="sxs-lookup"><span data-stu-id="681a1-154">**\</members>**</span></span>  
<span data-ttu-id="681a1-155">**\</doc>**</span><span class="sxs-lookup"><span data-stu-id="681a1-155">**\</doc>**</span></span>   
## <a name="compiling-the-code"></a><span data-ttu-id="681a1-156">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="681a1-156">Compiling the Code</span></span>  
 <span data-ttu-id="681a1-157">Pour compiler l’exemple, tapez ce qui suit sur la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="681a1-157">To compile the example, type the following command line:</span></span>  
  
 `csc XMLsample.cs /doc:XMLsample.xml`  
  
 <span data-ttu-id="681a1-158">Cela créera le fichier XML XMLsample.xml, que vous pouvez afficher dans votre navigateur ou à l’aide de la commande TYPE.</span><span class="sxs-lookup"><span data-stu-id="681a1-158">This will create the XML file XMLsample.xml, which you can view in your browser or by using the TYPE command.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="681a1-159">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="681a1-159">Robust Programming</span></span>  
 <span data-ttu-id="681a1-160">Le début de la documentation XML est symbolisé par trois barres obliques (///).</span><span class="sxs-lookup"><span data-stu-id="681a1-160">XML documentation starts with ///.</span></span> <span data-ttu-id="681a1-161">Lorsque vous créez un projet, les Assistants insèrent quelques lignes de début (///) pour vous.</span><span class="sxs-lookup"><span data-stu-id="681a1-161">When you create a new project, the wizards put some starter /// lines in for you.</span></span> <span data-ttu-id="681a1-162">Le traitement de ces commentaires présente certaines restrictions :</span><span class="sxs-lookup"><span data-stu-id="681a1-162">The processing of these comments has some restrictions:</span></span>  
  
-   <span data-ttu-id="681a1-163">La documentation doit être dans un format XML correct.</span><span class="sxs-lookup"><span data-stu-id="681a1-163">The documentation must be well-formed XML.</span></span> <span data-ttu-id="681a1-164">Si le XML n’est pas correct, un avertissement est généré. En outre, un commentaire indiquant qu’une erreur s’est produite est ajouté au fichier de documentation.</span><span class="sxs-lookup"><span data-stu-id="681a1-164">If the XML is not well-formed, a warning is generated and the documentation file will contain a comment that says that an error was encountered.</span></span>  
  
-   <span data-ttu-id="681a1-165">Les développeurs sont libres de créer leur propre jeu de balises.</span><span class="sxs-lookup"><span data-stu-id="681a1-165">Developers are free to create their own set of tags.</span></span> <span data-ttu-id="681a1-166">Il existe un jeu de balises recommandé (voir la section « Informations supplémentaires »).</span><span class="sxs-lookup"><span data-stu-id="681a1-166">There is a recommended set of tags (see the Further Reading section).</span></span> <span data-ttu-id="681a1-167">Certaines des balises recommandées ont des significations spéciales :</span><span class="sxs-lookup"><span data-stu-id="681a1-167">Some of the recommended tags have special meanings:</span></span>  
  
    -   <span data-ttu-id="681a1-168">La balise \<param> est utilisée pour décrire les paramètres.</span><span class="sxs-lookup"><span data-stu-id="681a1-168">The \<param> tag is used to describe parameters.</span></span> <span data-ttu-id="681a1-169">Quand elle est utilisée, le compilateur vérifie que le paramètre existe et que tous les paramètres sont décrits dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="681a1-169">If used, the compiler will verify that the parameter exists and that all parameters are described in the documentation.</span></span> <span data-ttu-id="681a1-170">Si ce n’est pas le cas, le compilateur émet un avertissement.</span><span class="sxs-lookup"><span data-stu-id="681a1-170">If the verification failed, the compiler issues a warning.</span></span>  
  
    -   <span data-ttu-id="681a1-171">L’attribut `cref` peut être joint à n’importe quelle balise pour fournir une référence à un élément de code.</span><span class="sxs-lookup"><span data-stu-id="681a1-171">The `cref` attribute can be attached to any tag to provide a reference to a code element.</span></span> <span data-ttu-id="681a1-172">Le compilateur vérifie l’existence de cet élément de code.</span><span class="sxs-lookup"><span data-stu-id="681a1-172">The compiler will verify that this code element exists.</span></span> <span data-ttu-id="681a1-173">Si ce n’est pas le cas, le compilateur émet un avertissement.</span><span class="sxs-lookup"><span data-stu-id="681a1-173">If the verification failed, the compiler issues a warning.</span></span> <span data-ttu-id="681a1-174">Le compilateur respecte toutes les instructions `using` lorsqu’il recherche un type décrit dans l’attribut `cref`.</span><span class="sxs-lookup"><span data-stu-id="681a1-174">The compiler respects any `using` statements when it looks for a type described in the `cref` attribute.</span></span>  
  
    -   <span data-ttu-id="681a1-175">La balise \<summary> est utilisée par IntelliSense dans Visual Studio pour afficher des informations supplémentaires sur un type ou un membre.</span><span class="sxs-lookup"><span data-stu-id="681a1-175">The \<summary> tag is used by IntelliSense inside Visual Studio to display additional information about a type or member.</span></span>  
  
        > [!NOTE]
        >  <span data-ttu-id="681a1-176">Le fichier XML ne fournit pas des informations complètes sur le type et les membres (par exemple, il ne contient pas d’informations sur le type).</span><span class="sxs-lookup"><span data-stu-id="681a1-176">The XML file does not provide full information about the type and members (for example, it does not contain any type information).</span></span> <span data-ttu-id="681a1-177">Pour obtenir des informations complètes sur un type ou sur un membre, le fichier de documentation doit être utilisé avec la réflexion sur le type ou sur le membre.</span><span class="sxs-lookup"><span data-stu-id="681a1-177">To get full information about a type or member, the documentation file must be used together with reflection on the actual type or member.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="681a1-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="681a1-178">See Also</span></span>  
 [<span data-ttu-id="681a1-179">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="681a1-179">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="681a1-180">/doc (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="681a1-180">/doc (C# Compiler Options)</span></span>](../../../csharp/language-reference/compiler-options/doc-compiler-option.md)  
 [<span data-ttu-id="681a1-181">Commentaires sur la documentation XML</span><span class="sxs-lookup"><span data-stu-id="681a1-181">XML Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/xml-documentation-comments.md)
