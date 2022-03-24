---
title: TDS-útreikningur á greiðslum og eigin víxlum
description: Í þessu efnisatriði eru veittar tilvísunarupplýsingar um mismunandi greiðslufærslur sem skattur dreginn frá upprunalegri greiðslu (TDS) er reiknaður fyrir.
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
ms.openlocfilehash: d5c9822c2e4f71fb89776d1c1c76056bad85d484
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407662"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>TDS-útreikningur á greiðslum og eigin víxlum

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði eru veittar tilvísunarupplýsingar um mismunandi greiðslufærslur sem skattur dreginn frá upprunalegri greiðslu (TDS) er reiknaður fyrir.

| Raðnúmer | Færslugerð | Færsluupphæð | Síðuheiti og slóð | Gerð lykils og gerð mótlykils |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Fyrirframgreiðsla/Greiðsla á móti reikningi (TDS til greiðslu) | Debet- eða kreditkort | <ul><li>Almenn færslubók (**Fjárhagur \> Færslubókarfærslur \> Almennar færslubækur**)</li><li>Reikningabók (**Viðskiptaskuldir \> Reikningar \> Reikningabók**)</li><li>Greiðslubók (**Viðskiptaskuldir \> Greiðslur \> Greiðslubók lánardrottins**)</li></ul> | Lánardrottinn (Dr.), banki (Cr.) |
| 2             | Fyrirframgreiðsla/Greiðsla á móti reikningi (innkaup gerð af viðskiptavini – TDS til greiðslu) | Debet- eða kreditkort | <ul><li>Almenn færslubók (**Fjárhagur \> Færslubókarfærslur \> Almennar færslubækur**)</li><li>Reikningabók (**Viðskiptaskuldir \> Reikningar \> Reikningabók**)</li><li>Greiðslubók (**Viðskiptaskuldir \> Greiðslur \> Greiðslubók lánardrottins**)</li></ul> | Viðskiptavinur (Dr.), banki (Cr.) |
| 3             | Eigin víxlar | Debet | Gefa út eigin víxilbók (**Viðskiptaskuldir \> Greiðslur \> Eigin víxlar \> Gefa út eigin víxilbók**) | Lánardrottinn (Dr.), fjárhagur (Cr.) |
| 4             | Ýmsar tekjur (TDS til innheimtu) | Debet- eða kreditkort | Almenn færslubók (**Fjárhagur \> Færslubókarfærslur \> Almennar færslubækur**) | Banki (Dr.), fjárhagur (Cr.) |
| 5             | Önnur útgjöld (TDS til greiðslu) | Debet- eða kreditkort | Almenn færslubók (**Fjárhagur \> Færslubókarfærslur \> Almennar færslubækur**) | Banki (Dr.), fjárhagur (Cr.) |

Fylgið þessum skrefum til að reikna út TDS fyrir greiðslur og eigin víxla.

1. Á færslubókarsíðunni skal stofna færslubókarlínur. Veljið gerð lykils og gerð mótlykils.
2. Veljið **Aðgeðrir \> Uppgjör** til að opna síðuna **Breytingar á opnum færslum**. Veljið siðan tiltekinn reikning sem þarf að gera upp. Ef TDS hefur þegar verið reiknað á reikningsstigi sýnir reiturinn **Uppruni upphæðar** grunnupphæðina sem TDS var reiknað fyrir. Reiturinn **TDS-upphæð** sýnir TDS-upphæðina sem var reiknuð fyrir færsluna. Reiturinn **Upphæð** sýnir nettóupphæð greiðslu (þ.e. greiðsluupphæðina eftir að TDS hefur verið dregið frá).

    > [!NOTE]
    > Fyrir greiðslu sem var gerð vegna reiknings eiga eftirfarandi skilyrði við:
    >
    > - Ef greiðsluupphæðin og reikningsupphæðin er sú sama er TDS ekki reiknað ef það hefur þegar verið reiknað á reikningsstigi.
    > - Ef reikningsupphæðin eftir að TDS upphæðin er dregin frá er hærri en greiðsluupphæðin er TDS ekki reiknað.
    > - Ef reikningsupphæðin eftir að TDS-upphæðin er dregin frá er lægri en greiðsluupphæðin er TDS reiknað fyrir upphæðina sem fyrir yfir reikningsupphæðina.

