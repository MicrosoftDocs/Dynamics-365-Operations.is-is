---
title: Vinna handvirkt úr sölu og undantekningum á tiltekt í flutningslínu
description: Í þessari grein er lýst hvernig stjórnendur geta handvalið (eða hætt við að velja) birgðafærslur til að laga vandamál sem eru af völdum skemmdra gagna sölu- og flutningspöntunar.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404428"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Vinna handvirkt úr sölu og undantekningum á tiltekt í flutningslínu

[!include [banner](../includes/banner.md)]

Handvirk meðhöndlun á undantekningum á tiltekt sölu- og flutningslínu gerir stjórnendum kleift að laga vandamál af völdum skemmdra gagna sölu- og flutningspöntunar. Það gerir áreiðanlegum notendum kleift að velja handvirkt (eða afvelja) birgðafærslur sem tengjast sölu og flutningspöntunarlínum á meðan vöruhúsaferli eru þegar í gangi.

Virkninni sem lýst er hér ætti að aðeins að nota ef kerfið getur ekki lokið við vinnslu á stafla vöruhúsaferla á venjulegan hátt. Sjálfgefið er að aðeins notendur sem hafa kerfisstjórahlutverk mega nota það. Hins vegar geturðu veitt aðgang að því með því að úthluta réttindunum *Tína sölulínur handvirkt* á önnur hlutverk eftir þörfum.

## <a name="turn-on-this-feature-for-your-system"></a>Kveikja á þessum eiginleika fyrir kerfið

Áður en þú getur notað eiginleikana sem lýst er í þessari grein verður að kveikja á þeim í kerfinu þínu. Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikanna og kveikja á þeim. Á vinnusvæðinu **Eiginleikastjórnun** eru eiginleikarnir tilgreindir með því að nota eftirfarandi heiti:

- *Handvirk tiltektarþjónusta sölulínu fyrir stjórnanda eða aðra trausta notendur*<br>(Frá og með útgáfu 10.0.25 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.)
- *Handvirk tiltektarþjónusta flutningslínu fyrir stjórnanda eða aðra trausta notendur*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Leiðrétta færslur sem tengjast sölu- eða flutningspöntunarlínum

Notaðu eftirfarandi ferli til að leiðrétta færslur sem tengjast sölu eða flutningspöntunarlínum.

1. Fylgdu einu af eftirfarandi skrefum, eftir því hvers konar röð þú þarft að leiðrétta:

    - Til að leiðrétta færslu sem tengist sölupöntun skal fara í **Vöruhúsakerfi \> Reglubundin verk \> Hreinsun \> Tína sölulínu handvirkt**.
    - Til að leiðrétta færslu sem tengist flutningspöntun skal fara í **Vöruhúsakerfi \> Reglubundin verk \> Hreinsun \> Tína flutningslínur handvirkt**.

1. Á síðunni **Tína sölulínur handvirkt** eða **Tína flutningslínur handvirkt** skal nota síurnar efst í hnitanetinu til að finna línuna sem leitað er að og síðan velja tilheyrandi pöntunarlínu í efra hnitanetinu.
1. Notaðu flipana **Birgðafærslur**, **Hleðslulínur**, **Vinnulínur** og **Gámalínur** í neðri hlutanum til að skoða frekari upplýsingar um valda línu. Upplýsingarnar á þessum flipum gefa yfirlit um tengda vöruhúsaferla og stöðu þeirra.
1. Á aðgerðasvæðinu skal velja **Tína** til að opna valda pöntunarlínu á síðunni **Tína** fyrir birgðafærslur. Hægt er að ljúka þessu skrefi jafnvel fyrir pöntunarlínur sem þegar er búið að losa í vöruhúsið. (Yfirleitt er ekki hægt að opna pöntunarlínur sem hafa verið sendar í vöruhúsið á síðunni **Tínsla**.)

    > [!NOTE]
    > Þú gætir fengið ýmsar viðvaranir þegar þú opnar síðuna **Tína**. Grípa til aðgerða sem þessar viðvaranir mæla með. Til dæmis gætir þú fengið viðvörun um pöntunarlínur sem eru tengdar vöruhúsavinnu. Í þessu tilviki er skynsamlegt að reyna að hætta við vinnuna með því að nota hefðbundna aðgerð [afturköllunarvinnu](cancel-warehouse-work.md) áður en handvirk leiðrétting er gerð.

1. Veldu línuna í hnitanetinu **Færslur** og veldu síðan **Bæta við tiltektarlínu** á tækjastikunni **Færslur**.
1. Valda línan er færð á **Tiltektarlínur**. Stilla viðeigandi gildi fyrir alla dálka þar sem nauðsynlegar upplýsingar vantar. (Tilgreinið til dæmis staðsetningu og númeraplötu sem varan ætti að vera sótt/tekin af.)
1. **Staðfesta tiltekt á öllu** á tækjastikunni **Tiltektarlínur**.

## <a name="correct-load-line-quantities"></a>Lagfæra magn farmlínu

Notið eftirfarandi aðferð til að leiðrétta magn hleðslulínu.

1. Fylgdu einu af eftirfarandi skrefum, eftir því hvers konar röð þú þarft að leiðrétta:

    - Til að leiðrétta færslu sem tengist sölupöntun skal fara í **Vöruhúsakerfi \> Reglubundin verk \> Hreinsun \> Tína sölulínu handvirkt**.
    - Til að leiðrétta færslu sem tengist flutningspöntun skal fara í **Vöruhúsakerfi \> Reglubundin verk \> Hreinsun \> Tína flutningslínur handvirkt**.

1. Á síðunni **Tína sölulínur handvirkt** eða **Tína flutningslínur handvirkt** skal nota síurnar efst í hnitanetinu til að finna línuna sem leitað er að og síðan velja tilheyrandi pöntunarlínu í efra hnitanetinu.
1. Á flipanum **Hlaða línum** í neðri hlutanum, veldu **Leiðrétta hleðslulínur handvirkt** á tækjastikunni.
1. Á síðunni **Lagfæra farmlínur handvirkt**, í hnitanetinu **Birgðafærslur**, skal fara yfir birgðafærslurnar sem tengjast valdri farmlínu.
1. Í efra netinu, leiðréttið magn hleðslulínu í eftirfarandi dálkum eftir þörfum:

    - **Magn stofnaðrar vinnu**
    - **Tiltekið magn**
    - **Áætlað magn til dreifingar frá dreifingarstöð**

    Kerfið mun staðfesta allar breytingar sem gerðar eru á þessum dálkum.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
