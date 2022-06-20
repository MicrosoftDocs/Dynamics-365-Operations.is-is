---
title: Stofna gjaldakóða
description: Þessi grein útskýrir hvernig á að stilla gjaldkóða fyrir bæði viðskiptaskuldir og viðskiptakröfur.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866084"
---
# <a name="create-charges-codes"></a>Stofna gjaldakóða

Þessi grein útskýrir hvernig á að stilla gjaldkóða fyrir bæði viðskiptaskuldir og viðskiptakröfur. Ef fyrirtæki þitt krefst þess að söluupphæðir eða innkaupaupphæðir séu raktar til viðbótar við línur í sölupöntun eða innkaupapöntun, geturðu notað gjaldakóða í þessu skyni. Til dæmis greiðir þú frakt og tryggingar á innkaupapöntun og þessar upphæðir eru sundurliðaðar sérstaklega á innkaupapöntuninni. Í þessu tilviki er hægt að tilgreina hvort upphæðirnar séu bókaðar á kostnaðarreikninga eða bætt við kostnað vörunnar.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Settu upp gjaldakóða fyrir viðskiptakröfur

Til að búa til gjaldakóða fyrir viðskiptakröfur skaltu fylgja þessum skrefum.

1. Fara til **Reikningur fáanlegur** &gt; **Uppsetning gjalda** &gt; **Gjaldkóði**.
2. Veljið **Nýtt**.
3. Í **Gjaldkóði** reit, sláðu inn kóða fyrir gjaldið.
3. Í **Lýsing** reit, sláðu inn lýsingu á gjaldinu.
4. Valfrjálst: Í **Vöruskattsflokkur** reit, veldu söluskattsflokk.
5. Á **Birting** Flýtiflipi, tilgreinið hvernig skuldfærsla ætti að vera sjálfkrafa skuldfærð og innfærð.
6. Ef þú valdir **Fjárhagsreikningur** sem debettegund eða kredittegund, tilgreindu bókunartegund **Birting** reiti og tilgreindu aðalreikninginn í **Reikningur** sviðum.

### <a name="example"></a>Dæmi

Viðskiptavinur þinn greiðir gjaldið. Þess vegna er því bætt við heildartölur sölupöntunar. Þú setur upp eftirfarandi færsluupplýsingar:

- Í **Tegund** sviði í **Debet** kafla, veldu **Viðskiptavinur/seljandi** til að bæta reikningsgjaldinu á reikning viðskiptavinarins.
- Í **Tegund** sviði í **Inneign** kafla, veldu **Fjárhagsreikningur**. Þá, í **Reikningur** reit, veldu aðalreikning fyrir tekjur af reikningsgjöldum.

> [!NOTE]
> Ef debettegund eða kredittegund fyrir valda kóða er annaðhvort **Fjárhagsreikningur** eða **Atriði**, þú getur slegið inn annan gjaldmiðil fyrir gjaldfærsluna.

Þú getur prentað texta fyrir gjöld á því tungumáli sem er úthlutað til viðskiptavinarins. Til að tilgreina texta fyrir gjaldkóðann á öðrum tungumálum skaltu velja **Þýðingar**.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Settu upp gjaldakóða fyrir Viðskiptaskuldir

Til að búa til gjaldakóða fyrir Viðskiptaskuldir, fylgdu þessum skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Fara til **Viðskiptaskuldir** &gt; **Gjöld** **uppsetningu** &gt; **Gjaldkóði**.
    - Fara til **Innkaup og innkaup** &gt; **Uppsetning** &gt; **Gjöld** &gt; **Gjaldkóði**.

2. Veljið **Nýtt**.
3. Í **Gjaldkóði** reit, sláðu inn kóða fyrir gjaldið.
3. Í **Lýsing** reit, sláðu inn lýsingu á gjaldinu.
4. Valfrjálst: Í **Vöruskattsflokkur** reit, veldu söluskattsflokk.
5. Valfrjálst: Í **Hámarksupphæð** reit, sláðu inn hámarksupphæð sem er leyfileg fyrir gjaldkóðann.

    Þessi reitur er notaður til að staðfesta gjöld fyrir reikninga lánardrottins. Til að virkja staðfestingu gjalda skaltu velja **Virkja reikningssamsvörun** gátreitinn á **Staðfesting reikninga** flipi á **Færibreytur viðskiptaskulda** síðu.

    > [!IMPORTANT]
    > Til að sannreyna gjöld fyrir reikninga verður þú einnig að búa til tilvik af gerð stefnureglu sem er byggð á gjöldum fyrir tiltekna reikningsreglu lánardrottins.

6. Á **Birting** Flýtiflipi, tilgreinið hvernig skuldfærsla ætti að vera sjálfkrafa skuldfærð og innfærð.
7. Ef þú valdir **Fjárhagsreikningur** sem debettegund eða kredittegund, tilgreindu bókunartegund sem **Debetfærsla** og **Kreditbókun** reiti og tilgreindu aðalreikninginn í **Debetreikningur** og **Kreditreikningur** sviðum.
8. Til að virkja samanburð á gjaldgildum fyrir reikning sem inniheldur gjöldin úr samsvarandi innkaupapöntunarhaus eða línum skaltu velja **Berðu saman innkaupapöntun og reikningsgildi** gátreit.

### <a name="example"></a>Dæmi

Hægt er að skrá gjaldið sem kostnað, sem hluta af heildarupphæð fyrir innkaupapöntun eða reikning lánardrottins. Fylgdu þessum skrefum til að setja upp færsluupplýsingar. 

- Í **Tegund** sviði í **Inneign** kafla, veldu **Viðskiptavinur/seljandi** til að bæta reikningsgjaldinu við reikning lánardrottins.
- Í **Tegund** sviði í **Debet** kafla, veldu **Fjárhagsreikningur**. Þá, í **Reikningur** reit, veldu aðalreikning fyrir útgjöld frá reikningsgjöldum.

Fylgdu þessum skrefum til að setja upp bókunarupplýsingar þannig að einingargjaldið bætist við vörukostnaðinn.

- Í **Tegund** sviði í **Inneign** kafla, veldu **Viðskiptavinur/seljandi** til að bæta reikningsgjaldinu við reikning lánardrottins.
- Í **Tegund** sviði í **Debet** kafla, veldu **Atriði** til að bæta gjaldinu við vörukostnaðinn.

> [!NOTE]
> Þú gætir viljað nota gjaldmiðil sem er frábrugðinn þeim gjaldmiðli sem tilgreindur er á innkaupapöntun eða reikningi. Þú getur slegið inn annan gjaldmiðil ef debettegund eða kredittegund fyrir valinn kóða er annaðhvort **Fjárhagsreikningur** eða **Atriði**.

Þú getur prentað texta fyrir gjöld á því tungumáli sem er úthlutað til viðskiptavinarins. Til að tilgreina texta fyrir gjaldkóðann á öðrum tungumálum skaltu velja **Þýðingar**.
