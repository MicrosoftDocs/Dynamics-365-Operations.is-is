---
title: Skilgreina stighækkaða reiti fyrir skref í farsímaforriti Warehouse Management
description: Í þessu efnisatriði er lýst hvernig á að stighækka og auðkenna tilteknar upplýsingar fyrir hvaða skref sem er í verkflæðum fyrir farsímaforrit Warehouse Management.
author: MarkusFogelberg
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 392fc4d7e4f423b38e8394fa25d2e42de913bfc6
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860459"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Skilgreina stighækkaða reiti fyrir skref í farsímaforriti Warehouse Management

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until GA with 10.0.23 -->

> [!IMPORTANT]
> Eiginleikarnir sem lýst er í þessu efnisatriði eiga aðeins við um nýja farsímaforrit Warehouse Management. Þeir hafa ekki áhrif á gamla vöruhúsaforrið, sem nú er úrelt.

Í þessu efnisatriði er lýst hvernig á að stighækka og auðkenna tilteknar upplýsingar fyrir hvaða skref sem er í verkflæðum fyrir farsímaforrit Warehouse Management. Þessi möguleiki getur hjálpað starfsmönnum að einblína á mikilvægustu reitina þegar þeir vinna sig í gegnum flæði. Fyrir hvert skref í öllum ferlum geta stjórnendur valið hvaða reiti á að stighækka og auðkenna.

## <a name="enable-promoted-fields-in-your-system"></a>Virkja stighækkaða reiti í kerfinu þínu

Áður en hægt er að setja upp stighækkaða reiti þarf að ljúka eftirfarandi ferli til að virkja nauðsynlega eiginleika og búa til heiti áskildra reita í farsímaforriti Warehouse Management.

1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.
1. Á vinnusvæðinu [**Eiginleikastjórnun** ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)skal virkja eiginleikann sem er sýndur á eftirfarandi hátt:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Leiðbeiningar fyrir skref vöruhúsaforrits*

    Frekar upplýsingar um eiginleikann *Leiðbeiningar fyrir skref vöruhúsaforrits* er að finna í [Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management ](mobile-app-titles-instructions.md). Þessi eiginleiki er skilyrði fyrir eiginleikann *Stighækkaðir reitir vöruhúsaforrits*.

1. Virkjaðu eiginleikann sem er sýndur á eftirfarandi hátt:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Stighækkaðir reitir vöruhúsaforrits*

    Þessi eiginleiki er eiginleikinn sem lýst er í þessu efnisatriði.

1. Uppfærðu heiti reita í farsímaforriti Warehouse Management með því að fara í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Reitarheiti vöruhúsaforrits** og veldu **Búa til sjálfgefna uppsetningu**. Frekari upplýsingar eru í [Skilgreina reiti fyrir farsímaforrit vöruhúsakerfis](configure-app-field-names-priorities-warehouse.md).
1. Endurtaktu fyrra skrefið fyrir hvern lögaðila (fyrirtæki) þar sem þú notar farsímaforrit Warehouse Management.

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Skilgreina stighækkaða reiti úr hnekkingu valmyndar

Notaðu eftirfarandi ferli til að setja upp stighækkaða reiti.

1. Búðu til hnekkingu valmyndar fyrir tiltekna valmynd og skref eins og lýst er í [Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management](mobile-app-titles-instructions.md).
1. Finndu samsetningu gilda fyrir **Kenni skrefs** og **Heiti valmyndaratriðis** sem þú vilt breyta og veldu síðan gildið í dálknum **Kenni skrefs**.
1. Á síðunni sem birtist, á flýtiflipanum **Velja stighækkaða reiti**, skal velja **Velja reiti** á tækjastikunni.
1. Í svarglugganum **Stighækkaðir reitir** skal velja reitina sem á að stighækka. Þú getur einnig auðkennt allt að tvo stighækkaða reiti. Auðkenndir reitir verða sýndir feitletraðir í farsímaforriti Warehouse Management. Þegar þú velur reiti skaltu hafa í huga þá staðreynd að sumir skjáir geta verið nógu stórir til að sýna aðeins efstu einn eða tvo stighækkaða reiti. Dæmi sem sýnir hvernig á að nota þessar stillingar er að finna í aðstæðunum síðar í þessu efnisatriði.

    > [!NOTE]
    > Listinn **Tiltækir reitir** takmarkast við reitina sem geta birst fyrir valmyndaratriðið. Aðrir þættir (t.d. vörusamsetning) skera hinsvegar úr um hvort reitur birtist í raun í farsímaforriti Warehouse Management. Ef þú hefur skilgreint stighækkaða reiti munu aðeins valdir reitir birtast á aðalsíðu farsímaforrits Warehouse Management. Starfsmenn geta hinsvegar enn skoðað hina reitina með því að pikka á upplýsingasíðuna.

