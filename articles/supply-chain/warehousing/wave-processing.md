---
title: Stofnun og meðhöndlun bylgju
description: Þetta efnisatriði lýsir því hvernig má stofna vinnslu og losa bylgju til að stofna tiltekt fyrir farm, sendingar, framleiðslupöntun eða kanban-pöntun.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 5d3e8038c4651bb75b3d36ed0d398be0d032b591dedda757d2fc3a6399e512c6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773058"
---
# <a name="wave-creation-and-processing"></a>Stofnun og meðhöndlun bylgju

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig má stofna vinnslu og losa bylgju til að stofna tiltekt fyrir farm, sendingar, framleiðslupöntun eða kanban-pöntun. Hægt er að búa til bylgjur fyrir eftirfarandi gerðir pantana:

- **Sölupantanir** – Notið sendingarbylgjur sem innihalda línur úr sölupöntunum. Þegar sölupöntun er losuð í vöruhúsið er hægt að taka sölupöntunarlínurnar með í bylgjunni.
- **Framleiðslupantanir** – Notið framleiðslubylgjur til að taka með línur úr uppskriftum fyrir afurð.
- **Kanban pantanir** - Kanban bylgjur innihalda tiltektarlistalínur úr kanban pöntunum.

Fyrir sölupantanir og kanbanpantanir verður að taka frá birgðir áður en pöntun er losuð í vöruhús. Annars er ekki hægt að vinna úr vörum og úthlutunarlínum í bylgju. Framleiðslupantanir eru hins vegar örlítið sveigjanlegri. Fyrir framleiðslupantanir er hægt að velja annan af eftirfarandi valkostum:

- Krefjast þess að allt efni sé tekið frá áður en pöntun er losuð í vöruhúsið.
- Leyfa að losa framleiðslupantanir í vöruhúsið þótt ekki sé hægt að taka frá allt efni. Ef þessi valkostur er valinn verður handvirkt að endurtaka losun í vöruhúsaferli þegar viðbótar efni verða tiltækar. Þetta er til dæmis hentugt ef efnin sem þarf til að hefja framleiðslu eru til staðar og geta beðið þar til viðbótarefni verða tiltæk.

Hægt er að tilgreina hvaða valkostir framleiðslupöntunar eigi að nota að sjálfgefnu með því að nota reitinn **Kröfur vegna frátekningu efnis** á síðunni **Færibreytur framleiðslustýringar**. Hins vegar er hægt að breyta stillingunni fyrir hverja tiltekna framleiðslupöntun eftir þörfum. Frekari upplýsingar er að finna í [Færibreytur vöruhúss fyrir bylgjuvinnslu](wave-warehouse-parameters.md).

## <a name="create-and-process-a-wave"></a>Stofna og vinna úr bylgju

Eftirfarandi skýringarmynd sýnir flæðið fyrir stofnun sendingarbylgja, úrvinnslu þeirra og losanir. Númerin samsvara hlutunum sem er lýst síðar í þessu efnisatriði.

![Ferli fyrir stofnun bylgju.](media/wave-processing-diagram.png "Ferli fyrir stofnun bylgju")

### <a name="prerequisites"></a>Forkröfur

Áður en hafist er handa verður bylgjusniðmát að vera tiltækt fyrir gerð bylgju sem á að stofna (sending, framleiðsla eða kanban). Bylgjusniðmátið setur margar stillingar fyrir það hvernig bylgjan verður búin til og unnið úr henni, þ.m.t. hvaða skref þarf að gera handvirkt og hver eru gerð sjálfkrafa. Frekari upplýsingar er að finna í [Bylgjusniðmát](wave-templates.md).

### <a name="create-a-wave"></a>Stofna bylgju

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Búa sjálfkrafa til bylgjur samkvæmt vöruhúsi og gerð pöntunar

