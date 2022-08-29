---
title: Stjórnborð notkunarstjórnunar
description: Þessi grein útskýrir hvernig á að nota stjórnborð notkunarstjórnunar til að fylgjast með notkun rafrænnar reikningaþjónustu og halda áfram að uppfylla kröfur.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 74f3d88faf192474c177da971a9f7bb0e58e1279
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272210"
---
# <a name="usage-management-dashboard"></a>Stjórnborð notkunarstjórnunar

[!include [banner](../includes/banner.md)]

Stjórnborðið **Notkunarstjórnun** hjálpar til við að fylgjast með notkun rafrænnar reikningsfærsluþjónustu og hjálpar því fyrirtækinu þínu að halda sig við mánaðarlega notkun. Reglufylgni ákvarðast með því að reikna út magn innsendingar og bera það saman við fengið magn innsendingar til að greina frávik milli fengins magns og notaðs magns.

Stjórnborðið inniheldur eftirfarandi vísa:

- Einn kostnaðarvísi sem hægt er að nota til að fylgjast með notkun vegna reglufylgni við leyfisveitingar:

    - Notkun á mánuði (útflutningur)

- Þrír rekstrarvísar sem hægt er að nota til að fylgjast með notkun rafrænnar reikningsfærsluþjónustu í stjórnunarskyni:

    - Notkun eftir eiginleika
    - Notkun eftir umhverfi
    - Notkun á mánuði (innflutningur)

## <a name="measurement-scope"></a>Umfang mælinga

- Mælieining: 

    Stjórnborð **Notkunarstjórnunar** telur innsendingu á viðskiptaskjölum og innfluttum rafrænum reikningum.

- Fyrirtæki: 

    Talning er tekin saman með auðkenni leigjanda fyrirtækisins þíns, óháð fjölda tilvika af Microsoft Dynamics 365 Fjármál eða Dynamics 365 Supply Chain Management, eða fjölda lögaðila þar sem rafræn reikningaþjónusta er virkjuð.


## <a name="indicator-usage-per-month-export"></a>Vísir: Notkun á mánuði (útflutningur)

Þessi vísir veitir upplýsingar um rafræna reikninga sem fyrirtækið gefur út á skilgreindu tímabili.

### <a name="scope"></a>Gildissvið
- Fjöldi viðskiptaskjala sem eru send frá Finance og Supply Chain Management til rafrænu reikningsfærsluþjónustunnar, óháð fjölda lína sem þessi viðskiptaskjöl innihalda.
- Fjöldi innsendra viðskiptaskjala sem rafræna reikningsfærsluþjónustan hefur unnið úr. Skjal telst hafa verið unnið þegar flæði aðgerða sem eru skilgreindar í uppsetningu eiginleika er lokið.

> [!NOTE]
> Þegar rafrænn reikningur er sendur á utanaðkomandi vefþjónustu er talning óháð niðurstöðum úr vinnslu vefþjónustu (samþykkt, hafnað eða villa skemaprófunar). Ef vefþjónustunni barst beiðni frá rafrænni reikningsfærsluþjónustu og svaraði henni telst innsendingin gild talning.

- **Undantekning:** Viðskiptaskjöl eru ekki talin ef þau eru send aftur frá Finance og Supply Chain Management til rafrænnar reikningsfærsluþjónustu eins og í þeim tilvikum þar sem endursending á sama viðskiptaskjalinu er nauðsynleg til að breyta stöðu rafræna reikningsins. Útgáfa á brasilískum rafrænum reikningi (fjárhagsskjali) telst til dæmis gild en beiðni um afturköllun hans er ekki talin.


### <a name="calculation"></a>Útreikningur

Útreikningur á stöðunni er reiknaður á eftirfarandi hátt:

Staða = Laust + keypt – notað

Hvar:

