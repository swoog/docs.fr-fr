---
title: Schéma des paramètres d’application
ms.date: 03/30/2017
helpviewer_keywords:
- schema application settings
- application settings, schema [Windows Forms]
- Windows Forms, application settings schema
- configuration schema [.NET Framework], application settings
ms.assetid: 5797fcff-6081-4e8c-bebf-63d9c70cf14b
author: mcleblanc
ms.author: markl
ms.openlocfilehash: f11be59941759687806591feb1edcce28b2119e6
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48844228"
---
# <a name="application-settings-schema"></a><span data-ttu-id="942c0-102">Schéma des paramètres d’application</span><span class="sxs-lookup"><span data-stu-id="942c0-102">Application Settings schema</span></span>

<span data-ttu-id="942c0-103">Paramètres d’application permettent à une application Windows Forms ou ASP.NET stocker et récupérer des paramètres de portée application et de portée utilisateur.</span><span class="sxs-lookup"><span data-stu-id="942c0-103">Application settings allow a Windows Forms or ASP.NET application to store and retrieve application-scoped and user-scoped settings.</span></span> <span data-ttu-id="942c0-104">Dans ce contexte, un *paramètre* est n’importe quel élément d’information qui peut-être être spécifiques à l’application ou spécifiques à l’utilisateur actuel, quoi que ce soit à partir d’une chaîne de connexion de base de données à l’utilisateur préféré par taille de fenêtre par défaut.</span><span class="sxs-lookup"><span data-stu-id="942c0-104">In this context, a *setting* is any piece of information that may be specific to the application or specific to the current user — anything from a database connection string to the user's preferred default window size.</span></span>

