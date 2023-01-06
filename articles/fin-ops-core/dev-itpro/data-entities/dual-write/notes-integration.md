---
title: Samþætting athugasemdar
description: Þessi grein lýsir samþættingu athugasemdagagna í tvöfaldri skráningu.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f09d455181b7929e25d5238949a0236ac60d457b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289017"
---
# <a name="note-integration"></a>Samþætting athugasemdar

[!include [banner](../../includes/banner.md)]



Í viðskiptaferlum safna notendur Microsoft Dynamics 365 oft saman upplýsingum um viðskiptavini sína. Þessar upplýsingar eru skráðar sem verkþættir og athugasemdir. Þessi grein lýsir samþættingu athugasemdagagna í tvöfaldri skráningu.

Hægt er að flokka upplýsingar um viðskiptavin á eftirfarandi hátt:

+ **Aðgerðartengdar upplýsingar sem notandi Dynamics 365 framkvæmir fyrir hönd viðskiptavinar** – Til dæmis Contoso (notandi Dynamics 365) er að stjórna spurningakeppni. Einn af viðskiptavinum Contoso (viðskiptavinur) vill mæta á spurningakeppnina. Viðskiptavinurinn biður starfsmann Contoso að bóka pláss fyrir sig í spurningakeppninni. Bókunin á sér stað í dagatali þátttakanda fyrir viðburð Contoso.
+ **Aðgerðartengdar upplýsingar fyrir notanda Dynamics 365** – Til dæmis færir viðskiptavinur sem er að kaupa Surface-tölvu inn sérstakar upplýsingar sem gefa til kynna að pakka eigi tækinu inn í gjafapappír fyrir afhendingu. Þessar leiðbeiningar eru aðgerðartengdar upplýsingar sem starfsmaður Contoso, sem er ábyrgur fyrir pökkun, á að sjá um.
+ **Upplýsingar sem tengjast ekki aðgerð** – Til dæmis heimsækir viðskiptavinur verslun Contoso og í samtali við starfsmann verslunarinnar segist hann hafa áhuga á *Halo-leikjum* og aukabúnaði tölvuleikja. Starfsmaður verslunarinnar skrifar athugasemd varðandi þessar upplýsingar. Tillöguvél afurða notar hana þá til að senda viðskiptavini tillögur.

Almennt eru aðgerðartengdar upplýsingar sóttar sem *verkþættir* í forritum fjármála- og reksturs og forritum viðskiptavina. Upplýsingar sem tengjast ekki aðgerð eru sóttar sem *athugasemdir* í forritum fjármála- og reksturs og sem *skýringar* í forritum viðskiptavina.

> [!TIP]
> Þótt athugasemdir séu ætlaðar fyrir upplýsingar sem tengjast ekki aðgerð munu forritin ekki koma í veg fyrir að þær séu notaðar til að geyma og meðhöndla aðgerðartengdar upplýsingar ef ætlunin er að nota þær í þeim tilgangi.

Microsoft er að gefa út virkni fyrir samþættingu athugasemda. (Virkni fyrir samþættingu verkþáttar verður gefin út síðar.) Samþætting athugasemdar er í boði fyrir viðskiptavini, lánardrottna, sölupantanir og innkaupapantanir.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Búa til athugasemd í forriti viðskiptavinar

Til að búa til athugasemd í fjármála- og reksturs-forriti og því næst samstilla hana við forrit viðskiptavinar skal fylgja þessum skrefum.

1. Í forriti viðskiptavinar skal opna reikningsfærslu viðskiptavinar.
2. Á svæðinu **Tímalína** skal velja plúsmerkið (**+**) og síðan velja **Athugasemd** til að búa til athugasemd.

    ![Athugasemd búin til í forriti viðskiptavinar.](media/notes-ce-1.png)

3. Færið inn titil og lýsingu og veljið síðan **Bæta við athugasemd**.

    ![Titill og lýsing færð inn.](media/notes-ce-2.png)

    Nýja athugasemdin bætist við tímalínu viðskiptavinar.

    ![Ný athugasemd á tímalínu viðskiptavinar.](media/notes-ce-3.png)

