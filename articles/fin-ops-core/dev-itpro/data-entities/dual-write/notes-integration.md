---
title: Samþætting athugasemdar
description: Í þessu efnisatriði er lýst samþættingu athugasemdagagna í tvöfaldri skráningu.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ed068f4264269334babec9acd59d9d58551333b4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018387"
---
# <a name="note-integration"></a>Samþætting athugasemdar

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í viðskiptaferlum safna notendur Microsoft Dynamics 365 oft saman upplýsingum um viðskiptavini sína. Þessar upplýsingar eru skráðar sem verkþættir og athugasemdir. Í þessu efnisatriði er lýst samþættingu athugasemdagagna í tvöfaldri skráningu.

Hægt er að flokka upplýsingar um viðskiptavin á eftirfarandi hátt:

+ **Aðgerðartengdar upplýsingar sem notandi Dynamics 365 framkvæmir fyrir hönd viðskiptavinar** – Til dæmis Contoso (notandi Dynamics 365) er að stjórna spurningakeppni. Einn af viðskiptavinum Contoso (viðskiptavinur) vill mæta á spurningakeppnina. Viðskiptavinurinn biður starfsmann Contoso að bóka pláss fyrir sig í spurningakeppninni. Bókunin á sér stað í dagatali þátttakanda fyrir viðburð Contoso.
+ **Aðgerðartengdar upplýsingar fyrir notanda Dynamics 365** – Til dæmis færir viðskiptavinur sem er að kaupa Surface-tölvu inn sérstakar upplýsingar sem gefa til kynna að pakka eigi tækinu inn í gjafapappír fyrir afhendingu. Þessar leiðbeiningar eru aðgerðartengdar upplýsingar sem starfsmaður Contoso, sem er ábyrgur fyrir pökkun, á að sjá um.
+ **Upplýsingar sem tengjast ekki aðgerð** – Til dæmis heimsækir viðskiptavinur verslun Contoso og í samtali við starfsmann verslunarinnar segist hann hafa áhuga á *Halo-leikjum* og aukabúnaði tölvuleikja. Starfsmaður verslunarinnar skrifar athugasemd varðandi þessar upplýsingar. Tillöguvél afurða notar hana þá til að senda viðskiptavini tillögur.

Almennt eru aðgerðartengdar upplýsingar sóttar sem *verkþættir* í Finance and Operations-forritum og forritum viðskiptavina. Upplýsingar sem tengjast ekki aðgerð eru sóttar sem *athugasemdir* í Finance and Operations-forritum og sem *skýringar* í forritum viðskiptavina.

> [!TIP]
> Þótt athugasemdir séu ætlaðar fyrir upplýsingar sem tengjast ekki aðgerð munu forritin ekki koma í veg fyrir að þær séu notaðar til að geyma og meðhöndla aðgerðartengdar upplýsingar ef ætlunin er að nota þær í þeim tilgangi.

Microsoft er að gefa út virkni fyrir samþættingu athugasemda. (Virkni fyrir samþættingu verkþáttar verður gefin út síðar.) Samþætting athugasemdar er í boði fyrir viðskiptavini, lánardrottna, sölupantanir og innkaupapantanir.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Búa til athugasemd í forriti viðskiptavinar

Til að búa til athugasemd í forriti viðskiptavinar og því næst samstilla hana við Finance and Operations-forrit skal fylgja þessum skrefum.

1. Í forriti viðskiptavinar skal opna reikningsfærslu viðskiptavinar.
2. Á svæðinu **Tímalína** skal velja plúsmerkið (**+**) og síðan velja **Athugasemd** til að búa til athugasemd.

    ![Athugasemd búin til í forriti viðskiptavinar](media/notes-ce-1.png)

3. Færið inn titil og lýsingu og veljið síðan **Bæta við athugasemd**.

    ![Titill og lýsing færð inn](media/notes-ce-2.png)

    Nýja athugasemdin bætist við tímalínu viðskiptavinar.

    ![Ný athugasemd á tímalínu viðskiptavinar](media/notes-ce-3.png)

