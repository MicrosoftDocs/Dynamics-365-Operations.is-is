---
title: Sýna orlofsstöður í framkvæmdarviðmóti framleiðslugólfs
description: Þetta efni gefur dæmi um atburðarás sem sýnir hvernig á að setja upp Microsoft Dynamics 365 Supply Chain Management þannig að það notar launatölfræði til að veita starfsmönnum yfirsýn yfir orlofsstöðu sína á yfirstandandi ári.
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
ms.openlocfilehash: a97858c72b0be50609cee552bd0635e2d68ea478
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648167"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Sýna orlofsstöður í framkvæmdarviðmóti framleiðslugólfs

[!include [banner](../includes/banner.md)]

Þetta efni gefur dæmi um atburðarás sem sýnir hvernig á að setja upp Microsoft Dynamics 365 Supply Chain Management þannig að það notar launatölfræði til að veita hverjum starfsmanni yfirsýn yfir orlofsstöðu sína á yfirstandandi ári. Starfsmenn munu geta séð orlofsstöðu sína í **Minn dagur** svargluggi í framkvæmdarviðmóti framleiðslugólfs.

Þessi atburðarás notar dönsku orlofslögin, þar sem orlofsárið er frá 1. september til 31. ágúst. Í þessari atburðarás hefur fyrirtækið þitt ráðið nýjan starfsmann og mun veita þeim starfsmanni eftirstöðvar 10 orlofsdaga það sem eftir er af yfirstandandi orlofsári.

## <a name="turn-on-the-required-features"></a>Kveiktu á nauðsynlegum eiginleikum

