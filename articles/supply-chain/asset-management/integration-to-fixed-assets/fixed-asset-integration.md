---
title: Samþætta eignastýringu með eignum
description: Þetta efnisatriði útskýrir hvernig á að samþætta einingar eignastýringar og eigna til að tengja saman eignir og viðhaldseignir.
author: kamaybac
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 63ab3e772d54c7d27ade1c0cef07f275f49a143ad382fe618035117bca2cd43d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746281"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Samþætta eignastýringu með eignum

[!include [banner](../../includes/banner.md)]

Með því að samþætta einingar **Eignastýringar** og **Eigna**, geturðu tengt eignir við viðhaldseignir. Notendur eigna geta síðan búið til viðhaldseign úr nýrri eða núverandi eign og notendur eignastýringar geta tengt viðhaldseign við núverandi eign. Þessi eiginleiki gerir það einnig auðvelt fyrir notendur eigna að skoða kostnaðinn sem var bókaður úr verkbeiðnum vegna tengdra viðhaldseigna.

> [!NOTE]
> Í þessu efnisatriði vísa *viðhaldseignir* til eigna úr einingu **Eignastýringar** og *eignir* vísa til eigna úr einingunni **Eignir**.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Veldu sjálfgefna staðsetningu að eigin vali fyrir nýjar viðhaldseignir sem eru búnar til úr eignum (valfrjálst)

Þessi valfrjálsa stilling gerir þér kleift að stilla sjálfgefna staðsetningu fyrir nýjar viðhaldseignir sem eru búnar til úr eignum. Yfirleitt lýkur þú við þessa grunnstillingu í eitt sinn, ef þú lýkur við hana yfirhöfuð.

Fylgið eftirfarandi skrefum til að ljúka þessum skilgreiningum.

1. Opnaðu **Eignastýringu \> Uppsetningu \> Færibreytur eignastýringar**.
1. Veldu flipann **Eignir** á svæðinu **Virk staðsetning** og veldu sjálfgefnu staðsetninguna.
1. Í aðgerðarúðunni skal velja **Vista**.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Vinna með samþættar viðhaldseignir og eignir

Þessi hluti inniheldur safn aðferða sem sýnir ýmsar leiðir til að vinna með eiginleika samþættrar eignastýringar og eigna.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Tengja núverandi viðhaldseign við eign

Fylgdu þessum skrefum til að tengja viðhaldseign sem fyrir er við eign.

1. Opnaðu **Eignastýringu \> Eignir \> Allar eignir** (eða **Virkar eignir**).
1. Veljið eign.
1. Á flýtiflipanum **Eign** á svæðinu **Númer eignar** skal velja núverandi eign.
1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Skoða eignina sem er tengd valinni viðhaldseign

Fylgdu þessum skrefum til að skoða eignina sem er tengd valinni viðhaldseign.

1. Opnaðu **Eignastýringu \> Eignir \> Allar eignir** (eða **Virkar eignir**).
1. Veljið eign.
1. Á flýtiflipanum **Eign** á svæðinu **Númer eignar** skaltu velja tengilinn.

    Síðan **Eignir** fyrir valdar eignir er opnuð. (Yfirleitt er þessa síðu að finna undir **Eignir \> Eignir \> Eignir**.)

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Skoðaðu viðhaldseignina sem er tengd valinni eign

Fylgdu þessum skrefum til að skoða viðhaldseignina sem er tengd valinni eign.

1. Opna **Eignir \> Eignir \> Eignir**.
1. Veljið eign.
1. Veldu flipann **Eignastýring** í hópnum **Skoða** og veldu **Viðhaldseign**.

    Síðan **Viðhaldseign** verður opnuð fyrir eignina sem er tengd valinni eign. (Yfirleitt er þessa síðu að finna undir **Eignastýring \> Eignir \> Allar eignir**.)

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Skoða viðhaldskostnað sem tengist eign

Hægt er að bóka verkbeiðnir fyrir viðhaldseignir og yfirleitt fylgir kostnaður hverri slíkri verkbeiðni. Þegar eign er tengd við viðhaldseign getur þú farið beint frá eigninni til að skoða tengdan kostnað.

Fylgdu þessum skrefum til að skoð viðhaldskostnað sem tengist eign.

1. Opna **Eignir \> Eignir \> Eignir**.
1. Veljið eign.
1. Á Aðgerðasvæðinu á flipanum **Eignastýring** í flokknum **Skoða** skaltu velja **Viðhaldskostnaður**.

    Síðan **Viðhaldskostnaður** er opnuð og sýnir tengdan kostnað.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Búa til nýja viðhaldseign fyrir núverandi eign

Fylgdu þessum skrefum til að búa til nýja viðhaldseign fyrir núverandi eign.

1. Opna **Eignir \> Eignir \> Eignir**.
1. Veljið eign.
1. Veldu flipann **Eignastýring** í hópnum **Nýtt** og veldu **Búa til viðhaldseign**. (Ef þessi valkostur er ekki tiltækur gæti viðhaldseign þegar verið tengd valinni eign.)
1. Ljúktu við að búa til eignina eins og lýst er í [Búa til eign](../objects/create-an-object.md).

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Búa til nýja eign og bæta við viðhaldseign fyrir hana

Fylgdu þessum skrefum til að búa til nýja eign og bæta við nýrri viðhaldseign fyrir hana.

1. Opna **Eignir \> Eignir \> Eignir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Ljúktu við að búa til eign eins og lýst er í [Búa til eign](../../../finance/fixed-assets/tasks/create-fixed-asset.md).
1. Veldu flipann **Eignastýring** í hópnum **Nýtt** og veldu **Búa til viðhaldseign**.
1. Ljúktu við að búa til eignina eins og lýst er í [Búa til eign](../objects/create-an-object.md).

### <a name="remove-the-association-between-two-assets"></a>Fjarlægið tengslin milli tveggja eigna

Í sumum tilfellum gætirðu þurft að fjarlægja tengslin á milli viðhaldseignar og eignar hennar. Til dæmis, ef þú vilt [búa til nýja viðhaldseign](#new-maintenance-from-fixed) úr eign, verður þú fyrst að fjarlægja öll núverandi tengsl.

Fylgdu þessum skrefum til að fjarlægja núverandi tengsl milli viðhaldseignar og eignar.

1. Opnaðu **Eignastýringu \> Eignir \> Allar eignir** (eða **Virkar eignir**).
1. Finndu og opnaðu eignina.
1. Á flýtiflipanum **Eign** hreinsaðu gildið af svæðinu **Virk staðsetning**.
1. Í aðgerðarúðunni skal velja **Vista**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]