1. Veldu **Í lagi** til að setja á breytingarnar. Valdir reitir eru nú sýndir á flýtiflipanum **Velja stighækkaða reiti**.

## <a name="example-scenario"></a>Dæmi

### <a name="enable-sample-data"></a>Virkja gögn sýnishorna

Til að nota tiltekin dæmi um færslur og gildi til að fara í gegnum þessar aðstæður þarftu að nota kerfi þar sem stöðluð sýnigögn eru uppsett. Þú verður einnig að velja lögaðilann **USMF** áður en þú byrjar.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Skilgreina sölutiltekt með stighækkuðum reitum í skrefi númeraplötu

Í þessu ferli verða settir upp stighækkaðir og auðkenndir reitir fyrir valmyndaratriðið **Tiltekt sölu** í skrefi númeraplötu.

1. Farðu í **Warehouse Management \> Uppsetning \> Fartæki \> Skref fartækis**.
1. Finndu skrefakennið sem heitir *LicensePlateId* og veldu það.
1. Á aðgerðasvæðinu skal velja **Bæta við skilgreiningu skrefs**.
1. Í felliglugganum skaltu nota reitinn **Valmyndaratriði** til að finna og velja *Tiltekt sölu*.
1. Veldu **Í lagi**.
1. Upplýsingasíðan fyrir hnekkinguna sem var búin til birtist. Á flýtiflipanum **Velja stighækkaða reiti** skal velja **Velja reiti** á tækjastikunni.
1. Í svarglugganum **Stighækkaðir reitir** er hægt að velja reiti til að stighækka og auðkenna. Í listanum **Tiltækir reitir** skal leita að og velja eftirfarandi reiti og nota hnappana til að færa þá yfir í listann **Valdir reitir**:

    - Staðsetning
    - Vara
    - Afurðarheiti
    - Birgðastaða

1. Notaðu örvarhnappana upp og niður til að sérstilla röð reitanna í listanum **Valdir reitir**. Í farsímaforriti Warehouse Management munu reitirnir birtast í röðinni sem er sett hér.
1. Veldu reitinn **Staðsetning** og síðan **Auðkenna**.
1. Veldu **Í lagi** til að vista skilgreininguna.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Skoða stighækkaða reiti í farsímaforriti Warehouse Management

Í þessu ferli opnar þú farsímaforrit Warehouse Management og ferð í gegnum skrefin til að skoða reitina sem þú stighækkaðir og auðkenndir í ferlinu hér á undan.

1. Í Microsoft Dynamics 365 Supply Chain Management skal stofna sölupöntun sem þarf tiltektarskref til að tína úr staðsetningu sem er rakin með númeraplötu. Losaðu svo sölupöntunina í vöruhúsið. Skráið niður vinnuauðkennið sem er myndað.
1. Opnaðu farsímaforrit Warehouse Management og skráðu þig inn í vöruhús 24. (Í stöðluðum kynningargögnum skráirðu þig inn með því að nota *24* sem notandakenni og *1* sem lykilorð.)
1. Veldu valmyndina **Á útleið** og veldu svo valmyndaratriðið **Tiltekt sölu**.
1. Fylgdu leiðbeiningum um gagnaskráningu á skjánum til að færa inn vinnukennið sem var búið til í skrefi 1.
1. Í skrefinu sem inniheldur textann **Skanna númeraplötu** ættir þú að sjá breytingarnar sem þú gerðir á upplýsingasíðunni. Reitirnir birtast í þeirri röð sem þú stillir fyrir stighækkaða reiti og reiturinn **Staðsetning** er sýndur feitletraður.
