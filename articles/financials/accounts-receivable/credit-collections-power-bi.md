---
title: Skulda- og innheimtuumsjón Power BI efni
description: Þetta efnisatriði lýsir því hvað er innifalið í skulda- og innheimtuumsjón Power BI efnis. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a80a180623d1cca77c633f12bcd92a088e089ee5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "325182"
---
# <a name="credit-and-collections-management-power-bi-content"></a>Skulda- og innheimtuumsjón Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í **Skulda- og innheimtuumsjón** Microsoft Power BI efnis. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Skulda- og innheimtuumsjón** Power BI efni var búið til fyrir stjórnendur skulda og innheimta og innheimtufulltrúa. Hún hefur að geyma mikilvæga mælikvarða í skulda- og innheimtumálum, eins og útistandandi dagsölu, vanskil, váhrif lánamarks og viðskiptavini sem eru komnir yfir lánamörk. Hún notast við færslugögn og veitir samantekna sýn yfir skulda- og innheimtumál fyrir öll fyrirtæki. Hún gefur einnig sundurliðun á fyrirtæki, viðskiptavinahópa og viðskiptavini.

Þetta Power BI efni samanstendur af 10 skýrslusíðum:

- Tvær yfirlitssíður (ein síða fyrir skuldayfirlit og ein fyrir innheimtuyfirlit)
- Átta ítarlegar síður sem veita upplýsingar um mælieiningar í skulda- og innheimtumálum sem hægt er að skoða samkvæmt ýmsum víddum.

Allar upphæðir eru sýndar í gjaldmiðli kerfisins. Hægt er að stilla gjaldmiðil kerfis á síðunni **Kerfisfæribreytur**.

Sjálfgefið er að skulda- og innheimtugögn fyrir núverandi fyrirtæki séu sýnd. Til að skoða gögnin í öllum fyrirtækjum, úthlutaðu skyldunni **CustCollectionsBICrossCompany** á hlutverkið.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni
**Skulda- og innheimtustjórnun** Power BI efni er sýnt í vinnusvæðinu **Skuldir og innheimta viðskiptavinar**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðar með í Power BI efni

**CustCollectionsBICrossCompany** Power BI efni inniheldur skýrslu sem samanstendur af safni mælikvarða. Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur. Eftirfarandi tafla veitir yfirlit yfir myndrænar framsetningar í **CustCollectionsBICrossCompany** Power BI efni.

| Skýrslusíða                 | Myndbirting |
|-----------------------------|---------------|
| Innheimtuyfirlit        | <ul><li>Viðskipatvinir komnir fram yfir gjalddaga</li><li>Viðskiptavinir yfir kreditmörk</li><li>Dagar útistandandi sölu 30</li><li>Opin mál</li><li>Dagar að meðaltali til lokunar tilviks</li><li>Opnir verkþættir</li><li>Dagar að meðaltali til lokunar aðgerða</li><li>Opna vaxtanótur</li><li>Opna innheimtubréf</li><li>Viðskiptavinur á bið</li><li>Sala á bið</li><li>Aldursgreindar stöður</li><li>Upphæðir innheimtustöðu</li><li>Upphæðir innheimtukóða</li><li>Afskriftir eftir ástæðum</li><li>Gjaldfallið eftir svæðum</li><li>Væntanlegar greiðslur</li></ul> |
| Yfirlit yfir lánamark             | <ul><li>Viðskipatvinir komnir fram yfir gjalddaga</li><li>Lánamark gegn gjaldfallinni stöðu</li><li>Hnitanet fyrir viðskiptavini yfir lánamörkum</li><li>Viðskiptavinir yfir lánamörkum á hvert fyrirtæki</li><li>Nýtt lánamark gegn heildarlánamarki</li><li>Lánamark gegn notuðu lánsfé eftir svæðum</li><li>Viðskiptavinir á hver lánamörk</li></ul> |
| Lánamörk                | <ul><li>Lánamörk</li><li>Upplýsingar um lánamark</li><li>Lánamark á viðskiptavin</li><li>Lánamark á hvern viðskiptavinaflokk</li><li>Lánamark á hverja lánshæfiseinkunn á hvert fyrirtæki</li><li>Lánamark gegn notuðu lánsfé eftir svæðum</li></ul> |
| Viðskiptavinir yfir kreditmörk | <ul><li>Viðskiptavinir yfir kreditmörk</li><li>Upplýsingar um viðskiptavini yfir lánamörkum</li><li>Viðskiptavinir yfir lánamörkum á hvert fyrirtæki</li><li>Viðskiptavinur yfir lánamarki á hvern viðskiptavinaflokk</li><li>Viðskiptavinir yfir lánamörkum eftir svæðum</li></ul> |
| Viðskipatvinir komnir fram yfir gjalddaga          | <ul><li>Viðskipatvinir komnir fram yfir gjalddaga</li><li>Upplýsingar um viðskiptavini komna fram yfir gjalddaga</li><li>Viðskiptavinur með gjaldfallna skuld á hvert fyrirtæki</li><li>Viðskiptavinur með gjaldfallna skuld á hvern viðskiptavinaflokk</li><li>Viðskiptavinur með gjaldfallna skuld eftir svæðum</li></ul> |
| Aldursgreindar stöður               | <ul><li>Aldursgreindar stöður</li><li>Upplýsingar um aldursgreindar stöður</li><li>Aldursgreindar stöður á hvert fyrirtæki</li><li>Aldursgreindar stöður á hvern viðskiptavinaflokk</li></ul> |
| Væntanlegar greiðslur           | <ul><li>Væntanlegar greiðslur</li><li>Upplýsingar um væntanlegar greiðslur</li><li>Greiðslur sem er búist við fyrir hvert fyrirtæki</li><li>Greiðslur sem er búist við fyrir hvern viðskiptavinaflokk</li><li>Greiðslur sem er búist við eftir svæðum</li></ul> |
| Afskriftir                  | <ul><li>Afskriftir eftir svæðum</li><li>Upplýsingar um afskriftir</li><li>Afskriftir eftir aðallyklum</li><li>Afskriftir fyrir hvert fyrirtæki</li><li>Afskriftir á hvern flokk viðskiptavina</li><li>Afskriftir eftir svæðum</li></ul> |
| Staða innheimtu          | <ul><li>Umdeild</li><li>Loforð um greiðslu svikið</li><li>Gefa loforð um greiðslu</li><li>Upplýsingar um innheimtustöðu</li><li>Upphæðir innheimtustöðu</li><li>Opin mál</li><li>Opnir verkþættir</li></ul> |
| Innheimtubréf         | <ul><li>Upphæðir innheimtukóða</li><li>Upplýsingar um upphæðir innheimtukóða</li><li>Upphæðir innheimtubréfa á hvert fyrirtæki</li><li>Upphæðir innheimtubréfa á hvern viðskiptavinaflokk</li><li>Upphæðir innheimtubréfa eftir svæðum</li></ul> |

