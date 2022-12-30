---
title: Aðgerðir fyrir ósamkvæmni.
description: Þessi grein lýsir því hvernig á að stofna og nota aðgerðir vegna ósamkvæmni.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2e63156dd2b230da7f1ea89e2c2006c1b4f3eeb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847992"
---
# <a name="operations-for-nonconformances"></a>Aðgerðir fyrir ósamkvæmni.

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að stofna og nota aðgerðir vegna ósamkvæmni.

Notið síðuna **Aðgerðir** til þess að skilgreina flokkun á vinnu sem hægt er að framkvæmda fyrir samþykkta ósamkvæmni. Þegar tengdri aðgerð er úthlutað á ósamkvæmni, er hægt að gefa upp upplýsingar eins og um tengt efni, vinnustundir og gjöld sem eru nauðsynleg til þess að framkvæma aðgerðina. Kerfið notar þessar upplýsingar til að reikna út áætlaðan kostnað fyrir aðgerðina. Upplýsingarnar og áætlaður kostnaður er notaður fyrir tilvísanir. Tengdar aðgerðir varðandi gæði eru öðruvísi en aðgerðir sem hægt er að skilgreina fyrir framleiðsluleið.

> [!NOTE]
> Þó hægt sé að fylgjast með kostnaði, tíma og vörum sem notaðar eru í aðgerð sem tengist ósamkvæmi, eru gögnin sem þú færir inn aðeins til upplýsinga. Hún er ekki sjálfkrafa samþætt fjárhag, undirbók birgða eða **Tími og viðvera** einingunni.

## <a name="examples-of-operations"></a>Dæmi um aðgerðir

Þú vinnur fyrir framleiđslufyrirtæki. Ósamkvæmni var stofnað og samþykkt fyrir atriði sem mistókst í gæðaprófun. Leiðrétting var gerð til að gefa til kynna að vandamálið tengdist lélegri legu í vél. Fara þarf í gegnum nokkur skref til að skipta út legunni og ábyrgðin fyrir hverja aðgerð er rakin. Til dæmis gætu eftirfarandi skref verið nauðsynleg:

1. Framleiðslulínan stöðvast og hreinsunarferlið er framkvæmt.
1. Viðgerðarmaður skiptir um leguna.
1. Starfsfólk gæðatryggingar skoðar vélina áður en kveikt er á henni á nýjan leik.

Í þessu dæmi er hægt að búa til eftirfarandi aðgerðir til að tákna það verk sem þarf að framkvæma:

- Stöðvið framleiðslulínuna.
- Hreinsaðu framleiðslulínuna.
- Framkvæmið viðhald á vél.
- Skoðið vélina.

## <a name="create-an-operation"></a>Stofna aðgerð

1. Fara í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Aðgerðir**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Aðgerð** – Færið inn einkvæmt kenni eða heiti fyrir aðgerðina.
    - **Lýsing** – Færið inn ítarlega lýsingu á aðgerðinni.
    - **Gerð** – Ef aðgerðina er aðeins hægt að nota vegna ósamkvæmni sem tengist tiltekinni gerð pöntunar skal velja pöntunargerðina (*Innkaupapöntun* eða *Sölupöntun*).

1. Lokið síðunni.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gæðastjórnunaryfirlit](quality-management-processes.md)
- [Virkja stjórnun gæða og ósamkvæmni](enable-quality-management.md)
- [Stofna og meðhöndla ósamkvæmi](tasks/create-process-non-conformance.md)
- [Starfsmenn ábyrgir fyrir samþykki ósamkvæmni](quality-responsible-workers.md)
- [Biðgeymslusvæði fyrir ósamkvæmi](quality-quarantine-zones.md)
- [Gerðir greininga fyrir ósamkvæmni](quality-diagnostic-types.md)
- [Gæðagjöld fyrir ósamkvæmi](quality-charges.md)
- [Gerðir vandamála fyrir ósamkvæmni](quality-operations.md)
- [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