4. Skráið ykkur inn í Finance and Operations-forritið og opnið sömu viðskiptavinafærsluna. Takið eftir að hnappurinn **Viðhengi** (bréfaklemmutákn) efst í hægra horninu gefur til kynna að færslan sé með viðhengi.

    ![Tilkynning um viðhengi](media/notes-ce-4.png)

5. Veljið hnappinn **Viðhengi** til að opna síðuna **Viðhengi**. Athugasemdin sem var búin til ætti að finnast í forriti viðskiptavinar.

    ![Athugasemd úr forriti viðskiptavinar](media/notes-ce-5.png)

Allar uppfærslur á athugasemdinni eru samstilltar fram og til baka milli Finance and Operations-forritsins og forrits viðskiptavinar.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Búa til athugasemd í Finance and Operations forriti

Einnig er hægt að búa til athugasemd í Finance and Operations-forriti og verður hún samstillt við forrit viðskiptavinar.

Til að búa til athugasemd í Finance and Operations-forriti og því næst samstilla hana við forrit viðskiptavinar skal fylgja þessum skrefum.

1. Í Finance and Operations-forritinu, á síðunni **Viðhengi**, skal velja **Ný** \> **Athugasemd**.

    ![Athugasemd búin til í Finance and Operations-forritinu](media/notes-fo-1.png)

2. Færið inn titil og leiðbeiningar í stuttu máli og veljið síðan **Vista**.

    ![Titill og leiðbeiningar færðar inn](media/notes-fo-2.png)

3. Uppfærið færsluna í forriti viðskiptavinar. Nýja athugasemdin ætti að sjást í tímalínunni.

    ![Ný athugasemd á tímalínunni í forriti viðskiptavinar](media/notes-fo-3.png)

Hægt er að flokka athugasemd sem annaðhvort innri eða ytri.

- Í Finance and Operations-forritinu, á síðunni **Viðhengi**, skal opna athugasemdina og síðan í reitnum **Takmörkun** skal velja **Innri** eða **Ytri**.

    ![Takmörkunarreitur](media/notes-fo-4.png)

Einnig er hægt að búa til vefslóð.

1. Í Finance and Operations-forritinu, á síðunni **Viðhengi**, skal velja **Ný** \> **Vefslóð**.
2. Færið inn titil og vefslóð.
3. Í reitnum **Takmörkun** skal velja **Innri** eða **Ytri**.

    ![Vefslóð búin til í Finance and Operations-forritinu](media/notes-fo-5.png)

4. Veljið **Vista**.

    Þar sem forrit viðskiptavina eru ekki með vefslóðargerð, er vefslóðin samþætt með tvöfaldri skráningu sem athugasemd.

    ![Vefslóð sem birtist sem athugasemd í forriti viðskiptavinar](media/notes-ce-6.png)

> [!NOTE]
> Skráarviðhengi eru ekki studd.

## <a name="templates"></a>Sniðmát

Samþætting athugasemdar inniheldur safn af töfluvörpunum sem vinnur saman í gagnasamskiptum eins og sýnt er í eftirfarandi töflu.

| Finance and Operations-forritið | Forrit viðskiptavinatengsla | lýsing |
|----------------------------|-------------------------|-------------|
| [Fylgiskjöl viðskiptamanns](mapping-reference.md#230) | Skýringar | Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um viðskiptavini (bæði fyrir fyrirtæki og einstaklinga). |
| [Viðhengd skjöl lánardrottins](mapping-reference.md#231) | Skýringar | Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um lánardrottna (bæði fyrir fyrirtæki og einstaklinga). |
| [Viðhengt skjal fyrir sölupöntunarhaus](mapping-reference.md#229) | Skýringar | Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um sölupantanir. |
| [Viðhengd skjöl fyrir haus innkaupapöntunar](mapping-reference.md#232) | Skýringar | Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um innkaupapantanir. |

Frekari upplýsingar er að finna í [Tilvísun vörpunar á tvöfaldri skráningu](mapping-reference.md).
