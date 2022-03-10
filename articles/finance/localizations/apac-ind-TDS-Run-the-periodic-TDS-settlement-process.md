---
title: Keyra reglubundið uppgjörsferli TDS
description: Í þessu efnisatriði er útskýrt hvernig á að gera upp reglubundinn skatt sem dreginn er frá uppruna (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 05438b11f446da57016ff66f4deafd0c07fd62f32eba6f10c4b08b3f1de88e6b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739930"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Keyra reglubundið uppgjörsferli TDS

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að gera upp reglubundinn skatt sem dreginn er frá uppruna (TDS).

1. Farið í **Skattur \> Skattskýrslur \> Staðgreiðsluskattur \> Greiðsla staðgreiðsluskatts**.

    [![Svargluggi staðgreiðsluskattsgreiðslu.](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. Í svarglugganum **Greiðsla staðgreiðsluskatts**, í reitnum **Skattgerð**, skal velja **TDS**.
3. Í reitnum **Númer skattlykils (TAN)** skal velja númer skattlykils (TAN) til að keyra uppgjörsferlið fyrir.
4. Í reitnum **Flokkur staðgreiðsluskattshluta** skal velja flokk TDS-hluta til að keyra uppgjörsferlið fyrir.
5. Í reitnum **Uppgjörsferli** skal velja uppgjörsferli TDS til að keyra uppgjörsferlið fyrir.

    > [!NOTE]
    > TDS-uppgjörsferlið er keyrt fyrir öll tímabil sem eru sett upp fyrir TDS-uppgjörstímabilið í flipanum **Tímabil** á síðunni **Uppgjörstímabil staðgreiðsluskatts** (**Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Uppgjörstímabil staðgreiðsluskatts**).

6. Í reitnum **Frá dagsetningu** skal velja upphafsdagsetningu til að keyra TDS-uppgjörsferlið frá.

    Fyrir tiltekið tímabil innan uppgjörstímabilsins er upphafsdagsetningin sem er skilgreind fyrir tímabilið tekin sem „frá“ dagsetningin. Til dæmis hefur TDS-uppgjörstímabilið tvö tímabil: 1. apríl til 30. apríl 2009 og 1. maí til 31. maí 2009. Ef valið er **06/04/2009** (6. apríl 2009) sem upphafsdagsetning í reitnum **Frá dagsetningu** mun uppgjörsferlið enn keyra frá 1. apríl 2009.

    Ef seinna tímabil er fært inn í reitinn **Frá dagsetningu**, en án þess að gera upp fyrra tímabil innan uppgjörstímabilsins mun uppgjörið ekki eiga sér stað fyrir neitt eldra tímabil. Til dæmis hefur TDS-uppgjörstímabilið þrjú tímabil: 1. apríl til 30. apríl 2009, 1. maí til 31. maí 2009 og 1. júní til 30. júní 2009. Ef valið er **01/05/2009** (1. maí 2009) sem upphafsdagsetning í reitnum **Frá dagsetningu** mun uppgjörsferlið aðeins keyra frá 1. maí til 31. maí 2009. Uppgjörið á sér ekki stað 1. apríl til 30. apríl 2009.

7. Í reitnum **Færsludagsetning** skal velja dagsetninguna til að bóka færslu TDS-uppgjörs.
8. Í reitnum **Greiðsluútgáfa staðgreiðsluskatts** skal velja útgáfu TDS-uppgjörs:

     - **Upprunalegt** – Notið þennan valkost til að keyra TDS-uppgjörsferli í fyrsta skipti. Upprunaleg greiðsluútgáfa er aðeins notuð í eitt skipti til að keyra TDS-uppgjörsferlið fyrir samsetningu af TAN, flokki staðgreiðsluskattshluta og uppgjörstímabili staðgreiðsluskatts.
    - **Nýjustu útgáfur** Þ Notið þennan valkost ef TDS-uppgjörsferlið hefur þegar verið keyrt fyrir tiltekið tímabil. Hafa með færslur færðar aftur í tíma sem voru bókaðar eftir að uppgjörsferlið var keyrt áður fyrir tímabilið. Hægt er að nota þenna valkost til að keyra uppgjörsferlið eins oft og þarf.

9. Veljið gátreitinn **Uppfæra** til að keyra TDS-uppgjörsferlið og bóka upphæðirnar á fjárhagslyklana. Ef þessi gátreitur er hreinsaður verður uppgjörsferlið ekki keyrt og fjárhagsfærslurnar verða ekki myndaðar.
10. Veljið **Í lagi** til að keyra TDS-uppgjörsferlið og mynda greiðsluskýrslu staðgreiðsluskatts. Staðan á TDS-færslum sem eru teknar með í uppgjörsferlinu er sýnd sem **Jöfnuð** á síðunni **Uppgjör** (farið í **Viðskiptaskuldir \> Greiðslur \> Færslubók viðskiptakrafa**, veljið **Línur**, veljið **Aðgerðir** og veljið því næst **Uppgjör**).

### <a name="important-points"></a>Mikilvæg atriði

- Ef flokkur staðgreiðsluskattshluta er ekki valinn í uppgjörsferlinu á uppgjörið sér stað fyrir alla flokka staðgreiðsluskattshluta fyrir valið TAN og uppgjörtímabil. Sérstök lína er stofnuð fyrir hvern flokk staðgreiðsluskattshluta á síðunni **Breytingar á opnum færslum**.
- Uppgjörsferlið byggir á eðli skattgreiðendaflokks fyrir uppgjörstímabil. Færslur þar sem eðli skattgreiðendaflokks er **Fyrirtæki** eru gerðir upp og sýndir sem ein lína á síðunni **Breytingar á opnum færslum**. Færslur þar sem eðli skattgreiðenda er eitthvað annað en **Fyrirtæki** eru gerðar upp og sýndar sem ein lína á síðunni **Breytingar á opnum færslum**.
- Gjalddagi fyrir jafnaðar TDS-færslulínur á síðunni **Breytingar á opnum færslum** er byggð á greiðsluskilmálum sem eru skilgreindir fyrir TDS-lánardrottnayfirvald á síðunni **Lánardrottnar**. Ef greiðsluskilmálarnir eru ekki skilgreindir fyrir TDS-lánardrottnayfirvald er síðasti dagur uppgjörstímabilsins sýndur sem gjalddagi.
