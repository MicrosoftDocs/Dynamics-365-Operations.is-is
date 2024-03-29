---
title: Berðu saman geymsluskýrslu vöruverðs
description: Lærðu hvernig á að búa til samanburðarskýrslu um vöruverð og fletta síðan og/eða flytja út niðurstöðuna.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c6373679299b68413d75236ca8cc18ceba03e091
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334986"
---
# <a name="compare-item-prices-storage-report"></a>Berðu saman geymsluskýrslu vöruverðs

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að keyra **Berðu saman geymsluskýrslu vöruverðs** og gera úttakið aðgengilegt stafrænt, annað hvort sem gagnvirka síðu í Dynamics 365 Supply Chain Management eða á skjali sem hægt er að flytja út á nokkrum sniðum.

Þegar þú skoðar skýrsluna í vafranum er dálkum og samanlögðum stöðum gagnvirkt breytt, allt eftir stilltu skipulagi. Þú getur flokkað niðurstöðurnar, síað þær, borað niður í gögnin og fleira.

Niðurstöður skýrslunnar eru vistaðar í gagnaeiningunni **Bera saman vöruverð**, sem gerir þér kleift að sía og flytja niðurstöðurnar á snið eins og CSV eða Microsoft Excel.

Skýrslan **Bera saman vöruverðsgeymslu** er gagnleg í tilfellum þar sem úttakið inniheldur margar línur. Til dæmis mun framleiðsla innihalda margar línur ef þú ert með meira en 40.000 hluti sem eru með verð á vöru í bið í útgáfu kostnaðarútreiknings.

## <a name="turn-the-compare-item-prices-storage-feature-on-or-off"></a>Slökkva/kveikja á geymslueiginleikanum fyrir samanburð vöruverðs

Til að nota þennan eiginleika þarf að kveikja á honum fyrir kerfið þitt. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Bera saman vöruverðsgeymslu* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="generate-a-compare-item-prices-storage-report"></a>Búa til skýrsluna Bera saman vöruverðsgeymslu

Fylgdu þessum skrefum til að búa til og geyma skýrsluna **Bera saman geymslu vöruverðs**:

1. Farðu í **Kostnaðarstjórnun > Fyrirspurnir og skýrslur > Fyrirframákveðnar kostnaðarskýrslur > Bera saman geymslu vöruverðs**.

1. Veldu **Nýtt** til að opna gluggann **Bera saman vöruverð**. Stilltu eftirfarandi valkosti til að skilgreina hvaða verð á að bera saman í skýrslunni:

    - Á flýtiflipanum **Færibreytur** gefurðu skýrslunni einkvæmt **Heiti** og notar reitina í hlutunum **Verð bíður samanburðar** og **Verð notað til samanburðar** til að skilgreina hvaða verð og dagsetningar á að bera saman.
    - Á flýtiflipanum **Færslur til að taka með** seturðu upp síur og skorður til að skilgreina hvaða gögn skýrslan á að innihalda.
    - Á flýtiflipanum **Keyra í bakgrunni** seturðu upp hvernig, hvenær og hversu oft þú vilt búa til skýrsluna.
    > [!NOTE]
    > Þessi skýrsla er alltaf framkvæmd sem hluti af runuvinnslu.

1. Veldu **Í lagi** til að beita stillingum þínum og loka glugganum.

1. Eftir að runuvinnslunni er lokið verður hún skráð á síðunni **Bera saman geymslu vöruverðs**. Það gæti þurft að endurræsa síðuna til að sjá skýrsluna.

## <a name="explore-the-compare-item-prices-storage-report"></a>Skoðaðu skýrsluna Bera saman vöruverðsgeymslu

Eftir að þú hefur búið til skýrslu geturðu skoðað og kannað hana hvenær sem er á eftirfarandi hátt:

1. Farðu í **Kostnaðarstjórnun > Fyrirspurnir og skýrslur > Fyrirframákveðnar kostnaðarskýrslur > Bera saman geymslu vöruverðs**.

1. Velja skýrslu af listanum.

1. Gerið eitt af eftirfarandi:

    - Veldu **Yfirlit** til að fá yfirsýn yfir niðurstöður skýrslunnar.
    - Veldu **Skoða upplýsingar** til að fá nánari yfirsýn yfir skýrsluna þína

