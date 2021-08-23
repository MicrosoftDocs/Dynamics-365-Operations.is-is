---
title: Reikna út TDS á reikningum með færslubókum
description: Í þessu efnisatriði eru talin upp skrefin fyrir útreikning á TDS fyrir færslubækur.
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
ms.openlocfilehash: cfe473f39ee729957924fd7c161aed01138cd507eea56766af35177891676f65
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778894"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>Reikna út TDS á reikningum með færslubókum

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði eru talin upp skrefin fyrir útreikning á TDS fyrir færslubækur.

Byrjið á því að opna síðuna **Almennar færslubækur** (**Fjárhag > Færslubókarfærslur > Almennar færslubækur**).

[![Almennar færslubækur.](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Stofnið færslubókarlínur með skjámyndum færslubókar sem eru gefnar upp í töflunni. Veljið gerð lykils og gerð mótlykils og sláið inn upphæð færslunnar. 

   > [!NOTE]
   > Á síðunni **Færslubókarsamþykkt reiknings** skal velja **Finna fylgiskjöl** og velja reikninga til að reikna út TDS fyrir. Skoðið reikningana sem stofnaðir eru á síðunni **Skráning reiknings** eða síðunni **Finna fylgiskjöl**.  

2. Í flipanum **Almennt** á síðunni **Fylgiskjal færslubókar** skal skoða eða breyta sjálfgefnum TDS-flokki sem skilgreindur er fyrir lánardrottin eða viðskiptavin í reitnum **TDS-flokkur**. TDS-upphæðin sem er reiknuð út í færslubókarlínum byggir á formúlu sem skilgreind er fyrir TDS-skattkóðana sem gefnir eru upp í reitnum **TDS-flokkur**. 

   > [!NOTE]
   > Reiturinn **Staðgreiðsluskattsflokkur** og reiturinn **TCS-flokkur** verða ekki í boði þegar TDS-flokkur er valinn í reitnum **TDS-flokkur**. Reiturinn **Staðgreiðsluskattsflokkur** er aðeins í boði á síðunni **Almenn færslubók**. TDS er aðeins reiknað ef gátreiturinn **Reikna staðgreiðsluskatt** er valinn fyrir lánardrottin eða viðskiptavin á síðunum **Allir lánardrottnar** eða **Allir viðskiptavinir**.   

3. Veljið flipann **Skattaupplýsingar**. Veljið önnur aðsetur fyrirtækis sem sett er upp fyrir fyrirtækið í þessum reit ef á þarf að halda. Hægt er að skoða heiti fyrirtækis í reitnum **Heiti** sem er undir reitahópnum **Upplýsingar um fyrirtæki**. 

4. Skoðið eðli skattgreiðendaflokksins fyrir lánardrottin eða viðskiptavin í reitnum **Eðli skattgreiðanda** sem er undir reitahópnum **Staðgreiðsluskattur**. Í reitnum **Skattlykilnúmer** (**TAN**) skal skoða TAN fyrir valið heiti fyrirtækis sem er sýnt.  

5. Veljið **Staðgreiðsluskattur** í valmyndinni **Staðgreiðsluskattur** til að opna síðuna **Tímabundnar staðgreiðsluskattsfærslur**. Eftirfarandi reitir eru sýndir í efri rúðunni á síðunni **Tímabundnar staðgreiðsluskattsfærslur**.

   - **Upphæð staðgreiðsluskatts samtals** - Samtals TDS reiknað út fyrir færsluna fyrir TDS-flokkinn.

   - **Gildi** - Heildarprósenta notuð til að reikna út TDS fyrir færsluna. Heildarprósentan er byggð á formúlunni sem er skilgreind fyrir TDS-skattkóða sem hengdir eru við TDS-flokkinn.

   - **Samtals leiðrétt upphæð staðgreiðsluskatts** - Leiðrétt heildarupphæð TDS fyrir alla skattkóða í TDS-flokknum.

   - **TDS** - Ef valið er TDS-flokkur hengdur við færsluna.

  Reitirnir í flipunum **Yfirlit**, **Almennt** og **Leiðrétting** á síðunni **Tímabundnar staðgreiðsluskattsfærslur** sýna upplýsingar um reiknaða TDS-upphæð og leiðrétta TDS-upphæð fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.

6. Veljið **Mörk** til að opna síðuna **Mörk**. Skoðið mörkin og undantekningarmörkin sem skilgreind eru fyrir TDS-skattþáttinn sem hengdur er við tiltekinn TDS-skattkóða á þessari síðu.

   Veljið **Formúluhönnuður** til að opna skjámyndina **Formúluhönnuður**. Skoðið formúluna sem er skilgreind fyrir tiltekinn TDS-skattkóða á þessari síðu. Lokið síðunum **Formúluhönnuður** og **Tímabundnar staðgreiðsluskattsfærslur** til að fara aftur á síðuna **Fylgiskjal færslubókar**.

8. Færið inn aðrar áskildar upplýsingar. Villuleita og bóka færslubók. TDS-upphæðin sem er reiknuð í innkaupareikningum er bókuð á lykil viðskiptaskulda. TDS-upphæðin sem reiknuð er fyrir innkaupareikninga er bókuð á lykil viðskiptakrafa sem er skilgreindur fyrir hvern TDS-skattkóða í TDS-skattflokknum. Lyklar viðskiptaskulda er viðskiptakrafa fyrir TDS-skattkóða eru skilgreindir á síðunni **Staðgreiðsluskattskóðar**.

9. Veljið **Bókaður staðgreiðsluskattur** til að opna síðuna **Staðgreiðsluskattsfærslur**. Í reitnum **Gildi** er heildarprósentan sem er notuð til að reikna út TDS fyrir færsluna sýnd.

   Reitirnir í flipunum **Yfirlit**, **Almennt** og **Upphæð** á síðunni Tímabundnar staðgreiðsluskattsfærslur sýna upplýsingar um reiknaða TDS-upphæð og leiðrétta TDS-upphæð fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.
