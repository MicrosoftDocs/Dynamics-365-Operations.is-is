---
title: Reikna út TDS-reikninga með skjámynd innkaupapöntunar eða sölupöntunar
description: Í þessu efnisatriði eru talin upp skrefin fyrir útreikning á TDS fyrir ýmsar gerðir reikninga.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 28f83b3d5aa028d819b837350fe69c2a9c9833ea
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407870"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>Reikna út TDS-reikninga með skjámynd innkaupapöntunar eða sölupöntunar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði eru talin upp skrefin fyrir útreikning á TDS fyrir ýmsar gerðir reikninga með síðunum **Innkaupapöntun**, **Innkaupabók**, **Standandi pöntun** og **Sölupöntun**.

1. Stofnið innkaupapöntun, innkaupabók, standandi innkaupapöntun eða sölupöntun með síðunni sem gefin er upp. Færið inn nauðsynlegar upplýsingar.

2. Veljið flipann **Uppsetning** til að skoða eðli skattgreiðanda fyrir lánardrottin eða viðskiptavin. Þessar upplýsingar eru taldar upp í reitnum **Eðli skattgreiðanda** undir reitahópnum **Staðgreiðsluskattsflokkur**.

3. Í reitnum **TDS-flokkur** skal skoða eða breyta sjálfgefnum TDS-flokki sem skilgreindur er fyrir lánardrottin eða viðskiptavin.

   > [!NOTE]
   > Reiturinn **TDS-flokkur** er ekki í boði þegar TDS-flokkur er valinn í reitnum **TDS-flokkur**. TDS er aðeins reiknað ef gátreiturinn **Reikna staðgreiðsluskatt** er valinn fyrir lánardrottin eða viðskiptavin á síðunni **Allir lánardrottnar** eða **Allir viðskiptavinir**.  

4. Stofnið vörulínur í flipanum **Línur** og færið inn nauðsynlegar upplýsingar.

5. Veljið flipann **Uppsetning** (línustig) til að skoða eða breyta TDS-flokknum sem skilgreindur er á hausastigi. TDS-flokkurinn birtist í reitnum **TDS-flokkur** sem er undir reitahópnum **Staðgreiðsluskattsflokkur**.

6. Veljið flipann **Skattaupplýsingar** og veljið önnur aðsetur sem eru sett upp fyrir heiti fyrirtækis sem sýnt er í þessum reit. Heiti fyrirtækis er sýnt í reitnum **Heiti** sem er undir reitahópnum **Upplýsingar um fyrirtæki**. 

   TAN fyrir valið heiti fyrirtækis er sýnt í reitnum **Skattlykilnúmer** (**TAN**) undir reitahópnum **Staðgreiðsluskattur**. 

7. Veljið **Staðgreiðsluskattur** til að opna síðuna **Tímabundnar staðgreiðsluskattsfærslur**. Skoðið eftirfarandi reiti í efri rúðunni á síðunni **Tímabundnar staðgreiðsluskattsfærslur**.

   - **Upphæð** **skatta** **upphæðar** **í** **alls** - Samtals TDS reiknað út fyrir færsluna fyrir TDS-flokkinn.

   - **Gildi** - Heildarprósenta notuð til að reikna út TDS fyrir færsluna. Heildarprósentan er byggð á formúlunni sem er skilgreind fyrir TDS-skattkóða sem hengdir eru við TDS-flokkinn.

   - **Samtals leiðrétt upphæð staðgreiðsluskatts** - Leiðrétt heildarupphæð TDS fyrir alla skattkóða í TDS-flokknum.

   - **TDS** - Ef valið er TDS-flokkur hengdur við færsluna.

Reitirnir í flipunum **Yfirlit**, **Almennt** og **Leiðrétting** á síðunni **Tímabundnar staðgreiðsluskattsfærslur** sýna upplýsingar um reiknaða TDS-upphæð og leiðrétta TDS-upphæð fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.

8. Veljið **Mörk** til að opna síðuna **Mörk**. Skoðið mörkin sem skilgreind eru fyrir TDS-skattþáttinn sem hengdur er við tiltekinn TDS-skattkóða á þessari síðu.

9. Veljið **Formúluhönnuður** til að opna síðuna **Formúluhönnuður**. Skoðið formúluna sem er skilgreind fyrir tiltekinn TDS-skattkóða á þessari síðu. 

10. Senda reikninginn. TDS-upphæðin sem reiknuð er fyrir innkaupareikninga er bókuð á lykil viðskiptaskulda og TDS-upphæðin sem reiknuð er fyrir sölureikninga er bókuð á lykil viðskiptakrafa sem er skilgreindur fyrir hvern TDS-skattkóða í TDS-skattflokknum. Lyklar viðskiptaskulda er viðskiptakrafa fyrir TDS-skattkóða eru skilgreindir á síðunni **Staðgreiðsluskattskóðar**.

11. Veljið hnappinn **Fyrirspurn** hnappinn **> Reikningur > Bókaður staðgreiðsluskattur** til að opna síðuna **Staðgreiðsluskattsfærslur**. Þú getur skoðað heildarprósentuna sem notuð er til að reikna út TDS fyrir viðskiptin í reitnum **Gildi**

Reitirnir í flipanum **Yfirlit**, **Almennt** og **Upphæð** á síðunni **Staðgreiðsluskattsfærslur** sýna upplýsingar um útreikning TDS fyrir færsluna. Skoðið upplýsingar um útreikning TDS fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.
