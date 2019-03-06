---
title: Collections de schémas ODBC
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: ffe80120ceffbe29c0a117cf1194860c5782be8c
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57365904"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="ce7c8-102">Collections de schémas ODBC</span><span class="sxs-lookup"><span data-stu-id="ce7c8-102">ODBC Schema Collections</span></span>

<span data-ttu-id="ce7c8-103">Cette section traite de la prise en charge des collections de schémas pour les pilotes ODBC Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="ce7c8-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>

## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="ce7c8-104">Pilote Microsoft SQL Server ODBC</span><span class="sxs-lookup"><span data-stu-id="ce7c8-104">Microsoft SQL Server ODBC Driver</span></span>

<span data-ttu-id="ce7c8-105">Le pilote ODBC de Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="ce7c8-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>

- <span data-ttu-id="ce7c8-106">Tables</span><span class="sxs-lookup"><span data-stu-id="ce7c8-106">Tables</span></span>

- <span data-ttu-id="ce7c8-107">Index</span><span class="sxs-lookup"><span data-stu-id="ce7c8-107">Indexes</span></span>

- <span data-ttu-id="ce7c8-108">Columns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-108">Columns</span></span>

- <span data-ttu-id="ce7c8-109">Procédures</span><span class="sxs-lookup"><span data-stu-id="ce7c8-109">Procedures</span></span>

- <span data-ttu-id="ce7c8-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-110">ProcedureColumns</span></span>

- <span data-ttu-id="ce7c8-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="ce7c8-111">ProcedureParameters</span></span>

- <span data-ttu-id="ce7c8-112">Vues</span><span class="sxs-lookup"><span data-stu-id="ce7c8-112">Views</span></span>

### <a name="tables-and-views"></a><span data-ttu-id="ce7c8-113">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="ce7c8-113">Tables and Views</span></span>

|<span data-ttu-id="ce7c8-114">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-114">ColumnName</span></span>|<span data-ttu-id="ce7c8-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-115">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="ce7c8-116">TABLE_CAT</span></span>|<span data-ttu-id="ce7c8-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-117">String</span></span>|
|<span data-ttu-id="ce7c8-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ce7c8-118">TABLE_SCHEM</span></span>|<span data-ttu-id="ce7c8-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-119">String</span></span>|
|<span data-ttu-id="ce7c8-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-120">TABLE_NAME</span></span>|<span data-ttu-id="ce7c8-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-121">String</span></span>|
|<span data-ttu-id="ce7c8-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-122">TABLE_TYPE</span></span>|<span data-ttu-id="ce7c8-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-123">String</span></span>|
|<span data-ttu-id="ce7c8-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-124">REMARKS</span></span>|<span data-ttu-id="ce7c8-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-125">String</span></span>|

### <a name="indexes"></a><span data-ttu-id="ce7c8-126">Index</span><span class="sxs-lookup"><span data-stu-id="ce7c8-126">Indexes</span></span>

|<span data-ttu-id="ce7c8-127">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-127">ColumnName</span></span>|<span data-ttu-id="ce7c8-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-128">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="ce7c8-129">TABLE_CAT</span></span>|<span data-ttu-id="ce7c8-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-130">String</span></span>|
|<span data-ttu-id="ce7c8-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ce7c8-131">TABLE_SCHEM</span></span>|<span data-ttu-id="ce7c8-132">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-132">String</span></span>|
|<span data-ttu-id="ce7c8-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-133">TABLE_NAME</span></span>|<span data-ttu-id="ce7c8-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-134">String</span></span>|
|<span data-ttu-id="ce7c8-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-135">NON_UNIQUE</span></span>|<span data-ttu-id="ce7c8-136">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-136">Int16</span></span>|
|<span data-ttu-id="ce7c8-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="ce7c8-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-138">String</span></span>|
|<span data-ttu-id="ce7c8-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-139">INDEX_NAME</span></span>|<span data-ttu-id="ce7c8-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-140">String</span></span>|
|<span data-ttu-id="ce7c8-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-141">TYPE</span></span>|<span data-ttu-id="ce7c8-142">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-142">Int16</span></span>|
|<span data-ttu-id="ce7c8-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="ce7c8-144">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-144">Int16</span></span>|
|<span data-ttu-id="ce7c8-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-145">COLUMN_NAME</span></span>|<span data-ttu-id="ce7c8-146">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-146">String</span></span>|
|<span data-ttu-id="ce7c8-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="ce7c8-147">ASC_OR_DESC</span></span>|<span data-ttu-id="ce7c8-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-148">String</span></span>|
|<span data-ttu-id="ce7c8-149">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="ce7c8-149">CARDINALITY</span></span>|<span data-ttu-id="ce7c8-150">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-150">Int32</span></span>|
|<span data-ttu-id="ce7c8-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="ce7c8-151">PAGES</span></span>|<span data-ttu-id="ce7c8-152">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-152">Int32</span></span>|
|<span data-ttu-id="ce7c8-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-153">FILTER_CONDITION</span></span>|<span data-ttu-id="ce7c8-154">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-154">String</span></span>|
|<span data-ttu-id="ce7c8-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ce7c8-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="ce7c8-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-156">String</span></span>|
|<span data-ttu-id="ce7c8-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-158">Byte</span><span class="sxs-lookup"><span data-stu-id="ce7c8-158">Byte</span></span>|

