---
title: Sýna stöðu frís í viðmóti fyrir framkvæmd á framleiðslugólfi
description: Í þessari grein er að finna dæmi um aðstæður sem sýnir hvernig á að setja upp Microsoft Dynamics 365 Supply Chain Management þannig að það noti launatölfræði til að gefa starfskröftum yfirlit yfir innistæðu orlofs á yfirstandandi ári.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: 2a6b6f52bfa7539b7c9bb5841536b0d564d0274c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852274"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Sýna stöðu frís í viðmóti fyrir framkvæmd á framleiðslugólfi

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna dæmi um aðstæður sem sýnir hvernig á að setja upp Microsoft Dynamics 365 Supply Chain Management þannig að það noti launatölfræði til að gefa hverjum starfskrafti yfirlit yfir innistæðu orlofs á yfirstandandi ári. Starfsmenn munu geta séð orlofsstöðu sína í svarglugganum **Dagurinn minn** í viðmóti fyrir framkvæmd á framleiðslugólfi.

Í þessu tilviki er notast við dönsku orlofslögin þar sem orlofsárið er frá 1. september til og með 31. ágúst. Í þessu tilfelli hefur fyrirtækið ráðið nýjan starfskraftog mun veita viðkomandi starfskrafti að jafnaði 10 orlofsdaga það sem eftir er af yfirstandandi orlofsári.

## <a name="turn-on-the-required-features"></a>Kveiktu á nauðsynlegum eiginleikum

