---
title: Grunnstilla færibreytur Human Resources
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp fyrirtækjaháðar færibreytur í Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 24d30aa06805b530cc069be0517279a11dff9ed4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356537"
---
# <a name="configure-human-resources-parameters"></a>Grunnstilla færibreytur Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Stillingar fyrir sumar færibreytur Mannauðs eru eins milli fyrirtækja, á meðan stillingar annara færibreyta eru bundnar tilteknu fyrirtæki. Í þessu efnisatriði er útskýrt hvernig á að setja upp færibreytur fyrir mannauð.

Tvær síður eru notaðar til að setja upp færibreytur mannauðs. Fyrir Færibreytur sem fyrirtæki samnýta, notarðu **samnýttar færibreytur fyrir mannauð** síðu. Fyrir færibreytur sem eru bundin tilteknu fyrirtæki (með öðrum orðum, stillingar eiga við um eitt fyrirtæki), notarðu **færibreytum mannauðs** síðu.

![Opna færibreytur Human Resources.](./media/hr-employee-self-service-human-resources-parameters.png)

Á **færibreytur Mannauðs** síða, er stillingum deild á sex flipa:

- **Almennt**
- **Ráðning** (Þessi flipi er ekki tekinn með í Dynamics 365 Human Resources)
- **Laun**
- **Númeraraðir**
- **FMLA**
- **Sjálfsafgreiðsla starfsmanns**
- **Sjálfsafgreiðsla stjórnanda**
- **Fríðindastjórnun**
- **Leyfi og fjarvera**
- **Greiðsluhættir**

Hver flipi inniheldur upplýsingar sem tengjast einu fyrirtæki.

## <a name="general"></a>Almennt

Stillingar á í **Almennt** flipanum skilgreina útlit hvers upplýsinga um fjarvistir, meiðsla og veikinda og nýráðningar. Stillingar á þessum flipa skilgreina einnig sumar sjálfgefnar færslur sem birtast meðfram vinnu. Þessi flipi gerir þér kelift að:

- Veljið lit til að hafa á opnum fjarvistafærslum.
- Tilgreinið stílblað sem nota á fyrir skýrslur.
- Virkja samþættingu milli þjálfunarnámskeiða og fjarvistaskráningar.
- Veljið fjarvistarkóðann sem er notaður til að hafa stjórna þessari samþættingu.
- Tilgreinið hversu lengi á að geyma tilfelli meiðsla og veikinda.
- Tilgreinið sjálfgefna auðkennisnúmerið sem birtist þegar nýr starfskraftur er ráðinn.
- Tilgreinið dagsetninguna sem er notuð til að reikna út þjónustu í árum. 

