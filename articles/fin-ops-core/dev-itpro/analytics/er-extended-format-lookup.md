---
title: Rafræn skýrslugerð (ER) útbreidd snið leit
description: Þessi grein lýsir því hvernig hægt er að setja upp ER-sniðstilvísun í ER-sniðsuppflettingunni þegar nauðsynlegt snið er geymt í alþjóðlegu geymslunni.
author: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: 624f5c347c27cc2075f9602087c1c49e84340565
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274920"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Leyfa notendum að setja upp tilvísun á ER snið þar sem spurt er um snið frá altæku geymslunni

[!include [banner](../includes/banner.md)]

Þú getur notað [Rafræn skýrslugerð](general-electronic-reporting.md) (ER) ramma til að stilla snið fyrir skjöl á útleið í samræmi við lagalegar kröfur ýmissa landa/svæða. Þú getur líka notað ER ramma til að stilla snið til að flokka á heimleið skjöl og nota upplýsingar úr skjölunum til að bæta við eða uppfæra gögn umsóknar. Hvert þessara sniða er hægt að nota í Dynamics 365 Finance tilvikinu þínu til að meðhöndla viðskiptaskjöl á innleið eða útleið sem hluta af ákveðnu viðskiptaferli.

Venjulega verður þú að tilgreina hvaða ER snið verður að nota í ákveðnu viðskiptaferli. Til að gera það skaltu velja eitt ER snið í uppflettigrein sem er stillt sem hluti af viðskiptaferlum sem eru sértækir. Þessir uppflettingarreitir eru venjulega útfærðir með því að nota viðeigandi API í ER ramma. Fyrir frekari upplýsingar, sjá [ER ramma API - kóða til að sýna sniðkortagerð](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Til dæmis þegar þú stillir [færibreytur erlendra viðskipta](../../../finance/localizations/emea-intrastat.md#set-up-foreign-trade-parameters) þarftu að setja upp tilvísanir í einstök ER snið sem verða notuð til að búa til Intrastat yfirlýsinguna og stjórnunarskýrsluna fyrir Intrastat yfirlýsinguna. Skjámyndirnar hér að neðan sýna hvernig útlit reiturinn fyrir ER snið lítur út á síðunni **Færibreytur erlendra viðskipta**.

Þegar núverandi fjármálatilvik inniheldur engin snið rafrænnar skýrslugerðar fyrir Intrastat-viðskiptaferli verður þessi uppflettireitur auður.

[![Síðan Færibreytur erlendra viðskipta, vörpunarsvæði fyrir tómt skýrslusnið.](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Ef núverandi tilvik Finance inniheldur Intrastat-viðskiptaferli sem tengjast ER-sniðum býður þessi uppflettireitur ER-sniðmátin.

[![Síðan Færibreytur erlendra viðskipta, vörpunarsvæði fyrir skýrslusnið með valkostum.](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Þessi uppfletting býður aðeins upp á ER snið sem þegar hafa verið flutt inn í núverandi tilvik Finance. Til að [flytja inn](./tasks/er-import-configuration-lifecycle-services.md) ER-lausnir í núverandi tilvik Finance þarftu að hafa heimildir til að keyra viðeigandi aðgerð ER ramma sem styður [líftíma](general-electronic-reporting-manage-configuration-lifecycle.md) ER-lausna sem innihalda ER-snið.

Byrjað er á útgáfu 10.0.9 af Finance (útgáfa apríl 2020), notendaviðmót ER-sniðsins, sem er útfært með því að nota ER-ramma API, hefur verið framlengt. Þú getur samt valið núverandi ER snið, sem er á flýtiflipanum **Velja sniðstillingu**. Þar að auki býður útvíkkun uppflettingar upp á nýjan valkost til að leita í altækri geymslu (GR) til að finna tiltekin snið rafrænnar skýrslugerðar. Öll ER snið GR eru í boði á flýtiflipanum **Flytja úr altækri geymslu**.

[![Síðan Færibreytur erlendra viðskipta, flytja inn frá flýtiflipa altækrar geymslu.](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Svipað flipanum **Velja sniðstillingu**, sýnir flýtiflipinn **Flytja úr altækri geymslu** aðeins ER-snið sem eiga við um viðskiptaferlið sem ER-snið er valið fyrir í þessum uppflettisreit. Í þessu dæmi, kynslóð af Intrastat skýrslunni. ER sniðið gildir fyrir fyrirtækið sem notandinn er skráður inn í, allt eftir samhengi fyrirtækislandsins.

Þegar þú velur ER snið á flýtiflipanum **Flytja úr altækri geymslu** er valið ER-snið [stillingar](general-electronic-reporting.md#Configuration) flutt inn úr GR í núverandi tilvik Finance.

[![Síðan Færibreytur erlendra viðskipta, vinnsla á athugasemd aðgerðar.](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Ef innflutningi lýkur síðan er tilvísunin í innflutt ER snið geymd í þessum uppflettisreit. Þegar altæk geymsla (GR) er opnuð í fyrsta sinn verður að smella á viðkomandi tengil til að skrá sig fyrir [Skilgreiningarþjónustu reglugerðar](https://aka.ms/rcs) (RCS) sem er notuð til að stjórna aðgangi að altæku geymslunni (GR).

[![Síðan Færibreytur erlendra viðskipta, tengill til að skrá þig fyrir RCS.](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Sjálfgefið er flýtiflipinn **Flytja úr altækri geymslu** kynnir lista yfir ER snið úr tímabundinni geymslu sem er sjálfkrafa búin til á grundvelli GR innihalds til að bæta árangur. Þetta gerist þegar flýtiflipinn **Flytja úr altækri geymslu** er opnaður í fyrsta skipti sem getur tekið nokkrar sekúndur.

Ef þú sérð ekki nauðsynlegt ER snið á flýtiflipanum **Flytja úr altækri geymslu** en þú ert viss um að þetta ER snið sé geymt í GR velurðu valkostinn **Samstilla**. Þessi valkostur uppfærir tímabundnu geymsluna og samstillir hana við núgildandi efni altæku geymslunnar (GR).

## <a name="feature-activation"></a>Aðgerð virkjun

Aðgengi að þessari aðgerð er stjórnað af eiginleikanum **Útvíkkun á útfærslum á ER sniði sem gerir kleift að spyrjast fyrir um altæka geymslu** í **Eiginleikastjórnun**. Þessi eiginleiki er sjálfgefið virkur.

[![Síðan Stjórnun eiginleika.](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Öryggisatriði

Réttindin **Viðhalda uppsetningargeymslum** (**ERMaintainSolutionRepositories**) stjórna aðgangi að GR fyrir notanda sem opnar ER-sniðaleit með virkjaða flýtiflipanum **Flytja úr altækri geymslu**. Til að leyfa notendum að fá aðgang að GR efninu úr uppflettimati á ER sniði þarftu að breyta öryggisstillingunum með því að veita réttindi **ERMaintainSolutionRepositories** fyrir notendur annaðhvort beint eða með því að nota þegar úthlutað hlutverk og skyldur.

Eftirfarandi skjámynd sýnir hvernig þessi réttindi geta verið veitt notendum sem eru úthlutaðir á hlutverkið **Endurskoðandi**. Þetta hlutverk gerir notendum kleift að skilgreina færibreytur erlendra viðskipta og setja upp tilvísanir í snið rafrænnar skýrslugerðar í svæðunum **Vörpun skráarsniðs** og **Vörpun skýrslusniðs** á síðunni **Færibreytur erlendra viðskipta**.

[![Síðan Öryggisskilgreining.](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Takmarkanir

Aðgangur að GR í leit að ER sniði er sem stendur aðeins studdur við val á ER sniðum sem eru notuð til að búa til útleið skjöl.

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Af hverju get ég ekki nálgast Global geymslu frá ER sniði útlit?

Ef þú hefur virkjað eiginleikann **Útvíkkun á útfærslum á ER sniði sem gerir kleift að spyrjast fyrir um altæka geymslu** á síðunni **Stjórnun eiginleika** en notendur geta ekki séð ER snið á flýtiflipanum **Flytja úr altækri geymslu** og valkosturinn **Samstilla** er sýnilegur en óvirkur, skaltu passa að réttindin **Viðhalda uppsetningargeymslum** (**ERMaintainSolutionRepositories**) hafi verið veitt notanda. Hafðu samband við kerfisstjórann þinn til að fá þessi réttindi.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Umgjörð API rafrænnar skýrslugerðar (ER)](er-apis-app73.md)
- [Stjórnun líftíma skilgreiningar fyrir rafræna skýrslugerð](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
