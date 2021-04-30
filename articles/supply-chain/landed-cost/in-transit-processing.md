---
title: Vinnsla á vörum í flutningi
description: Þetta efnisatriði útskýrir hvernig á að vinna með pantanir á vörum í flutningi. Þegar pöntun eða ferð er sett upp til að nota vinnslu á vörum í flutningi er hægt að reikningsfæra vörur áður en þær hafa verið mótteknar í vöruhúsi fyrir notkun.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: fff3c3cfe5d0628fd4df6e719b72bc134c9d9c0a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909452"
---
# <a name="goods-in-transit-processing"></a>Vinnsla á vörum í flutningi

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að vinna með pantanir á vörum í flutningi. Þessi gerð pöntunar er aðeins notuð af **Heildarkostnaður** einingunni. Þegar pöntun eða ferð er sett upp til að nota vinnslu á vörum í flutningi þarf ekki að bíða þar til vörur hafa verið mótteknar í vöruhúsinu áður en hægt er að reikningsfæra þær. Þess í stað eru vörurnar reikningsfærðar þegar þær fara úr vöruhúsi lánardrottins eða höfn upprunastað og fjármagnskostnaður er viðurkenndur þegar ferðin hefst. Þessi virkni gerir kleift að taka yfir eignarhald á birgðum með réttu vegna þess að vörur verða oft eign fyrirtækisins þegar þær fara frá sendingarhöfn.

Þegar vöruflutningspantanir eru notaðar eru fjárhagslega uppfærðar vörurnar mótteknar í bráðabirgðavöruhúsi sem er þekkt sem flutningsvöruhús. Vörurnar eru síðan geymdar í þessu vöruhúsi þangað til hægt er að taka á móti þeim í vöruhúsi lokaáfangastaðar (þ.e. vöruhúsið sem er skilgreint í innkaupalínunni). Ekki er hægt að fjarlægja þær handvirkt.

Svo framarlega sem vörurnar eru í flutningi eru þær ekki í boði í birgðum og ekki er hægt að tína þær úr birgðum fyrir afhendingu. Hins vegar er hægt að skoða birgðir á vörum í flutningi. Einnig er hægt að nota vörurnar fyrir aðaláætlanagerð. Í þessu tilfelli skal nota staðfestan afhendingardag innkaupapöntunarlínunnar sem væntanlega dagsetningu þegar hægt verður að nota birgðir.

Í eftirfarandi hlutum er lýst uppsetningunni sem er nauðsynleg til að vinna úr birgðum og ferðum með því að nota hugmyndina og virknina fyrir vörur í flutningi.

## <a name="terms-of-delivery"></a>Afhendingarskilmálar

Þegar einingin **Heildarkostnaður** er virkjuð er einingin fyrir venjulega *afhendingarskilmála* aukin til að styðja eiginleikann fyrir vörur í flutningi.

Þegar valkosturinn **Stjórnun á vörum í flutningi** er stilltur á *Já* fyrir viðeigandi skrá notkunarskilmála eru vörunum komið fyrir í flutningsvöruhúsi. Þessi aðgerð er aðeins ræst ef ekki er unnið úr birgðamóttökunni áður en unnið er úr reikningnum. Þegar afhendingarskilmálar fyrir pöntun eru stilltir til að nota vörur í flutningi geta notendur ekki lengur bókað innhreyfingarskjal fyrir innkaupapöntunina. Villa kemur upp ef það er reynt. Villuboðin gefa upp að nota þurfi virkni fyrir vörur í flutningi til að halda áfram.

