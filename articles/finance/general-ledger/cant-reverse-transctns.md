---
title: Hvers vegna get ég ekki bakfært þessa færslu?
description: Þetta efnisatriði lýsir mismunandi ástæðum fyrir því að ekki er hægt að bakfæra færslur. Þar eru einnig taldar upp lausnir á þessu vandamáli.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e18caf1dbdf8191713c17b1793f5da44cf2f182b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724530"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Hvers vegna get ég ekki bakfært þessa færslu?

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir mismunandi ástæðum fyrir því að ekki er hægt að bakfæra færslur. Þar eru einnig taldar upp lausnir á þessu vandamáli.

## <a name="symptom"></a>Einkenni

Stofnanir gætu lent í aðstæðum þar sem þær verða að bakfæra færslu sem þær hafa bókað. Stundum kemur kerfið í veg fyrir að þær geti bakfært þessar færslur. Þessi hegðun getur vakið upp tvær spurningar:

- Hvers vegna get ég ekki bakfært færsluna?
- Hvaða áhrif hefur eiginleiki fjöldabakfærslu á þessa hegðun?

## <a name="resolution"></a>Lausn

Færslur verða að uppfylla tiltekin skilyrði áður en hægt er að bakfæra þær. Eftirstandandi hlutar í þessu efnisatriði bjóða upp á staðfestingu á hverri einingu fyrir sig. Þó að þetta efni einblíni á viðskipti í Microsoft Dynamics 365 Finance, sum hugtaka og staðfestingu er hægt að beita á önnur öpp, svo sem Dynamics 365 Supply Chain Management.

Að auki getur staðurinn þar sem færslan er bakfærð haft áhrif á hvort hægt sé að bakfæra hana. Til dæmis er aðeins hægt að bakfæra greiðslu lánardrottins sem er ávísun í hlutanum **Ávísanir** á færslusíðunni fyrir bankareikninganna. Ekki er hægt að bakfæra hana á síðunni **Færslur fylgiskjals** í fjárhag.

Ef kveikt er á eiginleikanum **Fjöldabakfærsla fyrir mörg skjöl** (einnig þekkt sem eiginleiki fjöldabakfærslu) á vinnusvæðinu **Eiginleikastjórnun** hefur það áhrif á hversu margar færslur er hægt að bakfæra og hvar hægt er að bakfæra þær. Þessi eiginleiki veitir tvo kosti þegar kveikt er á honum:

- Fyrir sumar færslugerðir er hægt að velja og bakfæra fleiri en eina færslu í einu úr færslubókinni sem hún var bókuð úr eða af síðunni **Færslur fylgiskjals**. Einstakar færslur verða þó að hafa bakfæranlegar áður en kveikt var á eiginleikanum. Áður en þessi eiginleiki var innleiddur þurfti að bakfæra eina færslu í einu.
- *Sumar* fjárhagsfærslur er hægt að bakfæra úr færslubókinni (almennu færslubókinni) eða á síðunni **Færslur fylgiskjals**. Það þarf ekki að bakfæra þær af síðu undirbókar. Til dæmis var áður aðeins hægt að bakfæra reikningabók lánardrottins af síðunni **Lánardrottnafærslur**. Nú er hins vegar hægt að bakfæra hana í fjárhagsbókinni, færslubókinni eða á síðunni **Færslur fylgiskjals**. Hver hluti í þessu efnisatriði útskýrir færslugerðirnar sem þessi ávinningur gildir ekki um.

Eiginleiki fjöldabakfærslu virkjar **ekki** fleiri færslugerðir fyrir bakfærslu. Ef ekki var áður hægt að bakfæra færslugerð er samt ekki hægt að bakfæra hana eftir að kveikt er á eiginleikanum. Til dæmis er ekki hægt að bakfæra lánardrottnareikninga innkaupapöntunar burtséð frá því hvort kveikt er á eiginleika fjöldabakfærslu.

Frekari upplýsingar um eiginleika fjöldabakfærslu er að finna í [Bakfæra bókun í færslubók](reverse-journal-posting.md).

## <a name="general-ledger"></a>Fjárhagur

Leiðréttingar fjárhags eru aðeins færðar inn með því að nota fjárhagslykla. Því uppfæra þær aðeins fjárhag.

