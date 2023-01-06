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
ms.openlocfilehash: 6e346c6ff881d3a33743196b45247493fd19ed1d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573252"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Leyfa breytingar á innri gögnum á fylgiskjölum fjárhags

[!include[banner](../includes/banner.md)]


Þegar bókhaldsfærslur eru bókaðar í fjárhag er reiturinn **Lýsing** oft notaður til að geyma innri athugasemdir eða gögn. Ef upplýsingarnar eru rangar getur það valdið ruglingi og gert lokun tímabils erfiðari. Þessi eiginleiki gerir bókhaldsstjórnanda eða yfirmanni bókhalds kleift að laga mistök með því að breyta reitnum **Lýsing** á bókuðum fylgiskjölum fjárhags.

Breytingar á birtum fylgiskjölum í fjárhaginum takmarkast við gögn sem eru innri. Þessi eiginleiki leyfir þér aldrei að breyta gögnum eins og upphæðum, bókunardagsetningum, fjárhagslyklum og gjaldmiðli færslu. Breytingar á þeim gögnum hafa áhrif á ytri skýrslugjöf fyrir fjárhagsskýrslur og verða aðeins gerðar með nýjum fylgiskjölum fjárhags.

> [!NOTE]
> Fyrir Dynamics 365 Finance útgáfu 10.0.29 er þessi eiginleiki takmarkaður við breytingar á reitnum **Lýsing**.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Breyta innri gögnum á fylgiskjölum fjárhags

Áður en hægt er að breyta innri gögnum á fylgiskjölum í fjárhag verður þú að virkja **Leyfa breytingar á innri gögnum á fylgiskjölum fjárhags** á vinnusvæðinu **Eiginleikastjórnun**.
Eftir að eiginleikinn er virkur verður notandinn sem mun breyta bókuðum fylgiskjölum að fá úthlutað hlutverki bókhaldsstjórnanda eða yfirmanns bókhalds. Hægt er að bæta heimildum við önnur hlutverk með því að sérsníða öryggishlutverkin.

Aðeins er heimilt að breyta á síðunni „Færslur á fylgiskjal“.

1. Opnið **Fjárhag** > **Fyrirspurnir og skýrslur** > **Fylgiskjalafærslur**.
2. Í svarglugganum **SysQuery** skaltu slá inn leitarskilyrði til að velja fylgiskjöl.
3. Veljið línurnar fyrir fylgiskjölin sem á að breyta og síðan er valið **Breyta fylgiskjali** > **Breyta innri gögnum fylgiskjals**.

    [![Síðan Færslur fylgiskjals.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
Á síðunni **Breyta innri gögnum fylgiskjals** eru eftirfarandi upplýsingar sýndar fyrir hverja línu sem þú valdir:
  
  - Fjárhagslykill
  - Heiti lykils
  - Fylgiskjal
  - Núgildandi lýsing
  - Ný lýsing

    [![Fylgiskjal færslubókar.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Aðeins er hægt að breyta reitnum **Ný lýsing**. Gildið samsvarar sjálfgefið gildinu í reitnum **Núverandi lýsing**, þannig að þú getur fljótt lagað minniháttar mistök í lýsingunni.

4. Breyttu reitnum **Ný lýsing** í hverri línu, eða eyddu lýsingunni úr hverri línu.

   Ef uppfæra þarf margar línur með sama gildi er einnig hægt að fylgja þessum skrefum:

      1. Veljið línurnar sem á að breyta og veljið síðan **Magnuppfæra valdar færslur**.
      2. Í reitnum **Reitur til að breyta** skal velja reitinn sem á að breyta. Sem stendur inniheldur uppflettingin aðeins reitinn **Ný lýsing**.
      3. Í reitinn **Nýtt gildi** er færð inn ný lýsing.
      4. Veldu **Uppfæra**. Allar völdu færslurnar eru uppfærðar með nýja gildinu.

      [![Svargluggi magnuppfærslu valdra færsla.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. Í reitnum **Ástæða breytinga** er sett inn athugasemd til að útskýra hvers vegna breytingin var gerð. Þessi athugasemd birtist á síðunni **Endurskoðunarslóð fylgiskjalsbreytinga**.

   Hægt er að gera margar breytingar á sama fylgiskjalinu og fylgjast með hverri breytingu.

## <a name="audit-trail-of-voucher-edits"></a>Endurskoðunarslóð fylgiskjalsbreytinga

Slóð færslna er haldið sérstaklega til að fylgjast með þeim breytingum sem eru gerðar með þessum eiginleika. Hægt er að fá aðgang að endurskoðunarslóð fylgiskjalsbreytinga á tvo vegu:

  - Opnið **Fjárhag** > **Fyrirspurnir og skýrslur** > **Fylgiskjalafærslur**. Á síðunni **Fylgiskjalsfyrirspurnir** skaltu velja **Breyta fylgiskjali** > **Endurskoðunarslóð fylgiskjalsbreytinga**. Endurskoðunarslóðin birtist aðeins fyrir valda fylgiskjalsfærslu. 
   
    Með því að opna fyrirspurnina á þennan hátt getur þú einbeitt þér að öllum breytingum sem gerðar voru á einni fylgiskjalsfærslu.
  
  - Farðu í**Fjárhagur** > **Reglubundin verkefni** > **Endurskoðunarslóð fylgiskjalsbreytinga**. Færið inn skilyrði í svargluggann til að tilgreina fylgiskjölin sem á að skoða endurskoðunarslóð breytinga fyrir. Til að skoða endurskoðunarslóð fyrir öll fylgiskjöl skaltu skilja viðmiðin eftir auð og velja **Í lagi**. 
    
    Með því að opna fyrirspurnina á þennan hátt er hægt að sía eftir breytingum sem voru gerðar á tilteknum degi eða af tilteknum notanda.

Á síðunni **Endurskoðunarslóð breytinga** birtast eftirfarandi upplýsingar:

- **Stofnuð dagsetning og tími** – Dagsetning og tími breytingar.
- **Ástæða breytingar** – Ástæðan fyrir því að notandinn sló inn fyrir breytinguna.
- **Búið til af** – Notandinn sem gerði breytinguna.

Til að skoða upplýsingar um hverja endurskoðunarslóð, kafa niður á gildið **Stofnuð dagsetning og tími**. Síðan **Skoða breytta eiginleika fylgiskjals** sýnir sömu upplýsingar og á upphaflega síðunni, þar á meðal fyrri lýsinguna og uppfærðu lýsinguna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
