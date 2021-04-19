---
title: Skýrsla um birgðavirði í geymslu
description: Þetta efnisatriði útskýrir hvernig á að keyra skýrslu um birgðarvirði í geymslu og gera úttakið aðgengilegt stafrænt, annað hvort sem gagnvirka síðu í Microsoft Dynamics 365 Supply Chain Management eða á skjali sem hægt er að flytja út á nokkrum sniðum.
author: AndersGirke
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f32e175319d93ed1323129f1ea2896a435d8081c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821562"
---
# <a name="inventory-value-storage-report"></a>Skýrsla um birgðavirði í geymslu

Þetta efnisatriði útskýrir hvernig á að keyra **Skýrslu um birgðarvirði í geymslu** og gera úttakið aðgengilegt stafrænt, annað hvort sem gagnvirka síðu í Microsoft Dynamics 365 Supply Chain Management eða á skjali sem hægt er að flytja út á nokkrum sniðum.

Þegar þú skoðar skýrsluna í vafranum þínum eru dálkar og samanlagðri stöðu er breytt á kvikan hátt, miðað við skipulagið sem þú hefur grunnstillt. Þú getur flokkað niðurstöðurnar, síað þær, borað niður í gögnin og fleira.

Niðurstöður skýrslunnar eru vistaðar í gagnaeiningu **Birgðavirðis**. Þar af leiðandi getur þú síað og flutt niðurstöðurnar út á sniði eins og á CSV-skrá eða Microsoft Excel-sniði.

**Skýrsla um birgðavirði í geymslu** er gagnleg þegar úttakið inniheldur margar línur. Til dæmis hefur þú 50.000 vörur og 300 verslanir hafa verið stofnaðar sem vöruhús. Í þessu tilfelli, ef þú biður um lokastöður birgða eftir vöru, síðu og vöruhúsi, mun úttakið innihalda margar línur.

> [!NOTE]
> Skýrslan mun ekki innihalda millisamtölur sem eru skilgreind í útliti skýrslunnar. Hún mun heldur ekki fela í sér fjárhagsstöður, jafnvel ekki þegar þær eru skilgreindar í útliti skýrslu. Afstemming við Fjárhag verður að fara fram með því að nota prófjöfnuð.

## <a name="turn-on-the-inventory-value-storage-feature"></a>Kveikja á eiginleikanum fyrir birgðavirði í geymslu

Áður en þú getur útbúið skýrslu fyrir **Birgðarvirði í geymslu** verður þú að kveikja á eiginleikanum í kerfinu þínu. Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining** – Kostnaðarstjórnun
- **Heiti eiginleika** – Birgðarvirði í geymslu

## <a name="generate-an-inventory-value-storage-report"></a>Búa til skýrslu um birgðarvirði í geymslu

Fylgdu þessum skrefum til að búa til og geyma skýrslu um **Birgðarvirði í geymslu**.

1. Fara í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla skýrslu fyrir birgðavirði í geymslu**.
1. Veljið **Nýtt**.
1. Í valmyndinni **Birgðavirði** sem birtist skaltu stilla eftirfarandi gildi til að skilgreina hvaða skrár skal taka með í skýrslunni:

    - Sláðu inn einkvæmt heiti skýrslunnar í flýtiflipanum **Færibreytur** og notaðu svæðin í hlutanum **Dagsetningabil** til að skilgreina hvaða skrár eru teknar með í skýrslunni. Til að tilgreina dagsetningabilið geturðu annað hvort valið forstillt svið (miðað við hvenær skýrslan var búin til) í svæðinu **Kóði dagsetningabils** eða valið ákveðin dagsetningar í reitunum **Frá dagsetningu** og **Til dagsetningar**.
    - Á flýtiflipanum **Færslur til að taka með** skaltu setja upp síur og takmarkanir til að skilgreina hvaða gögn á að taka með í skýrslunni.
    - Á flýtiflipanum **Keyra í bakgrunni** skaltu tilgreina hvernig, hvenær og hversu oft á að búa skýrsluna til.

    > [!NOTE]
    > Þessi skýrsla er alltaf keyrð sem hluti af runuvinnslu.

1. Veldu **Í lagi** til að beita stillingum þínum og loka svarglugganum.

Eftir að runuvinnslunni er lokið birtist skýrslan á síðu **Skýrslu um birgðarvirði í geymslu**. Hugsanlega verður að endurhlaða síðuna til að skýrslan birtist.

## <a name="explore-an-inventory-value-storage-report"></a>Skoða skýrslu um birgðarvirði í geymslu

