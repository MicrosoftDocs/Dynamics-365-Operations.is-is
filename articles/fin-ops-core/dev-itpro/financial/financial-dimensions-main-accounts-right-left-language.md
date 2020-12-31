---
title: Fjárhagsvíddir og aðallyklar í tungumálum sem rituð eru frá hægri til vinstri
description: Í þessu efnisatriði er lýst nokkrum innleiðingu ákvarðanir sem ætti að íhuga að þegar notuð hægri til vinstri tungumál og setja verður upp aðallykla og fjárhagsvíddir.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 192ed371eec24ed4e0532aaca341bb249a4933c7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680483"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="7a20f-103">Fjárhagsvíddir og aðallyklar í tungumálum sem rituð eru frá hægri til vinstri</span><span class="sxs-lookup"><span data-stu-id="7a20f-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a20f-104">Í þessu efnisatriði er lýst nokkrum innleiðingu ákvarðanir sem ætti að íhuga að þegar notuð hægri til vinstri tungumál og setja verður upp aðallykla og fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="7a20f-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="7a20f-105">Fjárhagsvíddir og aðallykla eru lykilíhluti í áætlunaráfanginn við innleiðingu.</span><span class="sxs-lookup"><span data-stu-id="7a20f-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="7a20f-106">Eftir að fjárhagsvíddir og aðallyklar eru stofnaðir í kerfinu, þær eru notaðar á **Skilgreina lykilskipulög**, **Ítarlegt regluskipulag**, og **fjárhagsvíddarskilgreining fyrir samþættingu forrita** síður.</span><span class="sxs-lookup"><span data-stu-id="7a20f-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="7a20f-107">Röðin sem er skilgreindur á þessum síðum er notaður í kerfinu fyrir innslátt gagna og notkun.</span><span class="sxs-lookup"><span data-stu-id="7a20f-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="7a20f-108">Í sumum stöðum í kerfinu birtast fjárhagsvíddir og aðallykla í sérstök svæði.</span><span class="sxs-lookup"><span data-stu-id="7a20f-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="7a20f-109">Á öðrum stöðum eins og færslubækur, birtast fjárhagsvíddir og aðallyklar sem einn strengur.</span><span class="sxs-lookup"><span data-stu-id="7a20f-109">In other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="7a20f-110">Bestu venjur við að setja upp aðallykla og fjárhagsvíddir í kerfi hægri til vinstri</span><span class="sxs-lookup"><span data-stu-id="7a20f-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

- <span data-ttu-id="7a20f-111">Þegar skiltákn fyrir bókhaldslykil er valinn, veldu einn af tveimur kostum tvöföld skiltákn: tvöfalda bandstrik (`--`), tvöföldu strikamerki (`||`) eða tvöfaldur punktur (`..`) eða tvöföldu undirstrik (`\\`).</span><span class="sxs-lookup"><span data-stu-id="7a20f-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (`--`), double bar (`||`), double period (`..`), or double underscore (`\\`).</span></span>
- <span data-ttu-id="7a20f-112">Þegar þú stofnar fjárhagsvíddir og gildi aðallykla, notaðu eingöngu númer og stafi tungumála frá hægri til vinstri.</span><span class="sxs-lookup"><span data-stu-id="7a20f-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
- <span data-ttu-id="7a20f-113">Komast hjá því að nota valda skiltákn bókhaldslykils í gildum fjárhagsvíddar og aðallykilinn.</span><span class="sxs-lookup"><span data-stu-id="7a20f-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="7a20f-114">Með því að fara eftir Eftirfarandi bestu venjur, hjálpa til við tryggja samræmda framsetningu notandaskilgreint röðun í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="7a20f-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>
