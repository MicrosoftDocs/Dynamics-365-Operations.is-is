---
title: Skilgreina afurðarsíur fyrir vöruhúsakerfifærslur
description: Þessi grein lýsir því hvernig á að stilla vörusíur og síunarkóða til að flokka birgðavörur í vöruhúsi. Einnig er hægt að nota síur til að tilgreina hvaða viðskiptavinir geta pantað tiltekna vöru og tilgreina hvaða vörur er hægt að kaupa frá tilteknum lánardrottni.
author: Mirzaab
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: f3d6cd373699d374c019f0db7befaffc169f4f6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850439"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Skilgreina afurðarsíur fyrir vöruhúsakerfifærslur

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að stilla vörusíur og síunarkóða til að flokka birgðavörur í vöruhúsi. Einnig er hægt að nota síur til að tilgreina hvaða viðskiptavinir geta pantað tiltekna vöru og tilgreina hvaða vörur hægt er að kaupa frá tilteknum lánardrottni.

Þar að auki er hægt að setja upp og nota afurðarsíur til að skipuleggja birgðavöru í vöruhúsi og sameina síaða vörur í síuflokka. Hægt er að nota síur til að setja vörur í flokka fyrir meðhöndlun, innkaup og söluferli. Hægt er að flokka vörur saman eða aðgreina þær hver frá annarri þegar þær eru meðhöndlaðar samkvæmt þyngdar- eða afgreiðslutakmörkunum. Einnig er hægt að tilgreina hvaða viðskiptavini eða lánardrottnum er hægt að kaupa vöru frá eða selja til.

## <a name="prerequisites"></a>Forkröfur

Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en byrjað er.

| Skilyrði | Fyrirmæli |
|---|---|
| Áður en hafist er handa við að skilgreina afurðir á síðunni **Upplýsingasíða um losaðar afurðir** þarf að kveikja á vöruhúsafærvinnslu fyrir geymsluvíddarflokk afurðarinnar. | Opnið **Afurðarupplýsingastjórnun \> Uppsetning \> Vídda- og afbrigðaflokkar \> Geymsluvíddaflokkur** og veljið eða stofnið geymsluvíddaflokk þar sem valkosturinn **Nota ferli vöruhúsakerfis** er stilltur á *Já*. |
| Ef notaðar eru viðskiptavinasíur og/eða lánardrottnasíur verður að virkja notkun þeirra í færibreytum vöruhúsakerfis. | Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**. Í flipanum **Afurðarsíur** skal stilla valkostinn **Virkja síur viðskiptavinar** og/eða **Virkja síur lánardrottins** á *Já*. |

## <a name="set-up-product-filters"></a>Setja upp afurðasíur

Afurðarsíur bjóða upp á allt að 10 **Síuheiti**, sem eru fasttextagildi (fasttexti). Þessi fasttextagildi eru tiltæk fyrir val þegar afurðsía er búin til. Fasttextagildin *1* til *kóða 10* eru skilgreind sem kerfisbundin og tákna ákveðna eiginleika eða eigind vöru. Til dæmis gæti *Kóði 1* táknað vörur með hættulega efnisflokkun. *Kóði 2* gæti táknað vörur sem aðeins lánardrottnar geta keypt. Afurðarsíur skilgreina síðan gildið fyrir **Síukóða** sem er tengdur við gildi fyrir **Síuheiti**.

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Afurðarsíur \> Afurðarsíur**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta afurðarsíu við hnitanetið.
1. Veljið gildi í reitnum **Síuheiti**.
1. Sláið inn gildi í reitinn **Síukóði**.

    ![Uppsetning afurðarsíu.](media/Product_Filters10.png "Uppsetning afurðarsíu")

