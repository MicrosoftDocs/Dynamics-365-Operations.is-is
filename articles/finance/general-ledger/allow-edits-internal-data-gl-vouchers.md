---
title: Leyfa breytingar á innri gögnum á fylgiskjölum fjárhags
description: Þessi grein veitir upplýsingar um hvernig á að breyta innri gögnum á fylgiskjölum í fjárhag.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 26fc6518f0b4eae815e047db1dbaadd7c56a2e67
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220720"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Leyfa breytingar á innri gögnum á fylgiskjölum fjárhags

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]


Þegar þú bókar bókhaldsfærslur í fjárhag, **Lýsing** reiturinn er oft notaður til að geyma innri athugasemdir eða skjöl. Ef upplýsingarnar eru rangar getur það valdið ruglingi og gert tímabilslok erfiðari. Þessi eiginleiki gerir bókhaldsstjóra eða bókhaldsstjóra kleift að laga mistök með því að breyta **Lýsing** reit á bókuðum fylgiskjölum í aðalbók.

Breytingar á bókuðum fylgiskjölum í fjárhag takmarkast við gögn sem eru innri í eðli sínu. Þessi eiginleiki mun aldrei leyfa þér að breyta gögnum eins og upphæðum, bókunardagsetningum, höfuðbókarreikningum og viðskiptagjaldmiðlinum. Breytingar á þeim gögnum munu hafa áhrif á ytri skýrslugerð reikningsskila og verður aðeins að gera með nýjum fylgiskjölum í aðalbók.

> [!NOTE]
> Fyrir Dynamics 365 Finance útgáfu 10.0.29 er þessi eiginleiki takmarkaður við breytingar á **Lýsing** sviði.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Breyta innri gögnum á fylgiskjölum í aðalbók

Áður en hægt er að breyta innri gögnum á fylgiskjölum í aðalbók verður þú að virkja **Leyfa breytingar á innri gögnum á fylgiskjölum í aðalbók** eiginleiki í **Eiginleikastjórnun** vinnurými.
Eftir að eiginleikinn hefur verið virkjaður verður notandinn sem mun breyta innsendum fylgiskjölum að vera úthlutað í hlutverk bókhaldsstjóra eða bókhaldsstjóra. Þú getur bætt heimildum við önnur hlutverk líka með því að sérsníða öryggishlutverkin.

Breytingarferlið er aðeins leyft frá færslumiðasíðunni.

1. Fara til **Aðalbók** > **Fyrirspurnir og skýrslur** > **Viðskipti með skírteini**.
2. Í **SysQuery** valmynd, sláðu inn leitarskilyrði til að velja fylgiskjöl.
3. Veldu línurnar fyrir fylgiskjölin sem þú vilt breyta og veldu síðan **Breyta skírteini** > **Breyta innri fylgiskjalsgögnum**.

    [![Vörubréfaviðskipti síða.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
Á **Breyta innri fylgiskjalsgögnum** síðu eru eftirfarandi gögn sýnd fyrir hverja línu sem þú valdir:
  
  - Fjárhagslykill
  - Heiti lykils
  - Fylgiskjal
  - Núgildandi lýsing
  - Ný lýsing

    [![Fylgiskjal færslubókar.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Aðeins **Ný lýsing** reit er hægt að breyta. Sjálfgefið er að gildið passar við gildið á **Núverandi lýsing** reit, svo að þú getir fljótt lagað minniháttar mistök í lýsingunni.

4. Breyttu **Ný lýsing** reit í hverri röð, eða eyða lýsingunni úr hverri línu.

   Að öðrum kosti, ef uppfæra þarf margar línur með sama gildi, fylgdu þessum skrefum:

      1. Veldu línurnar til að breyta og veldu síðan **Magnuppfæra valdar færslur**.
      2. Í **Reitur til að breyta** reit, veldu reitinn sem á að breyta. Eins og er inniheldur uppflettingin aðeins **Ný lýsing** sviði.
      3. Í **Nýtt gildi** reit, sláðu inn nýja lýsingu.
      4. Veldu **Uppfæra**. Allar valdar færslur eru uppfærðar með nýja gildinu.

      [![Magnuppfærslu valinna færsluglugga.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. Í **Ástæða fyrir breytingu** reit skaltu slá inn athugasemd til að útskýra hvers vegna breytingin var gerð. Þessi athugasemd er sýnd á **Endurskoðunarslóð breytinga á fylgiskjölum** síðu.

   Hægt er að gera margar breytingar á sama skírteini og fylgst verður með hverri breytingu.

## <a name="audit-trail-of-voucher-edits"></a>Endurskoðunarslóð fylgiskjalsbreytinga

Úttektarslóð er viðhaldið sérstaklega til að fylgjast með breytingunum sem eru gerðar með þessum eiginleika. Þú getur fengið aðgang að endurskoðunarferil breytinga á fylgiskjölum á tvo vegu:

  - Fara til **Aðalbók** > **Fyrirspurnir og skýrslur** > **Viðskipti með skírteini**. Á **Fyrirspurnir um fylgiskjöl** síðu, veldu **Breyta skírteini** > **Endurskoðunarslóð breytinga á fylgiskjölum**. Endurskoðunarferillinn er aðeins sýndur fyrir valda fylgiskjalaskrá. 
   
    Með því að opna fyrirspurnina á þennan hátt geturðu einbeitt þér að öllum breytingum sem gerðar voru á einni fylgiskjalsskrá.
  
  - Farðu í** Fjárhagsbók** >**Reglubundin verkefni** > **Endurskoðunarslóð breytinga á fylgiskjölum**. Í svarglugganum, sláðu inn skilyrði til að tilgreina fylgiskjölin sem þú vilt skoða endurskoðunarferil breytinga fyrir. Til að skoða endurskoðunarferil allra fylgiskjala, skildu viðmiðin eftir auð og veldu **Allt í lagi**. 
    
    Með því að opna fyrirspurnina á þennan hátt er hægt að sía eftir breytingum sem voru gerðar á tilteknum degi eða af tilteknum notanda.

The **Endurskoðunarslóð breytinga** síða sýnir eftirfarandi upplýsingar:

- **Búin til dagsetning og tími** – Dagsetning og tími breytingarinnar.
- **Ástæða fyrir breytingu** – Ástæðan fyrir því að notandinn kom inn fyrir breytinguna.
- **Búið til af** - Notandinn sem gerði breytinguna.

Til að skoða upplýsingar um hverja endurskoðunarslóð skaltu kafara niður í **Búin til dagsetning og tími** gildi. The **Skoðaðu breytta fylgiseiginleika** síða sýnir sömu upplýsingar og upprunalega breytingasíðan, þar á meðal fyrri lýsing og uppfærða lýsing.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
