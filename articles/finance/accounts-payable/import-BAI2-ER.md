---
title: Settu upp háþróaðan bankaafstemmingarinnflutning með því að nota rafræna skýrslugerð
description: Þessi grein útskýrir hvernig á að nota rafræna skýrslugerð til að setja upp háþróaða innflutningsferli bankaafstemmingar.
author: angelad116
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 46a50f4b00125656fc185ad569b94eeef00dc3c3
ms.sourcegitcommit: 649f1db26da8f20602f11180fc565b7c59eaf545
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337568"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Settu upp háþróaðan bankaafstemmingarinnflutning með því að nota rafræna skýrslugerð

[!include [banner](../includes/banner.md)]

Ítarlegri bankaafstemmingareiginleikinn gerir þér kleift að flytja inn rafræn bankayfirlit og samræma þau sjálfkrafa við bankafærslur í Microsoft Dynamics 365 Fjármál. Þessi skrá útskýrir hvernig á að setja upp mikilvægar aðgerðir fyrir innflutning fyrir bankayfirlitið. Uppsetning fyrir innflutning bankayfirlits er breytileg, eftir snið rafrænnar bankayfirliti. Microsoft Dynamics 365 Finance styður þrjú bankayfirlitssnið: ISO20022, MT940 og BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Settu upp rafræna skýrslugerð

1. Fara til **Vinnurými \> Rafræn skýrslugerð**.
2. Á flísum fyrir **Microsoft** stillingarveita, veldu **Geymslur**.
3. Veldu **Altækt** og síðan **Opna**.
4. Ef það þarf að koma á tengingu við geymsluna skaltu velja bláa tengilinn í svarglugganum.
5. Í stillingarlistanum, finndu **Fyrirmynd bankayfirlits \> Bankayfirlitslíkan af BAI2**.
6. Veldu **BAI2** sniði.
7. Á **Útgáfur** Flýtiflipi, veldu nýjustu útgáfuna og veldu síðan **Flytja inn**.

## <a name="set-up-the-bank-statement-format"></a>Settu upp bankayfirlitssniðið

1. Fara til **Handbært fé og bankastjórnun \> Uppsetning \> Ítarleg uppsetning bankaafstemmingar \> Bankayfirlitssnið**.
2. Veljið **Nýtt**.
3. Stilltu **Yfirlýsingasnið** og **Nafn** sviðum.
4. Veldu **Almennt rafrænt innflutningssnið** gátreit.
5. Stilltu **Flytja inn sniðstillingar** sviði til **BAI2** sniði.

## <a name="set-up-the-bank-account"></a>Settu upp bankareikninginn

1. Farið í **Reiðufjár- og bankastjórnun \> Bankareikningar \> Bankareikningar**.
2. Opnaðu bankareikninginn.
3. Á **Sátt** flýtiflipann, stilltu **Ítarleg bankaafstemming** valmöguleika til **Já**.
4. Stilltu **Yfirlýsingasnið** sviði til **BAI2** sniði sem var búið til áður.

## <a name="import-the-bank-statement"></a>Flyttu inn bankayfirlitið

1. Fara til **Handbært fé og bankastjórnun \> Afstemming bankayfirlits \> Bankayfirlit**.
2. Efst á **Bankayfirlit** síðu, veldu **Innflutningsyfirlýsing**.
3. Stilltu **bankareikning** reitinn á bankareikninginn í yfirlitinu.
4. Stilltu **Yfirlýsingasnið** sviði til **BAI2** sniði sem var búið til áður.
5. Veldu **Skoðaðu**, og veldu **BAI** skrá.
6. Veldu **Hlaða upp**.
7. Veldu **Allt í lagi** til að flytja inn valda skrá.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Dæmi um bankayfirlitssnið og tæknilegar útlit
Hér að neðan eru dæmi um skilgreiningar tæknilegs útlits fyrir innflutningsskrá ítarlegrar bankaafstemmingar og þrjú skráardæmi um tengd bankayfirlit: [Flytja inn skrá dæmi](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Skilgreining tæknilegs útlits                             | Dæmi bankayfirlitsskránni          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

