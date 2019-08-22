---
title: Verkflæði lánardrottins
description: Breyta lánardrottnaupplýsingum og nota verkflæði til að samþykkja þær.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 112f9d6adeee583a63da8ab700d7adc179de2c1d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835311"
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

Verkflæðið fylgir venjulegu verkflæðisferli í Microsoft Dynamics 365 for Finance and Operations. Samþykktaraðila er beint á síðuna **Lánardrottinn** þar sem hann eða hún getur yfirfarið breytingar á síðunni **Fyrirhugaðar breytingar** og síðan valið **Verkflæði \> Samþykkja** til að samþykkja verkflæðið. Þegar búið er að samþykkja allt eru reitirnir uppfærðir með gildunum sem lögð voru til.
