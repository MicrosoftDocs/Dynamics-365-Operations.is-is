---
title: Skilgreina stighækkaða reiti fyrir skref í farsímaforriti Warehouse Management
description: Þessi grein lýsir því hvernig á að kynna og auðkenna sérstakar upplýsingar fyrir hvaða skref sem er í verkefnaflæðinu fyrir vöruhúsastjórnun farsímaforritsins.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepSelectPromotedFields, WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour, WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e2d65f20febaf9bd1d143414054b121f8decb7c0
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689831"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Skilgreina stighækkaða reiti fyrir skref í farsímaforriti Warehouse Management

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Eiginleikarnir sem lýst er í þessari grein eiga aðeins við um nýja vöruhússtjórnun farsímaforritið. Þeir hafa ekki áhrif á gamla vöruhúsaforrið, sem nú er úrelt.

Þessi grein lýsir því hvernig á að kynna og auðkenna sérstakar upplýsingar fyrir hvaða skref sem er í verkefnaflæðinu fyrir vöruhúsastjórnun farsímaforritsins. Þessi möguleiki getur hjálpað starfsmönnum að einblína á mikilvægustu reitina þegar þeir vinna sig í gegnum flæði. Fyrir hvert skref í öllum ferlum geta stjórnendur valið hvaða reiti á að stighækka og auðkenna.

## <a name="enable-promoted-fields-in-your-system"></a>Virkja stighækkaða reiti í kerfinu þínu

Ef þú ert að keyra Supply Chain Management útgáfu 10.0.28 eða eldri, áður en þú getur sett upp kynnta reiti, verður þú að ljúka eftirfarandi ferli til að virkja nauðsynlega eiginleika og búa til nauðsynleg svæðisnöfn í vöruhúsastjórnun farsímaforritinu. Ef þú ert að keyra Supply Chain Management útgáfu 10.0.29 eða nýrri eru eiginleikarnir nauðsynlegir og ekki er hægt að slökkva á þeim, svo þú getur sleppt þessu ferli.

1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**. (Sjá [Yfirlit yfir eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) fyrir frekari upplýsingar um þessa síðu.)
1. Gakktu úr skugga um að *Skrefleiðbeiningar fyrir vöruhús app* kveikt er á eiginleikanum fyrir kerfið þitt. Þessi eiginleiki er skilyrði fyrir eiginleikann *Stighækkaðir reitir vöruhúsaforrits*. Frá og með Supply Chain Management útgáfu 10.0.29 er það skylda og ekki hægt að slökkva á henni. Frekar upplýsingar um eiginleikann *Leiðbeiningar fyrir skref vöruhúsaforrits* er að finna í [Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management ](mobile-app-titles-instructions.md).
1. Gakktu úr skugga um að *Vöruhúsaforrit kynntir reitir* kveikt er á eiginleikanum fyrir kerfið þitt. Þetta er eiginleikinn sem lýst er í þessari grein. Frá og með Supply Chain Management útgáfu 10.0.29 er það skylda og ekki hægt að slökkva á henni.
1. Uppfærðu heiti reita í farsímaforriti Warehouse Management með því að fara í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Reitarheiti vöruhúsaforrits** og veldu **Búa til sjálfgefna uppsetningu**. Endurtaktu þetta skref fyrir hvern lögaðila (fyrirtæki) þar sem þú notar vöruhúsastjórnun farsímaforritið. Frekari upplýsingar eru í [Skilgreina reiti fyrir farsímaforrit vöruhúsakerfis](configure-app-field-names-priorities-warehouse.md).

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Skilgreina stighækkaða reiti úr hnekkingu valmyndar

Notaðu eftirfarandi ferli til að setja upp stighækkaða reiti.

1. Búðu til hnekkingu valmyndar fyrir tiltekna valmynd og skref eins og lýst er í [Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management](mobile-app-titles-instructions.md).
1. Finndu samsetningu gilda fyrir **Kenni skrefs** og **Heiti valmyndaratriðis** sem þú vilt breyta og veldu síðan gildið í dálknum **Kenni skrefs**.
1. Á síðunni sem birtist, á flýtiflipanum **Velja stighækkaða reiti**, skal velja **Velja reiti** á tækjastikunni.
1. Í svarglugganum **Stighækkaðir reitir** skal velja reitina sem á að stighækka. Þú getur einnig auðkennt allt að tvo stighækkaða reiti. Auðkenndir reitir verða sýndir feitletraðir í farsímaforriti Warehouse Management. Þegar þú velur reiti skaltu hafa í huga þá staðreynd að sumir skjáir geta verið nógu stórir til að sýna aðeins efstu einn eða tvo stighækkaða reiti. Fyrir dæmi sem sýnir hvernig á að nota þessar stillingar, sjá atburðarás síðar í þessari grein.

    > [!NOTE]
    > Listinn **Tiltækir reitir** takmarkast við reitina sem geta birst fyrir valmyndaratriðið. Aðrir þættir (t.d. vörusamsetning) skera hinsvegar úr um hvort reitur birtist í raun í farsímaforriti Warehouse Management. Ef þú hefur skilgreint stighækkaða reiti munu aðeins valdir reitir birtast á aðalsíðu farsímaforrits Warehouse Management. Starfsmenn geta hinsvegar enn skoðað hina reitina með því að pikka á upplýsingasíðuna.

1. Veldu **Í lagi** til að setja á breytingarnar. Valdir reitir eru nú sýndir á flýtiflipanum **Velja stighækkaða reiti**.

## <a name="example-scenario"></a>Dæmi

### <a name="enable-sample-data"></a>Virkja gögn sýnishorna

Til að nota tilgreindar sýnishornsfærslur og gildi til að vinna í gegnum þessa atburðarás verður þú að nota kerfi þar sem staðallinn [kynningargögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er sett upp. Þú verður einnig að velja lögaðilann **USMF** áður en þú byrjar.

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
