---
title: Verkflæði viðskiptavinar
description: Í þessu efnisatriði er að finna upplýsingar um verkflæði viðskiptavinar. Tilgreindum reitum fyrir viðskiptavin er breytt og breytingarnar eru síðan sendar til samþykktar með því að nota verkflæðið áður en þeim er bætt við viðskiptavininn.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8ff91a1df82d6195da266b97c347ef27afec662d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175973"
---
# <a name="customer-workflow"></a>Verkflæði viðskiptavinar

[!include [banner](../includes/banner.md)]

Verkflæði viðskiptavinar hefur verið bætt við útgáfu 8.0.4. Hægt er að breyta tilgreindum reitum fyrir viðskiptavin og senda breytingarnar síðan til samþykktar með því að nota verkflæðið áður en þeim er bætt við viðskiptavininn.

## <a name="set-up-the-customer-workflow"></a>Setja upp verkflæði viðskiptavinar

Áður en hægt er að nota eiginleikann fyrir verkflæði viðskiptavinar þarf að virkja hann.

1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
2. Á flipanum **Almennt** á flýtiflipanum **Samþykki viðskiptavinar** skal stilla valkostinn **Virkja samþykki viðskiptavinar** á **Já** til að virkja eiginleikann.
3. Í reitnum **Hegðun gagnaeiningar** skal velja þá hegðun sem gagnaeiningarnar eiga að nota þegar gögn eru flutt:

    - **Leyfa breytingar án samþykkis** – eining getur uppfært færslu viðskiptavinar án þess að vinna hana í gegnum verkflæðið.
    - **Hafna breytingum** – ekki er hægt að gera breytingar á færslu viðskiptavinar. Innflutningur mun mistakast fyrir reitina sem eru virkir fyrir verkflæðið.
    - **Búa til tillögur að breytingum** – öllum reitum verður breytt nema reitunum sem eru virkir fyrir verkflæðið. Nýju gildunum fyrir þá reiti verður bætt við viðskiptavininn sem fyrirhuguðum breytingum og verkflæðið verður ræst sjálfkrafa.

4. Í listanum yfir reiti viðskiptavinar skal velja gátreitinn **Virkja** fyrir hvern reit sem þarf að samþykkja áður en breytingarnar eru gerðar.
5. Opnið **Viðskiptakröfur \> Setja upp \> Verkflæði viðskiptakrafna**.
6. Veljið **Nýtt**.
7. Veljið **Verkflæði fyrir fyrirhugaða breytingu á viðskiptavini**. 
8. Setjið upp verkflæðið svo að það passi við samþykktarferlið. Verkflæðissamþykktareiningin **Verkflæðissamþykki fyrir fyrirhugaða breytingu á viðskiptavini** mun gera breytingarnar á viðskiptavininum.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Breyta upplýsingum um viðskiptavin og senda breytingarnar í verkflæðið

Þegar reit sem er virkur fyrir verkflæðið er breytt birtist síðan **Fyrirhugaðar breytingar**. Þessi síða sýnir upphaflegt gildi reitarins og nýja gildið sem slegið var inn. Reitnum sem var breytt er breytt aftur í upprunalegt gildi. Stöðuskilaboð á síðunni gefa til kynna að breytingarnar hafa ekki verið sendar inn.

Í hvert sinn sem reit sem er virkur fyrir verkflæðið er breytt er honum bætt á listann yfir fyrirhugaðar breytingar. Til að fleygja fyrirhuguðu gildi fyrir reit skal nota hnappinn **Fleygja** við hliðina á reitnum í listanum. Til að fleygja öllum breytingum skal nota hnappinn **Fleygja öllum breytingum** neðst á síðunni. Velja skal **Í lagi** til að loka síðunni.

Eftir að a.m.k. ein fyrirhuguð breyting hefur verið gerð birtast tvær valmyndir á aðgerðarsvæðinu: **Fyrirhugaðar breytingar** og **Verkflæði**.

1. Velja skal **Fyrirhugaðar breytingar** til að opna síðuna **Fyrirhugaðar breytingar** og skoða breytingarnar.
2. Velja skal **Verkflæði \> Senda inn** til að senda breytingarnar í verkflæðið.

    Stöðunni á síðunni er breytt í **Breytingar bíða samþykkis**.

Verkflæðið fylgir venjulegu verkflæðisferli í forritinu. Samþykktaraðila er beint á síðuna **Viðskiptavinur** þar sem hann eða hún getur yfirfarið breytingar á síðunni **Fyrirhugaðar breytingar** og síðan valið **Verkflæði \> Samþykkja** til að samþykkja verkflæðið. Þegar búið er að samþykkja allt eru reitirnir uppfærðir með gildunum sem lögð voru til.