### <a name="columns"></a><span data-ttu-id="ce7c8-159">Columns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-159">Columns</span></span>

|<span data-ttu-id="ce7c8-160">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-160">ColumnName</span></span>|<span data-ttu-id="ce7c8-161">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-161">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="ce7c8-162">TABLE_CAT</span></span>|<span data-ttu-id="ce7c8-163">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-163">String</span></span>|
|<span data-ttu-id="ce7c8-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ce7c8-164">TABLE_SCHEM</span></span>|<span data-ttu-id="ce7c8-165">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-165">String</span></span>|
|<span data-ttu-id="ce7c8-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-166">TABLE_NAME</span></span>|<span data-ttu-id="ce7c8-167">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-167">String</span></span>|
|<span data-ttu-id="ce7c8-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-168">COLUMN_NAME</span></span>|<span data-ttu-id="ce7c8-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-169">String</span></span>|
|<span data-ttu-id="ce7c8-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-170">DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-171">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-171">Int16</span></span>|
|<span data-ttu-id="ce7c8-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-172">TYPE_NAME</span></span>|<span data-ttu-id="ce7c8-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-173">String</span></span>|
|<span data-ttu-id="ce7c8-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-174">COLUMN_SIZE</span></span>|<span data-ttu-id="ce7c8-175">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-175">Int32</span></span>|
|<span data-ttu-id="ce7c8-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="ce7c8-177">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-177">Int32</span></span>|
|<span data-ttu-id="ce7c8-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="ce7c8-179">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-179">Int16</span></span>|
|<span data-ttu-id="ce7c8-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="ce7c8-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="ce7c8-181">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-181">Int16</span></span>|
|<span data-ttu-id="ce7c8-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-182">NULLABLE</span></span>|<span data-ttu-id="ce7c8-183">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-183">Int16</span></span>|
|<span data-ttu-id="ce7c8-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-184">REMARKS</span></span>|<span data-ttu-id="ce7c8-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-185">String</span></span>|
|<span data-ttu-id="ce7c8-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="ce7c8-186">COLUMN_DEF</span></span>|<span data-ttu-id="ce7c8-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-187">String</span></span>|
|<span data-ttu-id="ce7c8-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-189">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-189">Int16</span></span>|
|<span data-ttu-id="ce7c8-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="ce7c8-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="ce7c8-191">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-191">Int16</span></span>|
|<span data-ttu-id="ce7c8-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="ce7c8-193">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-193">Int32</span></span>|
|<span data-ttu-id="ce7c8-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="ce7c8-195">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-195">Int32</span></span>|
|<span data-ttu-id="ce7c8-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-196">IS_NULLABLE</span></span>|<span data-ttu-id="ce7c8-197">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-197">String</span></span>|
|<span data-ttu-id="ce7c8-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ce7c8-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="ce7c8-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-199">String</span></span>|
|<span data-ttu-id="ce7c8-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ce7c8-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="ce7c8-201">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-201">String</span></span>|
|<span data-ttu-id="ce7c8-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-203">Byte</span><span class="sxs-lookup"><span data-stu-id="ce7c8-203">Byte</span></span>|

### <a name="procedures"></a><span data-ttu-id="ce7c8-204">Procédures</span><span class="sxs-lookup"><span data-stu-id="ce7c8-204">Procedures</span></span>