Hægt er að sía og festa Gröf og reitir á þessar skýrslur við mælaborð. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Einnig má nota virknina til að Flytja út undirliggjandi gögn til að flytja út undirliggjandi gögn sem eru sýnd í myndrænni samantekt.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Eftirfarandi gögn eru notuð til að fylla út skýrsluna í **Skulda- og innheimtuumsjón** Power BI efni. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Einingaverslunin er Microsoft SQL Server gagnagrunnur sem er fínstillt fyrir greiningar. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](../../dev-itpro/analytics/power-bi-integration-entity-store.md).


|                   Eining                    |      Lykiluppsafnaðar mælingar      |             Uppruni gagna              |                           Svæði                            |                                    lýsing                                     |
|---------------------------------------------|--------------------------------------|--------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities AveragecClosedTime  |            smmActivities             | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) |     Talning lokaðra aðgerða og meðaltími til stefnu til lokunar þeirra aðgerða.     |
|       CustCollectionsBIActivitiesOpen       |            ActivityNumber            |            smmActivities             |                   Count(ActivityNumber)                    |                           Talning á opnum aðgerðum.                            |
|        CustCollectionsBIAgedBalances        |             AgedBalances             |  CustCollectionsBIAgedBalancesView   |                 Sum(SystemCurrencyBalance)                 |                             Samtala á aldursgreindum stöðum.                              |
|        CustCollectionsBIBalancesDue         |         SystemCurrencyAmount         |   CustCollectionsBIBalanceDueView    |                 Sum(SystemCurrencyAmount)                  |                           Upphæðir sem eru komnir fram yfir gjalddaga.                            |
|    CustCollectionsBICaseAverageCloseTIme    |  NumOfCases, CaseAverageClosedTime   |      CustCollectionsCaseDetail       | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) |        Talning lokaðra tilvika og meðaltími til stefnu til lokunar þeirra tilvika.        |
|         CustCollectionsBICasesOpen          |                CaseId                |      CustCollectionsCaseDetail       |                       Count(CaseId)                        |                              Talning á opnum tilvikum.                              |
|      CustCollectionsBICollectionLetter      |         CollectionLetterNum          |       CustCollectionLetterJour       |                 Count(CollectionLetterNum)                 |                       Talning á opnum innheimtubréfum.                        |
|   CustCollectionsBICollectionLetterAmount   |       CollectionLetterAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                     Staða bókaða innheimtubréfa.                      |
|      CustCollectionsBICollectionStatus      |       CollectionStatusAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                Staða færslna með innheimtustöðu.                 |
|           CustCollectionsBICredit           | CreditExposed AmountOverCreditLimit |     CustCollectionsBICreditView      |       Sum(CreditExposed), Sum(AmountOverCreditLimit)       | Samtala á váhrifum lánamarka og upphæðum þar sem viðskiptavinir eru yfir lánamörkum sínum. |
|         CustCollectionsBICustOnHold         |               Læst                |      CustCollectionsBICustTable      |                       Count(Blocked)                       |                     Fjöldi viðskiptavina á bið.                      |
|            CustCollectionsBIDSO             |                DSO30                 |       CustCollectionsBIDSOView       |                  AverageOfChildren(DSO30)                  |                        Útistandandi sala fyrir 30 daga.                         |
|      CustCollectionsBIExpectedPayment       |           ExpectedPayment            | CustCollectionsBIExpectedPaymentView |                 Sum(SystemCurrencyAmounts)                 |                 Samtala væntanlegra greiðslna innan næsta árs.                 |
|        CustCollectionsBIInterestNote        |             InterestNote             |           CustInterestJour           |                    Count(InterestNote)                     |                Fjöldi stofnaðra vaxtanóta.                |
|        CustCollectionsBISalesOnHold         |               SalesId                |              SalesTable              |                       Count(SalesId)                       |                 Fjöldi heildarsölupantana sem eru á bið.                 |
|          CustCollectionsBIWriteOff          |            WriteOffAmount            |    CustCollectionsBIWriteOffView     |                 Sum(SystemCurrencyAmount)                  |                Samtala færslna sem hafa verið afskrifaðar.                 |