Til að búa til bylgjur sjálfkrafa skal setja upp [Bylgjusniðmát](wave-templates.md) sem gilda fyrir hverja viðeigandi gerð pöntunar og vöruhús. Gangið úr skugga um að hvert sniðmát sé með valkostinn **Sjálfvirk stofnun bylgju** stilltan á *Já*.

#### <a name="manually-create-waves"></a>Stofna bylgjur handvirkt

Til að stofna bylgju handvirkt, skal fylgja eftirfarandi skrefum:

1. Gangið úr skugga um að viðeigandi [Bylgjusniðmát](wave-templates.md) séu ekki stillt á að stofna bylgju sjálfkrafa fyrir vöruhús og gerðir pantana þar sem á að gera það handvirkt.
1. Gerið eitt af eftirfarandi eftir því hvaða gerð bylgju á að stofna:

    - Farið í **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Sendingarbylgjur** \> **Allar bylgjur**. Á aðgerðasvæðinu skal velja **Bylgja**.
    - Farið í **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Framleiðslubylgjur** \> **Allar framleiðslubylgjur**. Á aðgerðasvæðinu skal velja **Framleiðslubylgja**.
    - Farið í **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Kanban-bylgjur** \> **Allar kanban-bylgjur**. Í aðgerðasvæðinu velurðu **Stofna bylgju**.

1. Í reitinn **Lýsing** skal færa inn stutta lýsingu á bylgjunni. Þetta er ætti að tilgreina hvað verið sé að vinna í bylgjunni.

1. Í reitnum **Heiti bylgjusniðmáts** skal velja bylgjusniðmát fyrir þá gerð bylgju sem á að stofna. Bylgjusniðmátið inniheldur bylgjuaðferðir sem verður að framkvæma aðgerðir, s.s. að stofna vinnu fyrir bylgjuna. Til dæmis getur bylgjusniðmát fyrir sendingarbylgjur innihaldið aðferðir til að búa til hleðslur, úthluta línum á bylgjur, fylla á og stofna tiltekt fyrir bylgjuna.

1. Ef ætlunin er að nota bylgjueigindir sem viðbótarskilyrði fyrirspurnar fyrir bylgjuna skal velja eigindir í reitunum **Eigindir bylgju**.

### <a name="specify-what-to-include-in-a-wave"></a>Tilgreina hvað á að hafa með í bylgju

Þegar bylgja hefur verið stofnuð má fara að bæta efni í hana.

> [!NOTE]
> Ef þess gerist þörf er hægt að bæta línum við bylgju þótt búið sé að vinna úr henni, svo lengi sem ekki er búið að losa hana.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Tilgreina sjálfkrafa hvað á að hafa með í bylgju

Til að búa til bylgjur sjálfkrafa skal setja upp [Bylgjusniðmát](wave-templates.md) sem gilda fyrir hverja viðeigandi gerð pöntunar og vöruhús. Gangið úr skugga um að hvert sniðmát sé með valkostinn **Sjálfvirk stofnun bylgju** stilltan á *Já*. Annars gæti sniðmátið úthlutað línum sjálfkrafa í einhverja viðeigandi opna bylgju ef valkosturinn **Úthluta á opnar bylgjur** er stilltur á *Já*.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Tilgreina handvirkt hvað á að hafa með í bylgju

Þegar bylgja hefur verið stofnuð en ekki losuð er hægt að tilgreina handvirkt hvað á að hafa í henni. Til að bæta línum handvirkt við bylgju:

1. Gerið eitt af eftirfarandi eftir því hver gerð bylgju er sem bæta á línum við:

    - Farið í **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Sendingarbylgjur** \> **Allar bylgjur**. Á aðgerðasvæðinu skal velja **Bylgja**.
    - Farið í **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Framleiðslubylgjur** \> **Allar framleiðslubylgjur**. Á aðgerðasvæðinu skal velja **Framleiðslubylgja**.
    - Farið í **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Kanban-bylgjur** \> **Allar kanban-bylgjur**. Í aðgerðasvæðinu velurðu **Stofna bylgju**.