|<span data-ttu-id="ce7c8-205">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-205">ColumnName</span></span>|<span data-ttu-id="ce7c8-206">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-206">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="ce7c8-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="ce7c8-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-208">String</span></span>|
|<span data-ttu-id="ce7c8-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ce7c8-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="ce7c8-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-210">String</span></span>|
|<span data-ttu-id="ce7c8-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="ce7c8-212">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-212">String</span></span>|
|<span data-ttu-id="ce7c8-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="ce7c8-214">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-214">Int32</span></span>|
|<span data-ttu-id="ce7c8-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="ce7c8-216">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-216">Int32</span></span>|
|<span data-ttu-id="ce7c8-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="ce7c8-218">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-218">Int32</span></span>|
|<span data-ttu-id="ce7c8-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-219">REMARKS</span></span>|<span data-ttu-id="ce7c8-220">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-220">String</span></span>|
|<span data-ttu-id="ce7c8-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="ce7c8-222">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-222">Int16</span></span>|

### <a name="procedurecolumns"></a><span data-ttu-id="ce7c8-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-223">ProcedureColumns</span></span>

|<span data-ttu-id="ce7c8-224">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-224">ColumnName</span></span>|<span data-ttu-id="ce7c8-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-225">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="ce7c8-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="ce7c8-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-227">String</span></span>|
|<span data-ttu-id="ce7c8-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ce7c8-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="ce7c8-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-229">String</span></span>|
|<span data-ttu-id="ce7c8-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="ce7c8-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-231">String</span></span>|
|<span data-ttu-id="ce7c8-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-232">COLUMN_NAME</span></span>|<span data-ttu-id="ce7c8-233">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-233">String</span></span>|
|<span data-ttu-id="ce7c8-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-234">COLUMN_TYPE</span></span>|<span data-ttu-id="ce7c8-235">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-235">Int16</span></span>|
|<span data-ttu-id="ce7c8-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-236">DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-237">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-237">Int16</span></span>|
|<span data-ttu-id="ce7c8-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-238">TYPE_NAME</span></span>|<span data-ttu-id="ce7c8-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-239">String</span></span>|
|<span data-ttu-id="ce7c8-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-240">COLUMN_SIZE</span></span>|<span data-ttu-id="ce7c8-241">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-241">Int32</span></span>|
|<span data-ttu-id="ce7c8-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="ce7c8-243">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-243">Int32</span></span>|
|<span data-ttu-id="ce7c8-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="ce7c8-245">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-245">Int16</span></span>|
|<span data-ttu-id="ce7c8-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="ce7c8-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="ce7c8-247">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-247">Int16</span></span>|
|<span data-ttu-id="ce7c8-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-248">NULLABLE</span></span>|<span data-ttu-id="ce7c8-249">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-249">Int16</span></span>|
|<span data-ttu-id="ce7c8-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-250">REMARKS</span></span>|<span data-ttu-id="ce7c8-251">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-251">String</span></span>|
|<span data-ttu-id="ce7c8-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="ce7c8-252">COLUMN_DEF</span></span>|<span data-ttu-id="ce7c8-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-253">String</span></span>|
|<span data-ttu-id="ce7c8-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-255">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-255">Int16</span></span>|
|<span data-ttu-id="ce7c8-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="ce7c8-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="ce7c8-257">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-257">Int16</span></span>|
|<span data-ttu-id="ce7c8-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="ce7c8-259">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-259">Int32</span></span>|
|<span data-ttu-id="ce7c8-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="ce7c8-261">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-261">Int32</span></span>|
|<span data-ttu-id="ce7c8-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-262">IS_NULLABLE</span></span>|<span data-ttu-id="ce7c8-263">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-263">String</span></span>|
|<span data-ttu-id="ce7c8-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ce7c8-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="ce7c8-265">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-265">String</span></span>|
|<span data-ttu-id="ce7c8-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ce7c8-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="ce7c8-267">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-267">String</span></span>|
|<span data-ttu-id="ce7c8-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-269">Byte</span><span class="sxs-lookup"><span data-stu-id="ce7c8-269">Byte</span></span>|

### <a name="procedureparameters"></a><span data-ttu-id="ce7c8-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="ce7c8-270">ProcedureParameters</span></span>