Ef slökkt er á eiginleika fjöldabakfærslu er hægt að bakfæra flestar leiðréttingar fjárhags hverja fyrir sig á síðunni **Færslur fyrir \<main account\>** fyrir fjárhagsbókina (**LedgerTransAccount**). (Nákvæmur titill síðunnar er breytilegur eftir því hvaða aðallykill er valinn.) Síðan sýnir hverja færslu sem hefur verið bókuð á aðallykilinn. Hún er yfirleitt opnuð á síðunni **Listi prófjöfnuðar** eða með því að velja **Færslur** á síðunni **Færslur fylgiskjals**.

Ef kveikt er á eiginleika fjöldabakfærslu verður hægt að bakfæra eitt eða fleiri fylgiskjöl á síðunni **Færslur fylgiskjals** og úr færslubókinni þar sem færslan var bókuð. Undantekningarnar eru: Endurmat á erlendum gjaldmiðli fjárhagsbókar, sameining og færslur árslokalokunar. Þessar færslur eru bakfærðar af síðunum þar sem árslokalokunin var keyrð.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Ástæður þess að ekki er hægt að bakfæra færslur

Af eftirfarandi ástæðum er ekki hægt að afturkalla færslur:

- Almenn færslubók:

    - Fjárhagstímabilið er í bið eða lokað varanlega:

        - Ef bakfærsludagsetning er á fjárhagstímabili sem er ekki opið er ekki hægt að bakfæra færsluna.
        - Ef færslan styður innslátt bókunardagsetningar verður enn hægt að bakfæra færsluna með því að breyta bakfærsludagsetningunni til að opna tímabil.

    - Ferli árslokalokunar hefur verið keyrt:

        - Dagsetning reikningsskila fyrir færsluna er á reikningsári sem hefur farið í gegnum árslokalokun. Þrátt fyrir að tímabil á reikningsárinu gæti enn verið opið er ekki hægt að bakfæra færsluna ef ferli árslokalokunar hefur verið keyrt fyrir reikningsárið. Reikningsárið hefur aðra stöðu en tímabilin í því.
        - Hægt er að bakfæra árslokalokun og síðan er hægt að bakfæra færsluna. Þessi aðferð gæti ekki verið valkostur. Það gæti verið auðveldara að fara handvirkt inn í bakfærslu á opnu tímabili annaðhvort lokaða fjárhagsársins eða næsta fjárhagsárs, allt eftir stöðu fjárhagslokunar. Ef ný færsla er bókuð til að opna tímabil á reikningsárinu sem hefur farið í gegnum ferli árslokalokunar þarf að keyra árslokalokunina aftur.

    - Bakfærsla er þegar í gangi.

        - Ef verið er að bakfæra færsluna verður því ferli að vera lokið. Ekki er hægt að gera aðra bakfærslu. 
        - Eftir að bakfærslunni er lokið er hægt að bakfæra færslu aftur (það er, bakfærslan getur gengið til baka).

    - Fjárhagsjöfnun:

        - Ef ein eða fleiri línur færslunnar hafa verið jafnaðar í fjárhag með því að nota reglubundna verkið **Fjárhagsjafnanir** (**Fjárhagur \> Reglubundin verk \> Fjárhagsjafnanir**) þannig að færslan er til staðar í töflunni LedgerTransSettlement verður ekki hægt að bakfæra færsluna.
        - Hægt er að bakfæra fjárhagsjöfnunina og síðan bakfæra fylgiskjalið.

    - Innan samstæðu:

        - Ef færslan er samstæðufærsla er ekki hægt að bakfæra hana.
        - Færslan er **ekki** færsla innan samstæðu en er bókuð á „gjalddaga“ eða „gjalddaga frá“ aðallykils sem var skilgreint á síðunni **Uppsetning samstæðu**.

    - Uppsafnanir:

        - Ef uppsafnað fylgiskjal fjárhags er bakfært verður uppsöfnuð færsla og allar samsvarandi uppsafnaðar undirfærslur bakfærðar.
        - Ekki er hægt að bakfæra einstakar uppsafnaðar undirfærslur.

- Færslubók tekjuskráningar:

    - Ekki er hægt að bakfæra færslur vegna tekjuskráningar.
    - Þegar tekjur eru skráðar í gegnum tekjuskráningarbókina er fylgiskjalið aðeins bókað í fjárhagslyklum. Á síðum eins og **Fylgiskjalafærslur** birtast færslurnar því eins og þær séu aðeins almennar fjárhagsfærslur.

