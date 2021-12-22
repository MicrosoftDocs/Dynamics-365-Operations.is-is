---
title: Bæta við eða afrita leigusamninga (forskoðun)
description: Þetta efnisatriði lýsir því hvernig á að stofna nýjan leigu með því að færa inn upplýsingar um hana í Eignarleiga eða afrita upplýsingar úr fyrirliggjandi leigu.
author: moaamer
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ee4803c4653b8c2df2cb731652456b1ce2796cd0
ms.sourcegitcommit: e77d72fde17a43bd1780c265702254011af7407c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/07/2021
ms.locfileid: "7893646"
---
# <a name="add-or-copy-leases-preview"></a>Bæta við eða afrita leigusamninga (forskoðun)

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að stofna leigu frá grunni í Eignarleiga og einnig hvernig á að stofna leigu með því að afrita fyrirliggjandi leigu. Ferlið fyrir stofnun leigu frá grunni felur í sér að færa inn upplýsingar fyrir nýja leigu og búa síðan til leiguáætlun. Eftir að a.m.k. ein leiga hefur verið sett upp gæti reynst auðveldara að afrita upplýsingarnar úr fyrirliggjandi leigu og breyta þeim svo eftir því sem þörf krefur til að stofna nýja leigu.

## <a name="create-a-lease"></a>Búa til leigu

Fylgdu þessum skrefum til að búa til leigu á Eignleiga.

1. Á síðunni **Samantekt leigu**, á aðgerðasvæðinu, skal velja **Nýr**.
2. Færið inn leiguupplýsingar. Reitir sem eru nauðsynlegir eru með rauðan ramma.

> Upphafsdagur leigugreiðslunnar má ekki vera fyrr en upphafsdagur leigusamnings. Ef þú slærð inn upphafsdagsetningu leigugreiðslunnar sem er fyrr en upphafsdagsetning leigusamningsins færðu villuboð.
  
## <a name="create-a-lease-schedule"></a>Búa til leiguáætlun

Þegar búið er að færa inn upplýsingar fyrir leiguna, skal fylgja þessum skrefum til að stofna leiguáætlun.

> [!NOTE]
> Fjárhagsvíddir gætu breyst á grundvelli sérstilltra fjárhagsvídda.

1. Veljið **Stofna áætlanir** til að mynda leigubækurnar. Í leigubókum eru greiðslur, afborganir, afskriftir og kostnaðaráætlanir.
2. Til að fá aðgang að leigubókunum og skoða nýstofnaða tímaáætlun skal velja flipann **Bækur** .

    Á síðunni **Upplýsingar um bók** birtist hvernig leigan er gjaldfærð fyrir bækurnar sem hefur verið úthlutað á hana. Þaðan er hægt að skoða leiguáætlanir.

    Greiðsluáætlun inniheldur innbætur úr **Greiðsluáætlunarlínum** á flipanum **Bæta við leigusamningi**. Enn er hægt að breyta hverri greiðsluupphæð og breytilegri greiðslu. Leiguskuldbinding er reiknuð út á grundvelli breyttrar greiðsluáætlunar.

4. Eftir að lokið er að endurskoða greiðsluáætlun skal velja **Staðfesta áætlun**. Þegar áætlunin hefur verið staðfest er ekki lengur hægt að breyta leigunni.

    > [!NOTE]
    > Kerfið reiknar sjálfkrafa leigutíma úr greiðsluáætlunarlínunum á síðunni **Bæta við leigusamningi**.
    >
    > Til að reikna út leigutíma í mánuðum finnur kerfið mismuninn á milli upphafsdagsetningu og lokadagsetningu tiltekinnar greiðsluáætlunarlínu. Hún færist síðan í næstu greiðsluáætlunarlínu og finnur mismuninn aftur. Að lokum leggur kerfið sama allar upphæðir til að ákvarða leigutíma í mánuðum.

5. Til að skoða reiknaðan vexti tímabils skal opna **Afskriftaráætlun leiguskuldbindingar**. Til að skoða reiknaða línulega afskrift skal opna **Afskriftaráætlun eignar**.
6. Eftir að lokið hefur verið við að endurskoða reiknaða upphæð er hægt að stofna fyrstu skráningarbókarfærslu á síðunni **Upphafleg skráning**. Notandi fær skilaboð um að afritunarferlið sé lokið.

    > [!NOTE]
    > Bókarfærslan er ekki bókuð í fjárhag fyrr en búið er að bóka færsluna handvirkt.

7. Til að yfirfara fyrirhugaða upphaflega skráningarfærslu áður en hún er bókuð skal velja **Færslubók eignarleigu**.

    > [!NOTE]
    > Ekki er hægt að stofna bók fyrir Eignarleigu handvirkt. Það stofnast sjálfkrafa þegar leiguáætlanir eru stofnaðar.

8. Þegar lokið er við að endurskoða upphaflegu skráningarfærslu í bók og hún er tilbúin til bókunar skal velja **Bóka** til að staðfesta afnotarétt af eign og leiguskuldbindingu í fjárhag.

## <a name="copy-a-lease"></a>Afrita leigusamning

Eignarleiga gerir notendum kleift að afrita upplýsingar um leigu til að búa til nýja leigu sem er með sömu upplýsingar. Síðan er hægt að breyta leigureitum áður en áætlanir eru stofnaðar fyrir afrituðu leiguna.

1. Á síðunni **Samantekt leigu** skal velja leiguna sem á að afrita og síðan **Afrita leigusamning** á aðgerðasvæðinu.

    > [!NOTE]
    > Ef slökkt er á færibreytunni **Handvirkt** fyrir númeraröðina fyrir leigukenni er næsta númer í röðinni sjálfkrafa myndað sem leigukenni afritaðrar leigu. Ef kveikt er á færibreytunni **Handvirkt** birtast skilaboð með kvaðningu um að slá inn leigukennið áður en leigan er afrituð.

2. Velið **Afrita**. Upplýsingar um leigu úr valinni leigu eru afritaðar í nýja leigu. Síðan er hægt að breyta upplýsingum um nýju leiguna áður en hún er vistuð og leiguáætlanir stofnaðar.

## <a name="asset-leasing-journal"></a>Færslubók eignarleigu

Allar bókarfærslur sem eru stofnaðar í Eignarleigu eru í færslubók Eignarleigu. Á síðunni **Færslubók eignarleigu** (**Eignarleiga \> Bókarfærslur \> Færslubók eignarleigu**) er hægt að sía eftir bókunarstöðu, skoða tilteknar bókarfærslur og fylgiskjöl og bóka óbókaðar bókarfærslur.

> [!NOTE]
> Ekki er hægt að stofna bók fyrir Eignarleigu handvirkt. Það stofnast sjálfkrafa þegar leiguáætlanir eru stofnaðar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
