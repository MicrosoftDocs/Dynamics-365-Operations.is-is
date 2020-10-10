---
title: Yfirlit ítarlegrar bankaafstemmingar
description: Þessi grein lýsir flæðinu fyrir ítarlegt ferli bankaafstemmingar. Ítarleg afstemming aðgerð gerir það mögulegt að flytja inn bankayfirlit sem er hægt að stemma af beint innan úr bankafærslu.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26b6e1e50e5a9b53ca6b5315de760f5bcec4769
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899398"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="8326d-104">Yfirlit ítarlegrar bankaafstemmingar</span><span class="sxs-lookup"><span data-stu-id="8326d-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8326d-105">Þessi grein lýsir flæðinu fyrir ítarlegt ferli bankaafstemmingar.</span><span class="sxs-lookup"><span data-stu-id="8326d-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="8326d-106">Ítarleg afstemming aðgerð gerir það mögulegt að flytja inn bankayfirlit sem er hægt að stemma af beint innan úr bankafærslu.</span><span class="sxs-lookup"><span data-stu-id="8326d-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="8326d-107">Ítarleg afstemming aðgerð gerir það mögulegt að flytja inn bankayfirlit.</span><span class="sxs-lookup"><span data-stu-id="8326d-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="8326d-108">Innflutt bankayfirlit getur þá°verið afstemmt sjálfkrafa innan bankafærslna.</span><span class="sxs-lookup"><span data-stu-id="8326d-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="8326d-109">Hér eru þrep í ítarlegu bankaafstemmingar°flæði.</span><span class="sxs-lookup"><span data-stu-id="8326d-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="8326d-110">Setja upp innflutning bankayfirlits.</span><span class="sxs-lookup"><span data-stu-id="8326d-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="8326d-111">Flytja inn bankayfirlit gegnum umgjörð gagnaeininga.</span><span class="sxs-lookup"><span data-stu-id="8326d-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="8326d-112">Þrjú dæmigerð bankayfirlitssnið eru innbyggð: ISO20022, BAI2 og°MT940.</span><span class="sxs-lookup"><span data-stu-id="8326d-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="8326d-113">Hægt er að auka virknina í hvaða snið sem er.</span><span class="sxs-lookup"><span data-stu-id="8326d-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="8326d-114">Setja upp númeraröð til að nota°fyrir ítarlega bankaafstemmingu og skilgreina samsvörunarreglur bankaafstemmingar.</span><span class="sxs-lookup"><span data-stu-id="8326d-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="8326d-115">Jöfnunarregla afstemmingar er safn skilyrða sem eru notuð til að sía bankayfirlitslínur og bankaskjalslínur Microsoft Dynamics 365 Finance á meðan á afstemmingarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="8326d-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="8326d-116">Hægt er að setja upp fleiri en eina samsvörunarreglu til að gera sjálfvirkt og bæta ferli við afstemmingar eftir þörfum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8326d-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="8326d-117">Stemma af bankayfirlit með bankafærslum Finance.</span><span class="sxs-lookup"><span data-stu-id="8326d-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="8326d-118">Framkvæma sjálfvirka jöfnun og stofnun afstemmingafærslubóka.</span><span class="sxs-lookup"><span data-stu-id="8326d-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="8326d-119">Skoða bankayfirlit og bankafærslur Finance hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="8326d-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="8326d-120">Sjálfkrafa bókun á bankafærslum Finance ef þær birtast á bankayfirlitum en birtast ekki í forritinu Finance.</span><span class="sxs-lookup"><span data-stu-id="8326d-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="8326d-121">Búa til afstemmingaryfirlit.</span><span class="sxs-lookup"><span data-stu-id="8326d-121">Generate a reconciliation statement.</span></span>