3. Á síðunni **Fylgiskjal færslubókar**, í flipanum **Yfirlit**, í reitnum **TDS-flokkar**, skal yfirfara eða beryta sjálfgefnum TDS-flokki sem er skilgreindur fyrir lánardrottin eða viðskiptavin. TDS sem er reiknað fyrir færslubókarlínur byggir á formúlunni sem er skilgreind fyrir TDS-skattkóðana í TDS-flokknum.

    > [!NOTE]
    > TDS er aðeins reiknað ef valkosturinn **Reikna staðgreiðsluskatt** er stilltur á **Já** fyrir lánardrottin á síðunni **Lánardrottnar**.

4. Í flipanum **Skattaupplýsingar**, í hlutanum **Upplýsingar um fyrirtæki**, í reitnum **Heiti**, er hægt að velja heiti fyrirtækis fyrir aukaaðsetur sem eru sett upp fyrir fyrirtækið.

    Í hlutanum **Staðgreiðsluskattur** sýnir reiturinn **Eðli skattgreiðanda** eðli skattgreiðendaflokks lánardrottins eða viðskiptavinar. Reiturinn **Skattlykilnúmer (TAN)** sýnir skattlykilnúmer (TAN) fyrir valið fyrirtæki.

5. Veljið **Hnapp staðgreiðsluskatts \> staðgreiðsluskattur** til að opna síðuna **Tímabundnar staðgreiðsluskattsfærslur**. Efri hluti þessarar síðu hefur eftirfarandi reiti:

    - **Upphæð staðgreiðsluskatts samtals** - Samtals TDS sem var reiknað út fyrir færsluna fyrir TDS-flokkinn.
    - **Gildi** - Heildarprósenta sem var notuð til að reikna út TDS fyrir færsluna. Heildarprósentan er byggð á formúlunni sem er skilgreind fyrir TDS-skattkóða og hengd við TDS-flokkinn.
    - **Samtals leiðrétt upphæð staðgreiðsluskatts** – Leiðrétt heildarupphæð TDS fyrir alla skattkóða í TDS-flokknum.
    - **TDS** – Valinn gátreitur gefur til kynna að TDS-flokkurinn er hengdur við færsluna.

    Reitirnir í flipunum **Yfirlit**, **Almennt** og **Leiðrétting** sýna reiknaða upphæð TDS og upplýsingar um leiðrétta TDS-upphæð fyrir hvern TDS-skattkóða sem er hengdur við TDS-flokkinn.

6. Veljið **Mörk** til að opna síðuna **Mörk** þar sem hægt er að fara yfir hámarkið sem er skilgreint fyrir TDS-skatthluta sem er hengdur við tiltekinn TDS-skattkóða.
7. Veldu **Formúluhönnuður** til að opna síðuna **Formúluhönnuður** þar sem hægt er að fara yfir formúluna sem er skilgreind fyrir tiltekinn TDS-skattkóða.
8. Lokið síðunum **Formúluhönnuður** og **Tímabundnar staðgreiðsluskattsfærslur** til að fara aftur á síðuna **Fylgiskjal færslubókar**.
9. Villuleita og bóka færslubók. TDS-upphæðin sem var reiknuð er bókuð á lykil viðskiptaskulda sem er skilgreindur fyrir hvern TDS-skattkóða í TDS-flokknum. Lyklar viðskiptakrafa fyrir TDS-skattkóða eru skilgreindir á síðunni **Staðgreiðsluskattskóðar**.
10. Veljið **Bókaður staðgreiðsluskattur** til að opna síðuna **Staðgreiðsluskattsfærslur**. Reiturinn **Gildi** sýnir heildarprósentuna sem var notuð til að reikna út TDS fyrir færsluna.

    Reitirnir í flipunum **Yfirlit**, **Almennt** og **Upphæð** sýna TDS-upphæðirnar sem voru reiknaðar fyrir TDS-flokkinn sem hengdur er við færsluna.

11. Farið yfir upplýsingar um útreikning TDS fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.

## <a name="generate-payments"></a>Búa til greiðslur

Til að búa til greiðslur skal fylgja þessum skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Farið í **Viðskiptaskuldir \> Greiðslur \> Greiðslubók lánardrottins**.
    - Farið í **Viðskiptakröfur \> Greiðslur \> Greiðslubók viðskiptavinar**.
    - Farið í **Viðskiptaskuldir \> Greiðslur \> Eigin víxlar \> Gefa út eigin víxilbók**.
    - Farið í **Viðskiptakröfur \> Greiðslur \> Víxill \> Gefa út víxlabók**.
    - Farið í **Viðskiptakröfur \> Greiðslur \> Víxill \> Gefa aftur út víxlabók**.

2. Veldu **Línur**.
3. Veljið **Aðgerðir \> Búa til greiðslur**.