|<span data-ttu-id="ce7c8-271">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-271">ColumnName</span></span>|<span data-ttu-id="ce7c8-272">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-272">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="ce7c8-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="ce7c8-274">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-274">String</span></span>|
|<span data-ttu-id="ce7c8-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ce7c8-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="ce7c8-276">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-276">String</span></span>|
|<span data-ttu-id="ce7c8-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="ce7c8-278">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-278">String</span></span>|
|<span data-ttu-id="ce7c8-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-279">COLUMN_NAME</span></span>|<span data-ttu-id="ce7c8-280">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-280">String</span></span>|
|<span data-ttu-id="ce7c8-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-281">COLUMN_TYPE</span></span>|<span data-ttu-id="ce7c8-282">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-282">Int16</span></span>|
|<span data-ttu-id="ce7c8-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-283">DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-284">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-284">Int16</span></span>|
|<span data-ttu-id="ce7c8-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-285">TYPE_NAME</span></span>|<span data-ttu-id="ce7c8-286">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-286">String</span></span>|
|<span data-ttu-id="ce7c8-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-287">COLUMN_SIZE</span></span>|<span data-ttu-id="ce7c8-288">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-288">Int32</span></span>|
|<span data-ttu-id="ce7c8-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="ce7c8-290">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-290">Int32</span></span>|
|<span data-ttu-id="ce7c8-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="ce7c8-292">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-292">Int16</span></span>|
|<span data-ttu-id="ce7c8-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="ce7c8-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="ce7c8-294">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-294">Int16</span></span>|
|<span data-ttu-id="ce7c8-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-295">NULLABLE</span></span>|<span data-ttu-id="ce7c8-296">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-296">Int16</span></span>|
|<span data-ttu-id="ce7c8-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-297">REMARKS</span></span>|<span data-ttu-id="ce7c8-298">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-298">String</span></span>|
|<span data-ttu-id="ce7c8-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="ce7c8-299">COLUMN_DEF</span></span>|<span data-ttu-id="ce7c8-300">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-300">String</span></span>|
|<span data-ttu-id="ce7c8-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-302">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-302">Int16</span></span>|
|<span data-ttu-id="ce7c8-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="ce7c8-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="ce7c8-304">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-304">Int16</span></span>|
|<span data-ttu-id="ce7c8-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="ce7c8-306">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-306">Int32</span></span>|
|<span data-ttu-id="ce7c8-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="ce7c8-308">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-308">Int32</span></span>|
|<span data-ttu-id="ce7c8-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-309">IS_NULLABLE</span></span>|<span data-ttu-id="ce7c8-310">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-310">String</span></span>|
|<span data-ttu-id="ce7c8-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ce7c8-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="ce7c8-312">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-312">String</span></span>|
|<span data-ttu-id="ce7c8-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ce7c8-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="ce7c8-314">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-314">String</span></span>|
|<span data-ttu-id="ce7c8-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-316">Byte</span><span class="sxs-lookup"><span data-stu-id="ce7c8-316">Byte</span></span>|

## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="ce7c8-317">Pilote Microsoft Oracle ODBC</span><span class="sxs-lookup"><span data-stu-id="ce7c8-317">Microsoft Oracle ODBC Driver</span></span>

<span data-ttu-id="ce7c8-318">Le pilote Microsoft SQL Server Oracle ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="ce7c8-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>

- <span data-ttu-id="ce7c8-319">Tables</span><span class="sxs-lookup"><span data-stu-id="ce7c8-319">Tables</span></span>

- <span data-ttu-id="ce7c8-320">Columns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-320">Columns</span></span>

- <span data-ttu-id="ce7c8-321">Procédures</span><span class="sxs-lookup"><span data-stu-id="ce7c8-321">Procedures</span></span>

- <span data-ttu-id="ce7c8-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-322">ProcedureColumns</span></span>

- <span data-ttu-id="ce7c8-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="ce7c8-323">ProcedureParameters</span></span>

- <span data-ttu-id="ce7c8-324">Vues</span><span class="sxs-lookup"><span data-stu-id="ce7c8-324">Views</span></span>

- <span data-ttu-id="ce7c8-325">Index</span><span class="sxs-lookup"><span data-stu-id="ce7c8-325">Indexes</span></span>

### <a name="tables-and-views"></a><span data-ttu-id="ce7c8-326">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="ce7c8-326">Tables and Views</span></span>