1. Veljið bylgjuna. Á aðgerðasvæðinu skal velja eitt af eftirfarandi:

      - **Vinna með sendingar**
      - **Viðhalda framleiðslum**
      - **Viðhalda tiltektarlistum kanban-vinnslu**

1. Í efri hluta gluggans skal velja línuna sem bæta á við bylgjuna og síðan velja **Bæta við bylgju**. Línan er færð yfir í flýtiflipann **Bylgjulínur**.

    Endurtakið þetta skref fyrir hverja línu til að bæta við. Til að bæta öllum línum við skal velja **Bæta öllum við**.

    > [!TIP]
    > Fyrir sendingarbylgjur er hægt að finna á fljótlegan hátt tiltekna pöntun með því að velja sérstillta síu í reitnum **Bylgjuafmörkunarkóði**. Afmörkunarkóðar bylgju innihalda skilyrði fyrirspurnar fyrir sendingar sem eru stofnaðar í skjámyndinni **Bylgjuafmarkanir**. Þetta svæði er ekki tiltækt fyrir framleiðslubylgjur eða kanban-bylgjur.
    > Grænt gátmerki í **Í bylgju** dálkinum gefur til kynna að sendingunni hefur verið bætt við bylgjuna.

### <a name="process-the-wave-to-create-the-picking-work"></a>Vinna úr bylgjunni til að stofna vinnutiltekt

Þegar bylgja hefur verið stofnuð og inniheldur allar nauðsynlegar línur er hægt að vinna úr henni til að stofna samsvarandi tiltekt.

#### <a name="automatically-process-a-wave"></a>Vinna sjálfvirkt úr bylgju

Til að vinna sjálfkrafa úr bylgju skaltu setja upp viðeigandi [Bylgjusniðmát](wave-templates.md) með nauðsynlegum valkostum sjálfvirkrar úrvinnslu.

#### <a name="manually-process-a-wave"></a>Vinna handvirkt úr bylgju

Aðeins er hægt að vinna úr bylgju þegar **Staða bylgju** er *Stofnuð*. Þegar búið er að vinna úr bylgju verður **Stöðu bylgju** breytt í *Haldið*.

Til að vinna handvirkt úr bylgju sem er með allt nauðsynlegt efni skal fylgja þessum skrefum:

1. Eftir því hvaða gerð bylgju á að meðhöndla, gerið eitt af eftirfarandi:

    - Veljið **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Sendingarbylgjur** \> **Allar bylgjur**. Á aðgerðasvæðinu skal velja **Bylgja**.
    - Veljið **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Framleiðslubylgjur** \> **Allar framleiðslubylgjur**. Á aðgerðasvæðinu skal velja **Framleiðslubylgja**.
    - Veljið **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Kanban-bylgjur** \> **Allar kanban-bylgjur**. Í aðgerðasvæðinu velurðu **Stofna bylgju**.

1. Veljið til að vinna úr bylgju. Á aðgerðasvæðinu skal velja **Úrvinnsla**.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Losa bylgjuna í vöruhúsið til að hefja tiltekt og pökkun

Vinna þarf úr bylgju áður en hægt er að losa hana. Þegar bylgjan er losuð, er tiltektarvinnan tiltæk í vöruhúsinu. Hægt er að hætta við bylgju eftir að henni er sleppt og bæta við fleiri línum en ekki er hægt að breyta línunum.

#### <a name="automatically-release-a-wave"></a>Losa bylgju sjálfkrafa

Til að vinna sjálfkrafa úr bylgju skaltu setja upp viðeigandi [Bylgjusniðmát](wave-templates.md) með nauðsynlegum valkostum sjálfvirkrar úrvinnslu.

#### <a name="manually-release-a-wave"></a>Losa bylgju handvirkt

Til að losa bylgju handvirkt skal fylgja þessum skrefum:

1. Eftir því hvaða gerð bylgju á að losa, gerið eitt af eftirfarandi:

      - Veljið **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Sendingarbylgjur** \> **Allar bylgjur**. Á aðgerðasvæðinu skal velja **Bylgja**.
      - Veljið **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Framleiðslubylgjur** \> **Allar framleiðslubylgjur**. Á aðgerðasvæðinu skal velja **Framleiðslubylgja**.
      - Veljið **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Kanban-bylgjur** \> **Allar kanban-bylgjur**. Í aðgerðasvæðinu velurðu **Stofna bylgju**.

1. Veljið til að losa bylgjuna. Á aðgerðasvæðinu skal velja **Losa bylgju**.

## <a name="containerize-a-wave"></a>Gera gám úr bylgju

Sjálfvirk gámun stofnar gáma- og tínsluvinnu fyrir sendingar þegar bylgja er afgreidd. Frekari upplýsingar um hvernig á að setja það upp er að finna í [Gámun](wave-containerization.md).

## <a name="work-with-the-scheduled-work-creation"></a>Vinna með áætlaða vinnustofnun

Þegar aðgerðin *Áætla stofnun vinnu* er virkjuð mun bylgjuvinnsla stofna áætlaða vinnu sem verður á endanum notuð af nýju stofnferli vinnu. Við stofnun vinnu verður lokað fyrir vinnu með því að nota eiginleikann *Vinnulokun fyrir allt fyrirtækið*. Frekari upplýsingar er að finna í [Áætla stofnun vinnu í bylgju](configure-wave-schedule-work-creation.md).

Eftirfarandi flæðirit sýnir hvernig áætluð vinna er stofnuð við bylgjuvinnslu.

