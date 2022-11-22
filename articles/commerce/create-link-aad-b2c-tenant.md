---
title: Búðu til eða tengdu við núverandi Azure AD B2C leigjandi í Azure gáttinni
description: Þessi grein lýsir því hvernig búa til eða tengja við núverandi Azure Active Directory (Azure AD) leigjanda frá fyrirtæki til neytenda (B2C) í Microsoft Azure gátt.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785815"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Búðu til eða tengdu við núverandi Azure AD B2C leigjandi í Azure gáttinni

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig búa til eða tengja við Azure Active Directory (Azure AD) leigjanda frá fyrirtæki til neytenda (B2C) í Microsoft Azure gátt. Fyrir frekari upplýsingar, sjá [Kennsla: Búðu til Azure Active Directory B2C leigjandi](/azure/active-directory-b2c/tutorial-create-tenant).

Til að búa til eða tengja við núverandi Azure AD B2C leigjandi í Azure gáttinni, fylgdu þessum skrefum.

1. Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).
1. Úr Azure-vefsíðugáttinni velurðu **Stofna tilföng**. Athugaðu að nota áskriftina og skrána sem verða tengd Commerce-umhverfi þínu.

    ![Búðu til tilföng í Azure-gátt.](./media/B2CImage_1.png)

1. Farðu í **Auðkenni \> Azure Active Directory B2C**.
1. Þegar þú ert á síðunni **Stofna nýjan B2C leigjanda eða tengil á núverandi leigjanda** notarðu einn af valkostunum hér að neðan sem best hentar þörfum fyrirtækisins þíns:

    - **Búðu til nýtt Azure AD B2C leigjandi** : Notaðu þennan valkost til að búa til nýtt Azure AD B2C leigjandi.
        1. Veldu **Stofna nýjan Azure AD B2C-leigjanda**.
        1. Undir **Heiti fyrirtækisins** slærðu inn heiti fyrirtækisins.
        1. Undir **Upphaflegt lén** slærðu inn upphaflegt lén.
        1. Fyrir **Land eða svæði** velurðu landið eða svæðið.
        1. Veldu **Stofna** til að stofna leigjanda.

     ![Stofna nýjan Azure AD-leigjanda.](./media/B2CImage_2.png)

     - **Tengja fyrirliggjandi Azure AD B2C leigjandi við Azure áskriftina mína**: Notaðu þennan valkost ef þú ert þegar með Azure AD B2C leigjanda sem þú vilt tengjast.
        1. Veldu **Tengja núverandi Azure AD B2C leigjandi við Azure áskriftina mína**.
        1. Fyrir **Azure AD B2C leigjandi**, veldu viðeigandi B2C leigjanda. Ef skilaboðin „Engir hæfir B2C leigjendur fundust“ birtast í valröðinni, þá ert þú ekki með núverandi gjaldgengan B2C leigjanda og verður að búa til nýjan.
        1. Fyrir **Tilfangaflokkur**, veldu **Stofna nýtt**. Sláðu inn **Heiti** fyrir tilfangaflokkinn sem mun innihalda leigjandann, veldu **Staðsetning tilfangaflokks** og veldu síðan **Stofna**.

    ![Tengja núverandi Azure AD B2C leigjandi við Azure áskrift.](./media/B2CImage_3.png)

1. Þegar nýja Azure AD B2C skráin er búin til (þetta getur tekið smá stund), tengill á nýju skráasafnið birtist á yfirlitinu. Þessi hlekkur mun vísa þér á síðuna „Velkomin/n í Azure Active Directory B2C“.

    ![Tengill á nýtt Azure AD Skrá](./media/B2CImage_4.png)

> [!NOTE]
> Ef þú ert með margar áskriftir á Azure reikningnum þínum eða hefur sett upp leigjanda B2C án þess að tengjast virkri áskrift mun borði með **Úrræðaleit** vísa þér til að tengja leigjanda við áskrift. Veldu úrræðaleit og fylgdu leiðbeiningunum til að leysa áskriftarmálið.

Eftirfarandi mynd sýnir dæmi um borða með Azure AD B2C **Úrræðaleit**.

![Viðvörun sem sýnir skráarsafn hefur enga virka áskrift.](./media/B2CImage_5.png)

## <a name="next-steps"></a>Næstu skref

Til að halda áfram ferlinu við að setja upp B2C leigjanda í Commerce skaltu halda áfram að [Búðu til B2C forritið](create-b2c-app.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2C-leigjanda í Commerce](set-up-b2c-tenant.md)

[Stofna B2C forrit](create-b2c-app.md)

[Stofna notandaflæðisstefnu](create-user-flow-policies.md)

[Bæta við kennitöluveitendum (valfrjálst)](add-social-identity-providers.md)

[Uppfærðu höfuðstöðvar viðskipta með nýju Azure AD B2C upplýsingar](update-hq-aad-b2c-info.md)

[Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði](config-b2c-tenant-site-builder.md)

[Frekari B2C upplýsingar](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
