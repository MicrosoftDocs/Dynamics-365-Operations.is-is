---
title: Stofna gjaldakóða
description: Í þessari grein er útskýrt hvernig á að stilla skuldfærslukóða fyrir bæði viðskiptaskuldir og viðskiptakröfur.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d65952cb989672e4eac2dd6101ee9c7c9424daed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866084"
---
# <a name="create-charges-codes"></a>Stofna gjaldakóða

Í þessari grein er útskýrt hvernig á að stilla skuldfærslukóða fyrir bæði viðskiptaskuldir og viðskiptakröfur. Ef stofnunin/fyrirtækið gerir kröfu um að sölufjárhæðir eða innkaupaupphæðir séu raktar til viðbótar við línuvörur í sölupöntun eða innkaupapöntun getur þú notað gjaldakóða í þessu skyni. Til dæmis greiðir þú vörugjald og tryggingu á innkaupapöntun og þær upphæðir eru flokkaðar sérstaklega á innkaupapöntunina. Í því tilviki er hægt að tilgreina hvort upphæðin er birt á kostnaðarreikningum eða bætt við kostnað varanna.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Setja upp gjaldakóða fyrir viðskiptakröfur

Til að stofna gjaldakóða fyrir Viðskiptakröfur skal fylgja þessum skrefum.

1. Fara í **Viðskiptakröfur** &gt; **Uppsetning gjalda** &gt; **Gjaldakóði**.
2. Veljið **Nýtt**.
3. Í reitnum **Gjaldakóði** er færður inn kóði fyrir gjaldið.
3. Færið inn lýsingu á gjaldinu í svæðinu **Lýsing**.
4. Valkvæmt: Í reitnum **VSK-flokkur vöru** skal velja VSK-flokkur.
5. Á flýtiflipanum **Bókun** skaltu tilgreina hvernig skuldfærslan ætti að vera debet- og kreditfærð sjálfkrafa.
6. Ef þú valdir **Fjárhagslykill** sem debet- eða kreditfærslugerð, tilgreindu bókunargerð í reitunum **Bókun** og tilgreindu aðallykil í reitunum **Lykill**.

### <a name="example"></a>Dæmi

Viðskiptavinurinn greiðir gjaldið. Því er bætt við samtölur sölupöntunar. Þá þarf að setja upp eftirfarandi bókunarupplýsingar:

- Veljið reitinn **Gerð** í hlutanum **Debet**, veljið **Viðskiptamaður/Lánardrottinn** til að bæta reikningsgjöldum við lykil viðskiptavinar.
- Í reitnum **Gerð** í hlutanum **Kredit** skal velja **Fjárhagslykill**. Í reitnum **Lykill** velurðu aðallykil fyrir tekjur af reikningsgjöldum.

> [!NOTE]
> Ef debet- eða kreditfærslugerð fyrir valinn kóða er annað hvort **Fjárhagslykill** eða **Vara**, þá er hægt að færa inn annan gjaldmiðil fyrir gjaldfærsluna.

Þú getur prentað textann fyrir gjöld á því tungumáli sem viðskiptamanni er úthlutað. Veldu **Þýðingar** til að tilgreina textann fyrir kóðann á öðrum tungumálum.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Setja upp gjaldakóða fyrir viðskiptaskuldir

Til að stofna gjaldakóða fyrir Viðskiptaskuldir skal fylgja þessum skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Farið í **Viðskiptaskuldir** &gt; **Uppsetning** **gjalda** &gt; **Gjaldakóði**.
    - Farið í **Innkaup og aðföng** &gt; **Uppsetning** &gt; **Gjöld** &gt; **Gjaldakóði**.

2. Veljið **Nýtt**.
3. Í reitnum **Gjaldakóði** er færður inn kóði fyrir gjaldið.
3. Færið inn lýsingu á gjaldinu í svæðinu **Lýsing**.
4. Valkvæmt: Í reitnum **VSK-flokkur vöru** skal velja VSK-flokkur.
5. Valfrjálst: í reitinn **Hámarksupphæð** skal færa inn hámarksupphæð sem leyfð er fyrir gjaldakóðann.

    Þessi reitur er notaður til að staðfesta gjöld fyrir reikninga lánardrottins. Til að virkja staðfestingu gjalda skaltu velja gátreitinn **Gera villuprófun á reikningsjöfnun virka** á flipanum **Reikningaprófun** á síðunni **Færibreytusíða viðskiptaskulda**.

    > [!IMPORTANT]
    > Til að staðfesta gjöld fyrir reikninga þarftu einnig að stofna tilvik af stefnureglugerð sem er byggð á gjöldum fyrir tiltekna stefnu fyrir reikning lánardrottins.

6. Á flýtiflipanum **Bókun** skaltu tilgreina hvernig skuldfærslan ætti að vera debet- og kreditfærð sjálfkrafa.
7. Ef þú valdir **Fjárhagslykill** sem debet- eða kreditfærslugerð, tilgreindu bókunargerð í reitunum **Debet bókun** og **Kredit bókun** og tilgreindu aðallykilinn í reitunum **Debet lykill** og **Kredit lykill**.
8. Veljið gátreitinn **Bera saman gildi innkaupapöntunar og reiknings** til að virkja samanburð gjalda fyrir reikning sem inniheldur gjöld úr haus eða línum samsvarandi innkaupapöntunar.

### <a name="example"></a>Dæmi

Þú getur skráð skuldfærsluna sem kostnað, sem hluta af heildarupphæð fyrir innkaupapöntunina eða reikning lánardrottins. Fylgdu þessum skrefum til að setja upp bókunarupplýsingar. 

- Í reitnum **Gerð** í hlutanum **Kredit** velur þú **Viðskiptavinur/Lánardrottinn** til að bæta reikningsgjöldum við lykil lánardrottinsins.
- Í reitnum **Gerð** í hlutanum **Debet** skal velja **Fjárhagslykill**. Í reitnum **Lykill** velurðu svo aðallykil fyrir kostnað frá reikningsgjöldum.

Fylgdu þessum skrefum til að setja upp bókunarupplýsingar svo að einingargjaldið bætist við vörukostnaðinn.

- Í reitnum **Gerð** í hlutanum **Kredit** velur þú **Viðskiptavinur/Lánardrottinn** til að bæta reikningsgjöldum við lykil lánardrottinsins.
- Í reitnum **Gerð** í hlutanum **Debet**, veljið **Vara** til að bæta gjöldum við vörukostnað.

> [!NOTE]
> Þú gætir viljað nota gjaldmiðil sem er frábrugðinn þeim gjaldmiðli sem tilgreindur er á innkaupapöntuninni eða reikningnum. Ef debet- eða kreditfærslugerð fyrir valinn kóða er annað hvort **Fjárhagslykill** eða **Vara**, þá er hægt að færa inn annan gjaldmiðil.

Þú getur prentað textann fyrir gjöld á því tungumáli sem viðskiptamanni er úthlutað. Veldu **Þýðingar** til að tilgreina textann fyrir kóðann á öðrum tungumálum.
