---
title: Hlutar rafrænnar skýrslugerðar
description: Þessi grein lýsir rafrænum skýrslugerð (ER) íhlutum.
author: nselin
ms.date: 09/28/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.topic: overview
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2b8b197fdea0cd49fc5161a12b8f547cc1a27bf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892451"
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

1. Útgáfan sem var upphaflega stofnuð er merkt sem **Drög**. Útgáfan er hægt að breyta og er tiltæk fyrir prófunarkeyrslu.
2. Útgáfunni **Drög** má breyta í útgáfuna **Lokið**. Hægt er að nota þessa útgáfu í staðbundna skýrslugerðarferli.
3. Útgáfunni **Lokið** má breyta í útgáfuna **Samnýtt**. Þessi útgáfa er birt í Microsoft Dynamics Lifecycle Services (LCS) og hægt er að nota hana í altækum skýrslugerðarferlum.
4. Útgáfunni **Samnýtt** má breyta í útgáfuna **Hætt við**. Hægt er að eyða þessari útgáfu.

Útgáfur sem hafa stöðuna **Lokið** eða **Samnýtt** eru tiltækar fyrir önnur gagnaskipti. Hægt er að framkvæma eftirfarandi aðgerðir á þætti sem hefur þessar stöður:

- Þætti má raða í XML-snið og flytja út sem skrá á XML-sniði.
- Hægt er að endurraða þættinum úr XML-skrá og flytja inn í forritið sem nýja útgáfu ER-þáttar.

## <a name="component-date-effectivity"></a>Dagsetning á virkni íhlutar

ER þáttarútgáfur eru virkar eftir dagsetningum. Hægt er að stilla dagsetninguna „Virkt“ frá fyrir þátt rafrænnar skýrslugerðar þannig að hún tilgreini þá dagsetningu sem þátturinn verður virkur fyrir skýrsluferla. Lotudagsetning forrits er notuð til að skilgreina hvort þáttur er gildur fyrir framkvæmd. Nýjasta útgáfa er notuð fyrir skýrsluferli þegar fleiri en ein útgáfa er í gildi fyrir tiltekna dagsetningu.

## <a name="component-access"></a>Aðgangur að þáttum

Aðgangur að þáttum rafræns skýrslugerðarsniðs fer eftir stillingunni fyrir lands-/svæðiskóða Alþjóðlegu staðlastofnunarinnar (ISO). Ef þessi stilling er auð fyrir valda útgáfu skilgreiningar sniðs, er hægt að nálgast sniðsþátt úr hvaða fyrirtæki sem er á keyrslutíma. Ef þessi stilling inniheldur ISO lands-/ svæðiskóða, er sniðsþáttur tiltækur eingöngu frá fyrirtækjum þar sem aðalaðsetur er tilgreint fyrir einn sniðsþátt ISO lands-/svæðiskóða.

Mismunandi útgáfur af gagnasniðsþáttum mega vera með mismunandi stillingar ISO lands-/ svæðiskóða.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