1. Í reitnum **Lýsing** er fært inn heiti fyrir kóðann. Til dæmis gæti *Kóði 2* táknað lánardrottna. Síðan er hægt að stofna afurðassíu fyrir tiltekinn lánardrottin eða hóp lánardrottna. Fyrir frekari upplýsingar, sjá [Settu upp síukóða söluaðila](#vendor-product-filters) kafla síðar í þessari grein.

    ![Safn afurðarsía.](media/Product_Filters.png "Sett afurðarsía")

## <a name="set-up-product-filter-groups"></a>Skrá afurðasíuflokka

Hægt er að nota síuflokka til að taka saman síukóða. Þessi eiginleiki er gagnlegur þegar flokkurinn er notaður í fyrirspurn í staðsetningarleiðbeiningum og óskað er að leita að flokkur stað röð kóða. Hver síuflokkur er tengdur við vöruflokk.

> [!IMPORTANT]
> Ekki eru allir afurðarsíuflokkar tiltækir fyrir síukóða sem eru hærri en *Kóði 4* (þ.e. frá *Kóða 5* til *Kóða 10*). Til dæmis fyrir útgefnar afurðir, þótt öllum síukóðum afurða verði bætt við, verða flokkanir síukóða ekki uppfærðar. Þessi hegðun gæti verið uppfærð í síðari útgáfum.

Til að setja upp síuflokka skal fylgja þessum skrefum:

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Afurðarsíur \> Afurðarsíuflokkar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í reitunum **Hópur 1** og **Hópur 2** slærðu inn nöfn sem verða notuð til að flokka vörur.
1. Í flýtiflipanum **Upplýsingar** skal velja **Ný** til að bæta við línu.
1. Í reitina **Upphafsdagsetning/tími** og **Lokadagsetning/tími** skal færa inn upphafs- og lokadagsetningu fyrir síuflokkinn.
1. Í svæðinu **Vöruflokkur** skal velja vöruflokkinn sem afurðarsían á að gilda um.
1. Í reitunum **Kóði 1** til **Kóði 10** skal velja síukóðana sem á að hafa með í flokknum eins og þörf er á.

    ![Vöruflokkur.](media/ProdFilterGroup.png "Vöruflokkur")

> [!NOTE]
> Ef upp koma villuboð þegar síðunni er lokað er hugsanlegt að það vanti uppsetningu kóða. Á síðunni **Vöruflokkar** er hægt að gera kóðana áskilda fyrir vöruflokk með því að velja gátreitina **Úthluta síukóða 1 fyrir vöruflokkinn**, **Úthluta síukóða 2 fyrir vöruflokkinn** og svo framvegis.

## <a name="set-up-filter-codes-on-item-groups"></a>Setja upp síukóða á vöruflokkum

Með því að setja upp síukóða í vöruflokki er hægt að gera kóða sem eru nauðsynlegir fyrir afurðir sem eru tengdar við þann vöruflokk.

Til að setja upp síukóða í vöruflokkum, skal fylgja þessum skrefum:

1. Opnið **Birgðastjórnun \> Uppsetning \> Birgðir \> Vörulíkanaflokkar**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til vöruflokk.
1. Í reitinn **Vöruflokkur** skal slá inn heiti.
1. Færið inn lýsandi nafn í reitinn **Heiti**.
1. Í flýtiflipanum **Vöruhús**, í hlutanum **Sía sem krafist er**, skal velja gátreitina fyrir síukóðana sem verða að vera tilgreindir fyrir afurðir sem tengjast vöruflokknum.

    Til að uppfæra útgefna afurð skal opna síðuna **Upplýsingar um útgefnar afurðir** og síðan á aðgerðasvæðinu skal velja **Breyta**. Síurnar sem tengjast kóðum verða svo sýnilegar á flýtiflipanum **Vöruhús**.

    ![Vöruflokkar.](media/ItemGroup10.png "Vöruflokkar")

1. Í hlutanum **Sía fyrir vöruflokk** skal velja gátreitina fyrir síurnar sem verða að passa við síuflokkinn til að verða sjálfgefinn síuflokkur fyrir vöru.

    Ef til dæmis gátreitirnir **Nota síukóða 1** og **Nota síukóða 2** eru valdir, verða bæði síukóði 1 og síukóði 2 fyrir vöruna að passa við uppsetningu síuflokksins fyrir vöruflokkinn áður en hægt verður að velja síuflokkinn. Þegar ný vara er stofnuð verður valinn síuflokkur að sjálfgefnum síuflokki í reitunum **Flokkur 1** og **Flokkur 2** í flýtiflipanum **Vöruhús** á síðunni **Upplýsingar um útgefnar afurðir**.

> [!IMPORTANT]
> Afurðasíukóðar eru aðeins virkjaðir fyrir vörur sem nota ítarlegt vöruhúsakerfi.

## <a name="specify-filter-codes-for-released-products"></a>Tilgreina síukóða fyrir útgefin afurðir

Fylgið eftirfarandi skrefum til að gilgreina síukóða fyrir útgefnar afurðir. Til dæmis er hægt að nota síukóða til að flokka hættulegar vörur sem tilteknir lánardrottnar kaupa.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til vöru.
1. Í svarglugganum **Ný útgefin afurð** skal færa inn gögnin sem þarf til að stofna grunn nýrrar afurðar og síðan velja **Í lagi**.

    Afurðarsíukóðar eru ekki virkjaðir nema vöruflokkurinn sem er tengdur við afurðina hafi verið skilgreindur fyrir síukóðana.

    Nánari upplýsingar eru í [Stofna nýja afurð](../pim/tasks/create-new-product.md).

1. Í flýtiflipanum **Vöruhús**, í hlutanum **Afurðasíukóðar**, skal velja síukóða fyrir reitina **Kóði 1** til **Kóði 10** eftir þörfum til að tilgreina síukóða fyrir afurðina.

## <a name="set-up-generally-available-items"></a>Setja upp almennt tiltækar vörur

Hægt er að gera tilteknar birgðavörur tiltækar aðeins fyrir viðskiptavini, aðeins fyrir lánardrottna, eða fyrir bæði viðskiptavini og lánardrottna.

> [!NOTE]
> Síur viðskiptavinar og lánardrottins eiga ekki við um afurð sem er sett upp sem almennt tiltæk.

Til að setja upp almennt tiltækar vörur skal fylgja þessum skrefum:

1. Opnið **Vöruhúsakerfi \> Uppsetning \> Afurðarsíur \> Almennt tiltækar afurðir**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til færslu.
1. Í reitnum **Viðskiptavinur eða lánardrottinn** skal velja *Viðskiptavinur*, *Lánardrottinn* eða *Allir* til gera afurðirnar tiltækar fyrir viðskiptavini, lánardrottna eða bæði.
1. Í reitinn **Upphafsdagsetning/tími** skal færa inn dagsetningu og tíma þegar varan verður gerð tiltæk.
1. Veljið vöruflokkur á svæðinu **Vöruflokkur**.
1. Í reitunum **Kóði 1** til **Kóði 10** skal velja síukóðana til að takmarka vörurnar sem eru almennt í boði.

    Þegar vöruflokkur er valinn er hann stilltur þannig að vörurnar séu almennt tiltækar. Með því að velja síukóða í þessum reitum er eru vörurnar sem eru í boði takmarkaðar.

## <a name="set-up-customer-product-filters"></a>Setja upp afurðarsíur viðskiptavinar

Hægt er að nota þetta aukalega ferli sýnir hvernig á að tilgreina vörurnar sem ættu að vera tiltækar fyrir viðskiptavin til viðbótar við vörur sem eru gerðar tiltækar gegnum síuuppsetningu á síðunni **Almennt tiltækar vörur**. Þú getur sett upp margar síur fyrir einn viðskiptavin.

Til að setja upp síukóða viðskiptavina skal fylgja þessum skrefum.

1. Opnið **Sölu og markaðssetning \> Viðskiptavinir \> Allir viðskiptavinir**.
1. Veljið viðskiptavin.
1. Á aðgerðasvæðinu, í flipanum **Viðskiptavinur**, í flokknum **Uppsetning**, skal velja **Afurðarsíur**.
1. Á síðunni **Afurðasíukóðar**, á aðgerðasvæðinu, skal velja **Nýr**.
1. Í reitina **Upphafsdagsetning/tími** og **Lokadagsetning/tími** skal færa inn upphafs- og lokadagsetningu fyrir valdan vöruflokk.
1. Veljið vöruflokkur á svæðinu **Vöruflokkur**.
1. Í reitunum **Kóði 1** til **Kóði 10** skal velja síukóða til að nota sem skilyrði til að takmarka vörur sem eru tiltækar fyrir viðskiptavini í völdum vöruhóp. Velja verður fyrir hvern síukóða sem er settur upp fyrir vöruflokkinn.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Setja upp afurðarsíur lánardrottins

Hægt er að nota þetta aukalega ferli sýnir hvernig á að tilgreina vörurnar sem ættu að vera tiltækar fyrir lánardrottinn til viðbótar við vörur sem eru gerðar tiltækar gegnum síuuppsetningu á síðunni **Almennt tiltækar vörur**. Þú getur sett upp margar síur fyrir einn lánardrottinn.

Til að setja upp síukóða lánardrottins skal fylgja þessum skrefum.

1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Allir lánardrottnar**.
1. Veljið lánardrottin.
1. Á aðgerðasvæðinu, í flipanum **Lánardrottinn**, í flokknum **Uppsetning**, skal velja **Afurðarsíur**.
1. Á síðunni **Síukóðar**, á aðgerðasvæðinu, skal velja **Nýr**.
1. Í reitina **Upphafsdagsetning/tími** og **Lokadagsetning/tími** skal færa inn upphafs- og lokadagsetningu fyrir valdan vöruflokk.
1. Veljið vöruflokkur á svæðinu **Vöruflokkur**.
1. Í reitunum **Kóði 1** til **Kóði 10** skal velja síukóða til að nota sem skilyrði til að takmarka vörur sem eru tiltækar fyrir lánardrottna í völdum vöruhóp. Velja verður fyrir hvern síukóða sem er settur upp fyrir vöruflokkinn.

> [!NOTE]
> Uppsetning afurðarsía lánardrottins á við útgefnar afurðir þar sem vöruhúsakerfisferli eru virkjuð fyrir tengdan geymsluvíddaflokk. Síukóðar eru notaðir til að ákvarða hvort kerfið geri notendum kleift að kaupa tiltekna vöru frá tilteknum lánardrottni þegar þeir stofna innkaupapöntunarlínur. Microsoft Dynamics 365 Supply Chain Management inniheldur tvær leiðir til að meðhöndla samþykki lánardrottins. Ef ein eða fleiri útgefnar afurðir eru til staðar þar sem reiturinn **Samþykkt prófunaraðferð lánadrottins** er stilltur á *Aðeins viðvörun* eða *Ekki leyft*, væri hægt að virkja báðar samþykktaraðferðir lánardrottins fyrir þessar vörur. Þetta gæti valdið vandamálum þegar notendur búa til innkaupapöntunarlínur.

## <a name="see-also"></a>Sjá einnig

[Frekari upplýsingar er að finna í bloggfærslunni Síukóðar vöruhúsakerfis](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]