![Almennt flipi.](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Ráðning

Stillingarnar í flipanum **Ráðning** skilgreina skjalagerðir sem eru notaðar fyrir samskipti sem send eru sjálfkrafa til umsækjenda. Einnig er hægt að tilgreina ráðningarverk sem er notað fyrir lánardrottinsumsækjendur.

Tímabilið sem er skilgreint fyrir aldursgreiningu ráðningarverks ákvarðar ráðningarverk sem eru innifalin í reitnum **Aldursgreiningarverk** á vinnusvæðinu **Umsjón með ráðningum**. Tímabilið sem er skilgreint fyrir viðvörun lokafrests umsóknar er notað til að birta ráðningarverk sem eru að nálgast skilafrest sinn á í **skilafrestur umsóknar nálgast** reit í **Ráðningarverk** vinnusvæði.

Frekari upplýsingar um ráðningar er að finna í [Ráða umsækjendur](hr-personnel-recruit.md).

## <a name="compensation"></a>Laun

Í Dynamics 365 Finance skilgreina stillingar á **Laun** flipanum hvort notendur verða staðfesta að þeir vilji að vista upplýsingar fyrir fast eða breytilegt launafyrirkomulag. Ef **Virkja villuleit vistunar** er valið þegar notendur loka síðu sem tengist launum þar sem spurt er hvort þeir vilji vista færsluna. Sumar síður í lausnastjórnun leyfa ekki notendum að eyða upplýsingum. Með því að senda kvaðningu til notenda til að staðfesta að þeir vilja að vista upplýsingar, gætirðu takmarkað magn upplýsinga sem er vistað en ekki er hægt að eyða síðar. Ef **Virkja vistun villuleitar** er hreinsað vistast færslur um leið, hugsanlega áður en notandinn er tilbúinn. Ef frammistöðustjórnun er notuð leyfir flipinn **Laun** einnig að velja matslíkan til að nota í staðinn fyrir líkanið sem er úthlutað á launafyrirkomulag þegar frammistaða er metin.

Í Human Resources er hægt að nota flipann **Laun** til að velja að takmarka aðgang að launafyrirkomulagi og til að stilla sjálfgefinn gjaldmiðil.

Frekari upplýsingar um laun er að finna í [Yfirlit launafyrirkomulags](hr-compensation-overview.md).

![Launaflipi.](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>Númeraraðir

Stillingarnar í flipanum **Númeraröð** ákvarða raðirnar sem verða notuð til að úthluta auðkennum sjálfkrafa á atriði í Human Resources, t.d.:

- Hugbúnaður
- Fjarvistaskráningar
- Niðurstöður launavinnslu
- Málsnúmer
- Námskeið
- Dagskrá námskeiðs

Til að vinna með tilvísanir númeraraða og kóða skal nota **Númeraraðir** listasíðu (valið er **fyrirtækisstjórnun > Númeraraðir > Númeraraðir**).

Frekari upplýsingar er að finna í [Yfirlit númeraraða](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Fjölda stunda sem er unnið má ekki fara yfir 1,250 og lengd ráðningar má ekki fara yfir 12 mánuði. Þessi hámarksgildi eru samkvæmt alríkislögum í Bandaríkjunum.

![Númeraraðaflipi.](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

Í flipanum FMLA eru FMLA-hæfiskröfur og vinnustundir FMLA-réttinda. Frekari upplýsingar eru í [Grunnstilla færibreytur leyfis og fjarvista](hr-leave-and-absence-parameters.md).

![FMLA-flipi.](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Sjálfsafgreiðsla starfsmanns

Stillingarnar í flipanum **Sjálfsafgreiðsla starfsmanns** hafa áhrif á það hvernig sjálfsafgreiðsla starfsmanns birtist starfsmanni. Á þessum flipa er hægt að:

- Færið inn heiti á vinnusvæði fyrir sjálfsafgreiðslu starfsmanns
- Veljið hvaða upplýsingar yfirmaður getur fært inn fyrir starfsmenn
- Bæta við gagnlegum tenglum fyrir starfsmenn
- Takmarkið getu starfsmanni til að bæta við eða breyta tengiliðaupplýsingum fyrirtækis. Frekari upplýsingar er að finna [Við uppsetningu runuvinnslunnar](hr-employee-self-service-restrict-editing.md).

Frekari upplýsingar um uppsetningu á sjálfsafgreiðslu starfsmanna er að finna í [Yfirlit yfir sjálfsafgreiðslu starfsmanns og stjórnanda](hr-employee-manager-self-service-overview.md).

![Sjálfsafgreiðsluflipi starfsmanns.](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Sjálfsafgreiðsla stjórnanda

Stillingar í flipanum **Sjálfsafgreiðsla starfsmanns** hafa áhrif á hvað stjórnendur sjá í sjálfsafgreiðslu stjórnanda. Í þessum flipa er hægt að skilgreina eftirfarandi valkosti:

- Svið fyrir færslur sem eru að renna út
- Stjórnendur upplýsinga geta skoðað færslur sem eru að renna út
- Hvort stjórnendur geta skoðað opnar stöður fyrir stækkaðar skýrslur
- Yfirlit starfskrafta sem eru að hætta
- Gagnlegir tenglar fyrir stjórnendur

Frekari upplýsingar um uppsetningu á sjálfsafgreiðslu stjórnanda er að finna í [Yfirlit yfir sjálfsafgreiðslu starfsmanns og stjórnanda](hr-employee-manager-self-service-overview.md).

![Sjálfsafgreiðsluflipi stjórnanda.](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Fríðindastjórnun

Í flipa fríðindastjórnunar er hægt að skilgreina valkosti tölvupósts fyrir fríðindastjórnun. Frekari upplýsingar um uppsetningu og notkun fríðindastjórnunar er að finna í [Yfirlit fríðindastjórnunar](hr-benefits-management-overview.md).

![Fríðindastjórnunarflipi.](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Leyfi og fjarvera

Upplýsingar um uppsetningu og notkun leyfa og fjarvista er að finna í [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Greiðsluhættir

Í flipanum **Greiðslumátar** er hægt að velja greiðslumátana sem fyrirtækið styður. Frekari upplýsingar um skilgreiningu launa er að finna í [Yfirlit launafyrirkomulags](hr-compensation-overview.md).

![Flipi greiðsluhátta.](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