- Laust:
  
    Ókeypis magn viðskiptaskjala sem viðskiptavinurinn getur sent inn á mánuði. Það inniheldur pakka með 100 viðskiptaskjölum sem hægt er að senda til rafrænu reikningsfærsluþjónustunnar. Ókeypis magn safnast ekki upp og eftirstöðvar eru ekki færðar yfir á næsta tímabil.
  
- Innkeypt:
  
    Pakki með 1000 viðskiptaskjölum sem hægt er að senda til rafrænu reikningsfærsluþjónustunnar. Þennan pakka þarf að útvega mánaðarlega fyrir fyrirtækið þitt. Keypt magn safnast ekki upp og eftirstöðvar eru ekki færðar yfir á næsta tímabil.
  
- Notað: 

    Talning á innsendum viðskiptaskjölum til rafrænnar reikningsfærsluþjónustu samkvæmt skilgreindu skilyrði.
   
> [!IMPORTANT]
> Ef fyrirtækið áformar að fara yfir mánaðarlegt magn 100 ókeypis innsendinga skaltu kaupa hámarksmagn til að tryggja að þú fylgir reglum um leyfisveitingar Microsoft fyrir rafræna reikningsfærsluþjónustu.
>
> Sem stendur þarf að slá inn keypt magn handvirkt samkvæmt innkaupadagsetningunni sem margar pakkningar með 1000 innsendingum.

## <a name="indicator-usage-by-feature"></a>Vísir: Notkun eftir eiginleika

Þessi vísir sýnir notkun rafrænna reikningsfærslueiginleika fyrir útgáfu rafrænna reikninga á skilgreindu tímabili.

- Útreikningur:
  
    Notað = Talning á hversu oft hver rafrænn reikningsfærslueiginleiki var notaður við innsendingu viðskiptaskjala til rafrænnar reikningsfærsluþjónustu.

## <a name="indicator-usage-by-environment"></a>Vísir: Notkun eftir umhverfi

Þessi vísir sýnir notkun á umhverfum rafrænna reikningsfærsluþjónustu á skilgreindu tímabili.

- Útreikningur:
    
    Notað = Talning á hversu oft hver rafræn reikningsfærsluþjónusta var notað við innsendingu viðskiptaskjala til rafrænnar reikningsfærsluþjónustu.

## <a name="indicator-usage-per-month-import"></a>Vísir: Notkun á mánuði (innflutningur)

Þessi vísir sýnir magn á innflutningi rafrænna reikninga af hendi rafrænnar reikningsfærsluþjónustu til Finance og Supply Chain Management á skilgreindu tímabili.

- Umfang:

    Rafrænir reikningar sem eru fluttir inn í Finance og Supply Chain Management, burtséð frá fjölda lína sem þessir rafrænu reikningar innihalda.

- Útreikningur:

    Móttekið = Talning á rafrænum reikningum sem eru fluttir inn í Finance og Supply Chain Management.

## <a name="functions"></a>Aðgerðir
### <a name="purchase"></a>Innkaup

Í flipanum **Notkun á mánuði (útflutningur)** skal velja **Kaup** til að skrá handvirkt magn fenginna innsendinga.

Fyrir ákveðna dagsetningu er valið **Nýtt** og færður inn fjöldi **Pakkninga** sem fengnar voru fyrir þann dag.

**Magnið** er reiknað svona:

Magn = Pakkningar * 1.000

Reiknað **Magn** kemur fram í **Keypt** í vísinum **Notkun á mánuði (útflutningur)**.

### <a name="update"></a>Update

Smellið á **Uppfæra** á aðgerðasvæðinu til að uppfæra útreikninginn og uppfæra gögnin sem sýnd eru á síðunni og í grafinu.

### <a name="reset-history-data"></a>Hreinsa ferilsgögn

Veljið **Endurstilla ferilsgögn** á aðgerðasvæðinu til að uppfæra gagnagrunninn þar sem vísarnir eru reiknaðir.




> [!NOTE]
> Stjórnborðið **Notkunarstjórnun** sýnir ekki peningaupphæðir. Í staðinn sýnir það aðeins magn taldra innsendinga og innfluttra skjala.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