![Áætla stofnun vinnu.](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>áætluð vinna

Síðan **Upplýsingar um áætlaða vinnu** (**Vöruhúsakerfi \> Vinna \> Upplýsingar um áætlaða vinnu**) sýnir upplýsingar um áætlaða vinnu sem er upphaflega stofnuð í bylgjuvinnslu. Eftirtalin **Staða ferlis** gildi eru tiltæk:

- **Í biðröð** - Áætluð vinna bíður þess að vera notuð til að stofna vinnu.
- **Lokið** – Áætluð vinna hefur verið notuð til að stofna vinnu.
- **Mistókst** – Ekki tókst að vinna bylgjuna. Athugið að áætluð vinna getur verið í stöðu sem **Mistókst** með eða án tengdrar raunvinnu. Þegar stofnferli raunverulegrar vinnu tekst ekki helst raunveruleg vinna í stöðunni *Hætt við*.

### <a name="batch-job-for-the-work-creation-process"></a>Runuvinnsla fyrir stofnferli vinnu

Til að skoða runuvinnslur fyrir vinnslubylgjur skal velja **Runuvinnslur** á aðgerðasvæðinu á **Allar bylgjur** síðunni.

Héðan er hægt að skoða allar upplýsingar um runuverk fyrir hvert runuvinnslukenni.

## <a name="cancel-a-wave"></a>Hætta við bylgju

Ef þess gerist þörf er hægt að hætta við bylgju sem búið er að vinna úr. Til að hætta við bylgju og tiltektarvinnu sem var stofnuð, skal fylgja þessum skrefum:

1. Gerið eitt af eftirfarandi eftir því hver gerð bylgju er sem hætta á við:

      - Farið í **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Sendingarbylgjur** \> **Allar bylgjur**.
      - Farið í **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Framleiðslubylgjur** \> **Allar framleiðslubylgjur**.
      - Farið í **Vöruhúsakerfi** \> **Almennt** \> **Bylgjur** \> **Kanban-bylgjur** \> **Allar kanban-bylgjur**.

1. Veljið bylgjuna sem á að hætta við. Á aðgerðasvæðinu, í flipanum **Vinna**, skal velja **Hætta við**.

## <a name="review-wave-batch-job-details"></a>Skoða upplýsingar um runuvinnslu bylgju

Notið síðuna **Upplýsingar um runuvinnslu bylgju** til að skoða runuvinnslurnar og tengd verk sem tengjast einhverri bylgju. Þetta er mjög gagnlegt við úrræðaleit bylgju sem tókst ekki. Án þessa eiginleika munu aðeins stjórnendur yfirleitt hafa aðgang að upplýsingum um runuvinnslu. Hægt er að gera síðuna **Upplýsingar um runuvinnslu bylgju** aðgengilega notendum öðrum en stjórnendum og bjóða upp á skrifvarið yfirlit yfir runuvinnslur og tengd verk.

### <a name="enable-the-wave-batch-job-details-page"></a>Virkja upplýsingasíðu bylgjurunuvinnslu

Ef kerfið inniheldur ekki nú þegar síðuna **Upplýsingar um runuvinnslu bylgju** skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Upplýsingar um runuvinnslu bylgju*.

### <a name="use-the-wave-batch-job-details-page"></a>Nota upplýsingasíðu bylgjurunuvinnslu

Síðan **Upplýsingar um runuvinnslu bylgju** sameinar runuvinnslur og runuvinnsluverk, sem gerir kleift að skoða betur öll bylgjuskrefin án þess að þurfa að flakka fram og til baka á milli einnar runuvinnslu og lista yfir runuverk. Síðan veitir einnig aðgang að runukladdanum og, ef nauðsynlegar heimildir eru til staðar, tengil á síðuna **Runuvinnslur**.

Til að opna þessa síðu skal velja bylgju á einhverri bylgjusíðunni og síðan velja **Upplýsingar um runuvinnslu bylgju** á aðgerðasvæðinu.

## <a name="review-load-validation-and-error-messages"></a>Fara yfir villuleit hleðslu og villuboð

Við bylgjuvinnslu villuleitar kerfið og sýnir stöðuna fyrir hverja hleðslulínu í bylgjunni. Ef engar viðvaranir koma upp verður farið yfir í næsta bylgjaskref. Ef viðvaranir koma upp verður í staðinn sýnd eftirfarandi villa þegar búið er að villuleita alla bylgjuna:

> Fann ógildar hleðslulínur í bylgju. Fjarlægið ógildar hleðslulínur.

Því næst verður hægt að fara yfir lokastöðu hverrar hleðslulínu í bylgjunni og leiðrétta allar viðvaranir áður en reynt er aftur. Þetta gerir kleift að svara öllum viðvörunum strax áður en unnið er úr bylgjunni á nýjan leik. (Í fyrri útgáfum hætti kerfið að vinna úr bylgjunni eftir fyrstu viðvörun og var því aðeins hægt að laga eina viðvörun í einu.)

Það hvernig kerfið birtir stöðuskilaboð bylgjuvinnslunnar fer eftir því hvernig valkosturinn **Stofna sögukladda fyrir bylgjuvinnslu** var stilltur á síðunni **Færibreytur vöruhúsakerfis**.

- Þegar **Stofna sögukladda fyrir bylgjuvinnslu** er stillt á *Nei* verða stöðuskilaboð hleðslulínunnar sýnd í **Upplýsingaskránni**.
- Þegar **Stofna sögukladda fyrir bylgjuvinnslu** er stillt á *Já* eru stöðuskilaboð hleðslulínunnar sýnd á síðunni **Sögulegur kladdi fyrir bylgjuvinnslu**. Til að skoða kladdann skal fara í **Vöruhúsakerfi \> Bylgjur á útleið \> Sögulegur kladdi bylgjuvinnslu**.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Skilgreina dæmi um bylgjuvinnslu](tasks/configure-wave-processing.md)
- [Bylgjusniðmát](wave-templates.md)
- [Gámun](wave-containerization.md)