Eftir að þú hefur búið til skýrslu geturðu opnað og skoðað hana hvenær sem er með því að fylgja þessum skrefum.

1. Fara í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla skýrslu fyrir birgðavirði í geymslu**.
1. Veldu skýrslu á listanum.
1. Veldu **Skoða upplýsingar** til að sýna efni skýrslunnar.
1. Skoðaðu skýrsluna með því að fylgja einhverjum af þessum skrefum:

    - Eins og á við um flestar staðlaðar síður í Supply Chain Management geturðu valið næstum hvaða dálk sem er til að raða eða sía hnitanetið eftir gildunum í þeim dálki.
    - Notaðu svæðið **Sía** til að sía skýrsluna eftir hvaða gildi sem er í nokkrum tiltækum dálkum.
    - Notaðu valmyndina Skoða (fyrir ofan svæðið **Sía**) til að vista og hlaða inn eftirlætis samsetningum flokkunar- og síuvalkosta.

## <a name="export-an-inventory-value-storage-report"></a>Flytja út skýrslu um birgðarvirði í geymslu

Hver skýrsla sem þú býrð til er geymd í gagnaeiningunni **Birgðavirði**. Þú getur notað staðlaða eiginleika gagnastjórnunar fyrir Supply Chain Management til að flytja út gögn frá þessari einingu til allra studdra gagnasniða, eins og CSV- eða Excel-sniða.

Eftirfarandi dæmi sýnir hvernig á að flytja út skýrslu um **birgðarvirði í geymslu**.

1. Opnaðu **Kerfisstjórnun \> Vinnusvæði \> Gagnastjórnun**.
1. Í hlutanum **Flytja inn / Flytja út** velurðu reitinn **Flytja út**. 
1. Á síðunni **Útflutningur** sem birtist seturðu upp útflutningsverkið. Færið fyrst inn heiti hóps fyrir verkið.
1. Í hlutanum **Valdar einingar** velurðu **Bæta við einingu**.
1. Í svarglugganum sem birtist, skal velja eitt af eftirfarandi svæðum:

    - **Heiti einingar** – Veldu **Birgðarvirði**.
    - **Markmiðsgagnasnið** - Veldu sniðið sem á að flytja gögn út á.

1. Smelltu á **Bæta við** til að bæta við nýju línunni og smelltu síðan á **Loka** til að loka glugganum.
1. Venjulega muntu flytja út eina skýrslu í einu. Til að flytja út eina skýrslu skaltu setja upp síu fyrir línuna sem þú varst að bæta við í svarglugganum **Fyrirspurn**. Á þennan hátt geturðu skilgreint hvaða skýrslu frá einingunni **Birgðavirði** er innifalinn í útflutningi þínum. Fylgdu þessum skrefum til að stilla eftirfarandi síuvalkosti til að flytja út eina skýrslu:

    1. Veldu **Bæta við** til að bæta við röð á flipanum **Svið**.
    2. Stilltu svæðið **Tafla** á **Birgðavirði**.
    3. Stilltu svæðið **Afleidd tafla** á **Birgðavirði**.
    4. Stilltu svæðið **Svæði** á svæðið sem þú vilt sía eftir. Yfirleitt notarðu svæðið **Keyrsluheiti** og/eða svæðið **Keyrslutími**.
    5. Stilltu svæðið **Skilyrði** á gildi sem þú vilt leita að í valda svæðinu. (Ef þú valdir svæðið **Keyrsluheiti** í fyrra skrefi verður þetta gildi heiti skýrslunnar. Ef þú valdir svæðið **Keyrslutími** verður það tíminn sem skýrslan var búin til.)
    6. Bættu við eins mörgum línum við flipann **Svið** eins og þú þarft, þar til þú hefur borið einkvæm kennsl á skýrsluna sem þú ert að leita að.

1. Veldu **Í lagi** til að vista stillingarnar þínar og loka glugganum.
1. Veldu **Vista** til að vista uppsetningu á útflutningi.
1. Á flipanum **Valkostir útflutnings** velurðu **Flytja út núna** til að búa til útflutningsskrána.
1. Á **Yfirlitssíðu keyrslu** sem birtist geturðu skoðað stöðu útflutningsverksins þíns og lista yfir allar einingar sem voru fluttar út. Í hlutanum **Vinnslustaða einingar** velurðu **Birgðavirði** á listanum og smellir á **Hlaða niður skrá** til að hlaða niður gögnum sem flutt voru út frá þeirri einingu.

Nánari upplýsingar um hvernig á að nota gagnastjórnun til að flytja út gögn er að finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]