Til að keyra þessar aðstæður verður þú að virkja *yfirlitið „Dagurinn minn“ fyrir viðmóts fyrir framkvæmd á framleiðslugólfi* í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Frekari upplýsingar um hvernig á að virkja þetta og aðra eiginleika fyrir viðmót fyrir framkvæmd á framleiðslugólfi er að finna í [Stilla viðmót fyrir framkvæmd á framleiðslugólfi](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

## <a name="create-a-new-pay-type"></a>Stofna nýtt tegund greiðslu

Byrjaðu á því að búa til nýja *launagerð* sem rekur áunnum orlofsdögum starfsmanna (einnig nefnt *orlofsstaða*). Venjulega eru launagerðir notaðar til að reikna út laun starfskrafta. Launagerðin sem þú býrð til hér verður hins vegar notuð til að reikna út stöðu.

1. Fara í **Tími og viðvera \> Uppsetning \> Launaskrá \> Launagerð**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni skal stilla eftirfarandi gildi:

    - **Launagerð:** *5151-1*
    - **Lýsing:** *Teljari fyrir orlofsdaga starfskrafts*
    - **Taka með í skýrslu:** *Nei*

## <a name="update-the-pay-agreement"></a>Uppfærsla launasamning

Í þessum hluta breytir þú fyrirliggjandi *launasamningi* með því að bæta við nýju launagerðinni og setur reglurnar sem skilgreina hvernig orlofsstöðu hvers starfsmanns er breytt þegar orlofsdagar eru skráðir.

1. Fara í **Tími og viðvera \> Uppsetning \> Launaskrá \> Launasamningar**.
1. Veljið launasamninginn þar sem setja á upp orlofsreglurnar. (Ef þú vinnur með hefðbundin sýnigögn USMF er aðeins einn launasamningur, *Einstaklingur*.)
1. Gakktu úr skugga um að valinn launasamningur sé í gildi fyrir núverandi dagsetningu. Ef unnið er með hefðbundin sýnigögn frá USMF gæti reiturinn **Til dagsetningar** í launasamningnum *Einstaklingur* verið stillt á dagsetningu sem er liðin. Breyttu gildinu þannig að það verði eitt eða tvö ár fram í tímann, eftir þörfum.
1. Á aðgerðasvæðinu skaltu velja **Samningslínur**.
1. Á síðunni **Launasamningslínur** á flýtiflipanum **Yfirlit** skaltu stilla eftirfarandi gildi á tækjastikunni:

    - Í fyrsta fellilistanum skal velja **Mánudagur**.
    - Í öðrum fellilistanum skal velja **Fjarvistir**.

1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni skaltu stilla reitinn **Launagerð** samkvæmt launagerð sem þú bjóst til fyrir þessar aðstæður (*5151-1*). Skilja alla aðra reiti eftir í sjálfgildum.
1. Þegar nýja línan er enn valin stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Fjarvistarkóði:** *Orlof*
    - **Nota fast magn:** *Já*
    - **Fasti:** *-1*

1. Veldu **Afritunardagur** á aðgerðasvæðinu.
1. Í svarglugganum **Afritunardagur** skal stilla eftirfarandi gildi:

    - **Þriðjudagur**, **Miðvikudagur**, **Fimmtudagur** og **Föstudagur:** *Já*
    - **Skrifa yfir:** *Já*
    - **Fjarvistir:** *Já*

1. Veldu **Í lagi**.

## <a name="create-a-payroll-statistic-group"></a>Stofna flokk launatalnagagna

*Flokkar launatalnagagna* eru notaðir til að setja upp tölfræði fyrir skráningar starfskrafta á tilteknu tímabili. Í þessum aðstæður notar þú flokk launatalnagagna til að reikna út fjölda orlofsdaga sem starfsmenn vinna sér inn á orlofstímabili. Orlofstímabilið er frá 1. september til og með 31. ágúst í Danmörku.

1. Fara í **Tími og viðvera \> Uppsetning \> Launaskrá \> Flokkar launatalnagagna**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni skal stilla eftirfarandi gildi:

    - **Launatalningargagnahópur:** *VAC*
    - **Lýsing:** *Orlofsstaða*
    - **Flutningur:** *Nei*

1. Þegar nýja línan er enn valin stilltu **Uppsetning** á aðgerðarsvæðinu.
1. Á síðunni **Uppsetning**, á aðgerðasvæðinu, skal velja **Nýtt** til að bæta við röð við hnitið.
1. Í nýju línunni stillir þú reitinn **Launagerð** á *5151-1*.
1. Velja og halda niðri (eða hægrismella) í reitnum **Tímabilskóði** og velja síðan **Skoða upplýsingar**. Þú getur nú sett upp tímabilskóðann sem þú munt úthluta þessum reit síðar.
1. Á síðunni **Tímabilsgerð**, á aðgerðasvæðinu, skal velja **Nýtt** til að bæta línu við hnitanetið.
1. Á nýju línunni skal stilla eftirfarandi gildi:

    - **Tímabilsgerðir:** *VacYear*
    - **Lýsing:** *Orlofsár*
    - **Tíðni:** *Ár*

1. Þegar nýja línan er enn valin stilltu **Mynda tímabil** á aðgerðarsvæðinu.
1. Í svarglugganum **Stofna tímabil** skal stilla eftirfarandi gildi:

    - **Tilgreina upphafsdag tímabilsins:** *1. september 2021*
    - **Lengd tímabils:** *5*

1. Veldu **Í lagi**.
1. Lokið síðunni **Tímabilsgerðir** til að fara aftur á síðuna **Launatalnaflokkar**.
1. Stillir reitinn **Tímabilskóði** á tímabilsgerðina sem var búið til (*VacYear*).

## <a name="create-a-statistical-balance-setup"></a>Stofna uppsetningu á talnagagnastöðu

Í þessum hluta býrðu til *uppsetningu á talnagagnastöðu* sem er tengt við flokk launatalnagagna sem þú bjóst til í fyrri hlutanum. Síðar tengir þú þessa uppsetningu talnagagnastöðu við yfirlitið **Dagurinn minn** í viðmóti fyrir framkvæmd á framleiðslugólfi. Yfirlitið **Dagurinn minn** mun þá geta sýnt orlofsinnistæðurnar fyrir þá launagerð sem er úthlutað til tilheyrandi flokk launatalnagagna.

1. Fara í **Tími og viðvera \> Uppsetning \> Launaskrá \> Uppsetning talnagagnastöðu**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni skal stilla eftirfarandi gildi:

    - **Launatalningargagnahópur:** *VAC*
    - **Ytra heiti:** *Orlofsstaða*
    - **Sveigjanlegt:** *Nei*

## <a name="create-a-manual-premium"></a>Stofna handvirkan kaupauka

*Handvirk bónusgreiðslur* eru yfirleitt notuð til að veita starfsmönnum aukalaun fyrir aukavinnu. Í þessum aðstæður býrðu til handvirkan kaupauka sem þú getur notað til að stilla upphaflegu orlofsinnistæðuna fyrir hvern starfskraft.

1. Fara í **Tími og viðvera \> Uppsetning \> Launaskrá \> Handvirkir kaupaukar**.
1. Á aðgerðasvæðinu skal velja **Nýr** til að bæta við færslu.
1. Í nýju skránni skal setja inn eftirfarandi gildi:

    - **Kaupaukar:** *VAC*
    - **Lýsing:** *Leiðréttingar á orlofsstöðu starfsmanna*
    - **Launagerð:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Stilltu upphaflegt orlofshlutfall starfskrafts og breyttu því um einn dag

Launastjórar nota síðuna **Samþykkja** til að fara yfir og samþykkja daglegar skráningar starfskrafta. Í þessum aðstæðum tekur þú að þér hlutverk stjórnanda svo að þú getir stillt upphaflegu orlofsstöðuna fyrir starfskraft og skráð þá orlofsdaga sem starfskraftur tekur.

1. Farðu í **Tími og viðvera \> Farðu yfir og samþykktu \> Samþykktu**.
1. Í svarglugganum **Samþykkja** skal stilla eftirfarandi reiti:

    - **Samþykkisflokkur** – Veldu samþykkisflokkinn sem þú tilheyrir. (Ef unnið er með hefðbundin sýnigögn frá USMF er aðeins einn samþykkishópur, *AdmMan*.)
    - **Skoða allan hópinn, 1 dagur** – Veldu valkostinn og stilltu síðan reitinn á núverandi dagsetningu.

1. Veldu **Í lagi**.
1. Síðan **Samþykkja** sýnir lista yfir færslur sem passa við skilyrðin þín. Veldu starfskraft til samþykktar. Ef þú ert að vinna með stöðluð sýnigögn USMF skaltu velja starfskraft *000496* (*Christina Portra*).
1. Veita völdum starfsmanni 10 daga orlof:

    1. Á meðan starfskrafturinn er enn valinn, veljið **Bónusgreiðslulínur** á Aðgerðasvæði.
    1. Á síðunni **Kaupaukalínur**, á aðgerðasvæðinu, skal velja **Nýtt** til að bæta línu við hnitanetið.
    1. Á nýju línunni skal stilla eftirfarandi gildi:

        - **Kaupaukar:** *VAC*
        - **Magn:** *10*

    1. Lokið síðunni **Kaupaukalínur**.

1. Skráðu á síðunni **Samþykkja** að starfsmaðurinn hafi notað einn af orlofsdögunum sínum á núverandi dagsetningu:

    1. Þegar starfskraftur er enn valinn, á neðri hluta síðunnar, í flipanum **Yfirlit**, skal velja **Nýtt** á tækjastikunni til að bæta línu við hnitanetið.
    1. Á nýju línunni skal stilla eftirfarandi gildi:

        - **Gerð færslubókarskráningar:** *Fjarvist*
        - **Tilvísun:** *Orlof*

    1. Í efri hluta síðunnar velur þú **Flutningur** á tækjastikunni til að setja inn orlofsstöðuna og reikna út frádráttinn.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Stilla viðmót fyrir framkvæmd á framleiðslugólfi þannig að það innihaldi svargluggann Dagurinn minn

Í þessum hluta bætir þú hnappinum **Dagurinn minn** við viðmót fyrir framkvæmd á framleiðslugólfi. Starfskraftar geta síðan notað þennan hnapp til að opna svargluggann **Dagurinn minn**.

1. Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**.
1. Veldu stillingu, svo sem *Sjálfgefið*.
1. Í aðgerðarúðunni skal velja **Hönnun flipa**.
1. Á síðunni **Hönnunarflipar**, í listasvæðinu, velur þú *Öll verk* til að skoða stillingar fyrir þann flipa. Reiturinn **Aðalyfirlit** ætti nú að sýna gildi *Öll verk*.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á flýtiflipanum **Aukatækjastika**, í dálkinum **Aðgerðir í boði**, velur þú **Dagurinn minn**. Veljið hægri örvarhnappinn til að færa það yfir á dálkinn **Valdar aðferðir**.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Athugar stöðu þína í viðmót fyrir framkvæmd á framleiðslugólfi

Í þessum hluta skráir þú þig inn á viðmót fyrir framkvæmd á framleiðslugólfi sem starfskraftinn sem þú settir upp orlofstíma fyrr. Þú opnar þá svargluggann **Dagurinn minn** svargluggann til að skoða orlofsstöðuna þína.

1. Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Keyrsla framleiðslugólfs**.
1. Ef beðið er um að þú veljir stillingu, veldu þá stillinguna sem þú settir upp fyrr í þessum aðstæðum (*Sjálfgefið*).
1. Skráðu þig inn sem notandann sem þú settir upp fyrr í þessum aðstæðum. Ef þú vinnur með stöðluð sýnigögn USMF ættir þú að geta skráð þig inn með því að slá inn *123* í reitinn fyrir **Kortkenni**. Þetta kortkenni á við um Christina Portra.
1. Veldu **Dagurinn minn** á vinstri tækjastikunni.
1. Skoðið hlutann **Staða** í svarglugganum. Þessi hluti ætti nú að sýna að þú eigir inni níu orlofsdaga.
