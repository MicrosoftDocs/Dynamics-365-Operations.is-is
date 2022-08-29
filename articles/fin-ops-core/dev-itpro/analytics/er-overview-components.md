---
title: Hlutar rafrænnar skýrslugerðar
description: Þessi grein lýsir rafrænum skýrslugerðum (ER).
author: kfend
ms.date: 09/28/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: 4851374ca4943a84d35f063e0ee65b537ec3b6cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285032"
---
# <a name="electronic-reporting-components"></a>Hlutar rafrænnar skýrslugerðar

[!include [banner](../includes/banner.md)]

Rafræn skýrslugerð styður eftirfarandi gerðir hluta:

- Gagnalíkan
- Vörpun líkans
- Snið
- Lýsigögn

## <a name="data-model-component"></a>Þættir gagnalíkana

Þáttur gagnalíkans er óhlutbundin framsetning á gagnaskipulagi. Hann lýsir tilteknu viðskiptasviði á nógu nákvæman hátt til að uppfylla skýrslukröfur fyrir það svið. Íhlutir gagnalíkans samanstendur af eftirfarandi hluta:

- **Gagnalíkan** – hópur af viðskiptaeiningum fyrir tiltekin svið auk stigskiptra tengslaskilgreininga á milli þessara eininga.
- **Líkanavörpun** – Valdir gagnagjafar forrits eru tengdir við einstaka einingar gagnalíkans sem tilgreina á keyrslutíma gagnaflæðið og reglur um hvernig á að færa inn viðskiptagögn í gagnalíkanshluta.

Viðskiptaeining gagnalíkans er birt sem hólf eða færsla. Eiginleikar viðskiptaeininga eru sýndir sem gagnaatriði, eða svæði. Hvert gagnaatriði hefur einstakt heiti, merki, lýsingu og gildi. Hægt er að hanna virði hvers atriðis svo það sé viðurkennt sem strengur, heiltala, raunverulegt, dagsetning, tölusett (enum) eða Boole-gildi. Þar að auki getur gagnaatriðið verið önnur færsla eða færslulisti.

Einstakur þáttur gagnalíkans getur innihaldið mörg stigveldi sviða sem eru tilgreind eftir viðskiptaeiningum. Einnig getur hann innihaldið líkanavarpanir sem styðja skýrslutengt gagnaflæði á keyrslutíma. Stigveldin verða aðgreind eftir einni færslu sem er valin sem rót líkanavörpunar. Til dæmis, Gagnalíkan fyrir greiðslusvið gæti stutt eftirfarandi varpanir:


- Fyrirtæki \> Lánardrottinn \> Greiðslufærslur AP-sviðs
- Viðskiptavinur \> Fyrirtæki \> Greiðslufærslur AR-sviðs

Viðskiptaeiningar eins og fyrirtæki og greiðslufærslur eru hannaðar aðeins einu sinni. Mismunandi varpanir geta endurnotað þær eftir þörfum.

## <a name="model-mapping-component"></a>Hluti líkanavörpunar

Líkanavörpun tengir gagnagjafa forrits við einstaka einingar gagnalíkans sem tilgreina á keyrslutíma gagnaflæðið og reglur um hvernig á að færa inn viðskiptagögn í gagnalíkanshluta.

Líkanavörpun sem styður rafræn skjöl á útleið hefur eftirfarandi getu:

- Hægt er að nota mismunandi gagnagerðir sem gagnagjafa fyrir gagnalíkan. Þessar gagnagerðir eru til dæmis töflur, gagnaeiningar, aðferðir og fasttextar.
- Það styður ílagsfæribreytur notanda sem má skilgreina sem gagnagjafa gagnalíkans þegar tilgreina þarf gögn á keyrslutíma.
- Þær styðja umbreytingu gagna í nauðsynlega flokka. Það leyfir þér einnig að sía, raða og leggja saman gögn og skeyta við rökrétta útreiknaða reiti sem eru hannaðir með formúlum sem líkjast Microsoft Excel-formúlum. Frekari upplýsingar er að finna í [Formúluhönnuður í rafrænni skýrslugerð (ER)](general-electronic-reporting-formula-designer.md).

