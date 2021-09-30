---
title: Stjórna frádráttum með frádráttarvinnusvæðinu
description: Þetta efnisatriði lýsir hvernig á að nota frádráttarvinnusvæði til að vinna úr greiðslum viðskiptavina með frádrætti .
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: bf98529176fbed368708ea925f542a70f2936037
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500403"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Stjórna frádráttum með frádráttarvinnusvæðinu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að nota frádráttarvinnusvæði til að vinna úr greiðslum viðskiptavina með frádrætti .

Viðskiptavinur sem er á inni eftirágreiddan afslátt getur ákveðið að bíða ekki eftir að útborgun eftirágreidds afsláttar. Þess í stað getur viðskiptavinurinn sent greiðslu sem inniheldur frádrátt fyrir upphæð eftirágreidds afsláttar. Til að meðhöndla þessa gerð færslu, er hægt að nota frádráttarvinnusvæði til að jafna frádrætti til að opna kreditfærslur, skipta frádrætti, hafna frádrætti og afskrifa frádrátt.

> [!NOTE]
> Frádráttarvinnusvæðið hefur verið hluti af sölu- og markaðsaðgerðum í Microsoft Dynamics 365 Supply Chain Management í mjög langan tíma. Hins vegar hefur það nú verið aukið þannig að það virkar einnig með nýrri einingu **Stjórnunar eftirágreidds afsláttar**. Í þessu efnisatriði er lýst hvernig á að nota bæði eldri eiginleika og eiginleika vegna stjórnunar eftirágreidds afsláttar á frádráttarvinnusvæðinu. Ef þú hefur hins vegar ekki [kveikt á einingu **Stjórnunar eftirágreidds afsláttar** fyrir kerfið](rebate-management-enable.md) verða sumar aðgerðirnar sem er lýst hér ekki í boði fyrir þig.

## <a name="prerequisites"></a>Forkröfur

### <a name="set-up-the-old-deduction-management-system"></a>Uppsetning á gamla kerfi frádráttarstjórnunar

Þú getur notað frádráttarvinnusvæðið ásamt gömlu frádráttarstjórnunarmöguleikunum í Supply Chain Management, jafnvel þótt þú sért ekki að nota eininguna **Stjórnun eftirágreidds afsláttar**. Hins vegar þarf fyrst að undirbúa kerfið eins og lýst er í þessum hluta.

Áður en þú getur notað vinnusvæði verður þú að ljúka uppsetningarverkum sem er lýst í [Setja upp frádráttarstjórnun](/dynamicsax-2012/appuser-itpro/set-up-deduction-management). Einnig ætti að hafa einhvers konar samning um eftirágreiddan afslátt sem er settur upp fyrir viðskiptavin: annaðhvort eftirágreiddan afslátt viðskiptavinar, eins og lýst er í [Uppsetning og viðhald á eftirágreiddum afslætti viðskiptavinar](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates), eða eftirágreiddan afslátt.

Ef nota á frádrátt á eftirágreiddan afslátt viðskiptavinar þarf að ljúka þessum verkum:

