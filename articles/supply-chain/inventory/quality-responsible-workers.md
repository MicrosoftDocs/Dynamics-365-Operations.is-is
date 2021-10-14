---
title: Starfsmenn ábyrgir fyrir samþykki ósamkvæmni
description: Í þessu efnisatriði er lýst hvernig á að skilgreina starfsmenn sem bera ábyrgð á að samþykkja ósamkvæm atriði.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fd1c7c86ac8627bd332bc578e98b4d7f091cdc8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575897"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Starfsmenn ábyrgir fyrir samþykki ósamkvæmni

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig á að skilgreina starfsmenn sem bera ábyrgð á að samþykkja ósamkvæm atriði.

Samþykkja verður ósamkvæmni áður en notendur geta byrjað að færa inn upplýsingar á borð við leiðréttingar eða aðgerðir. Áður en notendur geta samþykkt eða hafnað ósamkvæmni verður að tengja notandakenni (notandafærslu) þeirra við starfsmannaskrá. Þú getur valið að velja starfskrafta sem bera ábyrgð á gæðum og leyfa síðan einum starfsmanni að samþykkja vinnu fyrir hönd annars starfsmanns.

## <a name="enable-a-user-for-nonconformance-processing"></a>Virkja notanda fyrir úrvinnslu ósamkvæmni

Áður en notandi getur samþykkt eða hafnað ósamkvæmni þarftu að tengja notanafærslu þeirra við starfsmannaskrá. Síðan er hægt að stilla samþykkissvæðin sjálfvirkt og fylla út núverandi notanda sjálfkrafa fyrir vinnukortið. Áður en notandi getur notað athugasemdir skjals þarftu að virkja skjalameðhöndlun í valkostum notanda.

1. Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.
1. Finnið og opnið notandann sem á að geta samþykkt eða hafnað ósamkvæmni.
1. Stillið reitinn **Einstaklingur** á heiti starfsmannsins sem tengist núgildandi notandafærslu.
1. Á aðgerðasvæðinu skal velja **Valkostir notanda**.
1. Á síðunni **Valkostir** fyrir núverandi færslu notanda, í flipanum **Kjörstillingar**, skal stilla valkostinn **Virkja skjalameðhöndlun** á *Já*.
1. Lokaðu síðunum.

## <a name="define-workers-that-are-responsible-for-quality"></a>Skilgreina starfskrafta sem bera ábyrgð á gæðum

1. Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Starfsmenn ábyrgir fyrir gæðum**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í reitnum **Starfskraftur** skal velja starfsmanninn sem slær inn gæðaupplýsingarnar.
4. Í retinum **Ábyrgur starfsmaður** skal velja starfsmanninn sem valinn starfsmaður slær inn vinnu fyrir. Þegar ósamkvæmni er búin til og uppfærð mun þessi starfsmaður vera sleginn inn sjálfgefið í reitinn **Starfskraftur**.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gæðastjórnunaryfirlit](quality-management-processes.md)
- [Virkja stjórnun gæða og ósamkvæmni](enable-quality-management.md)
- [Gæðagjöld](quality-charges.md)
- [Biðgeymslusvæði fyrir ósamkvæmi](quality-quarantine-zones.md)
- [Gerðir greininga fyrir ósamkvæmni](quality-diagnostic-types.md)
- [Gæðagjöld fyrir ósamkvæmi](quality-charges.md)
- [Aðgerðir fyrir ósamkvæmni.](quality-operations.md)
- [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