Líkanavörpun sem styður rafræn skjöl á innleið hefur eftirfarandi getu:

- Hægt er að nota mismunandi uppfæranlegar gagnaeiningar sem mörk. Á meðal þessara gagnaþátta eru töflur, gagnaeiningar og yfirlit. Hægt er að uppfæra gögnin með gögnum á innleið úr rafrænum skjölum. Hægt er að nota mörg mörk í einni líkanavörpun.
- Það styður ílagsfæribreytur notanda sem má skilgreina sem gagnagjafa gagnalíkans þegar tilgreina þarf gögn á keyrslutíma.

Þáttur gagnalíkans er hannaður fyrir hvert viðskiptasvið sem er notað sem sameinaður gagnagjafi fyrir skýrslugerð. Sameinaði gagnagjafinn einangrar skýrslugjöf frá efnislegri innleiðingu gagnagjafa. Ef þátturinn sýnir viðskiptahugtök fyrir tiltekin svið og virkni í skjámynd sem gerir frumhönnun og frekara viðhald á skýrslugerðarsniði skilvirkara.

## <a name="format-component"></a>Sniðsþáttur

### <a name="format-components-for-outgoing-electronic-documents"></a>Sniðsþáttur fyrir rafræn skjöl á útleið

Sniðsþáttur er skema fyrir úttak skýrslugjafar sem myndað er á keyrslutíma. Skema samanstendur af eftirfarandi þáttum:

- Snið sem skilgreinir skipulag og innihald í rafrænu skjali á útleið sem er myndað á keyrslutíma.
- Gagnagjafar, sem ílagsfæribreytur notanda og gagnalíkön fyrir tiltekin svið sem nota valda líkanavörpun.
- Sniðsvörpun, sem safn bindingar fyrir gagnagjafa sniða sem eru með einstakar sniðseiningar sem tilgreina, á keyrslutíma, gagnaflæði og reglur um myndun úttakssniðs.
- Villuleitarsnið, sem hópur af samskipanlegum reglum sem stýra skýrslugerð á keyrslutíma, háð samhengi keyrslu. Til dæmis gæti verið regla sem stöðvar úttaksmyndun fyrir greiðslur lánardrottins og beitir undantekningu þegar tilteknar eigindir valins lánardrottins vantar, eins og númer bankareiknings.

Þáttur sniðs styður eftirfarandi aðgerðir:

- Stofnun skýrslugerðarúttaks sem einstakar skrár í mismunandi sniði, t.d. texti, XML, Microsoft Word-skjal eða vinnublað
- Margar aðskildar skrár búnar til og þær þjappaðar í zip-skrár

Sniðsþáttur gerir þér kleift að hengja við tilteknar skrár sem hægt er að nota í skýrslugerðarúttaki:

- Excel-vinnubækur Sem inniheldur vinnublað sem sem má nota sem sniðmát fyrir úttak á OPENXML vinnublaðssniði;
- Word-skrár sem innihalda skjal sem hægt er að nota sem sniðmát fyrir úttak í sniði Microsoft Word-skjals.
- Aðrar skrár sem geta verið felldar inn í úttakssnið sem fyrirfram skilgreindar skrár.

Eftirfarandi dæmi sýnir gagnaflæðið fyrir þessi snið.

