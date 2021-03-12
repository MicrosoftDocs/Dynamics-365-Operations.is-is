---
title: Vinna með leigusamninga í innflutningsramma leigusamnings
description: Þetta efnisatriði útskýrir hvernig á að nota innflutningsramma leigusamnings til að breyta mörgum leigusamningum samtímis.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7df2f55f596cab54315c2da2ec0492422514f49c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971304"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Vinna með leigusamninga í innflutningsramma leigusamnings

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að nota innflutningsramma leigusamnings til að breyta mörgum leigusamningum í einu skrefi. Notaðu þennan eiginleika til að spara tíma og til að tryggja nákvæmari breytingar með því að draga úr líkum á mannlegum mistökum. Þar að auki getur þessi eiginleiki tengt Microsoft Dynamics 365 Finance við ytri gagnaeiningar til að hlaða upp gögnum á skilvirkan hátt.

Eftirfarandi gagnaeiningar er hægt að nota til að samþætta eignarleigu við ytri kerfi:

- Undirbúningur leigusamnings
- Undirbúningur greiðslusamnings
- Undirbúningur rekstrarsamnings

Hægt er að nota innflutningsferlið til að gera breytingar á leigusamningi, uppfæra aðrar upplýsingar en fjárhagsupplýsingar eða bæta við nýjum leigusamningum. Hægt er að skoða og breyta gögnum leigusamningsins áður en þau eru flutt inn.

Kerfið getur keyrt eftirfarandi þrjú ferli í gegnum innflutningspakka leigusamningsins.

| Gerð ferlis  | lýsing |
|---------------|-------------|
| Bæta við færslu    | Fluttir leigusamningar sem eru með þessa vinnslugerð stofna leigusamning í kerfinu. Greiðsluáætlunina þarf að staðfesta handvirkt og nauðsynlegt er að bóka fyrstu viðurkenndu bókarfærsluna handvirkt eftir flutninginn. |
| Uppfæra færslu | Fluttir leigusamningar sem eru með þessa gerð ferils uppfæra reitargildi fyrir leigusamning sem er þegar í kerfinu. Aðeins svæði valdin í **Val á uppfærslu svæða** eru uppfærð. Mælt er með því að notandi velji svæði sem ekki eru fjárhagslegir á síðunni **Val á uppfærslu svæða** vegna þess að þessi gerð ferlis breytir ekki leigusamningnum. |
| Leiðrétta færslu | Fluttir leigusamningar sem eru með þessa gerð ferlis gera breytingar á leigusamningnum. Þessi breyting veldur fjárhagsbreytingum á leigusamningnum. Þegar búið er að vinna úr leigusamningnum stofnar kerfið nýja greiðsluáætlun með því að nota nýju gögnin úr innflutningspakka leigusamningsins. Kerfið staðfestir ekki greiðsluáætlunina né bókar færslu leiðréttingarbókar. |

Eftir að upplýsingum hefur verið hlaðið upp í gegnum vinnusvæðið **Gagnastjórnun** skal opna síðuna **Flytja inn haus** (**Eignarleiga \> Innflutningsrammi leigusamnings \> Flytja inn haus**). Þessi síða sýnir allan innflutning á þrem gagnaeiningum sem voru áður skráðar.

Til að skoða sviðsetningargögn leigusamningsins áður en vinnsla er keyrð skal velja **Sviðsetningargögn**.

Samanburðaraðgerð gerir þér kleift að bera saman færslu sem þú ert að flytja inn við samsvarandi færslu sem er þegar í kerfinu. Til að bera saman hverja færslu leigusamnings skal velja leigusamning og síðan velja **Bera saman**. Þú ættir að ljúka þessu skrefi til að búa til skýrslu um **Mismun** -skýrslu áður en þú flytur færslur leigusamningsins. Samanburðarvirkni ber saman gildin í sviðsetningargögnunum við gildi leigusamninga sem þegar eru í kerfinu.

> [!NOTE]
> Samanburðarvirkni virkar ekki fyrir leigusamninga sem eru með **Bæta við færslu** gerð ferils, vegna þess að ekkert er til staðar til að bera saman við viðkomandi leigusamning.
>
> Til að bera saman marga leigusamninga samtímis er farið í **Eignarleiga \> Innflutningsrammi leigusamnings \> Reglubundið \> Bera saman** og velja **Bera saman**.

Fyrir hverja einingu er hægt að skoða mismuninn á því sem er í kerfinu og hvað er í sviðsetningartöflunum. Fyrir hverja einingu í sviðsetningartöflunum skal velja **Sjá mismun**. Svarglugginn sem birtist sýnir núverandi gildi og áætlað sviðsetningargildi.

Einnig er hægt að uppfæra sviðsetningargildið með því að breyta því í dálkinum **Nýtt gildi** og velja síðan **Uppfæra sviðsetningu**.

Hægt er að villuleita leigusamninga til að tryggja að hægt sé að færa færslurnar inn í kerfið villulaust. Áður en færsla leigusamnings er flutt keyrir kerfið nokkrar villuleitir til að tryggja að færslan verði flutt inn. Til að villuleita tiltekinn leigusamning skal velja **Villuleita**.

> [!NOTE]
> Til að villuleita marga leigusamninga samtímis er farið í **Eignarleiga \> Innflutningsrammi leigusamnings \> Reglubundið \> Villuleita** og velja **Bera saman**.

Til að vinna úr tilteknum leigusamningi skal velja **Flytja gögn leigusamnings** á síðunni **Flytja inn haus**. Þegar leigusamningur er fluttur framkvæmir kerfið aðgerðina sem er tilgreind í svæðinu **Gerð ferlis**.

> [!NOTE]
> Til að villuleita marga leigusamninga samtímis er farið í **Eignarleiga \> Innflutningsrammi leigusamnings \> Reglubundið \> Villuleita** og velja **Bera saman**.

Eftir að leigusamningar eru bornir saman er hægt að keyra skýrslu til að skoða mismuninn á hverjum leigusamningi sem er innifalinn í innflutningskenninu. Til að keyra þessa skýrslu fyrir einn leigusamning skal velja viðkomandi leigusamning í sviðsetningargögnum og velja svo **Bera saman og skoða skýrslu \> Skýrsla um mismun**.

> [!NOTE]
> Til að villuleita marga leigusamninga samtímis er farið í **Eignarleiga \> Fyrirspurnir og skýrslur \> Skýrsla um mismun** og velja **Bera saman**.

## <a name="set-up-update-fields"></a>Setja upp uppfærð svæði

Ef verið er að nota innflutningsramma leigusamnings til að uppfæra leigusamninga, og gerð ferlisins er **Uppfæra færslu** er hægt að velja tiltekin svæði til að uppfæra.

1. Opnaðu **Eignarleiga \> Innflutningsrammi leigusamnings \> Uppsetning \> Uppfæra val á svæði**.
2. Á síðunni sem birtist eru svæði valin til að uppfæra og síðan er græna örin valin til að færa þau yfir í listann yfir **Valin svæði**. Aðeins er hægt að uppfæra svæði á listanum **Valin svæði** með því að nota innflutningspakka leigusamnings.