- [Setja upp eftirágreidda afslætti viðskiptavinar](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- Samþykktu og afgreiddu eftirágreiddan afslátt svo þú getir notað frádráttarvinnusvæðið.

Ef nota á frádrátt á afslátt eftirágreidds afsláttar þarf að ljúka þessum verkum:

- Setja upp bakfærsluafslætti.
- Beita sér fyrir niðurgreiðslum á reikningum.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Stilla viðskiptakröfur og frádrætti

Kerfið skráir frádráttartilvik í kröfubók. Því verður kerfið þitt að innihalda dagbók sem hægt er að nota í þessum tilgangi. Ef þú ert ekki með kröfubók skaltu setja hana upp núna. Þessi færslubók er nauðsynleg til að búa til frádrætti beint á frádráttarvinnusvæðið, jöfnun viðskiptavinar eða síðu viðskiptavinar.

Til að setja upp nýja kröfudagbók fyrir frádrátt skal fylgja þessum skrefum.

1. Farðu í **Fjárhag \> Færslubókaruppsetning \> Færslubókarheiti**.
1. Veldu **Nýr** og stilltu eftirfarandi reiti fyrir nýja færslubókarheitið:

    - **Heiti** – Sláðu inn einkvæmt heiti fyrir kröfubókina.
    - **Lýsing** - Færðu inn lýsingu á nýju kröfubókinni.
    - **Færslubókargerð** – Veldu *Daglega*.
    - **Fylgiskjalaruna** – Úthlutaðu fyrirliggjandi númeraröð. Einnig getur þú búið til nýja númeraröð sem hefur umfang fyrirtækis og úthlutað henni á nýja færslubókarheitið.

1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
1. Í flipanum **Frádrættir**, í flýtiflipanum **Almennt**, skal stilla reitinn **Heiti kröfubókar** á færslubókarheitið sem þú varst að búa til.
1. Í flýtiflipanum **Skilapöntun** stillirðu eftirfarandi reiti:

    - **Búa til skilapöntun** – Veldu þennan valkost til að tilgreina hvað kerfið á að gera þegar krafa byggð á magni er samþykkt:

        - *Já* – Stofna skilapöntun.
        - *Nei* – Stofna neikvæða sölupöntun.

    - **Stofnun án viðhengds reiknings** – Veldu gildi til að tilgreina hvað kerfið ætti að gera þegar krafa byggð á magni er samþykkt en enginn reikningur fylgir:

        - *Samþykkja* – Stofna skilapöntun.
        - *Viðvörun* – Búðu til skilapöntun, en sýndu eftirfarandi viðvörunarskilaboð: „Krafa er ekki tengd við reikning.“
        - *Villa* – Ekki búa til skilapöntun og sýndu eftirfarandi villuboð: „Krafa er ekki tengd við reikning. Hætt hefur verið við uppfærslu.

    - **Búa til skilapöntun á undan samþykki á frádrætti** – Stilltu þennan valkost á *Já* ef hægt er að búa til skilapantanir áður en krafan er samþykkt. Þessi stilling á aðeins við um magnbundnar kröfur þar sem valkosturinn **Búa til skilapöntun** er stilltur á *Já*.

### <a name="configure-general-ledger-parameters"></a>Skilgreina fjárhagsfæribreytur

Þegar kerfið býr til kröfubók fyrir nýjan frádrátt býr það einnig til tvær nýjar færslur fyrir viðskiptavini: eina til að jafna upphæð kröfunnar á móti upphaflegum reikningi og eina til að skrá skuld viðskiptavinar vegna kröfuupphæðarinnar (vegna þess að krafan hefur ekki enn verið samþykkt). Því þarf að setja kerfið upp þannig að eitt fylgiskjal geti haft margar þjónustulínur.

Til að virkja eitt fylgiskjal á að hafa margar línur viðskiptavina, fylgja þessum skrefum.

1. Farðu í **Fjárhag \> Fjárhagsuppsetning \> Fjárhagsfæribreytur**.
1. Í flipanum **Fjárhagur**, í flýtiflipanum **Almennt**, skal stilla valkostinn **Leyfa margar færslur í einu fylgiskjali** á *Já*.
1. Ef þú færð viðvörunarboð skaltu velja **Loka** til að samþykkja breytinguna.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Búa til frádráttarástæður

Kerfið krefst þess að notendur tilgreini ástæðu fyrir hverjum frádrætti sem þeir slá beint inn á frádráttarvinnusvæðið, jöfnun viðskiptavinar eða síðu viðskiptavinar. Ástæðan ákvarðar hvernig farið er með frádráttinn þegar hann er samþykktur.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Ástæður frádrátta**.
1. Veldu **Ný** til að bæta línu við hnitanetið og stilltu síðan eftirfarandi reiti fyrir hana:

    - **Ástæða kröfu** – Sláðu inn einkvæmt heiti fyrir ástæðuna.
    - **Lýsing** – Sláið inn lýsingu hópsins til að veita frekari upplýsingar um hvernig á að nota hann.
    - **Kröfugrunnur** – Veldu kröfugrunn fyrir ástæðu kröfunnar:

        - *Byggt á verði* – Stofnaðu kreditreikning með frjálsum texta við samþykki.
        - *Byggt á magni* – Stofnaðu neikvæða sölupöntun eða skilapöntun við samþykki.

    - **Ástæðukóði skila** – Veldu ástæðukóða skila til að nota sem gildi fyrir **Ástæðukóða skila** fyrir skilapöntunina.
    - **Gerð** – Veljið frádráttargerð. Gildið **Mótbókun frádráttar** fyrir valda gerð verður notað til að stilla reitinn **Mótbókun frádráttar** þegar frádráttur eða krafa er búið til. Frádráttargerðir eru skilgreindar á síðunni **Frádráttargerðir** (**Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttargerðir**).
    - **Bókunarlykill kröfu** – Þessi reitur er aðeins í boði þegar reiturinn **Grundvöllur kröfu** er stilltur á *Byggt á verði*. Þegar verðbundin krafa er samþykkt úthlutar kerfið fjárhagslyklum sem þú velur hér sem gildið **Aðallykill** fyrir drög að kreditnótu með frjálsum texta.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>Setja upp og ganga frá samþykktum drögum að reglulegu verkefni

Fyrir frádrætti sem eru stofnaðir með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptainvar geturðu sett upp reglubundna verkið *Gera upp samþykkta frádrætti* til að sjálfkrafa jafna frádrætti og kreditfærslur sem eru með samsvarandi gildi og upphæðir fyrir **Frádráttarkenni**.

Til að tímasetja þetta verk skal fara í **Sala og markaðssetning \> Reglubundin verk \> Gera upp samþykkta frádrætti** og setja upp valkosti, síur og áætlun rétt eins og fyrir aðrar gerðir af reglubundnum verkum.

> [!NOTE]
> Ef valkosturinn **Sjálfvirk jöfnun** er stilltur á *Já* í flipanum **Jöfnun** á síðunni **Færibreytur viðskiptakrafna** (**Viðskiptakröfur \> Uppsetning \> Færibreytur viðskiptakrafna**) mun reglubundna verkið *Gera upp samþykkta frádrætti* ekki gera neitt vegna þess að kreditfærslan verður sjálfkrafa jöfnuð.

## <a name="create-a-deduction"></a>Búa til frádrátt

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Búa til frádráttardagbókarfærslu með því að nota greiðslubók viðskiptavinar

Fylgið eftirfarandi skrefum til að stofna færslu í færslubók frádráttar.

1. Farið í **Viðskiptakröfur \> Greiðslur \> Greiðslubók viðskiptavinar**.
1. Veldu **Ný** til að bæta línu við hnitanetið.
1. Í reitnum **Heiti** fyrir nýju línuna skal velja heiti færslubókarinnar.
1. Á aðgerðasvæðinu skal velja **Línur**.
1. Sláðu inn dagsetningu, fyrirtækjaaðgang og númer viðskiptavinalykils.
1. Í því **Reikningsfæra** reitnum skal velja reikninginn sem frádráttur er tengd við.
1. Í reitnum **Kredit** skal færa inn upphæðina sem viðskiptavinur greiddi.
1. Veldu **Í lagi** til að staðfesta að upphæðin sé undir heildarupphæð merktu færslunnar.
1. Veljið gerð mótlykils og mótlykil.
1. Á tækjastikunni fyrir ofan netið velurðu **Frádráttur**.
1. Á síðunni **Frádráttur**, á aðgerðasvæðinu, skal velja **Nýtt** til að bæta við röð við hnitið. Reiturinn **Frádráttarkenni** fyrir nýju línuna er sjálfkrafa stilltur.
1. Í reitnum **Gerð** skal velja frádráttargerðina.
1. Í reitinn **Upphæð** skal færa inn upphæðina sem kemur fram í reitnum **Staða** fyrir neðan frádráttarlistann. Þessi upphæð endurspeglar upphæð sem viðskiptavinur dregur frá greiðslu.
1. Lokaðu **Frádráttarsíðunni**. Þér er vísað aftur á síðuna **Greiðslur viðskiptavina** sem nú sýnir nýja línu fyrir frádráttinn.
1. Á aðgerðasvæðinu skal velja **Villuleita \> Villuleita**. Þú ætir að fá eftirfarandi skilaboðum: "Færslubók er í lagi."
1. Á aðgerðasvæðinu skal velja **Bóka**.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Búa til frádrátt með því að nota frádráttarvinnusvæðið

Til að búa til nýjan frádrátt á frádráttarvinnusvæðinu skal fylgja þessum skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Í aðgerðasvæðinu skal velja **Vinna með \> Nýr frádráttur**.

    Í svarglugganum **Nýr frádráttur** er reiturinn **Frádráttarkenni** stilltur samkvæmt númeraröð **Frádráttarkennis** sem er skilgreind á síðunni **Stjórnun á færibreytum fyrir afslátt** (**Sala og markaðssetning \> Uppsetning \> Afsláttur \> Stjórnun á færibreytum fyrir afslátt**).

1. Stilltu eftirfarandi svæði:

    - **Viðskiptavinalykill** – Veldu viðskiptavinalykil sem frádrátturinn gildir um.
    - **Utanaðkomandi kröfunúmer** – Sláðu inn kröfutilvísun viðskiptavinar.
    - **Kröfufjárhæð** – Færðu inn kröfufjárhæð með skatti. Gildið verður að vera jákvæð tala.
    - **Gjaldmiðill** – Veldu gjaldmiðil fyrir frádráttinn. Sjáfgefna gildið er gjaldmiðillinn sem er stilltur fyrir valinn viðskiptavinaraðgang.
    - **Kröfugrunnur** – Veldu kröfugrunn. Grundvöllur kröfu ákvarðar hvers konar kreditfærsla er stofnuð eftir að frádráttur eða krafa er samþykkt.

        - *Byggt á verði* – Búin verða til drög að reikningi með frjálsum texta.
        - *Magnbundin* – Neikvæð sölupöntun eða skilapöntun verður til.

    - **Dagsetning kröfu** – Veljið dagsetningu kröfunnar. Sjálfgefna gildið er dagurinn í dag.
    - **Ástæða kröfu** – Veldu ástæðukóðann sem á við um núverandi frádrátt. Sá kröfugrunnur sem þú valdir hefur áhrif á valkostina sem gilda. Nánari upplýsingar um hvernig stofna á og stilla ástæður kröfu sem er hægt að velja hér er að finna í hlutanum [Búa til frádráttarástæður](#deduction-reasons) fyrr í þessu efnisatriði.
    - **Athugasemdir** – Bættu við athugasemdum sem eiga við. Þegar krafan er samþykkt getur samþykkjandinn breytt eða bætt við athugasemdum við kröfuna.
    - **Búa til kröfudagbók** – Veldu þennan valkost til að tilgreina hvort kröfudagbókin eigi að vera búin til þegar krafan eða frádrátturinn er búinn til:

        - *Já* – Kerfið mun búa til og bóka færslubók með því að nota kröfubókina sem er sett upp á síðunni **Færibreytur viðskiptakrafna**. (Frekari upplýsingar eru í hlutanum [Stilla viðskiptakröfur og frádrátt](#accounts-receivable-deductions) fyrr í þessu efnisatriði.) Þegar reikningur er festur við kröfuna er kröfubókin notuð til að lækka stöðu viðkomandi reiknings. Ef kröfunni er síðar hafnað verður kröfubókin og jafnanirnar (ef reikningur var hengdur við) bakfærðar.
        - *Nei* – Engin kröfubók er búin til á þessum tímapunkti. Hún verður stofnuð þegar krafan er samþykkt. Enn er hægt að tengja reikning við nýju kröfuna þrátt fyrir að kröfudagbók sé ekki búin til. Hins vegar er ekki hægt að gera upp án kröfudagbókarinnar.

1. Veldu **Í lagi**.

    Nýr frádráttur er stofnaður. Ef þú stillir valkostinn **Búa til kröfubók** á *Já* eru eftirfarandi færslur bókaðar:

    - **Tvær nýjar færslur viðskiptavinar** – Ein færsla jafnar upphæð kröfunnar á móti upprunalega reikningnum. Hin færslan skráir skuld viðskiptavinar að upphæð kröfunnar vegna þess að krafan hefur ekki enn verið samþykkt. Upprunalega reikningsfærslan og jöfnuð kröfufærsla verða sjálfkrafa merktar til jöfnunar þegar þú festir reikninginn með því að velja **Vinna með \> Hengja við reikning** á aðgerðasvæðinu.
    - **Tvær jöfnunarfærslur** – Þessar færslur eru bókaðar á fjárhagslyklinum **Mótbókun frádráttar**.
    - **Kröfubók** – Til að skoða kröfubókina fyrir hvern frádrátt sem er sýndur á frádráttarvinnusvæðinu skal velja flipann **Tilvísanir**. Kröfubókin er sýnd í reitnum **Rununúmer færslubókar**. Einnig er hægt að skoða kröfubókina í flipanum **Frádráttartilvik**. Þar fær hún gildi fyrir **Uppfærslugerð** sem er *Jafna*.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Stofna frádrátt frá uppgjöri viðskiptamanns

Ferlið við að búa til frádrátt úr jöfnun viðskiptavinar líkist ferlinu við að búa til frádrátt í gegnum frádráttarvinnusvæðið. Viðskiptavinurinn og reikningsgjaldmiðillinn eru hins vegar sjálfkrafa stillt og reikningurinn fylgir með. Þú þarft ekki að velja **Vinna með \> Hengja við reikning** á aðgerðasvæðinu þegar þú stofnar kröfu eða frádrátt í gegnum jöfnunarsíðu viðskiptavinar.

1. Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.
1. Veljið viðskiptavin sem stofna á frádrátt fyrir.
1. Á aðgerðasvæðinu, í flipanum **Innheimta**, í flokknum **Gera upp**, skal velja **Jafna færslur**.
1. Í svarglugganum **Færslur stilltar**, í flipanum **Yfirlit**, skal velja reikninginn til að búa til frádráttinn á móti.
1. Á tækjastikunni skal velja **Frádráttur \> Nýr frádráttur**.

    Í svarglugganum **Nýr frádráttur** er reiturinn **Frádráttarkenni** stilltur samkvæmt númeraröð **Frádráttarkennis** sem er skilgreind á síðunni **Stjórnun á færibreytum fyrir afslátt** (**Sala og markaðssetning \> Uppsetning \> Afsláttur \> Stjórnun á færibreytum fyrir afslátt**). Reiturinn **Viðskiptavinalykill** er stilltur á þann viðskiptavinalykil sem frádrátturinn á við um.

1. Stilltu eftirfarandi svæði:

    - **Utanaðkomandi kröfunúmer** – Sláðu inn kröfutilvísun viðskiptavinar.
    - **Kröfufjárhæð** – Færðu inn kröfufjárhæð með skatti. Gildið verður að vera jákvæð tala.
    - **Gjaldmiðill** – Veldu gjaldmiðil fyrir frádráttinn. Sjáfgefna gildið er gjaldmiðillinn sem er stilltur fyrir valinn viðskiptavinaraðgang.
    - **Kröfugrunnur** – Veldu kröfugrunn. Grundvöllur kröfu ákvarðar hvers konar kreditfærsla er stofnuð eftir að frádráttur eða krafa er samþykkt.

        - *Byggt á verði* – Búin verða til drög að reikningi með frjálsum texta.
        - *Magnbundin* – Neikvæð sölupöntun eða skilapöntun verður til.

    - **Dagsetning kröfu** – Veljið dagsetningu kröfunnar. Sjálfgefna gildið er dagurinn í dag.
    - **Ástæða kröfu** – Veldu ástæðukóðann sem á við um núverandi frádrátt. Sá kröfugrunnur sem þú valdir hefur áhrif á valkostina sem gilda. Nánari upplýsingar um hvernig stofna á og stilla ástæður kröfu sem er hægt að velja hér er að finna í hlutanum [Búa til frádráttarástæður](#deduction-reasons) fyrr í þessu efnisatriði.
    - **Athugasemdir** – Bættu við athugasemdum sem eiga við. Þegar krafan er samþykkt getur samþykkjandinn breytt eða bætt við athugasemdum við kröfuna.
    - **Búa til kröfudagbók** – Veldu þennan valkost til að tilgreina hvort kröfudagbókin eigi að vera búin til þegar krafan eða frádrátturinn er búinn til:

        - *Já* – Kerfið mun búa til og bóka færslubók með því að nota kröfubókina sem er sett upp á síðunni **Færibreytur viðskiptakrafna**. (Frekari upplýsingar eru í hlutanum [Stilla viðskiptakröfur og frádrátt](#accounts-receivable-deductions) fyrr í þessu efnisatriði.) Þegar reikningur er festur við kröfuna er kröfubókin notuð til að lækka stöðu viðkomandi reiknings. Ef kröfunni er síðar hafnað verður kröfubókin og jafnanirnar (ef reikningur var hengdur við) bakfærðar.
        - *Nei* – Engin kröfubók er búin til á þessum tímapunkti. Hún verður stofnuð þegar krafan er samþykkt. Enn er hægt að tengja reikning við nýju kröfuna þrátt fyrir að kröfudagbók sé ekki búin til. Hins vegar er ekki hægt að gera upp án kröfudagbókarinnar.

1. Veldu **Í lagi**.

    Nýr frádráttur er stofnaður. Ef þú stillir valkostinn **Búa til kröfubók** á *Já* eru eftirfarandi færslur bókaðar:

    - **Tvær nýjar færslur viðskiptavinar** – Ein færsla jafnar upphæð kröfunnar á móti upprunalega reikningnum. Hin færslan skráir skuld viðskiptavinar að upphæð kröfunnar vegna þess að krafan hefur ekki enn verið samþykkt. Upprunalega reikningsfærslan og jöfnuð kröfufærsla verða sjálfkrafa merktar til jöfnunar þegar þú festir reikninginn með því að velja **Vinna með \> Hengja við reikning** á aðgerðasvæðinu.
    - **Tvær jöfnunarfærslur** – Þessar færslur eru bókaðar á fjárhagslyklinum **Mótbókun frádráttar**.
    - **Kröfubók** – Til að skoða kröfubókina fyrir hvern frádrátt sem er sýndur á frádráttarvinnusvæðinu skal velja flipann **Tilvísanir**. Kröfubókin er sýnd í reitnum **Rununúmer færslubókar**. Einnig er hægt að skoða kröfubókina í flipanum **Frádráttartilvik**. Þar fær hún gildi fyrir **Uppfærslugerð** sem er *Jafna*.

    Þú hefur farið aftur á síðuna **Jafna færslur** sem sýnir nú valinn reikning sem merktan. Hnappurinn **Bóka** er aðeins í boði ef þú stilltir valkostinn **Stofna kröfubók** á *Já*. Ef hann er í boði skaltu velja **Bóka** til að lækka eftirstöðvarnar á reikningnum um því sem nemur gildi **Kröfuupphæðar**.

### <a name="create-a-deduction-from-a-customer-page"></a>Stofna frádrátt af síðu viðskiptavinar

Ferlið við að búa til frádrátt af síðu viðskiptavinar líkist ferlinu við að búa til frádrátt í gegnum frádráttarvinnusvæðið. Hins vegar er viðskiptavinurinn sjálfkrafa stilltur.

1. Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.
1. Veljið viðskiptavin sem stofna á frádrátt fyrir.
1. Á aðgerðasvæðinu, í flipanum **Innheimta**, í flokknum **Frádrættir**, skal velja **Búa til frádrátt**.

    Í svarglugganum **Nýr frádráttur** er reiturinn **Frádráttarkenni** stilltur samkvæmt númeraröð **Frádráttarkennis** sem er skilgreind á síðunni **Stjórnun á færibreytum fyrir afslátt** (**Sala og markaðssetning \> Uppsetning \> Afsláttur \> Stjórnun á færibreytum fyrir afslátt**). Reiturinn **Viðskiptavinalykill** er stilltur á þann viðskiptavinalykil sem frádrátturinn á við um.

1. Stilltu eftirfarandi svæði:

    - **Utanaðkomandi kröfunúmer** – Sláðu inn kröfutilvísun viðskiptavinar.
    - **Kröfufjárhæð** – Færðu inn kröfufjárhæð með skatti. Gildið verður að vera jákvæð tala.
    - **Gjaldmiðill** – Veldu gjaldmiðil fyrir frádráttinn. Sjáfgefna gildið er gjaldmiðillinn sem er stilltur fyrir valinn viðskiptavinaraðgang.
    - **Kröfugrunnur** – Veldu kröfugrunn. Grundvöllur kröfu ákvarðar hvers konar kreditfærsla er stofnuð eftir að frádráttur eða krafa er samþykkt.

        - *Byggt á verði* – Búin verða til drög að reikningi með frjálsum texta.
        - *Magnbundin* – Neikvæð sölupöntun eða skilapöntun verður til.

    - **Dagsetning kröfu** – Veljið dagsetningu kröfunnar. Sjálfgefna gildið er dagurinn í dag.
    - **Ástæða kröfu** – Veldu ástæðukóðann sem á við um núverandi frádrátt. Sá kröfugrunnur sem þú valdir hefur áhrif á valkostina sem gilda. Nánari upplýsingar um hvernig stofna á og stilla ástæður kröfu sem er hægt að velja hér er að finna í hlutanum [Búa til frádráttarástæður](#deduction-reasons) fyrr í þessu efnisatriði.
    - **Athugasemdir** – Bættu við athugasemdum sem eiga við. Þegar krafan er samþykkt getur samþykkjandinn breytt eða bætt við athugasemdum við kröfuna.
    - **Búa til kröfudagbók** – Veldu þennan valkost til að tilgreina hvort kröfudagbókin eigi að vera búin til þegar krafan eða frádrátturinn er búinn til:

        - *Já* – Kerfið mun búa til og bóka færslubók með því að nota kröfubókina sem er sett upp á síðunni **Færibreytur viðskiptakrafna**. (Frekari upplýsingar eru í hlutanum [Stilla viðskiptakröfur og frádrátt](#accounts-receivable-deductions) fyrr í þessu efnisatriði.) Þegar reikningur er festur við kröfuna er kröfubókin notuð til að lækka stöðu viðkomandi reiknings. Ef kröfunni er síðar hafnað verður kröfubókin og jafnanirnar (ef reikningur var hengdur við) bakfærðar.
        - *Nei* – Engin kröfubók er búin til á þessum tímapunkti. Hún verður stofnuð þegar krafan er samþykkt. Enn er hægt að tengja reikning við nýju kröfuna þrátt fyrir að kröfudagbók sé ekki búin til. Hins vegar er ekki hægt að gera upp án kröfudagbókarinnar.

1. Veldu **Í lagi**.

    Nýr frádráttur er stofnaður. Ef þú stillir valkostinn **Búa til kröfubók** á *Já* eru eftirfarandi færslur bókaðar:

    - **Tvær nýjar færslur viðskiptavinar** – Ein færsla jafnar upphæð kröfunnar á móti upprunalega reikningnum. Hin færslan skráir skuld viðskiptavinar að upphæð kröfunnar vegna þess að krafan hefur ekki enn verið samþykkt. Upprunalega reikningsfærslan og jöfnuð kröfufærsla verða sjálfkrafa merktar til jöfnunar þegar þú festir reikninginn með því að velja **Vinna með \> Hengja við reikning** á aðgerðasvæðinu.
    - **Tvær jöfnunarfærslur** – Þessar færslur eru bókaðar á fjárhagslyklinum **Mótbókun frádráttar**.
    - **Kröfubók** – Til að skoða kröfubókina fyrir hvern frádrátt sem er sýndur á frádráttarvinnusvæðinu skal velja flipann **Tilvísanir**. Kröfubókin er sýnd í reitnum **Rununúmer færslubókar**. Einnig er hægt að skoða kröfubókina í flipanum **Frádráttartilvik**. Þar fær hún gildi fyrir **Uppfærslugerð** sem er *Jafna*.

## <a name="create-a-credit-note-for-a-customer"></a>Búa til inneignarnótuna fyrir viðskiptavininn

Þegar samþykktur eftirágreiddur afsláttur er til fyrir viðskiptavininn getur þú stofnað kreditnótu á reikning viðskiptavinarins til að tákna eftirágreiddan afslátt eftir þörfum. Kreditfærslan birtist síðan á frádráttarvinnusvæðinu þar sem hægt er að jafna hana við frádrátt.

Til að stofna kreditnótu, skal fylgja eftirfarandi skrefum.

1. Opnið **Sölu og markaðssetning \> Viðskiptavinir \> Allir viðskiptavinir**.
1. Velja viðskiptavin.
1. Á aðgerðasvæðinu, í flipanum **Innheimta**, í flokknum **Gera upp**, skal velja **Jafna færslur**.
1. Í svarglugganum **Jafna færslur** skal velja færsluna sem eftirágreiddur afsláttur var notaður.
1. Á tækjastikunni, í valmyndinni **Aðgerðir**, er valin sú tegund afsláttaráætlunar sem á við.
1. Á síðunni **Eftirágreiddur afsláttur**, í flipanum **Yfirlit**, skal velja gátreitinn **Merkja** við hliðina á viðkomandi kenni eftirágreidds afsláttar.
1. Á aðgerðasvæðinu skal velja **Aðgerðir \> Stofna kreditnótu**.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Vinna úr frádrætti á frádráttarvinnusvæðinu

Í frádráttarvinnuvæði er hægt að jafna frádrátt við opnar kreditfærslur, skiptan frádrátt, afneitaðan frádrátt og afskrifaðan frádrátt.

Það fer eftir því hvernig á að vinna úr frádrætti hvort eigi að klára eitt eða fleiri af ferlunum í eftirfarandi undirhluta. Þú getur sameinað aðgerðirnar eftir þörfum. Til dæmis er hægt að skipta frádrætti í tvo hluta og jafna síðan einn hluta við kreditfærslu en skilja afganginn eftir á vinnusvæðinu svo hægt sé að jafna hann við aðra kreditfærslu síðar. Einnig er hægt getur jafna frádrátt á inneign sem er minni en upphæð frádráttar, og síðan hafna eða afskrifa eftirstandandi stöðu frádráttar.

### <a name="match-a-deduction-to-a-credit"></a>Jafna frádrátt við inneign

Til að jafna frádrátt við kreditfærslu skal fylgja þessum skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Veldu gátreitinn **Merkja** til að vinna úr frádrættinum.
1. Í hlutanum **Opnar færslur** skal velja gátreitinn **Merkja** til að kreditfærslan jafni út frádráttinn. Ef margar inneign eru skráðar er hægt að velja fleiri en einn kredit til að passa við frádráttinn. Ef kerfið ætti að velja sjálfkrafa kreditfærslur sem samsvara upphæð frádráttar er á tækjastikunni valinn viðeigandi valkostur í valmyndinni **Velja frádráttarupphæð**.
1. Í aðgerðasvæðinu skal velja **Vinna með \> Jafna**. Kerfið samsvarar frádrátt á kredit. Ef eftirstöðvar eru í frádrættinum eru þær sýndar í reitnum **Eftirstandandi upphæð** í flipanum **Frádrættir**.

    > [!NOTE]
    > Fyrir frádrætti sem voru búnir til með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptavinar er skipunin **Vinna með \> Jafna** aðeins í boði ef reiturinn **Staða kröfu** er stilltur á *Samþykkt*. Þessa skipun er hægt að nota til að jafna handvirkt verðbundna eða magnbundna færslu við viðkomandi kreditfærslu í hlutanum **Opnar færslur**. Kreditfærslan er stofnuð annaðhvort þegar frádrátturinn er samþykktur (með því að nota skipunina **Vinna með \> Samþykkja frádrátt**) eða þegar hún er tengd við fyrirliggjandi kreditfærslu eins og lýst er í hlutanum [Kreditfærslur stofnaðar utan við samþykktarferli frádráttar](#credits-outside-approval) síðar í þessu efnisatriði. Einnig er hægt að nota reglubundan verkið *Jafna samþykkta frádrætti* (**Sala og markaðssetning \> Reglubundin verk \> Jafna samþykkta frádrætti**) til að sjálfkrafa jafna frádrætti og kreditfærslur sem eru með samsvarandi gildi fyrir **Frádráttarkenni** og upphæðir.

### <a name="split-a-deduction"></a>Skipta frádrætti

Til að skipta frádrætti skal fylgja eftirfarandi skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Veldu gátreitinn **Merkja** til að vinna úr frádrættinum.
1. Á aðgerðasvæðinu skal velja **Vinna með \> Skipta**.
1. Í svarglugganum **Skipta**, í reitinn **Skipta upphæð**, skal færa inn upphæðina sem á að skipta af aðalfrádrættinum. Veljið síðan **Í lagi**.
1. Á flipanum **Frádráttur** skaltu athuga að ný færsla birtist fyrir skipta upphæð. Upprunalega frádráttarfærslan inniheldur eftirstöðvar frádráttarins. Nú er hægt að stjórna tveimur hlutum upprunalega eftirágreiddan afsláttarins sérstaklega.
1. Veldu upprunalegu frádráttarfærsluna og veldu síðan flipann **Tilvísanir**. Reiturinn **Skipta upphæð** sýnir upphæðina sem var tekin af upprunalegu upphæðinni.

### <a name="attach-an-invoice-to-a-deduction"></a>Festa reikning við frádrátt

Hægt er að hengja reikning við frádrátt ef frádrátturinn var búinn til með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptavinar og ef enginn reikningur er hengdur við hann eins og er (þ.e. dálkurinn **Reikningur** er auður).

Til að hengja reikning við frádrátt skal fylgja þessum skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Veldu gátreitinn **Merkja** til að vinna úr frádrættinum.
1. Á aðgerðasvæðinu skal velja **Vinna með \> Hengja við reikning**.
1. Í svarglugganum **Hengja við reikning** skal velja reikning og velja síðan **Í lagi**.
1. Í svarglugganum **Jafna færslur** skal fylgja einu af þessum skrefum, eftir því hvort kröfubók var bókuð þegar frádrátturinn var búinn til:

    - Ef kröfubók var bókuð sýna reikningurinn sem þú valdir og kreditfærsla viðskiptavinar í kröfubókinn gátmerki í dálknum **Merkja**. Veldu **Bóka**. Eftirstöðvar á meðfylgjandi reikningi lækka um kröfufjárhæðina.
    - Ef kröfubók var ekki bókuð sýnir engin færsla gátmerki í dálknum **Merkja**. Þar sem ekki er hægt að mótbóka gagnvart kröfubók fyrr en frádrátturinn hefur verið samþykktur skal velja **Hætta við**.

### <a name="detach-an-invoice-from-a-deduction"></a>Losa reikning af frádrætti

Hægt er að losa reikning frá frádrætti ef frádrátturinn var búinn til með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptavinar ef reikningur er þegar hengdur við hann (þ.e. dálkurinn **Reikningur** sýnir reikningsnúmer) og ef reiturinn **Staða kröfu** er stilltur á *Opin*. Þú gætir lokið þessu verkefni því rangur reikningur fylgdi með. Reikningurinn er fjarlægður úr frádrættinum og eftirstöðvar hans eru uppfærðar ef þær voru lækkaðar þegar reikningurinn var hengdur við.

Til að losa reikning skal fylgja eftirfarandi skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Veldu gátreitinn **Merkja** til að vinna úr frádrættinum.
1. Á aðgerðasvæðinu skal velja **Vinna með \> Losa reikning**.

### <a name="approve-a-deduction"></a>Samþykkja frádrátt

Þú getur samþykkt frádrátt sem var stofnaður með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptavinar. Hins vegar er aðeins hægt að samþykkja frádrátt þar sem reiturinn **Staða kröfu** er stilltur á *Opin*.

Til að samþykkja frádrátt skal fylgja eftirfarandi skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Veldu gátreitinn **Merkja** til að vinna úr frádrættinum.
1. Á aðgerðasvæðinu skal velja **Vinna með \> Samþykkja frádrátt**.
1. Svarglugginn **Samþykkja frádrátt** skal breyta eða bæta við upplýsingum við gildið **Nóta** eftir þörfum.
1. Ef frádrátturinn er byggður á verði og reikningur hefur ekki verið hengdur við hann skaltu velja VSK-flokk vöru. Venjulega er skatthlutfallið í hverjum hópi ákveðið á reikningnum. Því verður að tilgreina vöruskattkóða þegar hann er ekki hengdur við reikning.
1. Veldu **Í lagi**.

    Á þessum tímapunkti er ekki hægt að gera frekari breytingar á frádrættinum. Ef valkosturinn **Búa til kröfubók** var stilltur á *Nei* þegar frádrátturinn var búinn til er kröfubókin búin til og bókuð þegar frádrátturinn er samþykktur. Inneignin er sjálfkrafa stofnuð og opnuð eftir að frádrátturinn hefur verið samþykktur. Gerðin fer eftir gildinu fyrir **Grundvöll kröfu** í frádrættinum:

    - *Byggt á verði* – Ef frádrátturinn byggir á verði er stofnaður reikningur með frjálsum texta fyrir viðskiptareikninginn. Hægt er að bæta við lýsingu og bóka kreditfærslu. Eftirfarandi reitir eru fylltir út með frádrættinum þegar drögin eru búin til:

        - **Frádráttarkenni** – Þessu svæði er bætt við hausinn til að hægt sé að rekja til baka til frádráttar.
        - **Aðalreikningur** – Gildið ákvarðast af gildinu fyrir **Bókunarreikningur kröfu** sem er stilltur á ástæðu frádráttar sem er frádrættinum er úthlutað.
        - **VSK-flokkur vöru** – Gildið er ákvarðað af viðhengdum reikningi eða gildinu sem þú valdir þegar þú samþykktir frádráttinn.
        - **Einingaverð** – Gildið er kreditfærsla fyrir kröfuupphæð frádráttarins.
        - **Texti reiknings** – Reiturinn er sjálfgefið stilltur á gildið fyrir **Nótur** í frádrættinum.

    - *Byggt á magni* – Ef frádrátturinn er byggður á magni er stofnuð opin sölupöntun eða skilapöntun. Stillingin **Stofna skilapöntun** á síðunni **[Færibreytur viðskiptakrafna](#accounts-receivable-deductions)** ákvarðar hvort sölupöntun eða skilapöntun sé stofnuð þegar frádrátturinn er samþykktur. Síðan **Afrita pantanir** birtist og er síuð til að sýna línur þar sem reiturinn **Reikningslykill** er stilltur á viðskiptavinalykil frádráttarins. Fylgið eftirfarandi skrefum:

        1. Í flýtiflipanum **Reikningur** sýnir **Haushlutinn** sölureikninga þar sem gildið fyrir **Reikningslykil** samsvarar viðskiptavinalykil frádráttarins. Veljið viðeigandi sölureikning.
        1. **Línuhlutinn** sýnir línur úr völdum sölureikningi. Veldu gátreitinn **Velja** fyrir hverja línu sem á að afrita. Að öðrum kosti í hlutanum **Hausar** skal velja gátreitinn **Velja allt** fyrir sölupöntunina til að velja allar línur hennar.
        1. Breyttu **Magninu** fyrir eina eða fleiri línur eftir þörfum.

            Allar línurnar sem þú hefur valið hingað til eru skráðar í flýtiflipanum **Valdar línur eða haus til afritunar**.

        1. Endurtaktu fyrri tvö skrefin eftir þörfum þar til allar nauðsynlegar línur eru skráðar í flýtiflipanum **Valdar línur eða haus til afritunar**.
        1. Veldu **Í lagi**.

            Nýja skilapöntunin er opnuð og eftirfarandi reitir eru sjálfkrafa stilltir:

            - **Frádráttarkenni** – Þessu svæði er bætt við hausinn til að hægt sé að rekja til baka til frádráttar.
            - **Ástæðukóði vöruskila** – Þetta svæði er sjálfgefið stillt á gildið fyrir **Ástæðukóði vöruskila** sem er stillt fyrir ástæðu frádráttar sem er frádrættinum er úthlutað.

Þegar kreditfærslan er reikningsfærð birtist hún í hlutanum **Opnar færslur** á frádráttarvinnusvæðinu á móti viðeigandi gildi fyrir **Frádráttarkennið** og reiturinn **Kröfugerð** er stilltur á *Aðrar kreditfærslur*. Kreditfærslan verður í boði þar til hún er jöfnuð við frádráttinn á einn af eftirfarandi háttum:

- Þú jafnar hana handvirkt með því að velja **Vinna með \> Jafna** á aðgerðasvæðinu.
- Hún er jöfnuð sjálfkrafa með reglubundnu verkinu *Jafna samþykktar kröfur* (**Sala og markaðssetning \> Reglubundin verk \> Jafna samþykktar kröfur**).
- Hún er sjálfkrafa jöfnuð vegna þess að valkosturinn **Sjálfvirk jöfnun** í flipanum **Jöfnun** á síðunni **Færibreytur viðskiptakrafna** er stilltur á *Já*.

Til að skoða kreditfærsluna sem er búin til þegar frádrátturinn er samþykktur er einnig hægt að nota hnappinn **Opna kreditfærslu** í hlutanum **Opnar færslur** á frádráttarvinnusvæðinu.

### <a name="create-a-return-order"></a>Stofna skilapöntun

Þú getur stofnað skilapöntun fyrir frádrætti sem voru stofnaðir með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptavinar. Þó verður að uppfylla öll eftirfarandi skilyrði:

- Reiturinn **Grundvöllur kröfu** er stilltur á *Byggt á magni*.
- Reiturinn **Staða kröfu** er stilltur á *Opin*.
- Valkosturinn **Stofna skilapöntun** í flipanum **Frádrættir** á síðunni **[Færibreytur viðskiptakrafna](#accounts-receivable-deductions)** er stilltur á *Já*.
- Valkosturinn **Stofna skilapöntun áður en frádráttur er samþykktur** í flipanum **Frádrættir** á síðunni **[Færibreytur viðskiptakrafna](#accounts-receivable-deductions)** er stilltur á *Já*.

Til að stofna skilapöntun skal fylgja eftirfarandi skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Veldu gátreitinn **Merkja** til að vinna úr frádrættinum.
1. Á aðgerðasvæðinu skal velja **Vinna með \> Stofna skilapöntun**.
1. Í svarglugganum **Samþykkja frádrátt** skal breyta eða bæta upplýsingum við gildið **Nótur** eftir þörfum og velja síðan **Í lagi**.
1. Í svarglugganum **Afrita pantanir**, í flýtiflipanum **Reikningar** sýnir **Haushlutinn** sölureikninga þar sem gildið fyrir **Reikningslykil** samsvarar viðskiptavinalykli frádráttarins. Veljið viðeigandi sölureikning.
1. **Línuhlutinn** sýnir línur úr völdum sölureikningi. Veljið **Velja** gátreitinn fyrir hverja línu sem á að afrita. Að öðrum kosti í hlutanum **Hausar** skal velja gátreitinn **Velja allt** fyrir sölupöntunina til að velja allar línur hennar.
1. Breyttu **Magninu** fyrir eina eða fleiri línur eftir þörfum.

    Allar línurnar sem þú hefur valið hingað til eru skráðar í flýtiflipanum **Valdar línur eða haus til afritunar**.

1. Endurtaktu fyrri tvö skrefin eftir þörfum þar til allar nauðsynlegar línur eru skráðar í flýtiflipanum **Valdar línur eða haus til afritunar**.
1. Veldu **Í lagi**.

    Nýja skilapöntunin er opnuð og eftirfarandi reitir eru sjálfkrafa stilltir:

    - **Frádráttarkenni** – Þessu svæði er bætt við hausinn til að hægt sé að rekja til baka til frádráttar.
    - **Ástæðukóði vöruskila** – Þetta svæði er sjálfgefið stillt á gildið fyrir **Ástæðukóði vöruskila** sem er stillt fyrir ástæðu frádráttar sem er frádrættinum er úthlutað.

### <a name="deny-a-deduction"></a>Hafna frádrætti

Til að hafna frádrætti skal fylgja þessum skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Veldu gátreitinn **Merkja** til að vinna úr frádrættinum.
1. Á aðgerðasvæðinu skal velja **Vinna með \> Hafna**.
1. Í svarglugganum **Hafna** skal velja ástæðukóða höfnunar og velja síðan **Í lagi**.
1. Í reitnum **Sýna** fyrir neðan aðgerðasvæðið skal velja *Lokað*.

    Flipinn **Frádrættir** sýnir frádrátt sem var hafnað og reiturinn **Eftirstandandi upphæð** fyrir frádráttinn er stilltur á *0,00*.

    Fyrir frádrætti sem voru stofnaðir með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptavinar koma upp eftirfarandi tilvik:

    - Í flipanum **Tilvísanir** eru reitir í hlutanum **Höfnun** uppfærðir.
    - Ef þú valdir að stofna kröfubókina þegar frádrátturinn var búinn til og ef reikningur hefur verið hengdur við frádráttinn sem lækkaði eftirstöðvar reikningsins er reikningurinn losaður og eftirstöðvar fyrri reiknings sem var hengdur við eru hækkaðar um það sem nemur hafnaðri upphæð kröfunnar.
    - Reiturinn **Staða** í frádrættinum er stilltur á *Lokuð*.
    - Reiturinn **Staða kröfu** í frádrættinum er stilltur á *Hafnað*.

Til að afturkalla neitun skal fylgja þessum skrefum.

1. Á flipanum **Frádráttur** skal velja frádrátt sem er hafnað.
1. Á aðgerðasvæðinu skal velja **Afturkalla höfnun**.

    Fyrir frádrætti sem voru stofnaðir með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptavinar koma upp eftirfarandi tilvik:

    - Í flipanum **Tilvísanir** eru reitir í hlutanum **Höfnun** uppfærðir.
    - Reiturinn **Staða** í frádrættinum er stilltur á *Opin*.
    - Reiturinn **Staða kröfu** í frádrættinum er stilltur á *Opin*.

### <a name="write-off-a-deduction"></a>Afskrifa frádrátt

Til að afskrifa frádrátt skal fylgja þessum skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Veldu gátreitinn **Merkja** til að vinna úr frádrættinum.
1. Á aðgerðasvæðinu skal velja **Vinna með \> Afskrift**.
1. Í svarglugganum **Afskrifa** skal velja ástæðukóða afskriftar og velja síðan **Í lagi**.
1. Í svæðinu **Sýna** skal velja *Allt*.

    Flipinn **Frádrættir** sýnir frádrátt sem var afskrifaður og reiturinn **Eftirstandandi upphæð** fyrir frádráttinn er stilltur á *0,00*.

    Fyrir frádrætti sem voru stofnaðir með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptavinar koma upp eftirfarandi tilvik:

    - Í flipanum **Tilvísanir** eru reitir í hlutanum **Afskrifa** uppfærðir.
    - Ef þú stofnaðir kröfubókina þegar frádrátturinn var búinn til er kröfubók bókuð í ástæðukóða afskriftar fyrir frádráttinn. Þú getur skoðað þessa færslu í flipanum **Frádráttartilvik** þar sem hún er með gildið **Uppfærslugerð** fyrir *Afskrift*.
    - Reiturinn **Staða** í frádrættinum er stilltur á *Lokuð*
    - Reiturinn **Staða kröfu** í frádrættinum er stilltur á *Afskrifa*.

Til að afturkalla afskrift skal fylgja þessum skrefum.

1. Á flipanum **Frádráttur** skal velja frádrátt sem er hafnað.
1. Á aðgerðasvæðinu skal velja **Afturkalla afskrift**.

    Fyrir frádrætti sem voru stofnaðir með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptavinar koma upp eftirfarandi tilvik:

    - Í flipanum **Tilvísanir** eru reitir í hlutanum **Afskrifa** uppfærðir.
    - Ef þú stofnaðir kröfubókina þegar frádrátturinn var búinn til er kröfubók bókuð í ástæðukóða afskriftar fyrir frádráttinn. Þú getur skoðað þessa færslu í flipanum **Frádráttartilvik** þar sem hún er með gildið **Uppfærslugerð** sem *Bakfæra afskrift*.
    - Reiturinn **Staða** í frádrættinum er stilltur á *Opin*.
    - Reiturinn **Staða kröfu** í frádrættinum er stilltur á *Opin*.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Kreditfærslur stofnaðar utan við samþykktarferli frádráttar

Þessi hluti á aðeins við um frádrætti sem voru stofnaðir með því að nota skipunina **Nýr frádráttur** á frádráttarvinnusvæðinu, jöfnun viðskiptavinar eða síðu viðskiptavinar.

Mismunandi notendur gætu þegar hafa búið til reikning með frjálsum texta, skilapöntun eða neikvæða sölupöntun fyrir kröfu viðskiptavinar utan við ferlið **Samþykkja frádrátt**. Þegar fyrirliggjandi frádráttur er samþykktur á frádráttarvinnusvæðinu býr kerfið sjálfkrafa til annan reikning með frjálsum texta, skilapöntun eða neikvæða sölupöntun. Þessi kafli lýsir því hvernig á að hengja fyrirliggjandi inneignir við frádrátt áður en frádrátturinn er samþykktur til að koma í veg fyrir endurteknar inneignir.

### <a name="attach-a-credit-to-deduction"></a>Bæta inneign við frádrátt

Þessi kafli lýsir því hvernig þú getur tengt inneign við frádrátt úr inneigninni.

Þegar kreditfærsla er hengd við frádráttinn er hægt að skoða hana með því að nota hnappinn **Opna kreditfærslu** á tækjastikunni í hlutanum **Opnar færslur** á frádráttarvinnusvæðinu.

Þegar kreditfærslan er reikningsfærð og frádrátturinn er samþykktur birtist hún í hlutanum **Opnar færslur** á frádráttarvinnusvæðinu á móti viðeigandi gildi fyrir **Frádráttarkennið** og reiturinn **Kröfugerð** er stilltur á *Aðrar kreditfærslur*.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Festa reikning með frjálsum texta við frádrátt

Til að festa reikning með frjálsum texta við frádrátt skaltu fylgja þessum skrefum.

1. Fara í **Viðskiptakröfur \> Reikningar \> Allir reikningar með frjálsum texta**.
1. Viðeigandi reikningur er valin.
1. Á aðgerðasvæðinu, í flipanum **Reikningur**, skal velja **Hengja kreditfærslu við frádrátt**. Þessi hnappur er aðeins í boði ef reiturinn **Frádráttarkenni** fyrir reikning með frjálsum texta er auður. Tómur reitur gefur til kynna að reikningurinn með frjálsum texta sé ekki þegar tengdur við frádrátt.
1. Á síðunni **Hengja kreditfærslu við frádrátt** er hægt að velja *einn* frádrátt. Aðeins er hægt að velja opna frádrætti sem *byggja á verði*.
1. Veldu **Í lagi**. Reiturinn **Frádráttarkenni** er stillt á haus reiknings með frjálsum texta.

#### <a name="attach-a-return-order-to-a-deduction"></a>Festa skilapöntun við frádrátt

Til að hengja skilapöntun við frádrátt skal fylgja þessum skrefum.

1. Farðu í **Viðskiptakröfur \> Pantanir \> Allar skilapantanir**.
1. Veldu viðeigandi móttekið eða opið númer vöruskilaheimildar (RMA) sem á við.
1. Á aðgerðasvæðinu, í flipanum **Skilapöntun**, skal velja **Hengja kreditfærslu við frádrátt**. Þessi hnappur er aðeins tiltækur ef reiturinn **Frádráttarkenni** fyrir skilapöntunina er auður. Tómur reitur gefur til kynna að pöntunin sé ekki þegar tengd við frádrátt.
1. Á síðunni **Hengja kreditfærslu við frádrátt** er hægt að velja *einn* frádrátt. Aðeins er hægt að velja opna frádrætti sem *byggja á magni*.
1. Veldu **Í lagi**. Reiturinn **Frádráttarkenni** er stillt á haus skilapöntunar.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Hengja sölupöntun við frádrátt

Til að hengja sölupöntun við frádrátt skal fylgja eftirfarandi skrefum.

1. Opna **Viðskiptakröfur \> Pantanir \> Allar sölupantanir**.
1. Veldu viðeigandi opna, afhenta eða reikningsfærða sölupöntun.
1. Á aðgerðasvæðinu, í flipanum **Reikningur**, skal velja **Hengja kreditfærslu við frádrátt**. Þessi hnappur er aðeins tiltækur ef reiturinn **Frádráttarkenni** fyrir sölupöntunina er auður. Tómur reitur gefur til kynna að sölupöntunin sé ekki þegar tengd við frádrátt.
1. Á síðunni **Hengja við frádrátt** er hægt að velja *einn* frádrátt. Aðeins er hægt að velja opna frádrætti sem *byggja á magni*.
1. Veldu **Í lagi**. Reiturinn **Frádráttarkenni** er stilltur á haus sölupöntunar.

#### <a name="detach-a-deduction-from-a-credit"></a>Losa frádrátt frá inneign

Ef rangur frádráttur hefur verið festur við getur þú losað hann frá inneigninni. Þó verður að uppfylla öll eftirfarandi skilyrði:

- Inneign er tengd frádrættinum.
- Reiturinn **Staða kröfu** er stilltur á *Opin*.

Til að losa frádrátt frá inneign skaltu fylgja einu af eftirfarandi skrefum, eftir gerð inneignarinnar:

- **Reikningar með frjálsum texta:** Á síðunni **Allir reikningar með frjálsum texta** skal velja reikning. Síðan á aðgerðasvæðið í flipanum **Reikningur** skal velja **Losa kreditfærslu frá frádrætti**.
- **Skilapantanir:** Á síðunni **Allar skilapantanir** skal velja pöntun. Síðan á aðgerðasvæðinu í flipanum **Skilapöntun** skal velja **Losa kreditfærslu frá frádrætti**.
- **Sölupantanir:** Á síðunni **Allar sölupantanir** skal velja pöntun. Síðan á aðgerðasvæðið í flipanum **Reikningur** skal velja **Losa kreditfærslu frá frádrætti**.

### <a name="attach-a-deduction-to-a-credit"></a>Festa frádrátt við inneign

Þessi kafli lýsir því hvernig hægt er að tengja frádrátt við inneign frá frádrættinum.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Festa frádrátt við lausan texta, skilapöntun eða inneignarnótu sölupöntunar

Til að hengja frádrátt við frjálsan texta, skilapöntun eða kreditfærslu sölupöntunar skal fylgja þessum skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Velja viðeigandi opinn frádrátt.
1. Á aðgerðasvæðinu skal velja **Vinna með \> Hengja frádrátt við kreditfærslu**. Þessi hnappur er aðeins í boði ef reiturinn **Staða kröfu** er stilltur á *Opin*.
1. Á síðunni **Hengja kreditfærslu við** er hægt að velja *eina* kreditfærslu. Gerðir af kreditfærslum sem eru sýndar fara eftir gildi fyrir **Grundvöll kröfu** í frádrættinum:

    - *Byggt á verði* – Síðan sýnir reikninga með frjálsum texta fyrir viðskiptavinalykilinn þar sem reiturinn **Frádráttarkenni** er auður. Innkaupabeiðnir viðskiptavina eru einnig sýndar vegna þess að textareikningurinn gæti verið óbókaður. Þess vegna gæti það ekki haft númer sem hægt er að vísa til.
    - *Byggt á magni* – Hvers konar kreditfærslur eru sýndar fer eftir stillingunni á valkostinum **Stofna skilapöntun** á síðunni **[Færibreytur viðskiptakrafna](#accounts-receivable-deductions)**:

        - *Já* – Síðan sýnir skilapantanir fyrir viðskiptavinalykilinn þar sem reiturinn **Frádráttarkenni** er auður.
        - *Nei* – Síðan sýnir sölupantanir fyrir viðskiptavinalykilinn þar sem reiturinn **Frádráttarkenni** er auður.

1. Veldu **Í lagi**. Reiturinn **Frádráttarkenni** er stilltur +i haus kreditfærslunnar.

Þegar kreditfærsla er hengd við frádráttinn er hægt að skoða hana með því að nota hnappinn **Opna kreditfærslu** á tækjastikunni í hlutanum **Opnar færslur** á frádráttarvinnusvæðinu.

Þegar kreditfærslan er reikningsfærð og frádrátturinn er samþykktur birtist hún í hlutanum **Opnar færslur** á frádráttarvinnusvæðinu á móti viðeigandi gildi fyrir **Frádráttarkennið** og reiturinn **Kröfugerð** er stilltur á *Aðrar kreditfærslur*.

#### <a name="detach-a-credit-from-the-deduction"></a>Losaðu inneign af frádrættinum

Ef ranga inneignin hefur verið hengd við getur þú losað hana frá frádrættinum. Á aðgerðasvæðinu, í flokknum **Vinna með**, skal velja **Losa frádrátt frá kreditfærslu**. Gildið **Frádráttarkenni** er fjarlægt úr kreditfærslunni.

Hnappurinn **Losa frádrátt úr kreditfærslu** er aðeins í boði ef eftirfarandi skilyrðum er mætt:

- Inneign er tengd frádrættinum.
- Reiturinn **Staða kröfu** er stilltur á *Opin*.

## <a name="create-a-one-time-promotion"></a>Búa til stakt kynningartilboð

Stundum þú ekki hafa samþykkta eftirágreiddur afsláttur sem þú getur látið passa við frádrátt. Í þessu tilviki getur þú notað eiginleikann *stakt kynningartilboð* til að jafna frádráttinn við afslátt sem tengist viðskiptavininum. Eiginleikinn *stakt kynningartilboð* stofnar nýjan afsláttarsamning og eingreiðslu smásölutilvik. Það samsvarar síðan eingreiðslunni við frádráttinn og framkvæmir færslurnar sem þarf til að loka frádrættinum.

Þessi aðgerð er gagnleg notaðir eru afsláttur. Nánari upplýsingar um eftirágreiddan afslátt er að finna í [Stjórnun afsláttar](../sales-marketing/trade-allowance.md).

Fyrst þarf að setja upp sniðmát sem hægt er að nota til að búa til nýjan afsláttarsamning. Til að setja upp sniðmát skal fylgja þessum skrefum:

1. Farðu í **Sala og markaðssetning \> Afslættir \> Sniðmát**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í svæðunum slærðu inn upplýsingarnar sem eiga að koma fram í samningunum sem eru búnir til úr sniðmátinu.
1. Í flýtiflipanum **Viðskiptavinir**, í reitnum **Stigveldi**, skal velja stig stigveldis.
1. Í stiveldislistanum skal velja viðskiptavininn sem er með ójafnaðan frádrátt og velja svo hægri örina (**\>**). Viðskiptavininum er bætt við listann **Viðskiptavinir afsláttarsamninga**.
1. Setja upp eftirstandandi reiti eins og þú krefst og loka síðan síðunni.
1. Farðu í **Sölu- og markaðsstarf \> Uppsetning \> Afsláttur \> Stjórnun á færibreytum fyrir afslátt**.
1. Á flýtiflipanum **Yfirlit**, í reitnum **Sniðmát fyrir stakt kynningartilboð**, velurðu nafn sniðmátsins til að nota til að búa til stakt kynningartilboð.

Því næst er hægt að stofna stakt kynningartilboð á frádráttarvinnusvæðinu. Til að búa til stakt kynningartilboð skal fylgja þessum skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Veldu gátreitinn **Merkja** við hlið frádráttar til að vinna úr.
1. Á aðgerðasvæðinu skal velja **Vinna með \> Jafna frádrátt sem stakt kynningartilboð**.
1. Í svarglugganum **Stakt kynningartilboð** skal fylgja þessum skrefum til að tengja frádráttinn við einn eða fleiri sjóði:

    1. Veldu **Nýtt** og síðan í reitnum **Sjóðskenni** skal velja sjóðskennið. Endurtakið þetta skref til að bæta við eins mörgum fjármagn og þarf.
    1. Í reitinn **Prósenta** við hliðina á hverju sjóðskenni skal færa inn prósentu frádráttar til að úthluta sjóðnum. Gildin sem færð eru inn í reitina **Prósenta** verða að vera samtals 100.

1. Veldu **Í lagi**. Kerfið býr til nýja afsláttarsamningurinn sem hefur smásölutilvik eingreiðslu og sem samsvarar eingreiðslu til frádráttur.

## <a name="do-a-mass-update-of-deductions"></a>Framkvæma fjöldauppfærslu á frádrætti

Ef nauðsynlegt er að gera sömu breytingar á mörgum frádrætti er hægt að velja þær frádrátt og framkvæma fjöldauppfærslu þeirra svæða.

Til að gera magnuppfærslu skal fylgja þessum skrefum.

1. Farðu í **Sala og markaðssetning \> Afslættir \> Frádrættir \> Frádráttarvinnusvæði**.
1. Í reitnum **Sýna** fyrir neðan aðgerðasvæðið skal velja hvers konar frádrátt á að skoða.
1. Veldu gátreitinn við hliðina á hverjum frádrætti sem á að uppfæra. Á aðgerðasvæðinu er síðan smellt á **Vinna með \> Magnuppfærsla**.
1. Svarglugginn **Magnuppfærsla** sýnir valda frádrætti. Uppfærðu reitina eftir þörfum og smelltu síðan á **Í lagi** til að samþykkja breytingarnar.