[![Gagnaflæði fyrir sniðsþætti á útleið](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Til að keyra eina sniðsskilgreiningu fyrir rafræna skýrslugerð og búa til rafrænt skjal til að senda út verður þú að auðkenna vörpun skilgreiningarsniðsins.

#### <a name="format-components-for-incoming-electronic-documents"></a>Sniðsþættir fyrir rafræn skjöl á innleið
Sniðsþáttur er skema skjals á innleið sem er flutt inn á keyrslutíma. Skema samanstendur af eftirfarandi þáttum:

- Snið sem skilgreinir skipulag og innihald rafræns skjals á innleið sem inniheldur gögn sem eru flutt inn á keyrslutíma. Sniðsþáttur er notaður til að þátta skjal á innleið á ýmis snið, eins og texta og XML.
- Sniðsvörpun sem bindur einstakar sniðseiningar í einingar í gagnalíkani fyrir tiltekin svið. Einingarnar í gagnalíkani tilgreina, á keyrslutíma, gagnaflæði og reglur fyrir innflutning gagna úr skjali á innleið og geyma svo gögnin í gagnalíkani.
- Villuleitarsnið, sem hópur af samskiptanlegum reglum sem stýra gagnainnflutningi á keyrslutíma, háð samhengi keyrslu. Til dæmis gæti verið regla sem stöðvar innflutning á gögnum bankayfirlits sem er með greiðslur lánardrottins og beitir undantekningu þegar tilteknar eigindir lánardrottins vantar, eins og auðkenniskóði lánardrottins.

Eftirfarandi dæmi sýnir gagnaflæðið fyrir þessi snið.

[![Gagnaflæði fyrir sniðsþætti á innleið](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Til að keyra eina sniðsskilgreiningu til að flytja gögn úr rafrænu skjali á innleið, verður að auðkenna tilætlaða vörpun skilgreiningarsniðsins og einnig samþættingarstað vörpunar líkans. Hægt er að nota sömu vörpun líkans og áfangastaði með mismunandi sniðum fyrir mismunandi gerðir skjala á innleið.


## <a name="component-versioning"></a>Sögugeymni íhlutar

Sögugeymnin er studd fyrir ER þætti. Eftirfarandi verkflæði er til staðar til að stýra breytingum í þáttum rafrænnar skýrslugerðar:

1. Útgáfan sem var upphaflega búin til er merkt sem a **Drög** útgáfu. Útgáfan er hægt að breyta og er tiltæk fyrir prófunarkeyrslu.
2. Útgáfunni **Drög** má breyta í útgáfuna **Lokið**. Hægt er að nota þessa útgáfu í staðbundna skýrslugerðarferli.
3. Útgáfunni **Lokið** má breyta í útgáfuna **Samnýtt**. Þessi útgáfa er birt í Microsoft Dynamics Lifecycle Services (LCS) og hægt er að nota hana í altækum skýrslugerðarferlum.
4. Útgáfunni **Samnýtt** má breyta í útgáfuna **Hætt við**. Hægt er að eyða þessari útgáfu.

Útgáfur sem hafa stöðuna **Lokið** eða **Samnýtt** eru tiltækar fyrir önnur gagnaskipti. Hægt er að framkvæma eftirfarandi aðgerðir á þætti sem hefur þessar stöður:

- Þætti má raða í XML-snið og flytja út sem skrá á XML-sniði.
- Hægt er að endurraða þættinum úr XML-skrá og flytja inn í forritið sem nýja útgáfu ER-þáttar.

Fyrir frekari upplýsingar, sjá [Flytja inn nýja gagnalíkanstillingu](er-quick-start1-new-solution.md#ImportDataModel) og [Flytja út lokið útgáfu af afleiddu sniði](er-calculated-field-type.md#export-completed-version-of-a-derived-format).

### <a name="draft-versions-at-runtime"></a>Drög að útgáfum á keyrslutíma

Í persónulegum notendabreytum þínum fyrir ER ramma geturðu virkjað valkostinn sem gerir þér kleift að tilgreina hvort nota þurfi drög að útgáfu ER uppsetningar á keyrslutíma. Fyrir upplýsingar um hvernig á að gera **Keyra Drög** valkostur í boði fyrir ER stillingar þínar, sjá [Merktu sérsniðið snið sem keyranlegt](er-quick-start2-customize-report.md#MarkFormatRunnable).

> [!NOTE]
> ER notendafæribreytur eru fyrirtækissértækar og notendasértækar.

### <a name="draft-format-versions-at-runtime"></a>Drög að útgáfusniði á keyrslutíma

Sjálfgefið er að þegar þú keyrir ER lausn eru drög að útgáfum af sniðhlutum hennar hunsuð. Þess í stað er aðeins viðkomandi útgáfa sem hefur aðra stöðu en **Drög** er notað. Stundum gætirðu viljað þvinga ER til að nota drög að útgáfa af ER sniðstillingunum þínum á keyrslutíma. Til dæmis, eftir að þú hefur kynnt nauðsynlegar breytingar á uppkastsútgáfunni þinni, geturðu notað þá uppkastsútgáfu til að gera prufukeyrsluna. Þannig geturðu sannreynt réttmæti breytinganna. Til að byrja að nota uppkastssniðsútgáfuna verður þú [sett](er-quick-start2-customize-report.md#MarkFormatRunnable) the **Keyra Drög** valmöguleika á viðeigandi ER uppsetningu til **Já**.

### <a name="draft-model-mapping-versions-at-runtime"></a>Drög að útgáfum líkanakorta á keyrslutíma

Sjálfgefið er að þegar þú keyrir ER lausn eru drög að útgáfum líkanakortahlutanna alltaf notuð. Stundum gætirðu viljað þvinga ER til að hunsa drög að útgáfu af ER líkanakortlagningu þinni á keyrslutíma. Í **útgáfu 10.0.29 og síðar**, þú getur virkjað **Taktu alltaf tillit til "Run draft" valkostinn fyrir kortlagningu ER líkana** eiginleiki til að stjórna líkanakortaútgáfunni sem er notuð á keyrslutíma. Þegar þessi eiginleiki er virkur gerist eftirfarandi hegðun:

- Þegar **Keyra Drög** valkostur er stilltur á **Nei** fyrir uppsetningu líkanakorta er hæsta útgáfan sem ekki er uppkast af þeirri stillingu notuð á keyrslutíma. Undantekning er gerð ef uppsetningin er ekki tiltæk í núverandi Finance tilviki.
- Þegar **Keyra Drög** valkostur er stilltur á **Já** fyrir uppsetningu líkanakorta er drög að útgáfu þeirrar stillingar notuð á keyrslutíma.

## <a name="component-date-effectivity"></a>Dagsetning á virkni íhlutar

ER snið íhlutaútgáfur eru dagsetningarvirkar. Þú getur stillt "gildandi frá" dagsetningu fyrir ER-sniðshluta til að tilgreina dagsetninguna þegar íhluturinn tekur gildi fyrir skýrsluferli. Lotudagsetning forrits er notuð til að skilgreina hvort þáttur er gildur fyrir framkvæmd. Nýjasta útgáfa er notuð fyrir skýrsluferli þegar fleiri en ein útgáfa er í gildi fyrir tiltekna dagsetningu.

## <a name="component-access"></a>Aðgangur að þáttum

Aðgangur að ER sniði og líkanakortlagningarhlutum á keyrslutíma fer eftir stillingum fyrir International Organization for Standardization (ISO) lands/svæðiskóða. Ef þessi stilling er auð fyrir valda útgáfu af sniði eða líkanavörpunarstillingu er hægt að nálgast snið eða líkanavörpun frá hvaða fyrirtæki sem er á keyrslutíma. Ef stillingin inniheldur ISO lands-/svæðiskóða er snið- eða módelkortunarhluti aðeins fáanlegur frá fyrirtækjum sem hafa aðal heimilisfang sem er skilgreint fyrir einn af ISO lands-/svæðiskóðum sniðshluta.

Mismunandi útgáfur af sniði eða líkanakortlagningarhluta geta haft mismunandi stillingar fyrir ISO lands-/svæðiskóða.

Fyrir frekari upplýsingar, sjá [Stilltu landasamhengisháðar ER líkanakortanir](er-country-dependent-model-mapping.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

