---
title: Importation et exportation de schémas
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF, schema import and export
- XsdDataContractExporter class
- XsdDataContractImporter class
ms.assetid: 0da32b50-ccd9-463a-844c-7fe803d3bf44
ms.openlocfilehash: 9f13f9d95c40b964c5eb416c590a5d603d714bac
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61991014"
---
# <a name="schema-import-and-export"></a>Importation et exportation de schémas
Windows Communication Foundation (WCF) inclut un nouveau moteur de sérialisation, le <xref:System.Runtime.Serialization.DataContractSerializer>. Le moteur de sérialisation `DataContractSerializer` traduit des objets [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] en langage XML et inversement. Outre le sérialiseur lui-même, WCF inclut l’importation de schéma associé et d’exporter les schémas afférents. *Schéma* est une description formelle, précise et lisible par machine de la forme du XML que le sérialiseur produit ou que le désérialiseur peut accéder. WCF utilise le langage de définition de World Wide Web Consortium (W3C) XML Schema (XSD) en tant que sa représentation sous forme de schéma, qui est largement interopérable avec nombreuses plateformes tierces.  
  
 L'importateur de schémas, <xref:System.Runtime.Serialization.XsdDataContractImporter>, utilise un document de schéma XSD pour générer des classes [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] (il s'agit en principe de classes de contrat de données) et faire correspondre les formes sérialisées générées au schéma donné.  
  
 Par exemple, le fragment de schéma suivant :  
  
 [!code-csharp[c_SchemaImportExport#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_schemaimportexport/cs/source.cs#8)]
 [!code-vb[c_SchemaImportExport#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_schemaimportexport/vb/source.vb#8)]  
  
 génère le type suivant (légèrement simplifié pour permettre une meilleure compréhension).  
  
 [!code-csharp[c_SchemaImportExport#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_schemaimportexport/cs/source.cs#1)]
 [!code-vb[c_SchemaImportExport#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_schemaimportexport/vb/source.vb#1)]  
  
 Notez que le type généré respecte les bonnes pratiques du contrat de données plusieurs (trouvé dans [meilleures pratiques : Le contrôle de version de contrat de données](../../../../docs/framework/wcf/best-practices-data-contract-versioning.md)) :  
  
- Ce type implémente l'interface <xref:System.Runtime.Serialization.IExtensibleDataObject>. Pour plus d’informations, consultez [Contrats de données compatibles avec des versions ultérieures](../../../../docs/framework/wcf/feature-details/forward-compatible-data-contracts.md).  
  
- Les membres de données sont implémentés sous forme de propriétés publiques qui encapsulent des champs privés.  
  
- La classe est une classe partielle et des éléments peuvent y être ajoutés sans modifier le code généré.  
  
 L'exportateur <xref:System.Runtime.Serialization.XsdDataContractExporter> vous permet d'effectuer l'opération inverse, c'est-à-dire de prendre des types pouvant être sérialisés à l'aide de `DataContractSerializer`, puis de générer un document de schéma XSD.  
  
## <a name="fidelity-is-not-guaranteed"></a>Fidélité non garantie  
 Lors de la conversion, puis reconversion des schémas ou types, la stricte fidélité des informations converties n'est pas garantie. (Un *aller-retour* consiste à importer un schéma pour créer un ensemble de classes et exporter le résultat pour recréer le schéma.) Il se peut que le schéma ainsi recréé ne soit pas exactement identique au schéma d'origine. Effectuer à nouveau le processus dans le sens inverse ne garantit pas en effet la fidélité aux informations d'origine. (Exportez un type pour générer son schéma, puis réimportez le type. Il est improbable que le même type soit retourné.)  
  
## <a name="supported-types"></a>Types pris en charge  
 Le modèle de contrat de données prend uniquement en charge un sous-ensemble limité de schémas WC3. Tout schéma ne se conformant pas à ce sous-ensemble provoquera la levée d'une exception lors de l'importation. Par exemple, il n'est pas possible d'indiquer qu'un membre de données d'un contrat de données doit être sérialisé sous forme d'attribut XML. Les schémas nécessitant l'utilisation d'attributs XML ne sont donc pas pris en charge et provoqueront la levée d'exceptions lors de l'importation, le contrat de données ne pouvant être généré à l'aide des attributs XML appropriés.  
  
 Par exemple, il est impossible d'importer le fragment de schéma suivant à l'aide des paramètres d'importation par défaut.  
  
 [!code-xml[c_SchemaImportExport#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_schemaimportexport/common/source.config#9)]  
  
 Pour plus d’informations, consultez [Data Contract Schema Reference](../../../../docs/framework/wcf/feature-details/data-contract-schema-reference.md). Lorsqu'un schéma ne se conforme pas aux règles des contrats de données, utilisez un autre moteur de sérialisation. Le moteur de sérialisation <xref:System.Xml.Serialization.XmlSerializer> utilise, par exemple, son propre mécanisme d'importation de schéma. De plus, il existe un mode spécial d'importation dans lequel la plage du schéma pris en charge est développée. Pour plus d’informations, consultez la section sur la génération <xref:System.Xml.Serialization.IXmlSerializable> tape [importation du schéma pour générer des Classes](../../../../docs/framework/wcf/feature-details/importing-schema-to-generate-classes.md).  
  
 L'exportateur `XsdDataContractExporter` prend en charge tous les types [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] qui peuvent être sérialisés à l'aide du moteur de sérialisation `DataContractSerializer`. Pour plus d’informations, consultez [Types pris en charge par le sérialiseur de contrat de données](../../../../docs/framework/wcf/feature-details/types-supported-by-the-data-contract-serializer.md). Remarque : le schéma généré à l'aide de `XsdDataContractExporter` contient en principe des données utilisables par l'importateur `XsdDataContractImporter`, sauf si <xref:System.Xml.Serialization.XmlSchemaProviderAttribute> est utilisé afin de personnaliser ce schéma).  
  
 Pour plus d’informations sur l’utilisation de la <xref:System.Runtime.Serialization.XsdDataContractImporter>, consultez [importation du schéma pour générer des Classes](../../../../docs/framework/wcf/feature-details/importing-schema-to-generate-classes.md).  
  
 Pour plus d’informations sur l’utilisation de la <xref:System.Runtime.Serialization.XsdDataContractExporter>, consultez [exportation de schémas à partir de Classes](../../../../docs/framework/wcf/feature-details/exporting-schemas-from-classes.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.Runtime.Serialization.XsdDataContractImporter>
- <xref:System.Runtime.Serialization.XsdDataContractExporter>
- [Importation du schéma pour générer des classes](../../../../docs/framework/wcf/feature-details/importing-schema-to-generate-classes.md)
- [Exportation de schémas à partir de classes](../../../../docs/framework/wcf/feature-details/exporting-schemas-from-classes.md)
