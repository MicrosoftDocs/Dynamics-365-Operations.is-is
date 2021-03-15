---
title: Setja upp sjálfgefnar lýsingar fyrir sjálfvirka bókun
description: Þetta efnisatriði útskýrir hvernig hægt er að setja upp sjálfgefinn texta sem er notaður til að fylla í svæðið fyrir bókhaldsfærslur sem eru bókaðar sjálfkrafa í fjárhag. Fyrir allar færslugerðir er hægt að setja upp sjálfgefna lýsingu með því að nota frjálsan texta eða með því að velja fastar breytur.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d1b73b104ed8a8a015cb97dcf3055a648cfb083d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994741"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Setja upp sjálfgefnar lýsingar fyrir sjálfvirka bókun

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig hægt er að setja upp sjálfgefinn texta sem er notaður til að fylla í svæðið fyrir bókhaldsfærslur sem eru bókaðar sjálfkrafa í fjárhag. Fyrir allar færslugerðir er hægt að setja upp sjálfgefna lýsingu með því að nota frjálsan texta eða með því að velja fastar breytur.

> [!NOTE]
> Fyrir sumar færslugerðir í sumum löndum eða svæðum, er einnig hægt að hafa með texta úr reitum í gagnagrunninum Microsoft Dynamics AX sem eru tengdar þessum færslugerðum. Sjá lista yfir færslugerðir og lönd og svæði í kaflanum [Valfrjálst: Bæta öðrum texta við að sjálfgildar lýsingar](#optional-add-other-text-to-default-descriptions) síðar í þessu efni.

## <a name="set-up-default-descriptions"></a>Setja upp sjálfgefnar lýsingar

1. Fara á **Fyrirtækisstjórnun** \> **Uppsetning** \> **Sjálfgefnar lýsingar**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í reitnum **Lýsing** velurðu tegund færslunnar til að stofna sjálfgefna lýsingu fyrir.
4. Í svæðið **Tungumál** skal velja tungumálið sem lýsingin á við.
5. Í svæðið **Texti** skal slá inn sjálfgefna lýsingu. Hægt er að slá texta inn í svæðið, eða hægt er að nota eina eða fleiri af eftirfarandi breytum með frjálsum texta:

    - **%1** – Bæta við færsludagsetningunni.
    - **%2** – Bæta við kenni sem svarar til skjaltegundarinnar sem er bókuð í fjárhag. Til dæmis fyrir færslugerðir sem tengjast reikningum, bætir breytan **%2** reikningsnúmeri við.
    - **%3** – Bæta við kenni sem tengist skjaltegundinni sem er bókuð í fjárhag. Til dæmis fyrir færslugerðir sem tengjast reikningum, bætir breytan **%3** viðskiptavinalykli við.

## <a name="optional-add-other-text-to-default-descriptions"></a>Valfrjálst: Bæta öðrum texta við að sjálfgildar lýsingar

Fyrir sumar færslugerðir í sumum löndum eða svæðum, geta sjálfgefnar lýsingar innihaldið texta sem kemur úr reitunum í gögnum þínum sem tengjast þeim færslugerðum. Eftirfarandi sýnir sýna færslugerðir og þau lönd og svæði sem þessi kostur er tiltækur fyrir.

**Færslugerðir**

Hægt er að bæta öðrum texta við sjálfgefnar lýsingar fyrir færslugerðir sem tengjast eftirfarandi skjalgerðum:

- Reikningar viðskiptavinar
- Kreditnótur viðskiptavina
- Staðgreiðslur viðskiptavina
- Greiðslur lánardrottna
- Sölupantanir
- Innkaupapantanir
- Birgðabækur
- Áætlanagerð (MRP)
- Eignir

**Lönd og landsvæði**

Þessi kostur er tiltækur fyrir eftirfarandi lönd og svæði:

- Brasilía
- Kína
- Tékkland
- Austur-Evrópa
- Ungverjaland
- Indland
- Japan
- Litháen
- Lettland
- Pólland
- Rússland

### <a name="add-text-to-default-descriptions"></a>Bæta texta við sjálfgefnar lýsingar

Eftir að þú hefur lokið við skrefin í kaflanum [Setja upp sjálfgefnar lýsingar](#set-up-default-descriptions) fyrr í þessu efnisatriði, skaltu fylgja þessum leiðbeiningum til að bæta öðrum texta við upphaflegar lýsingar.

1. Á flýtiflipanum **Færibreytur** velurðu **Bæta við**.
2. Í reitnum **Tilvísunartafla** skal velja tölfu gagnagrunns, þar sem bæta á færibreytugögnum við lýsinguna.
3. Í reitnum **Tilvísunarreitur** skal velja reitinn þar sem bæta á færibreytugögnum við lýsinguna.
4. Endurtakið skref 1 til 3 til að bæta við fleiri færibreytum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]