|<span data-ttu-id="ce7c8-327">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-327">ColumnName</span></span>|<span data-ttu-id="ce7c8-328">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-328">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="ce7c8-330">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-330">String</span></span>|
|<span data-ttu-id="ce7c8-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-331">TABLE_OWNER</span></span>|<span data-ttu-id="ce7c8-332">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-332">String</span></span>|
|<span data-ttu-id="ce7c8-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-333">TABLE_NAME</span></span>|<span data-ttu-id="ce7c8-334">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-334">String</span></span>|
|<span data-ttu-id="ce7c8-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-335">TABLE_TYPE</span></span>|<span data-ttu-id="ce7c8-336">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-336">String</span></span>|
|<span data-ttu-id="ce7c8-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-337">REMARKS</span></span>|<span data-ttu-id="ce7c8-338">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-338">String</span></span>|

### <a name="columns"></a><span data-ttu-id="ce7c8-339">Columns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-339">Columns</span></span>

|<span data-ttu-id="ce7c8-340">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-340">ColumnName</span></span>|<span data-ttu-id="ce7c8-341">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-341">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="ce7c8-343">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-343">String</span></span>|
|<span data-ttu-id="ce7c8-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-344">TABLE_OWNER</span></span>|<span data-ttu-id="ce7c8-345">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-345">String</span></span>|
|<span data-ttu-id="ce7c8-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-346">TABLE_NAME</span></span>|<span data-ttu-id="ce7c8-347">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-347">String</span></span>|
|<span data-ttu-id="ce7c8-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-348">COLUMN_NAME</span></span>|<span data-ttu-id="ce7c8-349">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-349">String</span></span>|
|<span data-ttu-id="ce7c8-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-350">DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-351">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-351">Int16</span></span>|
|<span data-ttu-id="ce7c8-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-352">TYPE_NAME</span></span>|<span data-ttu-id="ce7c8-353">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-353">String</span></span>|
|<span data-ttu-id="ce7c8-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-354">PRECISION</span></span>|<span data-ttu-id="ce7c8-355">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-355">Int32</span></span>|
|<span data-ttu-id="ce7c8-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-356">LENGTH</span></span>|<span data-ttu-id="ce7c8-357">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-357">Int32</span></span>|
|<span data-ttu-id="ce7c8-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-358">SCALE</span></span>|<span data-ttu-id="ce7c8-359">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-359">Int16</span></span>|
|<span data-ttu-id="ce7c8-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="ce7c8-360">RADIX</span></span>|<span data-ttu-id="ce7c8-361">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-361">Int16</span></span>|
|<span data-ttu-id="ce7c8-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-362">NULLABLE</span></span>|<span data-ttu-id="ce7c8-363">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-363">Int16</span></span>|
|<span data-ttu-id="ce7c8-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-364">REMARKS</span></span>|<span data-ttu-id="ce7c8-365">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-365">String</span></span>|
|<span data-ttu-id="ce7c8-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="ce7c8-367">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-367">Int32</span></span>|

### <a name="procedures"></a><span data-ttu-id="ce7c8-368">Procédures</span><span class="sxs-lookup"><span data-stu-id="ce7c8-368">Procedures</span></span>

|<span data-ttu-id="ce7c8-369">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-369">ColumnName</span></span>|<span data-ttu-id="ce7c8-370">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-370">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="ce7c8-372">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-372">String</span></span>|
|<span data-ttu-id="ce7c8-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="ce7c8-374">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-374">String</span></span>|
|<span data-ttu-id="ce7c8-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="ce7c8-376">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-376">String</span></span>|
|<span data-ttu-id="ce7c8-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="ce7c8-378">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-378">Int16</span></span>|
|<span data-ttu-id="ce7c8-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="ce7c8-380">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-380">Int16</span></span>|
|<span data-ttu-id="ce7c8-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="ce7c8-382">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-382">Int16</span></span>|
|<span data-ttu-id="ce7c8-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-383">REMARKS</span></span>|<span data-ttu-id="ce7c8-384">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-384">String</span></span>|
|<span data-ttu-id="ce7c8-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="ce7c8-386">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-386">Int16</span></span>|

### <a name="procedurecolumns"></a><span data-ttu-id="ce7c8-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-387">ProcedureColumns</span></span>