- Endurmat á erlendum gjaldmiðli:

    - Hægt er að bakfæra endurmatsfærslur á erlendum gjaldeyri, en aðeins úr fjárhagsbókarsíðunni **Endurmat á erlendum gjaldmiðli** þar sem endurmatið var keyrt.
    - Aðeins er hægt að ljúka bakfærslu ef hún er bókuð á opnu fjárhagstímabili.

- Samstæða:

    - Hægt er að bakfæra samstæðufærslur en aðeins af síðunni **Samstæðufærslur**.
    - Aðeins er hægt að ljúka bakfærslu ef hún er bókuð á opnu fjárhagstímabili.

- Árslokalokun:

    - Hægt er að bakfæra færslur árslokalokunar (bæði lokunar- og opnunarfærslur) á eftirfarandi hátt:

        - Ef slökkt er á eiginleikanum fyrir bætta árslokalokun fjárhagsbókar skal velja valkostinn **Afturkalla fyrri lokun** í svarglugganum **Árslokalokun**.
        - Ef kveikt er á eiginleika fyrir bætta árslokalokun fjárhagsbókar skal velja fyrirtækið og færslur reikningsárs sem voru stofnaðar fyrir árslokalokunina á síðunni **Árslokalokun** og síðan velja **Bakfæra árslokalokun**.

    - Athugaðu að bakfærsla árslokalokunar eyðir lokunar- og opnunarfærslunum. Bakfærsla er aldrei bókuð.

## <a name="accounts-payable"></a>Viðskiptaskuldir

Fjölmargar færslugerðir uppfæra undirbók viðskiptaskulda. Sem dæmi má nefna reikninga lánardrottna, reikningabækur lánardrottna og kostnaðarskýrslur.

Ef slökkt er á eiginleika fjöldabakfærslu er hægt að bakfæra hverja færslu fyrir sig á annaðhvort síðunni **Lánardrottnafærslur** fyrir reikninga eða á síðunni **Bankareikningur** fyrir greiðslur með ávísun.

Ef kveikt er á eiginleika fjöldabakfærslu verður hægt að bakfæra eina eða fleiri færslur viðskiptaskulda á síðunni **Færslur fylgiskjals** og úr færslubókinni þar sem færslurnar voru bókaðar. Enn er þó aðeins hægt að bakfæra greiðslur lánardrottna af bankareikningnum. Þar að auki er ekki hægt að bakfæra lánardrottnafærslur á síðunni **Færslur fyrir \<main account\>** fyrir fjárhagsbókina. Aðeins er hægt að bakfæra þær á síðunni **Færslur fylgiskjals**.

Athugaðu að sumar færslur er alls ekki hægt að bakfæra. Sem dæmi má nefna reikninga vegna innkaupapöntunar lánardrottins og rafrænar greiðslur lánardrottins.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Ástæður fyrir því að ekki er hægt að bakfæra fylgiskjöl

Af eftirfarandi ástæðum er ekki hægt að bakfæra fylgiskjöl:

- Fjárhagstímabilið er í bið eða lokað:

    - Ef bakfærsludagsetning er á fjárhagstímabili sem er ekki opið er ekki hægt að bakfæra færsluna.
    - Ef færslan styður innslátt bókunardagsetningar verður enn hægt að bakfæra færsluna með því að breyta bakfærsludagsetningunni til að opna tímabil.

- Ferli árslokalokunar fjárhags hefur verið keyrt:

    - Dagsetning reikningsskila fyrir færsluna er á reikningsári sem hefur verið lokað í fjárhag. Þrátt fyrir að tímabil á reikningsárinu gæti enn verið opið er ekki hægt að bakfæra færsluna ef ferli árslokalokunar hefur verið keyrt fyrir reikningsárið. Reikningsárið hefur aðra stöðu en tímabilin í því.
    - Hægt er að bakfæra árslokalokun og síðan er hægt að bakfæra færsluna. Þessi aðferð gæti ekki verið valkostur. Það gæti verið auðveldara að fara handvirkt inn í bakfærslu á opnu tímabili annaðhvort lokaða fjárhagsársins eða næsta fjárhagsárs, allt eftir stöðu fjárhagslokunar. Ef ný færsla er bókuð til að opna tímabil á reikningsárinu sem hefur farið í gegnum ferli árslokalokunar þarf að keyra árslokalokunina aftur.