Til að keyra þessa atburðarás verður þú að virkja *„Dagurinn minn“ yfirsýn fyrir framkvæmdarviðmót framleiðslugólfs* lögun í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Fyrir upplýsingar um hvernig á að virkja þetta og aðra eiginleika fyrir framkvæmdarviðmót framleiðslugólfs, sjá [Stilltu framkvæmdarviðmót framleiðslugólfs](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

## <a name="create-a-new-pay-type"></a>Búðu til nýja launategund

Byrjaðu á því að búa til nýtt *launategund* sem mun fylgjast með áunnnum orlofsdögum starfsmanna (einnig nefndir þeirra *orlofsstaða*). Venjulega eru launategundir notaðar til að reikna út laun starfsmanna. Hins vegar verður launategundin sem þú býrð til hér notuð til að reikna stöðu.

1. Fara til **Tími og mæting \> Uppsetning \> Launaskrá \> Launategundir**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni skaltu stilla eftirfarandi gildi:

    - **Greiðsla:** *5151-1*
    - **Lýsing:** *Teljari fyrir orlofsdaga starfsmanna*
    - **Taka með í útflutningi:** *Nei*

## <a name="update-the-pay-agreement"></a>Uppfærðu launasamninginn

Í þessum hluta muntu breyta núverandi *kjarasamningi* með því að bæta við nýju launategundinni og setja þær reglur sem skilgreina hvernig orlofsstaða hvers starfsmanns er leiðrétt þegar orlofsdagar eru skráðir.

1. Fara til **Tími og mæting \> Uppsetning \> Launaskrá \> Launasamningar**.
1. Veldu launasamninginn þar sem þú vilt setja upp orlofsstefnuna. (Ef þú ert að vinna með venjuleg USMF sýnishornsgögn, þá er aðeins einn launasamningur, *Maður* .)
1. Gakktu úr skugga um að valinn launasamningur gildi fyrir núverandi dagsetningu. Ef þú ert að vinna með stöðluð USMF sýnishornsgögn, þá **Hingað til** sviði á *Maður* launasamningur gæti verið stilltur á dagsetningu sem er í fortíðinni. Breyttu gildinu þannig að það sé eitt eða tvö ár fram í tímann, eftir þörfum.
1. Á aðgerðarrúðunni velurðu **Samningslínur**.
1. Á **Greiðslusamningslínur** síðu, á **Yfirlit** Flýtiflipi, stilltu eftirfarandi gildi á tækjastikunni:

    - Í fyrsta fellilistanum skaltu velja **Mánudagur**.
    - Í seinni fellilistanum skaltu velja **Fjarvera**.

1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju röðinni skaltu stilla **Greiðsla** reitnum við launategundina sem þú bjóst til fyrir þessa atburðarás (*5151-1*). Láttu alla aðra reiti vera stillta á sjálfgefin gildi.
1. Á meðan nýja röðin er enn valin, á **Almennt** Flýtiflipi, stilltu eftirfarandi gildi:

    - **Fjarvistarkóði:** *Frí*
    - **Notaðu fast magn:** *Já*
    - **Stöðugt:** *-1*

1. Á aðgerðarrúðunni velurðu **Afrita dagur**.
1. Í **Afrita dagur** valmynd, stilltu eftirfarandi gildi:

    - **þriðjudag**, **·**, **·**, og **Föstudagur:** *Já*
    - **Skrifa yfir:** *Já*
    - **Fjarvera:** *Já*

1. Veldu **Í lagi**.

## <a name="create-a-payroll-statistic-group"></a>Búðu til launatölfræðihóp

*Launatölfræðihópar* eru notaðar til að setja upp tölfræði fyrir starfsmannaskráningar á tímabili. Í þessari atburðarás muntu nota launatölfræðihóp til að reikna út fjölda orlofsdaga sem starfsmenn vinna sér inn á orlofstímabili. Í Danmörku er orlofstímabilið frá 1. september til 31. ágúst.

1. Fara til **Tími og mæting \> Uppsetning \> Launaskrá \> Launatölfræðihópar**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni skaltu stilla eftirfarandi gildi:

    - **Launatölfræðihópur:** *VAC*
    - **Lýsing:** *Orlofsjafnvægi*
    - **Flutningur:** *Nei*

1. Á meðan nýja röðin er enn valin skaltu velja **Uppsetning** á aðgerðasvæðinu.
1. Á **Uppsetning** síðu, á aðgerðarrúðunni, veldu **Nýtt** til að bæta línu við ristina.
1. Á nýju röðinni skaltu stilla **Greiðsla** sviði til *5151-1*.
1. Veldu og haltu inni (eða hægrismelltu) á **Tímabilskóði** reit og veldu síðan **Skoða smáatriði**. Þú getur nú sett upp tímabilskóðann sem þú munt úthluta þessum reit síðar.
1. Á **Tímabilsgerðir** síðu, á aðgerðarrúðunni, veldu **Nýtt** til að bæta línu við ristina.
1. Á nýju línunni skaltu stilla eftirfarandi gildi:

    - **Tímabilsgerðir:** *VacYear*
    - **Lýsing:** *Orlofsár*
    - **Tíðni:** *Ár*

1. Á meðan nýja röðin er enn valin skaltu velja **Búðu til tímabil** á aðgerðasvæðinu.
1. Í **Búðu til tímabil** valmynd, stilltu eftirfarandi gildi:

    - **Tilgreindu upphafsdag tímabilsins:** *1. september 2021*
    - **Lengd tímabils:** *5*

1. Veldu **Í lagi**.
1. Lokaðu **Tímabilsgerðir** síðu til að fara aftur á **Launatölfræðihópar** síðu.
1. Stilltu **Tímabilskóði** reit við tímabilsgerðina sem þú bjóst til (*VacYear*).

## <a name="create-a-statistical-balance-setup"></a>Búðu til tölfræðilega jafnvægisuppsetningu

Í þessum hluta muntu búa til a *uppsetning tölfræðilegrar jafnvægis* sem er tengt launatölfræðihópnum sem þú bjóst til í fyrri hlutanum. Síðar muntu tengja þessa tölfræðilegu jafnvægisuppsetningu við **Minn dagur** skoða í framkvæmdarviðmóti framleiðslugólfsins. The **Minn dagur** skoða mun þá geta sýnt orlofsstöður fyrir þá launategund sem er úthlutað til tengdum launatölfræðihópi.

1. Fara til **Tími og mæting \> Uppsetning \> Launaskrá \> Uppsetning tölfræðilegrar jafnvægis**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni skaltu stilla eftirfarandi gildi:

    - **Launatölfræðihópur:** *VAC*
    - **Ytra nafn:** *Orlofsjafnvægi*
    - **Flex:** *Nei*

## <a name="create-a-manual-premium"></a>Búðu til handvirkt aukagjald

*Handvirk iðgjöld* eru venjulega notuð til að veita starfsmönnum aukalaun fyrir aukavinnu. Í þessari atburðarás muntu búa til handvirkt iðgjald sem þú getur notað til að stilla upphaflega orlofsstöðu fyrir hvern starfsmann.

1. Fara til **Tími og mæting \> Uppsetning \> Launaskrá \> Handvirk iðgjöld**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við meti.
1. Í nýju skránni skaltu stilla eftirfarandi gildi:

    - **Iðgjöld:** *VAC*
    - **Lýsing:** *Leiðréttingar á orlofsstöðu starfsmanna*
    - **Greiðsla:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Stilltu upphaflega orlofsstöðu starfsmanns og stilltu hana um einn dag

Launastjórar nota **Samþykkja** síðu til að skoða og samþykkja daglegar skráningar starfsmanna. Í þessari atburðarás muntu taka að þér hlutverk stjórnanda þannig að þú getur stillt upphaflega orlofsstöðu fyrir starfsmann og skráð orlofsdaga sem starfsmaðurinn tekur.

1. Fara til **Tími og mæting \> Skoðaðu og samþykktu \> Samþykkja**.
1. Í **Samþykkja** valmynd, stilltu eftirfarandi reiti:

    - **Samþykkishópur** – Veldu samþykkishópinn sem þú tilheyrir. (Ef þú ert að vinna með stöðluð USMF sýnishornsgögn, þá er aðeins einn samþykkishópur, *AdmMan* .)
    - **Skoða allan hópinn, 1 dag** – Veldu valkostinn og stilltu síðan reitinn á núverandi dagsetningu.

1. Veldu **Í lagi**.
1. The **Samþykkja** síða sýnir lista yfir færslur sem passa við skilyrðin þín. Veldu starfsmanninn sem þú vilt samþykkja. Ef þú ert að vinna með stöðluð USMF sýnishornsgögn skaltu velja starfsmann *000496* (*Kristín Portra*).
1. Veittu völdum starfsmanni 10 daga orlof:

    1. Á meðan starfsmaðurinn er enn valinn skaltu velja **Premium línur** á aðgerðasvæðinu.
    1. Á **Premium línur** síðu, á aðgerðarrúðunni, veldu **Nýtt** til að bæta línu við ristina.
    1. Á nýju línunni skaltu stilla eftirfarandi gildi:

        - **Iðgjöld:** *VAC*
        - **Magn:** *10*

    1. Lokaðu **Premium línur** síðu.

1. Á **Samþykkja** síðu, skráðu þá staðreynd að starfsmaðurinn notaði einn af orlofsdögum sínum á núverandi dagsetningu:

    1. Á meðan starfsmaðurinn er enn valinn, neðst á síðunni, á **Yfirlit** flipa, veldu **Nýtt** á tækjastikunni til að bæta línu við hnitanetið.
    1. Á nýju línunni skaltu stilla eftirfarandi gildi:

        - **Tegund dagbókarskráningar:** *Fjarvera*
        - **Tilvísun:** *Frí*

    1. Veldu efst á síðunni **Flytja** á tækjastikunni til að nota orlofsupphæðina og reikna frádráttinn.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Stilltu framkvæmdarviðmót framleiðslugólfsins þannig að það innihaldi Daginn minn svargluggann

Í þessum hluta muntu bæta við a **Minn dagur** hnappinn að framkvæmdarviðmóti framleiðslugólfsins. Starfsmenn geta síðan notað þennan hnapp til að opna **Minn dagur** valmynd.

1. Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**.
1. Veldu stillingar, svo sem *Sjálfgefið*.
1. Á aðgerðarrúðunni velurðu **Hönnunarflipar**.
1. Á **Hönnunarflipar** síðu, í listaglugganum, veldu *Öll störf* til að skoða stillingar fyrir þann flipa. The **Aðalsýn** reiturinn ætti nú að sýna gildi á *Öll störf*.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á **Auka tækjastika** flýtiflipann, í **Tiltækar aðgerðir** dálk, veldu **Minn dagur**. Veldu síðan hægri örvarhnappinn til að færa hann á **Valdar aðgerðir** dálki.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Athugaðu stöðuna þína í framkvæmdarviðmóti framleiðslugólfsins

Í þessum hluta muntu skrá þig inn á framkvæmdarviðmót framleiðslugólfs sem starfsmaðurinn sem þú settir upp frítímann áður. Þú munt þá opna **Minn dagur** valmynd til að skoða orlofsstöðu þína.

1. Fara til **Framleiðslueftirlit \> Uppsetning \> Framleiðsluframkvæmd \> Framleiðslugólf framkvæmd**.
1. Ef þú ert beðinn um að velja stillingu skaltu velja stillinguna sem þú settir upp fyrr í þessari atburðarás (*Sjálfgefið*).
1. Skráðu þig inn sem notandinn sem þú settir upp fyrr í þessari atburðarás. Ef þú ert að vinna með venjuleg USMF sýnishornsgögn ættir þú að geta skráð þig inn með því að slá inn *123* í **Merki auðkenni** sviði. Þetta merki auðkennis samsvarar Christina Portra.
1. Veldu **Minn dagur** á vinstri tækjastikunni.
1. Skoðaðu **Jafnvægi** hluta svargluggans. Þessi hluti ætti nú að sýna að þú ert með níu orlofsdaga.