|<span data-ttu-id="ce7c8-388">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-388">ColumnName</span></span>|<span data-ttu-id="ce7c8-389">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-389">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="ce7c8-391">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-391">String</span></span>|
|<span data-ttu-id="ce7c8-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="ce7c8-393">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-393">String</span></span>|
|<span data-ttu-id="ce7c8-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="ce7c8-395">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-395">String</span></span>|
|<span data-ttu-id="ce7c8-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-396">COLUMN_NAME</span></span>|<span data-ttu-id="ce7c8-397">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-397">String</span></span>|
|<span data-ttu-id="ce7c8-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-398">COLUMN_TYPE</span></span>|<span data-ttu-id="ce7c8-399">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-399">Int16</span></span>|
|<span data-ttu-id="ce7c8-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-400">DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-401">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-401">Int16</span></span>|
|<span data-ttu-id="ce7c8-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-402">TYPE_NAME</span></span>|<span data-ttu-id="ce7c8-403">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-403">String</span></span>|
|<span data-ttu-id="ce7c8-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-404">PRECISION</span></span>|<span data-ttu-id="ce7c8-405">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-405">Int32</span></span>|
|<span data-ttu-id="ce7c8-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-406">LENGTH</span></span>|<span data-ttu-id="ce7c8-407">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-407">Int32</span></span>|
|<span data-ttu-id="ce7c8-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-408">SCALE</span></span>|<span data-ttu-id="ce7c8-409">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-409">Int16</span></span>|
|<span data-ttu-id="ce7c8-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="ce7c8-410">RADIX</span></span>|<span data-ttu-id="ce7c8-411">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-411">Int16</span></span>|
|<span data-ttu-id="ce7c8-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-412">NULLABLE</span></span>|<span data-ttu-id="ce7c8-413">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-413">Int16</span></span>|
|<span data-ttu-id="ce7c8-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-414">REMARKS</span></span>|<span data-ttu-id="ce7c8-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-415">String</span></span>|
|<span data-ttu-id="ce7c8-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="ce7c8-416">OVERLOAD</span></span>|<span data-ttu-id="ce7c8-417">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-417">Int32</span></span>|
|<span data-ttu-id="ce7c8-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="ce7c8-419">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-419">Int32</span></span>|

## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="ce7c8-420">Pilote Microsoft Jet ODBC</span><span class="sxs-lookup"><span data-stu-id="ce7c8-420">Microsoft Jet ODBC Driver</span></span>

<span data-ttu-id="ce7c8-421">Le pilote Microsoft Jet ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="ce7c8-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>

- <span data-ttu-id="ce7c8-422">Tables</span><span class="sxs-lookup"><span data-stu-id="ce7c8-422">Tables</span></span>

- <span data-ttu-id="ce7c8-423">Index</span><span class="sxs-lookup"><span data-stu-id="ce7c8-423">Indexes</span></span>

- <span data-ttu-id="ce7c8-424">Columns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-424">Columns</span></span>

- <span data-ttu-id="ce7c8-425">Procédures</span><span class="sxs-lookup"><span data-stu-id="ce7c8-425">Procedures</span></span>

- <span data-ttu-id="ce7c8-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-426">ProcedureColumns</span></span>

- <span data-ttu-id="ce7c8-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="ce7c8-427">ProcedureParameters</span></span>

- <span data-ttu-id="ce7c8-428">Vues</span><span class="sxs-lookup"><span data-stu-id="ce7c8-428">Views</span></span>

### <a name="tables-and-views"></a><span data-ttu-id="ce7c8-429">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="ce7c8-429">Tables and Views</span></span>

|<span data-ttu-id="ce7c8-430">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-430">ColumnName</span></span>|<span data-ttu-id="ce7c8-431">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-431">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="ce7c8-433">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-433">String</span></span>|
|<span data-ttu-id="ce7c8-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-434">TABLE_OWNER</span></span>|<span data-ttu-id="ce7c8-435">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-435">String</span></span>|
|<span data-ttu-id="ce7c8-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-436">TABLE_NAME</span></span>|<span data-ttu-id="ce7c8-437">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-437">String</span></span>|
|<span data-ttu-id="ce7c8-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-438">TABLE_TYPE</span></span>|<span data-ttu-id="ce7c8-439">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-439">String</span></span>|
|<span data-ttu-id="ce7c8-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-440">REMARKS</span></span>|<span data-ttu-id="ce7c8-441">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-441">String</span></span>|

### <a name="columns"></a><span data-ttu-id="ce7c8-442">Columns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-442">Columns</span></span>

