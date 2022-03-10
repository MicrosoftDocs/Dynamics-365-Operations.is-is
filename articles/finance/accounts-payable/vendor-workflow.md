---
title: Verkflæði lánardrottins
description: Breyta lánardrottnaupplýsingum og nota verkflæði til að samþykkja þær.
author: sunfzam
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 48d81c727de29a285e5e33672e8f6d2eccef6249
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753923"
---
# <a name="vendor-workflow"></a>Verkflæði lánardrottins

[!include [banner](../includes/banner.md)]

Þegar verkflæði lánardrottins er notað eru breytingar sem gerðar eru á tilteknum reitum sendar í verkflæðið til samþykktar áður en þeim er bætt við lánardrottin.

## <a name="set-up-the-vendor-workflow"></a>Setja upp verkflæði lánardrottins

Áður en hægt er að nota eiginleikann fyrir verkflæði þarf að virkja hann.

1. Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.
2. Á flipanum **Almennt** á flýtiflipanum **Samþykki lánardrottins** skal stilla valkostinn **Virkja samþykki lánardrottins** á **Já**.
3. Í reitnum **Hegðun gagnaeiningar** skal velja þá hegðun sem á að nota þegar gögn eru flutt:

    - **Leyfa breytingar án samþykkis** – gagnaeiningin getur uppfært færslu lánardrottins án þess að vinna hana í gegnum verkflæðið.
    - **Hafna breytingum** – ekki er hægt að gera breytingar á færslu lánardrottins. Innflutningur mun mistakast fyrir reitina sem eru virkir fyrir verkflæðið.
    - **Búa til tillögur að breytingum** – öllum reitum verður breytt nema reitunum sem eru virkir fyrir verkflæðið. Nýju gildunum fyrir þá reiti verður bætt við lánardrottin sem fyrirhuguðum breytingum og verkflæðið verður ræst sjálfkrafa.

4. Í listanum yfir reiti lánardrottins skal velja gátreitinn **Virkja** fyrir hvern reit sem þarf að samþykkja áður en breytingarnar eru gerðar.
5. Farðu í **Viðskiptaskuldir \> Uppsetning \> Verkflæði viðskiptaskulda**.
6. Velja **Nýja**.
7. Veldu **Verkflæði fyrir fyrirhugaðar breytingar**. 
8. Setjið upp verkflæðið svo að það passi við samþykktarferlið. Verkflæðissamþykktareiningin **Verkflæðissamþykki fyrir fyrirhugaða breytingu á lánardrottni** mun gera breytingarnar á lánardrottni.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Breyta upplýsingum um lánardrottin og senda breytingarnar í verkflæðið

Þegar reit sem er virkur fyrir verkflæðið er breytt birtist síðan **Fyrirhugaðar breytingar**. Þessi síða sýnir upphaflegt gildi reitarins og nýja gildið sem slegið var inn. Reitnum sem var breytt er breytt aftur í upprunalegt gildi. Stöðuskilaboð gefa einnig til kynna að breytingarnar hafa ekki verið sendar inn. 

Í hvert sinn sem reit sem er virkur fyrir verkflæðið er breytt er honum bætt á listann á síðunni **Fyrirhugaðar breytingar**. Til að fleygja fyrirhuguðu gildi fyrir reit skal nota hnappinn **Fleygja** við hliðina á reitnum í listanum. Til að fleygja öllum breytingum skal nota hnappinn **Fleygja öllum breytingum** neðst á síðunni. Velja skal **Í lagi** til að loka síðunni.

Eftir að a.m.k. ein fyrirhuguð breyting hefur verið gerð birtast tveir flipar í viðbót á aðgerðarsvæðinu: **Fyrirhugaðar breytingar** og **Verkflæði**.

1. Velja skal **Fyrirhugaðar breytingar** til að opna síðuna **Fyrirhugaðar breytingar** og skoða breytingarnar.
2. Velja skal **Verkflæði \> Senda inn til að senda breytingarnar í verkflæði**.

    Stöðunni á síðunni er breytt í **Breytingar bíða samþykkis**.

Verkflæðið fylgir venjulegu verkflæðisferli. Samþykktaraðila er beint á síðuna **Lánardrottinn** þar sem hægt er að fara yfir breytingar á síðunni **Fyrirhugaðar breytingar** og velja síðan **Verkflæði \> Samþykkja** til að samþykkja verkflæðið. Þegar búið er að samþykkja allt eru reitirnir uppfærðir með gildunum sem lögð voru til.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
