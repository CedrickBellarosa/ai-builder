---
title: Requirements and limitations -  AI Builder | Microsoft Docs
description: Describes the requirements and limitations of form processing models in AI Builder.
author: JoeFernandezMS
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/31/2019
ms.author: jofernan
ms.reviewer: v-dehaas
---

# Form processing AI model requirements and limitations


> [!NOTE]
> Make sure your administrator has assigned you a security role with all organization privileges over the entity **Note** from **Core Records**.

## Requirements

Form processing works on input documents that meet the following requirements:

- JPG, PNG, or PDF format (text or scanned). Text-embedded PDFs are better, because there won't be any errors in character extraction and location.
- The combined file size of the documents used for training must not exceed 50 MB and should not be more than 500 pages for PDF documents.
- For images, dimensions must be between 530 x 100 and 4200 x 4200 pixels.
- If scanned from paper documents, scans should be high-quality images.
- Must use the Latin alphabet (English characters).
- Must contain keys and values (for example, "company: Contoso" works; "Contoso" without a key label isn't supported). 
- Keys can appear above or to the left of the values, but not below or to the right.

## Optimization tips

- Use forms with different values in each field.
- When you create a new form processing model, upload documents with the same layout where each document is a separate instance. For example: invoices from the same provider, but each uploaded invoice is from a different month.
- If you are getting bad results or low confidence scores for certain fields, create a new Form Processing model and upload more documents. The more documents you tag, the more AI Builder will learn how to better recognize the fields. 
- You can optimize PDF files by using the **Print** > **Print to PDF** option to select certain pages within your document.

 > [!NOTE]
 > AI Builder does not currently support the following types of form processing input data:
 >
 > - Complex tables (nested tables, merged headers or cells, and so on)
 > - Check boxes or radio buttons
 > - Fillable PDFs 

### Next step

[Create a form processing model](create-form-processing-model.md)