|<span data-ttu-id="ce7c8-443">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-443">ColumnName</span></span>|<span data-ttu-id="ce7c8-444">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-444">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="ce7c8-446">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-446">String</span></span>|
|<span data-ttu-id="ce7c8-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-447">TABLE_OWNER</span></span>|<span data-ttu-id="ce7c8-448">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-448">String</span></span>|
|<span data-ttu-id="ce7c8-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-449">TABLE_NAME</span></span>|<span data-ttu-id="ce7c8-450">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-450">String</span></span>|
|<span data-ttu-id="ce7c8-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-451">COLUMN_NAME</span></span>|<span data-ttu-id="ce7c8-452">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-452">String</span></span>|
|<span data-ttu-id="ce7c8-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-453">DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-454">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-454">Int16</span></span>|
|<span data-ttu-id="ce7c8-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-455">TYPE_NAME</span></span>|<span data-ttu-id="ce7c8-456">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-456">String</span></span>|
|<span data-ttu-id="ce7c8-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-457">PRECISION</span></span>|<span data-ttu-id="ce7c8-458">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-458">Int32</span></span>|
|<span data-ttu-id="ce7c8-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-459">LENGTH</span></span>|<span data-ttu-id="ce7c8-460">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-460">Int32</span></span>|
|<span data-ttu-id="ce7c8-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-461">SCALE</span></span>|<span data-ttu-id="ce7c8-462">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-462">Int16</span></span>|
|<span data-ttu-id="ce7c8-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="ce7c8-463">RADIX</span></span>|<span data-ttu-id="ce7c8-464">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-464">Int16</span></span>|
|<span data-ttu-id="ce7c8-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-465">NULLABLE</span></span>|<span data-ttu-id="ce7c8-466">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-466">Int16</span></span>|
|<span data-ttu-id="ce7c8-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-467">REMARKS</span></span>|<span data-ttu-id="ce7c8-468">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-468">String</span></span>|
|<span data-ttu-id="ce7c8-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="ce7c8-470">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-470">Int32</span></span>|

### <a name="procedures"></a><span data-ttu-id="ce7c8-471">Procédures</span><span class="sxs-lookup"><span data-stu-id="ce7c8-471">Procedures</span></span>

|<span data-ttu-id="ce7c8-472">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-472">ColumnName</span></span>|<span data-ttu-id="ce7c8-473">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-473">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="ce7c8-475">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-475">String</span></span>|
|<span data-ttu-id="ce7c8-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="ce7c8-477">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-477">String</span></span>|
|<span data-ttu-id="ce7c8-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="ce7c8-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-479">String</span></span>|
|<span data-ttu-id="ce7c8-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="ce7c8-481">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-481">Int16</span></span>|
|<span data-ttu-id="ce7c8-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="ce7c8-483">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-483">Int16</span></span>|
|<span data-ttu-id="ce7c8-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="ce7c8-485">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-485">Int16</span></span>|
|<span data-ttu-id="ce7c8-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-486">REMARKS</span></span>|<span data-ttu-id="ce7c8-487">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-487">String</span></span>|
|<span data-ttu-id="ce7c8-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="ce7c8-489">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-489">Int16</span></span>|

### <a name="procedurecolumns"></a><span data-ttu-id="ce7c8-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="ce7c8-490">ProcedureColumns</span></span>

|<span data-ttu-id="ce7c8-491">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-491">ColumnName</span></span>|<span data-ttu-id="ce7c8-492">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-492">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="ce7c8-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-494">String</span></span>|
|<span data-ttu-id="ce7c8-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="ce7c8-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="ce7c8-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-496">String</span></span>|
|<span data-ttu-id="ce7c8-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="ce7c8-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-498">String</span></span>|
|<span data-ttu-id="ce7c8-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-499">COLUMN_NAME</span></span>|<span data-ttu-id="ce7c8-500">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-500">String</span></span>|
|<span data-ttu-id="ce7c8-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-501">COLUMN_TYPE</span></span>|<span data-ttu-id="ce7c8-502">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-502">Int16</span></span>|
|<span data-ttu-id="ce7c8-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-503">DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-504">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-504">Int16</span></span>|
|<span data-ttu-id="ce7c8-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-505">TYPE_NAME</span></span>|<span data-ttu-id="ce7c8-506">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-506">String</span></span>|
|<span data-ttu-id="ce7c8-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-507">PRECISION</span></span>|<span data-ttu-id="ce7c8-508">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-508">Int32</span></span>|
|<span data-ttu-id="ce7c8-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-509">LENGTH</span></span>|<span data-ttu-id="ce7c8-510">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-510">Int32</span></span>|
|<span data-ttu-id="ce7c8-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-511">SCALE</span></span>|<span data-ttu-id="ce7c8-512">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-512">Int16</span></span>|
|<span data-ttu-id="ce7c8-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="ce7c8-513">RADIX</span></span>|<span data-ttu-id="ce7c8-514">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-514">Int16</span></span>|
|<span data-ttu-id="ce7c8-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-515">NULLABLE</span></span>|<span data-ttu-id="ce7c8-516">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-516">Int16</span></span>|
|<span data-ttu-id="ce7c8-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-517">REMARKS</span></span>|<span data-ttu-id="ce7c8-518">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-518">String</span></span>|
|<span data-ttu-id="ce7c8-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="ce7c8-519">OVERLOAD</span></span>|<span data-ttu-id="ce7c8-520">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-520">Int32</span></span>|
|<span data-ttu-id="ce7c8-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="ce7c8-522">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-522">Int32</span></span>|

