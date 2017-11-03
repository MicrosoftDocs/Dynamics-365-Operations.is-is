---
title: "Skulda- og innheimtuumsjón í Power BI"
description: "Þetta efnisatriði lýsir því hvað er að finna í skulda- og innheimtuumsjón í Power BI. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 7aec3d81fca86abdab4f5fcee54f832f917ffe92
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>Skulda- og innheimtuumsjón í Power BI

Þetta efnisatriði lýsir því hvað er að finna í **Skulda- og innheimtuumsjón** í Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Skulda- og innheimtuumsjón** í Power BI var stofnuð fyrir skulda- og innheimtustjóra og starfsmenn í innheimtu. Hún hefur að geyma mikilvæga mælikvarða í skulda- og innheimtumálum, eins og útistandandi dagsölu, vanskil, váhrif lánamarks og viðskiptavini sem eru komnir yfir lánamörk. Hún notast við færslugögn og veitir samantekna sýn yfir skulda- og innheimtumál fyrir öll fyrirtæki. Hún gefur einnig sundurliðun á fyrirtæki, viðskiptavinahópa og viðskiptavini.

Þetta Power BI efni samanstendur af 10 skýrslusíðum:

- Tvær yfirlitssíður (ein síða fyrir skuldayfirlit og ein fyrir innheimtuyfirlit)
- Átta ítarlegar síður sem veita upplýsingar um mælieiningar í skulda- og innheimtumálum sem hægt er að skoða samkvæmt ýmsum víddum.

Allar upphæðir eru sýndar í gjaldmiðli kerfisins. Hægt er að stilla gjaldmiðil kerfis á síðunni **Kerfisfæribreytur**.

Sjálfgefið er að skulda- og innheimtugögn fyrir núverandi fyrirtæki séu sýnd. Til að skoða gögnin í öllum fyrirtækjum, úthlutaðu skyldunni **CustCollectionsBICrossCompany** á hlutverkið.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017) er **Skuldir og innheimta** Power BI efni sýnt í vinnusvæðinu **Skuldir og innheimta viðskiptavinar**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni

**CustCollectionsBICrossCompany** í Power BI inniheldur skýrslu sem samanstendur af safni mælikvarða. Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur. Í eftirfarandi töflu er yfirlit yfir myndræna framsetningu í **CustCollectionsBICrossCompany** í Power BI.

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

## <a name="extending-the-power-bi-content"></a>Stækkun efnis Power BI
Með því að nota þjónustupakka sem eru í boði í Microsoft Dynamics Lifecycle Services (LCS) er hægt að veita fólki sem skráir sig ekki inn í Finance and Operations öflugri greiningu. Hægt er að breyta þessum þjónustupökkum þannig að þeir innihaldi skýrslur eða myndræna framsetningu og afhenda svo leigjanda Power BI.com þjónustupakkana.

Hægt er að finna efnið **Skulda- og innheimtuumsjón** í Power BI í safninu Samnýttar eignir í LCS. Upplýsingar um hvernig á að sækja efnið og innleiða það í fyrirtæki er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md). Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office Mix.

Nauðsynlegt er að hlaða niður efninu **Skulda- og innheimtuumsjón** í Power BI sem á við um útgáfu Finance and Operations sem verið er að nota.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Eftirfarandi gögn eru notuð til að fylla út skýrsluna í **Skulda- og innheimtuumsjón** í Power BI. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Entity-verslunin er Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](../../dev-itpro/analytics/power-bi-integration-entity-store.md)

| Eining                                      | Lykiluppsafnaðar mælingar           | Uppruni gagna                                 | Svæði                                                      | lýsing |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | Talning lokaðra aðgerða og meðaltími til stefnu til lokunar þeirra aðgerða. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | Talning á opnum aðgerðum. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | Samtala á aldursgreindum stöðum. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | Upphæðir sem eru komnir fram yfir gjalddaga. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | Talning lokaðra tilvika og meðaltími til stefnu til lokunar þeirra tilvika. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | Talning á opnum tilvikum. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | Talning á opnum innheimtubréfum. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Staða bókaða innheimtubréfa. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Staða færslna með innheimtustöðu. |
| CustCollectionsBICredit                     | CreditExposed AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | Samtala á váhrifum lánamarka og upphæðum þar sem viðskiptavinir eru yfir lánamörkum sínum. |
| CustCollectionsBICustOnHold                 | Læst                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | Fjöldi viðskiptavina á bið. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | Útistandandi sala fyrir 30 daga. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | Samtala væntanlegra greiðslna innan næsta árs. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | Fjöldi stofnaðra vaxtanóta. |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | Fjöldi heildarsölupantana sem eru á bið. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | Samtala færslna sem hafa verið afskrifaðar. |