- Færsla í undirbók hefur ekki verið flutt í almenna færslubók:

    - Þessi ástæða á aðeins við um lánardrottnareikninga sem tengjast ekki innkaupapöntun.
    - Nota skal **Færslur undirfjárhags sem hafa enn ekki verið fluttar** síðuna til að flytja færsluna í fjárhag. Lánardrottnareikningur sem tengist ekki innkaupapöntun getur þá verið bakfærður á síðunni **Lánardrottnafærslur**.

- Jöfnun:

    - Færslan (svo sem reikningur eða greiðsla) er gerð upp eða merkt til jöfnunar.

        - Þú getur staðfest hvort færsla er gerð upp eða merkt til jöfnunar með því að velja **Skoða uppgjör** eða **Uppgjör \> Uppgjörssaga** á síðunni **Lánardrottnafærslur**.
        - Einnig er hægt að bakfæra jöfnun á síðunni **Lánardrottnafærslur** (**Jöfnun \> Afturkalla jöfnun**) ef þarf að bakfæra eina færsluna.

- Kóðinn inniheldur meira en eina færslu undirbókar sem var færð inn með því að nota sama fylgiskjalsnúmerið (ein útgáfa fylgiskjals).
- Reikningurinn hefur ekki verið samþykktur:

    - Ef gátreiturinn **Samþykki** er ekki valinn á reikningnum verður ekki hægt að bakfæra reikninginn.

        - Í þessu tilviki vísar samþykki ekki til samþykkis í verkflæðisferli heldur í valkostinn **Samþykki** á reikningnum. Þessi valkostur er notaður til að koma í veg fyrir að reikningur sé greiddur. Hann er yfirleitt notaður fyrir reikninga komubókar lánardrottins.

- Færslan er í reikningasafninu:

    - Ekki er hægt að bakfæra reikning í safninu beint af síðunni **Lánardrottnafærslur**. Þess í stað verður að afturkalla hann í gegnum afturköllunarferlið á síðunni **Færslubók reikningssamþykkis**.

- Færslan er með yfirreikning sem hefur verið leiðréttur (indversk staðfærsla).
- Færslan er með víxilstöðuna **Reikningur greiddur**.
- Færslan er notuð fyrir hlutaskattuppgjör.
- Færslan inniheldur lánardrottnalykil en er bakfærð á rangri síðu eins og síðunni **Færslur fyrir \<main account\>**:

    - Eins og þessi ástæða gefur til kynna, jafnvel þegar kveikt er á eiginleika fjöldabakfærslu, er aðeins hægt að bakfæra sumar færslur undirbókar af ákveðnum síðum.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Tegundir færslna sem ekki er hægt að bakfæra

Ekki er hægt að bakfæra eftirfarandi gerðir færslna:

- Endurmat á erlendum gjaldmiðli:

    - Ólíkt endurmati á erlendum gjaldmiðli fjárhags er ekki hægt að bakfæra endurmat á erlendum gjaldmiðli fyrir viðskiptakröfur og viðskiptaskuldir. Í staðinn þarf að keyra endurmatið aftur með því að nota reikningsdagsetninguna. Í þessu tilviki notar endurmatið gengið frá dagsetningu reikningsins og færir í meginatriðum óinnleystan hagnað eða tap í 0 (núll). Þar af leiðandi líkist niðurstaðan niðurstöðu þess að bakfæra fyrra endurmat. Athugaðu þó að sama upphæð verður ekki bakfærð ef sjálfgefnu gengi var breytt á reikningnum.

