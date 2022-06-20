---
title: Gæðapantanir
description: Þessi grein lýsir því hvernig eigi að búa til gæðapantanir handvirkt eða sjálfvirkt og hvernig eigi að vinna með þær til að framkvæma skoðanir og skrá prófunarniðurstöður í Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb7ab1de0fb4d93ed18f1862630c1af7af7f3095
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857780"
---
# <a name="quality-orders"></a>Gæðapantanir

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig eigi að búa til gæðapantanir handvirkt eða sjálfvirkt og hvernig eigi að vinna með þær til að framkvæma skoðanir og skrá prófunarniðurstöður í Microsoft Dynamics 365 Supply Chain Management.

## <a name="automatically-created-quality-orders"></a>Stofna gæðapantanir sjálfkrafa

Hægt er að skilgreina kerfið þannig að það búi sjálfkrafa til gæðapantanir sem byggja á reglum um sýnatöku vöru. Frekari upplýsingar er að finna í [Vörusýnataka gæðastjórnunar](quality-item-sampling.md).

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>Handvirkt stofnaðar gæðapantanir

Til að stofna gæðapöntun handvirkt, skal fylgja eftirfarandi skrefum:

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.
1. Veljið **Nýtt**.
1. Í svarglugganum **Gæðapantanir**, í reitnum **Tilvísunargerð**, skal velja birgðatilvísun sem gæðapöntunin þín mun tengjast. Fyrir lýsingu á tilvísunartegundum sem hægt er að velja um, sjá [Tilvísunargerðir gæðapöntunar](#ref-types) kafla síðar í þessari grein.

    > [!NOTE]
    > Birgðir sem tengjast völdu tilvísuninni verður að vera tiltæk. Ef engar birgðir eru í boði fyrir samsetningu af tilvísunargerð, magni og birgðavíddum sem er valið, koma upp villuboð.

1. Fylgdu einu af þessum skrefum, fer eftir gildinu sem þú valdir í reitinum **Gerð tilvísunar**.

    - Ef þú valdir **Birgðir** er ekki þörf á frekari upplýsingum um tilvísun.
    - Ef þú valdir **Sala** eða **Kaup** sklatu tilgreina eftirfarandi upplýsingar:

        - **Reikningsval** – Tilvísun í númer viðskiptavinar eða lánardrottins.
        - **Tilvísunarnúmer** – Vísa í númer sölupöntunar eða innkaupapöntunar.
        - **Tilvísunarlota** – Vísa í tiltekna sölupöntunarlínu eða innkaupapöntunarlínu.

    - Ef þú valdir **Framleiðsla**, **Biðgeymsla** eða **Framleiðsla aukaafurðar** í reitnum **Tilvísunarnúmer** skal vísa í framleiðslupöntunina, runupöntunina eða biðgeymslupöntunarnúmerið.
    - Ef valið var **Leiðaraðgerð** skal tilgreina eftirfarandi upplýsingar:

        - **Tilvísunarnúmer** – Vísa í númer framleiðslupöntunar eða runupöntunar.
        - **Aðg.nr.** – Vísa í tiltekið númer leiðaraðgerðar.
        - **Aðgerð** – Tilvísun í tiltekna leiðaraðgerð.
        - **Tilfang** – Vísa í tiltekið tilfang sem þarf að nota með leiðaraðgerðinni.

1. Veljið þann flokk prófana sem á að framkvæma í svæðinu **Prófunarflokkur**.
1. Í reitinn **Magn** skal færa inn vörumagnið sem á að prófa.
1. Í hlutanum **Birgðavíddir** skal færa inn frekari birgðavíddir sem eru nauðsynlegar fyrir valda vöru.
1. Veljið **Í lagi**.

Þegar gæðapöntun hefur verið stofnuð er hægt að hefja skoðun á birgðum og skrá niðurstöður prófana. Frekari upplýsingar um hvernig á að skrá og staðfesta prófunarniðurstöður er að finna í [Skoða vörugæði](tasks/inspect-quality-goods.md).

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Tilvísunargerðir gæðapöntunar

Gæðapantanir eru notaðar til að rekja upplýsingar um skoðanir og prófunarniðurstöður fyrir tiltekna birgðavöru í vöruhúsinu. Gæðapöntun verður að innihalda tilvísun sem táknar uppruna birgðanna sem verið er að prófa. Gæðapantanir geta verið tengdar eftirfarandi tilvísunargerðum:

- **Birgðir** – Þessi tilvísunartegund gefur til kynna að þú sért að skoða hvaða birgðir eru tiltækar. Eftirlit af þessari gerð er yfirleitt handahófskennt eða ófyrirhugað og er gert þegar vöruhúsastarfskraftur greinir vandamál.
- **Sala** – Þessi tilvísunargerð gefur til kynna að þú sért að skoða birgðir sem tengjast tiltekinni sölupöntun. Skoðanir af þessari gerð eru yfirleitt tengdar forskriftum viðskiptavinar eða myndun greiningarvottorðs (CoA) sem útvega þarf viðskiptavini sem hluta af sendingu. (CoA er stundum einnig kallað samræmisvottorð \[CoC\].)
- **Innkaup** – Þessi tilvísunargerð gefur til kynna að þú sért að skoða birgðir sem tengjast innkaupapöntun. Eftirlit af þessari gerð er oft notað til að skoða mótteknar vörur áður en þær eru settar í birgðir eða notaðar í framleiðsluferli.
- **Framleiðsla** – Þessi tilvísunargerð gefur til kynna að þú sért að skoða birgðir sem eru tengdar framleiðslupöntun. Eftirlit af þessari gerð er oft notað til að skoða tilbúnar vörur áður en þær eru settar í birgðir.
- **Biðgeymsla** – Þessi tilvísunargerð gefur til kynna að þú sért að skoða birgðir sem eru tengdar biðgeymslupöntun. Biðgeymslupantanir eru sérstök tegund pöntunar sem rekja birgðir í aðskildu vöruhúsi eða aðskildu svæði í vöruhúsinu. Eftirlit af þessari gerð er oft notað til að skoða vörur sem viðskiptavinur hefur skilað eða sem hafa verið settar í biðgeymslu til frekari greiningar. Biðgeymslupantanir er hægt að mynda úr gæðapöntununum. Einnig er hægt að búa þær til úr öðrum uppruna og síðan er hægt að tengja gæðapantanir við biðgeymslupantanirnar.
- **Leiðaraðgerð** – Þessi tilvísunartegund gefur til kynna að þú sért að skoða birgðir sem tengjast tilteknu skrefi leiðarinnar fyrir framleiðslupöntun. Skoðanir af þessari gerð eru yfirleitt notaðar til að greina verk í vinnslu (VÍV) fyrir afurð áður en þær fara yfir í næsta skref framleiðsluferlisins.
- **Framleiðsla aukaafurðar** – Þessi tilvísunargerð gefur til kynna að þú sért að skoða birgðir sem tengjast aukaafurð af framleiðslupöntun. Eftirlit af þessari gerð er venjulega notað til að skoða aukaafurð í runupöntun áður en aukaafurðinni er bætt við birgðir.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Skoða og stofna gæðapantanir úr ýmsum hlutum kerfisins

Gæðapantanir er hægt að má stofna handvirkt. Einnig er sjálfkrafa hægt að stofna þær byggðar á gæðatengslunum sem eru skilgreind. Nánari upplýsingar um hvernig á að búa til og stjórna sjálfvirkri stofnun gæðapantana eru í [Gæðatengingar](quality-associations.md).

Hægt er að nota síðu gæðapöntunar til að búa handvirkt til nýja gæðapöntun eða skoða stöðu gæðapöntunar sem tengist annarri færslu. Nokkrar leiðir eru til að opna síðuna fyrir gæðapöntun.

### <a name="from-the-quality-orders-page"></a>Af síðu gæðapöntunar

Til að búa gæðapantanir til handvirkt og skoða allar fyrirliggjandi gæðapantanir skal fara í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**. Eftirstöðvar þessarar greinar veita frekari upplýsingar um hvernig á að vinna með **Gæða pantanir** síðu.

### <a name="from-sales-orders"></a>Úr sölupöntunum.

Til að vinna með gæðapantanir sem tengjast sölupöntunum skal fara í **Sala og markaðssetning \> Sölupantanir \> Allar sölupantanir** og síðan fylgja einhverjum af þessum skrefum:

- Opnaðu sölupöntun eða veldu hana í hnitanetinu. Því næst skal á aðgerðasvæðinu, í flipanum **Taka til og pakka**, í flokknum **Gæðastjórnun**, velja **Gæðapantanir** til að opna síðuna **Gæðapantanir**. Þar er hægt að skoða, stofna eða uppfæra gæðapantanir sem tengjast sölupöntuninni.
- Opnið sölupöntun og síðan í flipanum **Haus** skal velja flýtiflipann **Almennt**. Reiturinn **Staða gæðapöntunar** sýnir heildarstöðu allra gæðapantana sem tengjast sölupöntuninni.
- Opnið sölupöntun og síðan í flipanum **Línur** skal velja flýtiflipann **Sölupöntunarlínur**. Dálkurinn **Staða gæðapöntunar** sýnir stöðu hverrar línu sölupöntunarinnar.

### <a name="from-purchase-orders"></a>Úr innkaupapöntun

Til að vinna með gæðapantanir sem tengjast innkaupapöntunum skal fara í **Innkaup og uppruni \> Innkaupapantanir \> Allar innkaupapantanir** og fylgið síðan einhverju af þessum skrefum:

- Opnaðu innkaupapöntun eða veldu hana í netinu. Því næst skal á aðgerðasvæðinu, í flipanum **Taka á móti**, í flokknum **Gæðastjórnun**, velja **Gæðapantanir** til að opna síðuna **Gæðapantanir**. Þar er hægt að skoða, stofna eða uppfæra gæðapantanir sem tengjast innkaupapöntuninni.
- Opnið innkaupapöntun og síðan í flipanum **Haus** skal velja flýtiflipann **Almennt**. Reiturinn **Staða gæðapöntunar** sýnir heildarstöðu allra gæðapantana sem tengjast innkaupapöntuninni.
- Opnið innkaupapöntun og síðan í flipanum **Línur** skal velja flýtiflipann **Innkaupapöntunarlínur**. Dálkurinn **Staða gæðapöntunar** sýnir stöðu hverrar línu innkaupapöntunarinnar.

### <a name="from-production-orders"></a>Úr framleiðslupöntunum

Til að vinna með gæðapantanir sem tengjast framleiðslupöntunum skal fara í **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** og síðan fylgja einhverju þessara skrefa:

- Opnaðu framleiðslupöntun eða veldu hana í netinu. Því næst skal á aðgerðasvæðinu, í flipanum **Yfirlit**, í flokknum **Stjórna gæðum**, skal velja **Gæðapantanir** til að opna síðuna **Gæðapantanir**. Þar er hægt að skoða, stofna eða uppfæra gæðapantanir sem tengjast framleiðslupöntuninni.
- Opnaðu framleiðslupöntun eða veldu hana í netinu. Því næst skal á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Framleiðslupplýsingar**, skal velja **Leið** til að opna síðuna **Framleiðsluleið**. Til að skoða gæðapantanir sem tengjast leiðaraðgerð skal fylgja einum þessara skrefa:

    - Veljið leiðaraðgerð markmiðs í hnitanetinu. Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Gæðapantanir**.
    - Veljið gildið í **Aðg.nr** reitnum fyrir leiðaraðgerð markmiðs til að opna upplýsingasíðuna **Framleiðsluleið**. Í flýtiflipanum **Almennt** sýnir reiturinn **Staða gæðapöntunar** stöðu gæðapantana sem tengjast leiðaraðgerðinni.

- Opnið framleiðslupöntun og veljið flýtiflipann **Almennt**. Reiturinn **Staða gæðapöntunar** sýnir stöðu gæðapantana sem tengjast framleiðslupöntuninni.

### <a name="from-quarantine-orders"></a>Úr biðgeymslupöntunum

Til að vinna með gæðapantanir sem tengjast biðgeymslupöntunum skal fara í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Biðgeymslupantanir** og síðan fylgja einu þessara skrefa:

- Farið yfir gildin í dálkinum **Staða gæðapöntunar**. Á þennan hátt er hægt að kynna sér heildarstöðu allra gæðapantana sem tengjast hverri biðgeymslupöntun í kerfinu.
- Veljið biðgeymslupöntun í hnitanetinu og síðan á aðgerðasvæðinu skal velja **Gæðapantanir** til að skoða, stofna eða uppfæra gæðapantanir sem tengjast biðgeymslupöntuninni.

## <a name="advanced-actions-for-quality-orders"></a>Ítarlegar aðgerðir fyrir gæðapantanir

Hægt er að grípa til ýmissa aðgerða á gæðapöntunum til að stjórna stöðunni, mynda skjöl og grennslast fyrir um frekari upplýsingar.

### <a name="reopen-a-quality-order"></a>Enduropna gæðapöntun

Að sjálfgefnu er ekki lengur hægt að breyta eða uppfæra gæðapöntun þegar búið er að staðfesta hana og hún staðist prófanir. Stundum gæti þó þurft að opna gæðapöntun aftur eftir að henni hefur verið lokið.

Til að opna gæðapöntun aftur skal fylgja eftirfarandi skrefum.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.
1. Opnaðu gilda gæðaröð eða veldu hana í hnitanetinu.
1. Á aðgerðasvæðinu skal velja **Enduropna gæðapöntun**.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Búa til greiningarskírteini fyrir gæðapöntun

CoA er skýrsla sem er búin til af gæðateymi fyrirtækisins. Það staðfestir að vara uppfylli ákveðnar reglur eða kröfur. Viðskiptavinir þínir eða eftirlitsstofnanir á þínu svæði gætu krafist CoA. Einnig gæti verið gerð krafa um það eftir því hver atvinnugreinin er og gerð afurða sem þú meðhöndlar, kaupir inn, framleiðir eða selur.

Supply Chain Management gerir þér kleift að mynda CoA úr gæðapöntun. Skýrslan mun innihalda niðurstöður allra prófana í gæðapöntuninni þar sem valkosturinn **Skýrsla greiningarvottorðs** er stillt á *Já*. Hægt er að stilla þennan valkost sjálfkrafa á grundvelli prófsins sem er skilgreint á síðunni **Prófanir**. Hins vegar er hægt að hnekkja stillingu tiltekinna prófa fyrir tiltekna gæðapöntun.

Til að búa til CoA fyrir gæðapöntun skal fylgja eftirfarandi skrefum.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.
1. Veljið gæðapöntunina sem búa á til CoA fyrir.
1. Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Greiningarskírteini**.
1. Á síðunni **Greiningarvottorð**, á aðgerðasvæðinu, skal velja **Nýtt**.
1. Valfrjálst: Í reitnum **Tengiliður** skal velja einstakling tengiliðar sem senda á vottorðið til.
1. Á aðgerðasvæðinu skal velja **Prenta**.
1. Skilgreindu hvernig á að prenta skýrsluna í glugganum **Greiningarskírtein**. Veljið síðan **Í lagi** til að prenta skýrsluna í prentara, á skjáinn, í skrá eða í tölvupóst.
1. Lokaðu síðunum.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Útiloka eða opna birgðir fyrir gæðapöntun

Þegar gæðapöntun er sjálfkrafa búin til út frá gæðatengingu er hægt að skilgreina vörusýnatökuna sem er úthlutað á gæðatenginguna til að loka fyrir fullt birgðamagn tilvísunarinnar sem verið er að prófa. Frekari upplýsingar um vörusýnatöku er að finna í [Vörusýnataka gæðastjórnunar](quality-item-sampling.md).

Ef þú ert ekki að nota fulla lokun eða ef þú ert að búa til gæðapöntun handvirkt býr kerfið sjálfkrafa til birgðalæsingu fyrir magni vörunnar sem verið er að prófa í gæðapöntuninni. Í færslunni sem stofnuð er á síðunni **Birgðalæsing** er reiturinn **Gerð birgðalæsingar** stilltur á *Gæðapöntun*.

Til að skoða og breyta birgðalæsingu fyrir gæðapöntun sem er valin á síðunni **Birgðalæsing** skal velja **Fyrirspurnir \> Birgðalæsing** á aðgerðasvæðinu. Frekari upplýsingar er að finna í [Birgðalæsingar](inventory-blocking.md).

### <a name="inquire-about-the-details-of-a-quality-order"></a>Fyrirspurn um upplýsingar gæðapöntunar

Notaðu eftirfarandi hnappa á aðgerðarúðunni á síðunni **Gæðapantanir** til að skoða frekari upplýsingar um eða tengdar gæðapöntun:

- **Fyrirspurnir \> Upplýsingar um verk** – Opnaðu síðu þar sem hægt er að skoða verk vöruhúss sem tengjast gæðapöntuninni.
- **Fyrirspurnir \> Ósamkvæmni** – Opnaðu síðu þar sem hægt er að skoða ósamkvæmi sem tengist gæðapöntuninni.
- **Birgðir** – Skipanirnar í þessari valmynd eru algengar fyrir allar birgðafærslur. Þú getur notað þær til að skoða eða uppfæra upplýsingar eins og færslur, lagerbirgðir, frátekningar og merkingar.

### <a name="create-cases-related-to-quality-orders"></a>Stofna mál sem tengjast gæðapöntunum

Þú getur búið til mál sem tengjast gæðapöntunum. Á þennan hátt er hægt að rekja upplýsingar um málin og vinna að lausn þeirra. Síðan er hægt að nota verkflæðiseiginleika málastjórnunar til að beina máli í gegnum fyrirframskilgreint viðskiptaferli til að fá frekari samþykktir eða fá frekari upplýsingar um tiltekið vandamál. Einnig er hægt að nota eiginleika þekkingarskráa til að búa til þekkingargrunn með úrlausnum á algengum vandamálum.

## <a name="case-management-examples-for-quality-management"></a>Dæmi málastjórnunar fyrir gæðastjórnun

### <a name="example-1"></a>Dæmi 1

Þú vinnur fyrir framleiðslufyrirtæki sem verður að fylgja ströngum reglugerðum sem tengjast framleiðslu á eftirlitsskyldum afurðum á borð við mat. Gæðapantanir eru notaðar til að skrá og fylgjast með upplýsingum um gæði vara í framleiðsluferlinu. Ef gæðapöntun fellur á tilteknum prófum gæti verið vandamál tengt búnaðinum. Mál eru notuð til að fylgja viðskiptaferli og koma vandamálinu til réttra hönnuða þannig að hægt sé að komast að rót vandans. Til að auðvelda eftirfylgni viðskiptaferla heldur fyrirtækið úti þekkingargrunni yfir algeng vandamál sem tengjast gæðapöntunum og vandamálum varðandi búnað.

### <a name="example-2"></a>Dæmi 2

Þú vinnur fyrir dreifingarfyrirtæki sem sendir afurðir sem hægt er að sérsníða að ýmsum löndum og svæðum. Sumir viðskiptavinir eru með strangar verklýsingar sem þarf að fylgja. Að öðrum kosti gætu gjöld og skil eða endurgreiðslur orðið til. Þú notar gæðapantanir til að rekja upplýsingar um hvert próf og niðurstöður sem samsvara kröfum viðskiptavina. Mál eru notuð til að fara yfir og samþykkja upplýsingar fyrir CoA áður en skjalið er myndað og hengt við ásamt annarri pappírsvinnu afhendingar.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gæðastjórnunarferli](quality-management-processes.md)
- [Gæðaprófun](quality-tests.md)
- [Gæðaprófunarflokkar](quality-test-groups.md)
- [Gæðatengingar](quality-associations.md)
- [Gæðastjórnunarferli](quality-management-processes.md)
- [Virkja stjórnun gæða og ósamkvæmni](enable-quality-management.md)
- [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