4. Skráið ykkur inn í fjármála- og reksturs-forritið og opnið sömu viðskiptavinafærsluna. Takið eftir að hnappurinn **Viðhengi** (bréfaklemmutákn) efst í hægra horninu gefur til kynna að færslan sé með viðhengi.

    ![Tilkynning um viðhengi.](media/notes-ce-4.png)

5. Veljið hnappinn **Viðhengi** til að opna síðuna **Viðhengi**. Athugasemdin sem var búin til ætti að finnast í forriti viðskiptavinar.

    ![Athugasemd úr forriti viðskiptavinar.](media/notes-ce-5.png)

Allar uppfærslur á athugasemdinni eru samstilltar fram og til baka milli forriti fjármála- og reksturs og forrits viðskiptavinar.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Búa til athugasemd í fjármála- og reksturs-forrit

Einnig er hægt að búa til athugasemd í fjármála- og reksturs-forriti og verður hún samstillt við forrit viðskiptavinar.

Til að búa til athugasemd í fjármála- og reksturs-forriti og því næst samstilla hana við forrit viðskiptavinar skal fylgja þessum skrefum.

1. Í forriti fjármála- og reksturs, á síðunni **Viðhengi**, skal velja **Ný** \> **Athugasemd**.

    ![Athugasemd búin til í fjármála- og reksturs-forriti.](media/notes-fo-1.png)

2. Færið inn titil og leiðbeiningar í stuttu máli og veljið síðan **Vista**.

    ![Titill og leiðbeiningar færðar inn.](media/notes-fo-2.png)

3. Uppfærið færsluna í forriti viðskiptavinar. Nýja athugasemdin ætti að sjást í tímalínunni.

    ![Ný athugasemd á tímalínunni í forriti viðskiptavinar.](media/notes-fo-3.png)

Hægt er að flokka athugasemd sem annaðhvort innri eða ytri.

- Í forriti fjármála- og reksturs, á síðunni **Viðhengi**, skal opna athugasemdina og síðan í reitnum **Takmörkun** skal velja **Innri** eða **Ytri**.

    ![Takmörkunarreitur.](media/notes-fo-4.png)

Einnig er hægt að búa til vefslóð.

1. Í forriti fjármála- og reksturs, á síðunni **Viðhengi**, skal velja **Ný** \> **Vefslóð**.
2. Færið inn titil og vefslóð.
3. Í reitnum **Takmörkun** skal velja **Innri** eða **Ytri**.

    ![Vefslóð búin til í fjármála- og reksturs-forriti.](media/notes-fo-5.png)

4. Veldu **Vista**.

    Þar sem forrit viðskiptavina eru ekki með vefslóðargerð, er vefslóðin samþætt með tvöfaldri skráningu sem athugasemd.

    ![Vefslóð sem birtist sem athugasemd í forriti viðskiptavinar.](media/notes-ce-6.png)

> [!NOTE]
> Skráarviðhengi eru ekki studd.

## <a name="templates"></a>Sniðmát

Samþætting athugasemdar inniheldur safn af töfluvörpunum sem vinnur saman í gagnasamskiptum eins og sýnt er í eftirfarandi töflu.

| Forrit fjármála- og reksturs | Forrit viðskiptavinatengsla | Lýsing |
|----------------------------|-------------------------|-------------|
| [Fylgiskjöl viðskiptamanns](mapping-reference.md#230) | Skýringar | Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um viðskiptavini (bæði fyrir fyrirtæki og einstaklinga). |
| [Viðhengd skjöl lánardrottins](mapping-reference.md#231) | Skýringar | Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um lánardrottna (bæði fyrir fyrirtæki og einstaklinga). |
| [Viðhengt skjal fyrir sölupöntunarhaus](mapping-reference.md#229) | Skýringar | Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um sölupantanir. |
| [Viðhengd skjöl fyrir haus innkaupapöntunar](mapping-reference.md#232) | Skýringar | Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um innkaupapantanir. |

## <a name="limitations"></a>Takmarkanir

Þegar athugasemdalausnin hefur verið uppsett er ekki hægt að fjarlægja hana. 

Frekari upplýsingar er að finna í [Tilvísun vörpunar á tvöfaldri skráningu](mapping-reference.md).