- Reikningur vegna innkaupapöntunar lánardrottins:

    - Stofna þarf kreditnótu til að bakfæra reikning seljanda. Frekari upplýsingar um hvernig á að stofna bakfærslu er að finna í [Stofna innkaupaskilapöntun](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- Eigin víxill
- Bankaábyrgð útflutningssendingar

## <a name="accounts-receivable"></a>Viðskiptakröfur

Nokkrar færslugerðir uppfæra undirbækur viðskiptakrafna. Sem dæmi má nefna reikninga viðskiptavina úr sölupöntun, reikninga viðskiptavina sem eru færðir inn í gegnum almennu færslubókina, reikninga með frjálsum texta, greiðslur frá viðskiptavinum og afskriftir.

Ef slökkt er á eiginleika fjöldabakfærslu er hægt að bakfæra hverja færslu fyrir sig á annaðhvort síðunni **Færslur viðskiptavinar** fyrir reikninga eða á síðunni **Bankareikningur** fyrir greiðslur með ávísun. Nánari upplýsingar um hvernig á að bakfæra greiðslu er að finna í hlutanum [Reiðufjár- og bankastjórnun](cant-reverse-transctns.md#cash-and-bank-management).

Ef kveikt er á eiginleika fjöldabakfærslu verður hægt að bakfæra eina eða fleiri færslur viðskiptakrafna á síðunni **Færslur fylgiskjals** og úr færslubókinni þar sem færslurnar voru bókaðar. Hins vegar er enn hægt að bakfæra innborganir frá eingöngu bankareikningi og reikningar með frjálsum texta er aðeins hægt að bakfæra af upprunalegu síðunni (ef kveikt er á eiginleikanum sem leyfir leiðréttingar). Þar að auki er enn ekki hægt að bakfæra færslur viðskiptavina á síðunni **Færslur fyrir \<main account\>** fyrir fjárhagsbókina. Hins vegar er hægt að bakfæra þær af síðunni **Færslur fylgiskjals**.

Athugaðu að ekki er hægt að bakfæra sumar færslur. Sem dæmi má nefna sölupöntunarreikninga viðskiptavina og afskriftir.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Ástæður þess að ekki er hægt að bakfæra færslur

Af eftirfarandi ástæðum er ekki hægt að afturkalla færslur:

- Fjárhagstímabilið er í bið eða lokað varanlega:

    - Ef bakfærsludagsetning er á fjárhagstímabili sem er ekki opið er ekki hægt að bakfæra færsluna.
    - Ef færslan styður innslátt bókunardagsetningar verður enn hægt að bakfæra færsluna með því að breyta bakfærsludagsetningunni til að opna tímabil.

- Ferli árslokalokunar fjárhags hefur verið keyrt:

    - Dagsetning reikningsskila fyrir færsluna er á reikningsári sem hefur farið í gegnum árslokalokun fjárhags. Þrátt fyrir að tímabil á reikningsárinu gæti enn verið opið er ekki hægt að bakfæra færsluna ef ferli árslokalokunar hefur verið keyrt fyrir reikningsárið. Reikningsárið hefur aðra stöðu en tímabilin í því.
    - Hægt er að bakfæra árslokalokun og síðan er hægt að bakfæra færsluna. Þessi aðferð gæti ekki verið valkostur. Það gæti verið auðveldara að fara handvirkt inn í bakfærslu á opnu tímabili annaðhvort lokaða fjárhagsársins eða næsta fjárhagsárs, allt eftir stöðu fjárhagslokunar. Ef ný færsla er bókuð til að opna tímabil á reikningsárinu sem hefur farið í gegnum ferli árslokalokunar þarf að keyra árslokalokunina aftur.

- Færsla í undirbók hefur ekki verið flutt í almenna færslubók:

    - Þessi ástæða á aðeins við um reikninga með frjálsum texta.
    - Nota skal **Færslur undirfjárhags sem hafa enn ekki verið fluttar** síðuna til að flytja færsluna í fjárhag. Síðan er hægt að afturkalla eða leiðrétta reikninginn með frjálsum texta ef leiðréttingaraðgerðin er virk.

- Jöfnun:

    - Færslan (svo sem reikningur eða greiðsla) er gerð upp eða merkt til jöfnunar.

        - Þú getur staðfest hvort færsla er gerð upp eða merkt til jöfnunar með því að velja **Skoða uppgjör** eða **Uppgjör \> Uppgjörssaga** á síðunni **Viðskiptavinafærslur**.
        - Einnig er hægt að bakfæra jöfnun á síðunni **Viðskiptavinafærslur** (**Jöfnun \> Afturkalla jöfnun**) ef þarf að bakfæra eina færsluna.

- Færslan inniheldur fleiri en eina færslu undirbókar sem var færð inn með því að nota sama fylgiskjalsnúmerið (ein útgáfa fylgiskjals).
- Reikningurinn hefur ekki verið samþykktur:

    - Ef gátreiturinn **Samþykki** er ekki valinn á reikningnum verður ekki hægt að bakfæra reikninginn.

        - Í þessu tilviki vísar samþykki ekki til samþykkis í verkflæðisferli heldur í valkostinn **Samþykki** í línum fylgiskjals. Þessi valkostur er notaður til að koma í veg fyrir að reikningur sé greiddur. Þrátt fyrir að þessi valkostur sé almennt notaður í viðskiptaskuldum er hann einnig í boði fyrir reikninga viðskiptakrafna sem eru færðir inn í gegnum færslubækur.

- Færslan er með yfirreikning sem hefur verið leiðréttur (indversk staðfærsla).
- Færslan inniheldur viðskiptavinalykil en er bakfærð á rangri síðu eins og síðunni **Færslur fyrir \<main account\>**:

    - Eins og þessi ástæða gefur til kynna, jafnvel þegar kveikt er á eiginleika fjöldabakfærslu, er aðeins hægt að bakfæra sumar færslur undirbókar af ákveðnum síðum.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Tegundir færslna sem ekki er hægt að bakfæra

Ekki er hægt að bakfæra eftirfarandi gerðir færslna:

- Endurmat á erlendum gjaldmiðli:

    - Ólíkt endurmati á erlendum gjaldmiðli fjárhags er ekki hægt að bakfæra endurmat á erlendum gjaldmiðli fyrir viðskiptakröfur og viðskiptaskuldir. Í staðinn þarf að keyra endurmatið aftur með því að nota reikningsdagsetninguna. Í þessu tilviki notar endurmatið gengið frá dagsetningu reikningsins og færir í meginatriðum óinnleystan hagnað eða tap í 0 (núll). Þar af leiðandi líkist niðurstaðan niðurstöðu þess að bakfæra fyrra endurmat. Athugaðu þó að sama upphæð verður ekki bakfærð ef sjálfgefnu gengi var breytt á reikningnum.

- Færsla sem hefur leiðrétt staðgreiðsluskatt
- Samstæðureikningur viðskiptavinar:

    - Stofna þarf kreditnótu eða skil til að bakfæra færsluna. Frekar upplýsingar um hvernig á að stofna eða bakfæra færslu er að finna í [Skil á vörum](../../supply-chain/warehousing/sales-returns.md).

- Víxill
- Peningagreiðslur afgreiðslukassa
- Leiðrétting fyrirframgreiðslu
- Vaxtanóta
- Innheimtubréf
- Bankaábyrgð
- Útflutningur
- Færslubók tekjuskráningar:

    - Þegar þú skráir tekjur í gegnum tekjuskráningarbókina eru fylgiskjölin bókuð í fjárhagslykla. Þar af leiðandi birtast þau eins og þau séu aðeins fjárhagsfærslur. Ekki er hægt að bakfæra þessar færslur vegna þess að tekjuáætlunin verður ekki opnuð aftur til að greina tekjurnar aftur.

## <a name="cash-and-bank-management"></a>Reiðufjár- og bankastjórnun

Nokkrar færslugerðir uppfæra bankaundirbók í gegnum almennu færslubókina. Sem dæmi má nefna greiðslur til lánardrottna, greiðslur til viðskiptavina og millifærslur í banka.

Ef slökkt er á eiginleika fjöldabakfærslu er hægt að bakfæra hverja færslu fyrir sig á annaðhvort síðunni **Bankareikningar** fyrir ávísanir og innborganir eða á síðunni **Viðskiptavinafærslur** fyrir greiðslur viðskiptavina.

Ef kveikt er á eiginleika fjöldabakfærslu verður hægt að bakfæra eina eða fleiri greiðslufærslur á síðunni **Færslur fylgiskjals** og úr færslubókinni þar sem færslurnar voru bókaðar. Enn er þó aðeins hægt að bakfæra innborganir af bankareikningnum. Þar að auki er enn ekki hægt að bakfæra bankafærslur á síðunni **Færslur fyrir \<main account\>** fyrir fjárhagsbókina. Hins vegar er hægt að bakfæra þær af síðunni **Færslur fylgiskjals**.

Athugaðu að ekki er hægt að bakfæra sumar færslur. Sem dæmi má nefna rafrænar lánardrottnagreiðslur.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Ástæður þess að ekki er hægt að bakfæra færslur

Af eftirfarandi ástæðum er ekki hægt að afturkalla færslur:

- Fjárhagstímabilið er í bið eða lokað varanlega:

    - Ef bakfærsludagsetning er á fjárhagstímabili sem er ekki opið er ekki hægt að bakfæra færsluna.
    - Ef færslan styður innslátt bókunardagsetningar verður enn hægt að bakfæra færsluna með því að breyta bakfærsludagsetningunni til að opna tímabil.

- Ferli árslokalokunar fjárhags hefur verið keyrt:

    - Dagsetning reikningsskila fyrir færsluna er á reikningsári sem hefur farið í gegnum árslokalokun fjárhags. Þrátt fyrir að tímabil á reikningsárinu gæti enn verið opið er ekki hægt að bakfæra færsluna ef ferli árslokalokunar hefur verið keyrt fyrir reikningsárið. Reikningsárið hefur aðra stöðu en tímabilin í því.
    - Hægt er að bakfæra árslokalokun og síðan er hægt að bakfæra færsluna. Þessi aðferð gæti ekki verið valkostur. Það gæti verið auðveldara að fara handvirkt inn í bakfærslu á opnu tímabili annaðhvort lokaða fjárhagsársins eða næsta fjárhagsárs, allt eftir stöðu fjárhagslokunar. Ef ný færsla er bókuð til að opna tímabil á reikningsárinu sem hefur farið í gegnum ferli árslokalokunar þarf að keyra árslokalokunina aftur.

- Jöfnun:

    - Færslan (greiðslan) er jöfnuð eða merkt til jöfnunar.

        - Þú getur staðfest hvort færsla er gerð upp eða merkt til jöfnunar með því að velja **Skoða uppgjör** eða **Uppgjör \> Uppgjörssaga** á síðunni **Lánardrottnafærslur** eða síðunni **Viðskiptavinafærslur**.
        - Einnig er hægt að bakfæra jöfnun á síðunni **Lánardrottnafærslur** eða síðunni **Viðskiptavinafærslur** (**Jöfnun \> Afturkalla jöfnun**) ef þarf að bakfæra eina færsluna.

- Færslan inniheldur fleiri en eina færslu undirbókar sem var færð inn með því að nota sama fylgiskjalsnúmerið (ein útgáfa fylgiskjals).
- Færsla á millilykil:

    - Ef færslan tengist milligreiðslu er ekki hægt að bakfæra hana.
    - Ef bakfæra þarf milligreiðslu þarf fyrst að ganga frá greiðslunni af millilyklinum og til bankans. Þá er hægt að bakfæra greiðsluna að því gefnu að hún uppfylli hin skilyrðin fyrir staðfestingu.

- Færslan inniheldur bankareikning en er bakfærð af síðunni **Færslur fyrir \<main account\>** eða frá rangri undirbók eins og viðskiptakröfur eða viðskiptaskuldir:

    - Eins og þessi ástæða gefur til kynna, jafnvel þegar kveikt er á eiginleika fjöldabakfærslu, er aðeins hægt að bakfæra sumar færslur undirbókar af ákveðnum síðum.

- Bankaendurmat á erlendum gjaldmiðli

    - Hægt er að bakfæra bankaendurmat á erlendum gjaldmiðli. Hins vegar gæti verið hægt að koma í veg fyrir bakfærslu ef bakfærsluskrefin eru ekki gerð í réttri röð. Ef endurmatið var til dæmis framkvæmt í mars og apríl er ekki hægt að afturkalla endurmatið í mars fyrr en endurmatið í apríl er afturkallað.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Tegundir færslna sem ekki er hægt að bakfæra

Ekki er hægt að bakfæra eftirfarandi gerðir færslna:

- Greiðslur lánardrottna sem voru gerðar sem rafrænar kortamillifærslur (EFT)
- Eigin víxlar
- Víxlar

## <a name="fixed-assets"></a>Eignir

Nokkrar færslugerðir uppfæra eignaundirbókina. Sem dæmi má nefna kaup og afskriftir.

Ef slökkt er á eiginleika fjöldabakfærslu er hægt að bakfæra hverja færslu fyrir sig á síðunni **Lánardrottnafærslur**, á síðunni **Eignafærslur** eða úr eignarleigu, eftir því hver færslugerðin er.

Ef kveikt er á eiginleika fjöldabakfærslu verður hægt að bakfæra eina eða fleiri eignafærslur á síðunni **Færslur fylgiskjals** í færslubókinni þar sem færslurnar voru bókaðar.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Ástæður þess að ekki er hægt að bakfæra færslur

Af eftirfarandi ástæðum er ekki hægt að afturkalla færslur:

- Fjárhagstímabilið er í bið eða lokað varanlega:

    - Ef bakfærsludagsetning er á fjárhagstímabili sem er ekki opið er ekki hægt að bakfæra færsluna.
    - Ef færslan styður innslátt bókunardagsetningar verður enn hægt að bakfæra færsluna með því að breyta bakfærsludagsetningunni til að opna tímabil.

- Ferli árslokalokunar fjárhags hefur verið keyrt:

    - Dagsetning reikningsskila fyrir færsluna er á reikningsári sem hefur verið lokað í fjárhag. Þrátt fyrir að tímabil á reikningsárinu gæti enn verið opið er ekki hægt að bakfæra færsluna ef ferli árslokalokunar hefur verið keyrt fyrir reikningsárið. Reikningsárið hefur aðra stöðu en tímabilin í því.
    - Hægt er að bakfæra árslokalokun og síðan er hægt að bakfæra færsluna. Þessi aðferð gæti ekki verið valkostur. Það gæti verið auðveldara að fara handvirkt inn í bakfærslu á opnu tímabili annaðhvort lokaða fjárhagsársins eða næsta fjárhagsárs, allt eftir stöðu fjárhagslokunar. Ef ný færsla er bókuð til að opna tímabil á reikningsárinu sem hefur farið í gegnum ferli árslokalokunar þarf að keyra árslokalokunina aftur.

- Kaup:

    - Ef kaupin áttu sér stað á reikningi söluaðila fyrir innkaupapöntun verður hún að ganga til baka með því að slá inn inneignarnótu söluaðila. Til að fá upplýsingar um hvernig á að slá inn viðsnúningsfærsluna má finna í [Stofnun innkaupaskilapöntunar](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - Kaupin áttu sér stað í verkfærslu.
    - Ekki er hægt að bakfæra kaupin eftir að afskriftir eru bókaðar fyrir eignina. Bakfæra þarf afskriftina áður en hægt er að bakfæra kaupin.
    - Ef staða virðislíkans eða afskriftarbókar fyrir eign er ekki opin verður ekki hægt að bakfæra færsluna.

- Losanir:

    - Losunin fer fram í gegnum reikning með frjálsum texta:

        - Lokað er fyrir leiðréttingu á reikningi með frjálsum texta ef hann inniheldur eign. Ef eignin er hinsvegar afskráð í færslubók verður ekki hægt að bakfæra reikning með frjálsum texta úr eignafærslunni.

    - Ef staða virðislíkans eða afskriftarbókar fyrir eign er ekki opin verður ekki hægt að bakfæra færsluna.

- Afskrift:

    - Afskriftina **má** bakfæra ef tilheyrandi afskrift er einnig bókuð. Hinsvegar færðu viðvörun vegna þess að þessi aðferð er ekki sú besta.
    - Ef staða virðislíkans eða afskriftarbókar fyrir eign er ekki opin verður ekki hægt að bakfæra færsluna.

- Færslur (eða bakfærslur) fyrir tiltekna eign og eignabók eru til fyrir færsludagsetningu fylgiskjalsins eða síðar.
- Færslan inniheldur eignalykil en er bakfærð af síðunni **Færslur fyrir \<main account\>** eða frá rangri undirbók eins og viðskiptakröfur eða viðskiptaskuldir:

    - Eins og þessi ástæða gefur til kynna, jafnvel þegar kveikt er á eiginleika fjöldabakfærslu, er aðeins hægt að bakfæra sumar færslur undirbókar af ákveðnum síðum.
    - Ef kaup eiga sér stað fyrir lánardrottnareikning sem tengist ekki innkaupapöntun eða fyrir reikningabók lánardrottins, er aðeins hægt að bakfæra þau af síðunni **Lánardrottnafærslur** í viðskiptaskuldum.
    - Ef eign er keypt af eignarleigu er hægt að bakfæra kaupin af síðunni **Skuldafærslur** í eignarleigu.