1. Eftir að valið yfirlit opnast er hægt að gera eftirfarandi:

    - Veldu næstum hvaða dálkafyrirsögn sem er til að flokka eða sía töfluna eftir gildum í þeim dálki, rétt eins og á flestum stöðluðum eyðublöðum í Supply Chain Management. Athugaðu að þú getur ekki flokkað eða síað dálkinn **Nettóbreyting verðs %** þar sem að það er reiknaður reitur.
    - Veldu **Birting vídda** til að opna glugga þar sem þú getur valið hvaða víddardálk á að hafa með í forminu. Stilltu **Vista skipulag** á **Já** ef þú vilt vista þessar stillingar svo þær verði varðveittar næst þegar þú opnar skýrsluna. Veldu **Í lagi** til að beita stillingum þínum og loka.
    - Veldu einhverja röð á forminu og veldu síðan **Skoða upplýsingar** til að sjá frekari upplýsingar um valda vöru. Þú getur borið niður í gögn héðan.
    - Veldu einhverja röð á forminu og veldu síðan **Skoða samanburðartöflu** til að sjá gagnvirka myndræna framsetningu á niðurstöðum þínum þegar þær tengjast vörunni sem þú valdir. Þú getur kannað þessar niðurstöður með því að velja ýmsa myndræna þætti í töflunni og skýringartextanum.
    - Veldu einhverja röð á forminu og veldu síðan **Skoða útreikningsupplýsingar** til að sjá frekari upplýsingar um útreikninga á valinni vöru. Þú getur borið niður í gögn héðan.

## <a name="export-the-compare-item-prices-storage-report"></a>Flyttu út skýrsluna Bera saman vöruverðsgeymslu

Sérhver skýrsla sem þú býrð til er vistuð í gagnaeiningunni **Bera saman vöruverð**. Þú getur notað staðlaða gagnastjórnunareiginleika Supply Chain Management til að flytja gögn út úr þessari einingu á hvaða studda gagnasnið sem er, þar á meðal CSV eða Microsoft Excel.

Eftirfarandi er dæmi um hvernig á að flytja út skýrsluna **Bera saman geymslu vöruverðs**:

1. Farðu í **Kerfisstjórnun > Vinnusvæði > Gagnastjórnun**.

1. Veldu hnappinn **Flytja út** í hlutanum **Gagnastjórnun**.

1. Síðan **Fltyja út** opnast, sem þú notar til að setja upp útflutningsvinnsluna. Byrjaðu á því að gefa vinnslunni **Heiti hóps**.

1. Í hlutanum **Valdar einingar** velurðu **Bæta við einingu** til að opna valmynd þar sem þú getur stillt eftirfarandi valkosti:

    - **Heiti einingar** - Veldu **Bera saman vöruverð**.
    - **Markgagnasnið** - Veldu sniðið sem þú vilt flytja út á.

1. Veldu **Bæta við** til að bæta við nýju röðinni og veldu síðan **Loka** til að loka glugganum.

1. Venjulega flyturðu út eina skýrslu í einu. Til að gera þetta seturðu upp **Síu** fyrir röðina sem þú varst að bæta við glugganum **Fyrirspurn**. Þetta gerir þér kleift að skilgreina hvaða skýrslur úr einingunni **Bera saman vöruverð** sem þú vilt hafa með í útflutningi þínum. Stilltu eftirfarandi síuvalkosti til að flytja út staka skýrslu:

    - Á flipanum **Svið** velurðu **Bæta við** til að bæta við nýrri röð.
    - Stilltu **Töflu** á **Bera saman vöruverð**.
    - Stilltu **Afleidda töflu** á **Bera saman vöruverð**.
    - Stilltu **Reit** á reitinn sem þú vilt sía eftir. Venjulega munt þú nota **Heiti framkvæmdar** eða **Framkvæmdartími**.
    - Stilltu **Viðmið** á gildið úr völdum reit sem þú vilt leita að (annaðhvort heiti skýrslunnar eða tíminn sem skýrslan var búin til).
    - Bætið við fleiri línum við töfluna **Svið** töflu þar til þú hefur bent á skýrsluna sem þú ert að leita að á einstakan hátt.

1. Veldu **Í lagi** til að vista stillingarnar og loka.

1. Veldu **Vista** til að vista uppsetningu á útflutningi.

1. Opnaðu flipann **Valkostir útflutnings** og veldu **Flytja út núna** til að búa til útflutningsskrána.

1. Síðan **Yfirlit framkvæmdar** opnast þar sem þú getur séð stöðuna á útflutningsvinnslunni og lista yfir þær einingar sem voru fluttar út. Veldu eininguna **Bera saman vöruverð** sem er skráð í reitinn **Vinnslustaða einingar** og veldu síðan **Sækja skrá** til að sækja gögnin sem flutt eru út úr þeirri einingu.

Nánari upplýsingar um hvernig á að nota gagnastjórnun til að flytja út gögn er að finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]