### <a name="procedureparameters"></a><span data-ttu-id="ce7c8-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="ce7c8-523">ProcedureParameters</span></span>

|<span data-ttu-id="ce7c8-524">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-524">ColumnName</span></span>|<span data-ttu-id="ce7c8-525">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce7c8-525">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="ce7c8-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="ce7c8-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="ce7c8-527">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-527">String</span></span>|
|<span data-ttu-id="ce7c8-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="ce7c8-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="ce7c8-529">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-529">String</span></span>|
|<span data-ttu-id="ce7c8-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="ce7c8-531">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-531">String</span></span>|
|<span data-ttu-id="ce7c8-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-532">COLUMN_NAME</span></span>|<span data-ttu-id="ce7c8-533">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-533">String</span></span>|
|<span data-ttu-id="ce7c8-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-534">COLUMN_TYPE</span></span>|<span data-ttu-id="ce7c8-535">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-535">Int16</span></span>|
|<span data-ttu-id="ce7c8-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-536">DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-537">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-537">Int16</span></span>|
|<span data-ttu-id="ce7c8-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="ce7c8-538">TYPE_NAME</span></span>|<span data-ttu-id="ce7c8-539">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-539">String</span></span>|
|<span data-ttu-id="ce7c8-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-540">COLUMN_SIZE</span></span>|<span data-ttu-id="ce7c8-541">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-541">Int32</span></span>|
|<span data-ttu-id="ce7c8-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="ce7c8-543">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-543">Int32</span></span>|
|<span data-ttu-id="ce7c8-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="ce7c8-545">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-545">Int16</span></span>|
|<span data-ttu-id="ce7c8-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="ce7c8-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="ce7c8-547">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-547">Int16</span></span>|
|<span data-ttu-id="ce7c8-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-548">NULLABLE</span></span>|<span data-ttu-id="ce7c8-549">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-549">Int16</span></span>|
|<span data-ttu-id="ce7c8-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="ce7c8-550">REMARKS</span></span>|<span data-ttu-id="ce7c8-551">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-551">String</span></span>|
|<span data-ttu-id="ce7c8-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="ce7c8-552">COLUMN_DEF</span></span>|<span data-ttu-id="ce7c8-553">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-553">String</span></span>|
|<span data-ttu-id="ce7c8-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="ce7c8-555">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-555">Int16</span></span>|
|<span data-ttu-id="ce7c8-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="ce7c8-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="ce7c8-557">Int16</span><span class="sxs-lookup"><span data-stu-id="ce7c8-557">Int16</span></span>|
|<span data-ttu-id="ce7c8-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ce7c8-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="ce7c8-559">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-559">Int32</span></span>|
|<span data-ttu-id="ce7c8-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="ce7c8-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="ce7c8-561">Int32</span><span class="sxs-lookup"><span data-stu-id="ce7c8-561">Int32</span></span>|
|<span data-ttu-id="ce7c8-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="ce7c8-562">IS_NULLABLE</span></span>|<span data-ttu-id="ce7c8-563">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ce7c8-563">String</span></span>|

## <a name="see-also"></a><span data-ttu-id="ce7c8-564">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce7c8-564">See also</span></span>

- [<span data-ttu-id="ce7c8-565">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="ce7c8-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