Til að vinna með upplýsingar um afhendingarskilmála skal fara í **Innkaup og aðföng \> Uppsetning \> Dreifing \> Afhendingarskilmálar**. Eftirfarandi tafla lýsir reitunum sem einingin **Heildarkostnaður** bætir við síðuna **Afhendingarskilmálar** til að styðja virknina fyrir vörur í flutningi. Báðir reitirnir eru á flýtiflipanum **Almennt**. Frekari upplýsingar um aðra reiti á þessari síðu er að finna í [Afhendingarskilmálar (skjámynd)](/dynamicsax-2012//terms-of-delivery-form).

| Svæði | lýsing |
|---|---|
| Afhendingarhöfn áskilin | Stillið þennan valkost á *Já* ef afhendingarhöfn er áskilin þegar afhendingarskilmálarnir eiga við. |
| Stjórnun á vörum í flutningi | Stillið þennan valkost á *Já* til að nota stjórnun á vörum í flutningi þegar afhendingarskilmálarnir eiga við. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Vöruhús fyrir vörur í flutningi og undirafhendingu

Þegar einingin **Heildarkostnaður** er virkjuð er einingin fyrir venjuleg *vöruhús* aukin til að gera kleift að reikningsfæra innkaupapantanir á meðan vörurnar eru í flutningsvöruhúsi.

Heildarkostnaður bætir við tveimur nýjum gerðum af vöruhúsi: *vörur í flutningi* og *undirafhending*. Hægt er að velja vöruhús af báðum gerðum sem sjálfgefið vöruhús. Árangursrík úrvinnsla á vöruflutningspöntunum krefst þess að bæði flutningsvöruhús og vöruhús undirafhendingar séu skilgreind á síðunni **Vöruhús**. Því næst, fyrir hvort sjálfgefið vöruhús sem verður notað með heildarkostnaði og vörum í flutningi, verður að velja flutningsvöruhúsið og vöruhús undirafhendingar fyrir tiltæk vöruhús af hvorri gerð fyrir sig.

Vöruhús af gerðinni *vörur í flutningi* verður tengt við flutningsvöruhúsið og það vöruhús verður notað til að vinna úr vörum í vöruflutningspöntunum áður en þær eru mótteknar í vöruhúsi á lokaáfangastað. Almennt er eitt flutningsvöruhús nóg fyrir hvert svæði ef svæði og vöruhús eru einu birgðavíddirnar sem eru notaðar fyrir birgðastjórnun. Ef birgðavídd staðsetningar er einnig notuð þarf að setja upp flutningsvöruhús fyrir báðar samsetningarnar af svæði og vöruhúsi þannig að einnig hægt sé að tilgreina sjálfgefna staðsetningu.

Til að vinna með stillingar á vörum í flutningi fyrir vöruhúsin skal fara í **Birgðastjórnun \> Uppsetning \> Sundurliðun birgða \> Vöruhús**. Eftirfarandi tafla lýsir reitunum sem einingin **Heildarkostnaður** bætir við síðuna **Vöruhús** til að styðja virknina fyrir vörur í flutningi. Báðir reitirnir birtast á flýtiflipanum **Almennt**. Frekari upplýsingar um aðra reiti á síðunni má finna í [Vöruhús (skjámynd)](/dynamicsax-2012//warehouses-form).

| Svæði | lýsing |
|---|---|
| Vörur í flutningsvöruhúsi | Auðkenna flutningsvöruhúsið sem tengist aðalvöruhúsinu. |
| Vöruhús vanafhendingar | Auðkenna vöruhús undirafhendingar sem tengist aðalvöruhúsinu. |

## <a name="posting-rules-for-landed-cost"></a>Bókunarreglur fyrir heildarkostnað

Heildarkostnaður bætir við tveimur nýjum bókunarreglum sem hægt er að skilgreina. Þessar bókunarreglur eru notaðar til að bóka beina reikningsupphæð innkaupapöntunar til að bera kennsl á eignarhald á vörunum þegar þær yfirgefa upprunastað. Þetta ferli kemur í stað hugtaksins *mótteknar vörur ekki reikningsfærðar* vegna þess að vörurnar eru reikningsfærðar áður en þær eru mótteknar. <!-- KFM: Add a link to the related scenario when available. -->

Til að vinna með bókunarreglur skal opna **Birgðastjórnun \> Uppsetning \> Bókun \> Bókun**. Á flipanum **Innkaupapöntun** eru eftirfarandi nýjar bókunarreglur í boði:

- **Heildarkostnaður, vörur í flutningi** – Tilgreinið bókunarreglur fyrir stjórnun á vörum í flutningi.
- **Heildarkostnaður, uppsafnað gjald** – Tilgreinið bókunarreglur fyrir uppsöfnun gjalds.

## <a name="goods-in-transit-orders"></a>Vöruflutningspantanir

Hægt er að yfirfara og stjórna vöruflutningspöntunum með beinum hætti úr einingunni **Heildarkostnaður**. Hægt er að vinna úr vöruflutningspöntunum með beinum hætti af síðunni **Vöruflutningspantanir**. Annars er hægt að fara í ferðina sem tengist vöruflutningspöntunum og vinna úr allri ferðinni, flutningagámnum eða fólíóinu. Þegar ferð er reikningsfærð og vöruflutningspantanir eru stofnaðar er ný vöruflutningspöntun stofnuð fyrir hverja samsetningu af birgðum og birgðavíddum sem tengjast innkaupapöntunarlínunni.

Til að stjórna vörum í flutningi notar heildarkostnaður tveggja þrepa ferli:

1. Vara er móttekin þegar unnið er úr birgðareikningi og hún fær úthlutaða stöðuna *Í flutningi*.
1. Unnið er úr vöruflutningspöntunum á síðunni **Vöruflutningspantanir** og þær síðan mótteknar í vöruhúsinu sem er tilgreint í innkaupapöntuninni. Á því stigi er stöðunni breytt í *Móttekið*.

Til að vinna með vöruflutningspantanir skal fara í **Heildarkostnaður \> Reglubundin verk \> Vöruflutningspantanir**.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Birgðir mótteknar úr flutningsvöruhúsinu

Hægt er að taka á móti vörum úr vöruflutningspöntun á margan hátt en það fer eftir uppsetningu kerfisins.

### <a name="in-transit-receiving"></a>Móttaka á vörum í flutningi

Hægt er að taka á móti flutningi á einhverjum af eftirfarandi síðum:

- Á síðunni **Vöruflutningspantanir** skal velja línuna og síðan á aðgerðasvæðinu skal velja **Taka á móti**.
- Á síðunni **Allar ferðir** skal velja eða opna ferð. Því næst skal á aðgerðasvæðinu, í flipanum **Stjórna**, í flokknum **Vörur í flutningi**, velja **Taka á móti vörum í flutningi**.
- Á síðunni **Allir vörugámar** skal velja eða opna gám. Því næst skal á aðgerðasvæðinu, í flipanum **Stjórna**, í flokknum **Vörur í flutningi**, velja **Taka á móti vörum í flutningi**.
- Á síðunni **Öll fólíó** skal velja eða opna fólíó. Því næst skal á aðgerðasvæðinu, í flipanum **Stjórna**, í flokknum **Vörur í flutningi**, velja **Taka á móti vörum í flutningi**.

> [!NOTE]
> Móttaka á vörum í flutningi er yfirleitt notuð í kringumstæðum þar sem staðsetningar og rakning runu/raðnúmers er ekki notað.

### <a name="arrival-journal"></a>Komubók

Einnig er hægt að taka á móti vörum með því að stofna komubók. Hægt er að stofna komubók beint af ferðasíðunni. Bestu starfsvenjur sem fyrirtækið hefur tileinkað sér skera úr um hvort komubókin er notuð til að taka á móti vörum.

1. Opnið ferð, gám eða fólíó.
1. Á aðgerðasvæðinu, í flipanum **Stjórna**, í flokknum **Aðgerðir**, skal velja **Stofna komubók**.
1. Í svarglugganum **Stofna komubók** skal stilla eftirfarandi gildi:
    - **Frumstilla magn** – Stillið þennan valkost á *Já* til að stilla magnið úr magni í sendingu. Ef þessi valkostur er stilltur á *Nei* er ekkert sjálfgefið magn stillt í línum fyrir vörur í flutningi.
    - **Stofna úr vörum í flutningi** – Stillið þennan valkost á *Já* til að taka magn úr völdum vöruflutningslínum fyrir valda ferð, gám eða fólíó.
    - **Stofna úr pöntunarlínum** – Stillið þennan valkost á *Já* til að stilla sjálfgefið magn í komubók úr innkaupapöntunarlínunum. Aðeins er hægt að stilla sjálfgefið magn í komubókina á þennan hátt ef magnið í innkaupapöntunarlínunni stemmir við magnið í vöruflutningspöntuninni.

1. Meðhöndla komubók eins og lýst er í [Skrá innhreyfingu vöru með vörukomubók](/dynamicsax-2012/appuser-itpro/register-item-receipts-with-an-item-arrival-journal).

> [!NOTE]
> Komubókin er yfirleitt notuð í kringumstæðum þar sem staðsetningar og rakning runu/raðnúmers er notað, en vöruhúsið er ekki notað.
>
> Sjálfgefnar staðsetningar innhreyfinga á ekki að tilgreina í pöntunarlínum ef staðsetning frágangs verður tilgreind í komubókinni.

## <a name="warehouse-management"></a>Vöruhúsakerfi

Þegar einingin **Heildarkostnaður** er virkjuð, er ýmsum síðum í einingunni **Vöruhúsastjórnun** breytt þannig að úrvinnsla pöntunarinnar (sérstaklega úrvinnsla vöruflutningspöntunar) sé hægt að gera í gegnum eininguna **Heildarkostnaður**. Þessi hluti lýsir svæðunum og ferlunum sem bætt er við í einingunni **Vöruhúsakerfi**.

### <a name="mobile-device-menu-items"></a>Valmyndaratriði fartækis

Hægt er að taka á móti vörum með því að nota fartæki, að því tilskildu að valmynd fartækis og einingin **Vöruhúsastjórnun** hafi verið sett upp til að taka á móti vörum í vöruflutningspöntun. Þessi hluti lýsir uppsetningunni sem tengist móttöku vara í flutningi.

Til að setja upp fartæki fyrir vörur í flutningi ferðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.

Heildarkostnaður bætir eftirfarandi ferlum vinnustofnunar við valmyndaratriði fartækis til að styðja úrvinnslu á vörum í flutningi:

- Vörumóttaka á vörum í flutningi
- Móttaka og frágangur á vörum í flutningi

Skilgreiningarstillingarnar fyrir þessi ferli líkjast stillingunum fyrir [móttökuferli innkaupapöntunar og stofnferli frágangsvinnu](/dynamicsax-2012/appuser-itpro/configure-mobile-devices-for-warehouse-work). Hins vegar bætir ferlið *Móttaka og frágangur á vörum í flutningi* einnig við eftirfarandi reit.

- **Virkja lok flutningagáms** – Ef þessi valkostur er stilltur á *Já*, þegar frágangsvinnu er lokið, mun farsímaforrit vöruhúsakerfis bjóða upp á aukalegan valkost sem heitir **Lok flutningagáms**. Þegar sá valkostur er valinn verður starfsmaðurinn beðinn að staðfesta að gámnum sé lokið. Á þessu stigi verður unnið úr öllum of litlum móttökum sem undirfærslu.

### <a name="location-directives"></a>Staðsetningarleiðbeiningar

Heildarkostnaður bætir við nýrri vinnupöntunargerð sem heitir *Vörur í flutningi* á síðuna **Staðsetningarleiðbeiningar**. Þessi gerð vinnupöntunar ætti að vera skilgreind á sama hátt og [vinnupöntunargerðir innkaupapantana](/dynamicsax-2012/appuser-itpro/create-a-work-template).

### <a name="work-templates"></a>Vinnusniðmát

Heildarkostnaður bætir við nýrri vinnupöntunargerð sem heitir *Vörur í flutningi* á síðuna **Vinnusniðmát**. Þessi gerð vinnupöntunar ætti að vera skilgreind á sama hátt og [vinnusniðmát innkaupapöntunar](/dynamicsax-2012/appuser-itpro/create-a-work-template).