<span data-ttu-id="942c0-105">Par défaut, les paramètres d’application dans une application Windows Forms utilise le <xref:System.Configuration.LocalFileSettingsProvider> (classe), qui utilise le système de configuration .NET pour stocker les paramètres dans un fichier de configuration XML.</span><span class="sxs-lookup"><span data-stu-id="942c0-105">By default, application settings in a Windows Forms application uses the <xref:System.Configuration.LocalFileSettingsProvider> class, which uses the .NET configuration system to store settings in an XML configuration file.</span></span> <span data-ttu-id="942c0-106">Pour plus d’informations sur les fichiers utilisés par les paramètres de l’application, consultez [Application Settings Architecture](~/docs/framework/winforms/advanced/application-settings-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="942c0-106">For more information about the files used by application settings, see [Application Settings Architecture](~/docs/framework/winforms/advanced/application-settings-architecture.md).</span></span>

<span data-ttu-id="942c0-107">Paramètres de l’application définit les éléments suivants dans le cadre des fichiers de configuration qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="942c0-107">Application settings defines the following elements as part of the configuration files it uses.</span></span>

| <span data-ttu-id="942c0-108">Élément</span><span class="sxs-lookup"><span data-stu-id="942c0-108">Element</span></span>                    | <span data-ttu-id="942c0-109">Description</span><span class="sxs-lookup"><span data-stu-id="942c0-109">Description</span></span>                                                                           |
| -------------------------- | ------------------------------------------------------------------------------------- |
| <span data-ttu-id="942c0-110">**\<applicationSettings >**</span><span class="sxs-lookup"><span data-stu-id="942c0-110">**\<applicationSettings>**</span></span> | <span data-ttu-id="942c0-111">Contient tous les  **\<paramètre >** balises spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="942c0-111">Contains all **\<setting>** tags specific to the application.</span></span>                         |
| <span data-ttu-id="942c0-112">**\<userSettings >**</span><span class="sxs-lookup"><span data-stu-id="942c0-112">**\<userSettings>**</span></span>        | <span data-ttu-id="942c0-113">Contient tous les  **\<paramètre >** balises spécifiques à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="942c0-113">Contains all **\<setting>** tags specific to the current user.</span></span>                        |
| <span data-ttu-id="942c0-114">**\<définition >**</span><span class="sxs-lookup"><span data-stu-id="942c0-114">**\<setting>**</span></span>             | <span data-ttu-id="942c0-115">Définit un paramètre.</span><span class="sxs-lookup"><span data-stu-id="942c0-115">Defines a setting.</span></span> <span data-ttu-id="942c0-116">Enfant de le  **\<applicationSettings >** ou  **\<userSettings >**.</span><span class="sxs-lookup"><span data-stu-id="942c0-116">Child of either **\<applicationSettings>** or **\<userSettings>**.</span></span> |
| <span data-ttu-id="942c0-117">**\<value>**</span><span class="sxs-lookup"><span data-stu-id="942c0-117">**\<value>**</span></span>               | <span data-ttu-id="942c0-118">Définit une valeur de paramètre.</span><span class="sxs-lookup"><span data-stu-id="942c0-118">Defines a setting's value.</span></span> <span data-ttu-id="942c0-119">Enfant de  **\<paramètre >**.</span><span class="sxs-lookup"><span data-stu-id="942c0-119">Child of **\<setting>**.</span></span>                                   |

## <a name="applicationsettings-element"></a><span data-ttu-id="942c0-120">\<applicationSettings > élément</span><span class="sxs-lookup"><span data-stu-id="942c0-120">\<applicationSettings> element</span></span>

<span data-ttu-id="942c0-121">Cet élément contient tous les  **\<paramètre >** balises qui sont spécifiques à une instance de l’application sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="942c0-121">This element contains all **\<setting>** tags that are specific to an instance of the application on a client computer.</span></span> <span data-ttu-id="942c0-122">Il ne définit aucun attribut.</span><span class="sxs-lookup"><span data-stu-id="942c0-122">It defines no attributes.</span></span>

## <a name="usersettings-element"></a><span data-ttu-id="942c0-123">\<userSettings > élément</span><span class="sxs-lookup"><span data-stu-id="942c0-123">\<userSettings> element</span></span>

<span data-ttu-id="942c0-124">Cet élément contient tous les  **\<paramètre >** balises qui sont spécifiques à l’utilisateur qui utilise actuellement l’application.</span><span class="sxs-lookup"><span data-stu-id="942c0-124">This element contains all **\<setting>** tags that are specific to the user who is currently using the application.</span></span> <span data-ttu-id="942c0-125">Il ne définit aucun attribut.</span><span class="sxs-lookup"><span data-stu-id="942c0-125">It defines no attributes.</span></span>

## <a name="setting-element"></a><span data-ttu-id="942c0-126">\<définition > élément</span><span class="sxs-lookup"><span data-stu-id="942c0-126">\<setting> element</span></span>

<span data-ttu-id="942c0-127">Cet élément définit un paramètre.</span><span class="sxs-lookup"><span data-stu-id="942c0-127">This element defines a setting.</span></span> <span data-ttu-id="942c0-128">Il a les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="942c0-128">It has the following attributes.</span></span>

| <span data-ttu-id="942c0-129">Attribut</span><span class="sxs-lookup"><span data-stu-id="942c0-129">Attribute</span></span>        | <span data-ttu-id="942c0-130">Description</span><span class="sxs-lookup"><span data-stu-id="942c0-130">Description</span></span> |
| ---------------- | ----------- |
| <span data-ttu-id="942c0-131">**name**</span><span class="sxs-lookup"><span data-stu-id="942c0-131">**name**</span></span>         | <span data-ttu-id="942c0-132">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="942c0-132">Required.</span></span> <span data-ttu-id="942c0-133">ID unique du paramètre.</span><span class="sxs-lookup"><span data-stu-id="942c0-133">The unique ID of the setting.</span></span> <span data-ttu-id="942c0-134">Les paramètres créés via Visual Studio sont enregistrés avec le nom `ProjectName.Properties.Settings`.</span><span class="sxs-lookup"><span data-stu-id="942c0-134">Settings created through Visual Studio are saved with the name `ProjectName.Properties.Settings`.</span></span> |
| <span data-ttu-id="942c0-135">**serializedAs**</span><span class="sxs-lookup"><span data-stu-id="942c0-135">**serializedAs**</span></span> | <span data-ttu-id="942c0-136">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="942c0-136">Required.</span></span> <span data-ttu-id="942c0-137">Le format à utiliser pour sérialiser la valeur en texte.</span><span class="sxs-lookup"><span data-stu-id="942c0-137">The format to use for serializing the value to text.</span></span> <span data-ttu-id="942c0-138">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="942c0-138">Valid values are:</span></span><br><br><span data-ttu-id="942c0-139">- `string`.</span><span class="sxs-lookup"><span data-stu-id="942c0-139">- `string`.</span></span> <span data-ttu-id="942c0-140">La valeur est sérialisée comme une chaîne en utilisant un <xref:System.ComponentModel.TypeConverter>.</span><span class="sxs-lookup"><span data-stu-id="942c0-140">The value is serialized as a string using a <xref:System.ComponentModel.TypeConverter>.</span></span><br><span data-ttu-id="942c0-141">- `xml`.</span><span class="sxs-lookup"><span data-stu-id="942c0-141">- `xml`.</span></span> <span data-ttu-id="942c0-142">La valeur est sérialisée à l’aide de la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="942c0-142">The value is serialized using XML serialization.</span></span><br><span data-ttu-id="942c0-143">- `binary`.</span><span class="sxs-lookup"><span data-stu-id="942c0-143">- `binary`.</span></span> <span data-ttu-id="942c0-144">La valeur est sérialisée sous forme binaire texte encodé à l’aide de la sérialisation binaire.</span><span class="sxs-lookup"><span data-stu-id="942c0-144">The value is serialized as text-encoded binary using binary serialization.</span></span><br /><span data-ttu-id="942c0-145">- `custom`.</span><span class="sxs-lookup"><span data-stu-id="942c0-145">- `custom`.</span></span> <span data-ttu-id="942c0-146">Le fournisseur de paramètres a une connaissance inhérente de ce paramètre et sérialise et désérialise il.</span><span class="sxs-lookup"><span data-stu-id="942c0-146">The settings provider has inherent knowledge of this setting and serializes and de-serializes it.</span></span> |

## <a name="value-element"></a><span data-ttu-id="942c0-147">\<valeur > élément</span><span class="sxs-lookup"><span data-stu-id="942c0-147">\<value> element</span></span>

<span data-ttu-id="942c0-148">Cet élément contient la valeur d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="942c0-148">This element contains the value of a setting.</span></span>

## <a name="example"></a><span data-ttu-id="942c0-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="942c0-149">Example</span></span>

<span data-ttu-id="942c0-150">L’exemple suivant montre un fichier de paramètres d’application qui définit deux paramètres de portée application et deux paramètres de portée utilisateur :</span><span class="sxs-lookup"><span data-stu-id="942c0-150">The following example shows an application settings file that defines two application-scoped settings and two user-scoped settings:</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <configSections>
    <sectionGroup name="applicationSettings" type="System.Configuration.ApplicationSettingsGroup, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">
      <section name="WindowsApplication1.Properties.Settings" type="System.Configuration.ClientSettingsSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />
    </sectionGroup>
    <sectionGroup name="userSettings" type="System.Configuration.UserSettingsGroup, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">
      <section name="WindowsApplication1.Properties.Settings" type="System.Configuration.ClientSettingsSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" allowExeDefinition="MachineToLocalUser" />
    </sectionGroup>
  </configSections>
  <applicationSettings>
    <WindowsApplication1.Properties.Settings>
      <setting name="Cursor" serializeAs="String">
        <value>Default</value>
      </setting>
      <setting name="DoubleBuffering" serializeAs="String">
        <value>False</value>
      </setting>
    </WindowsApplication1.Properties.Settings>
  </applicationSettings>
  <userSettings>
    <WindowsApplication1.Properties.Settings>
      <setting name="FormTitle" serializeAs="String">
        <value>Form1</value>
      </setting>
      <setting name="FormSize" serializeAs="String">
        <value>595, 536</value>
      </setting>
    </WindowsApplication1.Properties.Settings>
  </userSettings>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="942c0-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="942c0-151">See also</span></span>

<span data-ttu-id="942c0-152">[Vue d’ensemble des paramètres d’application](~/docs/framework/winforms/advanced/application-settings-overview.md) </span><span class="sxs-lookup"><span data-stu-id="942c0-152">[Application Settings Overview](~/docs/framework/winforms/advanced/application-settings-overview.md) </span></span>  
[<span data-ttu-id="942c0-153">Architecture des paramètres d'application</span><span class="sxs-lookup"><span data-stu-id="942c0-153">Application Settings Architecture</span></span>](~/docs/framework/winforms/advanced/application-settings-architecture.md)
