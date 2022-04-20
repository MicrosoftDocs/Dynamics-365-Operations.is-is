---
title: Settu upp og búðu til jákvæðar launaskrár með því að nota rafræna skýrslugerð
description: Þetta efnisatriði útskýrir hvernig á að setja upp jákvæð laun með því að nota rafræna skýrslugerð.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544545"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Settu upp jákvæðar launaskrár með því að nota rafræna skýrslugerð

Setja upp jákvæða greiðslu til að búa til rafræna lista yfir ávísanir sem eru gefnar í banka. Þegar ávísun er innleyst í bankanum ber bankinn ávísunina saman við lista yfir ávísanir. Ef ávísunin stemmir við ávísun í listanum samþykkir bankinn ávísunina. Ef ávísunin stemmir ekki við ávísun í listanum heldur bankinn henni eftir til skoðunar.

## <a name="set-up-the-electronic-reporting-configuration"></a>Settu upp rafræna skýrslugerð

1. Fara til **Vinnurými \> Rafræn skýrslugerð**.
2. Á flísum fyrir **Microsoft** stillingarveita, veldu **Geymslur**.
3. Veldu **Altækt** og síðan **Opna**.
4. Ef tenging við geymsluna þarf að koma á, velurðu bláa tengilinn í svarglugganum.
5. Finndu og veldu á stillingalistanum **Jákvæð launalíkan \> Jákvæð launaform**.
6. Á **Útgáfur** Flýtiflipi, veldu nýjustu útgáfuna og veldu síðan **Flytja inn**.

## <a name="set-up-a-positive-pay-format"></a>Setja upp snið jákvæðra greiðslna

1. Fara til **Handbært fé og bankastjórnun \> Uppsetning \> Jákvæð launaform**.
2. Veljið **Nýtt**.
3. Stilltu **Greiðslusnið** og **Lýsing** sviðum.
4. Veldu **Almennt rafrænt útflutningssnið** gátreit.
5. Stilltu **Flytja út sniðstillingar** sviði til **Jákvæð launaform**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Úthlutaðu jákvætt launasnið á bankareikning

1. Fara til **Handbært fé og bankastjórnun \> Reikningar banka \> Bankareikningar**.
2. Opnaðu bankareikninginn.
3. Á **Almennt** flýtiflipann, stilltu **Jákvæð launaform** reitnum á sniðið sem var búið til áður.
4. Stilltu **Jákvæð upphafsdagur launa** reit til núverandi dagsetningar.

## <a name="generate-a-positive-pay-file"></a>Mynda jákvæða greiðsluskrá

1. Fara til **Handbært fé og bankastjórnun \> Bankareikningar \> Bankareikningar**.
2. Opnaðu bankareikning sem jákvæð laun eru sett upp fyrir.
3. Veldu **Stjórna greiðslum \> Jákvæð laun \> Jákvæð launaskrá**.
4. Stilltu **Lokadagur** sviði. Ávísanir sem voru búnar til fyrir þessa dagsetningu verða teknar með.

XML skránni sem myndast verður hlaðið niður.
