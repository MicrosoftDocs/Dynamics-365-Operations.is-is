---
title: Nota samþykktarverkflæði leigusamnings
description: Þetta efnisatriði útskýrir hvernig á að nota verkflæði til að samþykkja eignaleigur og hvernig á að rekja stöðu og feril verkflæðanna.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 33faf7aa6bc9e5df4b8b0f004692b2c1803c6994264c7b9a8e3eb404387f6800
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726087"
---
# <a name="use-lease-approval-workflows"></a>Nota samþykktarverkflæði leigusamnings

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að nota verkflæði til að samþykkja eignaleigur og hvernig á að rekja stöðu og feril verkflæðanna. Verkflæði aðstoða við að samræma samþykktarstjórnun leigusamninga með því að bjóða upp á staðlað safn af samþykktarskrefum og úthluta tilteknum notendum sem samþykkja hvert skref ferlisins. Samþykktaraðili getur samþykkt leigu, hafnað henni, óskað eftir breytingu á henni eða úthlutað henni á annan notanda til samþykkis. Verkflæði geta einnig aukið sýnileika inn í samþykktarferlið með að leyfa þér að fylgjast með stöðu og ferli þeirra. Að auki er hægt að skoða miðstýrða vinnulista sem birta verk og samþykktir sem er úthlutað á tiltekna samþykkjendur.

Áður en þetta ferli er notað skal ganga úr skugga um að a.m.k. eitt samþykktarverkflæði leigutaka hafi verið stofnað. Ef ekkert verkflæði er til staðar skal stofna það. Upplýsingar um hvernig á að setja upp verkflæði er að finna í [Setja upp samþykktarverkflæði leigusamnings](set-up-lease-wrkflw.md).

1. Senda leigu til samþykktar. Á síðunni **Bókarupplýsingar** fyrir leigusamninginn skal velja **Verkflæði** og síðan velja **Senda**.
2. Í svarglugganum sem birtist er hægt að bæta við athugasemd. Tilnefndur samþykktaraðili mun sjá þessa athugasemd ásamt leigusamningi. Þegar þú hefur lokið við að slá inn athugasemdina skaltu velja **Senda**. Leigusamningurinn er sendur í verkflæðiskerfið og samþykktaraðilinn fær hann til samþykkis.
3. Til að skoða leigusamningana sem eru merktir til samþykkis skal fara í **Einingar \> Almennt \> Vinnuliðir \> Vinnuliðir sem mér var úthlutað**.
4. Á síðunni **Vinnuliðir sem úthlutað er á mig** skal velja **Leigukenni** tengilinn fyrir leiguna sem á að skoða. Síðan sem birtist er háð leigubókunum og leiguupplýsingum sem notandi hefur aðgang að.
5. Þegar þú hefur lokið við að skoða leigusamninginn skaltu velja **Verkflæði** og ákveða hvaða aðgerð á að taka. Valkostirnir eru m.a. **Samþykkja**, **Hafnað**, **Biðja um breytingu**, **Úthluta** og **Hætt við**. Einnig er hægt að velja **Skoða feril** til að skoða samþykktarferil fyrir valinn leigusamning.
6. Þegar aðgerð hefur verið valin skal færa inn athugasemd til að lýsa aðgerðinni. Þegar þú hefur lokið við að slá inn athugasemdina skaltu velja aðgerðina **Samþykkt** á listanum.
7. Til að skoða samþykktaraðgerðirnar skal fara aftur í **Upplýsingar um leigusamning** á síðunni **Samantekt leigusamnings** og síðan velja **Verkflæði \> Skoða feril**.

    Hægt er að skoða verkflæðisaðgerðir á síðunni **Verkflæðisferill** . Þessi síða sýnir verkflæðisskref sem hafa verið tekin á tilteknum leigusamningum. Einnig er hægt að nota svæðið **Vinnuliðir** til að skoða stöðu úthlutaðra vinnuliða.

8. Til að stöðva verkflæði, á síðunni **Verkflæðisferill** skal velja **Afturkalla**. Í svarglugganum sem birtist skal færa inn athugasemd og velja svo **Í lagi**.
9. Til að gera verkflæði óvirkt, eða til að virkja verkflæði sem var áður stofnað, skal fara í **Eignarleiga \> Uppsetning \> Verkflæði leigusamnings**. Síðan á síðunni **Verkflæði leigusamnings** skal velja **Verkflæði \> Útgáfur**. Til að gera núverandi verkflæði óvirkt skal velja virka leigusamninginn í svarglugga útgáfu leigusamningsins og velja svo **Gera óvirkt**. Til að gera fyrirliggjandi verkflæði virkt skal velja verkflæðið og velja svo **Gera virkt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
