---
title: Rafræn skýrslugerð (ER) útbreidd snið leit
description: Þetta efni lýsir því hvernig hægt er að setja upp ER-snið tilvísun í leit að ER-sniði þegar tilskilið snið er geymt í altæku geymslunni.
author: NickSelin
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c72335d7d83934146f827ef0bb568b79a585a7a5
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015261"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Leyfa notendum að setja upp tilvísun á ER snið þar sem spurt er um snið frá altæku geymslunni

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Hægt er að nota ramma [Rafrænnar skýrslugerðar](general-electronic-reporting.md) (ER) til að skilgreina [snið](general-electronic-reporting.md#FormatComponentOutbound) fyrir skjöl á útleið í samræmi við lagaskilyrði mismunandi landa/svæða. Þú getur líka notað ER ramma til að stilla [snið](general-electronic-reporting.md#FormatComponentInbound) til að flokka á heimleið skjöl og nota upplýsingar úr skjölunum til að bæta við eða uppfæra gögn umsóknar. Hvert þessara sniða er hægt að nota í þínu tilviki Dynamics 365 Finance til að meðhöndla viðskiptagögn á heimleið eða á útleið sem hluta af ákveðnu viðskiptaferli. 

Venjulega verður þú að tilgreina hvaða ER snið verður að nota í ákveðnu viðskiptaferli. Til að gera það skaltu velja eitt ER snið í uppflettigrein sem er stillt sem hluti af viðskiptaferlum sem eru sértækir. Þessir uppflettingarreitir eru venjulega útfærðir með því að nota viðeigandi API í ER ramma. Fyrir frekari upplýsingar, sjá [ER ramma API - kóða til að sýna sniðkortagerð](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Til dæmis þegar þú stillir [færibreytur erlendra viðskipta](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters) þarftu að setja upp tilvísanir í einstök ER snið sem verða notuð til að búa til Intrastat yfirlýsinguna og stjórnunarskýrsluna fyrir Intrastat yfirlýsinguna. Skjámyndirnar hér að neðan sýna hvernig útlit reiturinn fyrir ER snið lítur út á síðunni **Færibreytur erlendra viðskipta**.

Ef núverandi tilvik Finance inniheldur engin Intrastat viðskiptaferli sem tengjast ER sniðum, verður þessi uppflettireitur auður.

[![Síðan Færibreytur erlendra viðskipta](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Ef núverandi tilvik Finance inniheldur Intrastat-viðskiptaferli sem tengjast ER-sniðum býður þessi uppflettireitur ER-sniðmátin.

[![Síðan Færibreytur erlendra viðskipta](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Þessi uppfletting býður aðeins upp á ER snið sem þegar hafa verið flutt inn í núverandi tilvik Finance. Til að [flytja inn](./tasks/er-import-configuration-lifecycle-services.md) ER-lausnir í núverandi tilvik Finance þarftu að hafa heimildir til að keyra viðeigandi aðgerð ER ramma sem styður [líftíma](general-electronic-reporting-manage-configuration-lifecycle.md) ER-lausna sem innihalda ER-snið.

Byrjað er á útgáfu 10.0.9 af Finance (útgáfa apríl 2020), notendaviðmót ER-sniðsins, sem er útfært með því að nota ER-ramma API, hefur verið framlengt. Þú getur samt valið núverandi ER snið, sem er á flýtiflipanum **Velja sniðstillingu**. Að auki býður stækkuð uppfletting upp á nýjan möguleika til að leita í Global geymslunni (GR) til að finna sérstök ER snið. Öll ER snið GR eru í boði á flýtiflipanum **Flytja úr altækri geymslu**.

[![Síðan Færibreytur erlendra viðskipta](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Svipað flipanum **Velja sniðstillingu**, sýnir flýtiflipinn **Flytja úr altækri geymslu** aðeins ER-snið sem eiga við um viðskiptaferlið sem ER-snið er valið fyrir í þessum uppflettisreit. Í þessu dæmi, kynslóð af Intrastat skýrslunni. ER sniðið gildir fyrir fyrirtækið sem notandinn er skráður inn í, allt eftir samhengi fyrirtækislandsins.

Þegar þú velur ER snið á flýtiflipanum **Flytja úr altækri geymslu** er valið ER-snið [stillingar](general-electronic-reporting.md#Configuration) flutt inn úr GR í núverandi tilvik Finance.

[![Síðan Færibreytur erlendra viðskipta](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Ef innflutningi lýkur síðan er tilvísunin í innflutt ER snið geymd í þessum uppflettisreit. Athugaðu að þegar þú opnar GR í fyrsta skipti þarftu að fylgja tenglinum sem fylgir til að skrá þig í [Regulatory Configuration Service](https://aka.ms/rcs) (RCS) sem er notað til að stjórna aðgangi að GR geymslu.

[![Síðan Færibreytur erlendra viðskipta](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Sjálfgefið er flýtiflipinn **Flytja úr altækri geymslu** kynnir lista yfir ER snið úr tímabundinni geymslu sem er sjálfkrafa búin til á grundvelli GR innihalds til að bæta árangur. Þetta gerist þegar flýtiflipinn **Flytja úr altækri geymslu** er opnaður í fyrsta skipti sem getur tekið nokkrar sekúndur.

Ef þú sérð ekki nauðsynlegt ER snið á flýtiflipanum **Flytja úr altækri geymslu** en þú ert viss um að þetta ER snið sé geymt í GR velurðu valkostinn **Samstilla**. Þetta mun uppfæra tímabundna geymslu og samstilla það við núverandi innihald GR.

## <a name="feature-activation"></a>Aðgerð virkjun

Aðgengi að þessari aðgerð er stjórnað af eiginleikanum **Útvíkkun á útfærslum á ER sniði sem gerir kleift að spyrjast fyrir um altæka geymslu** í **Eiginleikastjórnun**. Þessi eiginleiki er sjálfgefið virkur.

[![Síðan Stjórnun eiginleika](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Öryggisatriði

Réttindin **Viðhalda uppsetningargeymslum** (**ERMaintainSolutionRepositories**) stjórna aðgangi að GR fyrir notanda sem opnar ER-sniðaleit með virkjaða flýtiflipanum **Flytja úr altækri geymslu**. Til að leyfa notendum að fá aðgang að GR efninu úr uppflettimati á ER sniði þarftu að breyta öryggisstillingunum með því að veita réttindi **ERMaintainSolutionRepositories** fyrir notendur annaðhvort beint eða með því að nota þegar úthlutað hlutverk og skyldur.

Eftirfarandi skjámynd sýnir hvernig þessi réttindi geta verið veitt notendum sem eru úthlutaðir á hlutverkið **Endurskoðandi**. Þetta hlutverk gerir notendum kleift að stilla færibreytur erlendra viðskipta og setja upp tilvísanir í ER snið í reitunum **Vörpun skráasniðs** og **Vörpun skýrslusniðs** á síðunni **Færibreytur erlendra viðskipta**.

[![Síðan Öryggisskilgreining](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Takmarkanir

Aðgangur að GR í leit að ER sniði er sem stendur aðeins studdur við val á ER sniðum sem eru notuð til að búa til útleið skjöl.

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Af hverju get ég ekki nálgast Global geymslu frá ER sniði útlit?

Ef þú hefur virkjað eiginleikann **Útvíkkun á útfærslum á ER sniði sem gerir kleift að spyrjast fyrir um altæka geymslu** á síðunni **Stjórnun eiginleika** en notendur geta ekki séð ER snið á flýtiflipanum **Flytja úr altækri geymslu** og valkosturinn **Samstilla** er sýnilegur en óvirkur, skaltu passa að réttindin **Viðhalda uppsetningargeymslum** (**ERMaintainSolutionRepositories**) hafi verið veitt notanda. Hafðu samband við kerfisstjórann þinn til að fá þessi réttindi.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Umgjörð API rafrænnar skýrslugerðar (ER)](er-apis-app73.md)
- [Stjórnun líftíma skilgreiningar fyrir rafræna skýrslugerð](general-electronic-reporting-manage-configuration-lifecycle.md)
